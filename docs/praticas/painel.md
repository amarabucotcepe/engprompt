---
search:
  exclude: true
hide:
  - toc
---

# 🎛️ Painel do Professor

Use esta página **projetada** durante as práticas: ela sorteia as cartas dos 10 grupos, revela a carta de cada rodada e controla o cronômetro. O sorteio fica salvo **neste navegador**; se trocar de computador, sorteie de novo antes de começar. O roteiro de cada rodada está na [Condução das Práticas](conducao.md).

<div id="painel">
<style>
#painel .barra{display:flex;flex-wrap:wrap;gap:.5rem;align-items:center;margin:.8rem 0}
#painel button{border:1px solid #3f51b5;background:#fff;color:#3f51b5;border-radius:6px;padding:.35rem .8rem;font-size:.75rem;cursor:pointer}
#painel button.ativo,#painel button.primario{background:#3f51b5;color:#fff}
#painel button:disabled{opacity:.4;cursor:default}
#painel .rotulo{font-size:.7rem;font-weight:700;color:#555;margin-right:.2rem}
#painel .grade{display:grid;grid-template-columns:repeat(auto-fill,minmax(170px,1fr));gap:.6rem;margin:.8rem 0}
#painel .carta{border:2px solid #c5cae9;border-radius:10px;padding:.6rem;min-height:150px;background:#fafbff;font-size:.72rem;line-height:1.35}
#painel .carta .grupo{font-weight:700;color:#3f51b5;font-size:.75rem}
#painel .carta .emoji{font-size:1.9rem;margin:.2rem 0}
#painel .carta .nome{font-weight:700;font-size:.85rem}
#painel .carta.verso{display:flex;flex-direction:column;align-items:center;justify-content:center;background:#e8eaf6;color:#3f51b5;font-size:2rem}
#painel .carta.sem{border-color:#c62828;background:#fff5f5}
#painel .fp{display:inline-block;margin-top:.3rem;background:#fff3cd;border:1px solid #f9a825;border-radius:4px;padding:0 .3rem;font-size:.65rem}
#painel .relogio{font-size:4rem;font-weight:700;font-variant-numeric:tabular-nums;text-align:center;padding:.4rem;border-radius:10px;background:#e8eaf6;color:#1a237e}
#painel .relogio.fim{background:#c62828;color:#fff}
#painel table{font-size:.7rem}
#painel .tarefa{font-size:.85rem;font-weight:700;margin:.4rem 0}
</style>
<div class="barra"><span class="rotulo">Prática:</span><button data-pratica="p1">1 · Engenharia de Prompt</button><button data-pratica="p2">2 · Contexto e Agentes</button></div>
<div class="barra"><button id="sortear" class="primario">🎲 Sortear os grupos</button><span id="status-sorteio" class="rotulo"></span></div>
<div class="barra"><span class="rotulo">Rodada:</span><button data-rodada="1">1</button><button data-rodada="2">2</button><button data-rodada="3">3</button><button data-rodada="4">4</button><button id="revelar" class="primario">🃏 Revelar as cartas</button><label class="rotulo"><input type="checkbox" id="mostrar-fp"> mostrar falsos positivos (para a revelação)</label></div>
<div class="tarefa" id="tarefa"></div>
<div class="grade" id="cartas"></div>
<h2>⏱️ Cronômetro</h2>
<div class="relogio" id="relogio">20:00</div>
<div class="barra"><span class="rotulo">Minutos:</span><button data-min="5">5</button><button data-min="20" class="ativo">20</button><button data-min="15">15</button><button id="iniciar" class="primario">▶️ Iniciar</button><button id="pausar">⏸️ Pausar</button><button id="zerar">↺ Reiniciar</button></div>
<h2>🗂️ Quadro do sorteio</h2>
<div id="quadro"></div>
<script>
(function () {
  var MATRIZES = {"p1": {"matriz": [["COT", "ROLE", "INS", "ZS"], ["RAG", "INS", "FMT", "ROLE"], ["META", "COT", "SEM", "PRI"], ["ZS", "META", "REF", "SEM"], ["PRI", "REF", "REACT", "RAG"], ["REF", "RAG", "ZS", "INS"], ["FMT", "FS", "ROLE", "REACT"], ["SEM", "ZS", "RAG", "FMT"], ["FS", "SEM", "META", "COT"], ["ROLE", "FMT", "COT", "REF"]], "falsos": [["COT"], ["RAG"], ["FMT"], ["FS", "REACT"]]}, "p2": {"matriz": [["SELEC", "SEM", "PROMPT", "DUO"], ["PROMPT", "DUO", "SEM", "TUDO"], ["SEM", "SELEC", "FERR", "GEM"], ["FERR", "PROMPT", "TUDO", "SELEC"], ["PIPE", "TUDO", "PROMPT", "FERR"], ["TUDO", "PROMPT", "GEM", "SEM"], ["PROMPT", "GEM", "FERR", "PIPE"], ["FERR", "PIPE", "SELEC", "PROMPT"], ["TUDO", "RESUMO", "DUO", "PROMPT"], ["GEM", "FERR", "PIPE", "RESUMO"]], "falsos": [["PIPE"], ["RESUMO"], ["TUDO"], []]}};
  var SEM = { e: '🚫', n: 'Sem IA', r: 'Nenhuma IA de nenhum tipo, inclusive Gemini no Gmail/Docs, Copilot no Word e sugestão automática de texto.' };
  var BARALHO = {
    p1: {
      SEM: SEM,
      ZS: { e: '0️⃣', n: 'Zero-Shot', r: 'Pedido direto: a tarefa e os dados, sem exemplos nem estrutura.', m: '0_zero_shot' },
      FS: { e: '🧪', n: 'Few-Shot', r: 'De 2 a 4 exemplos de entrada → saída antes da tarefa.', m: '1_few_shot' },
      INS: { e: '📐', n: 'Instruction', r: 'Tarefa + regras explícitas do que fazer e do que não fazer.', m: '2_instruction' },
      FMT: { e: '🧾', n: 'Formatting', r: 'Estrutura exata da saída: seções, ordem, tamanho.', m: '3_formatting' },
      PRI: { e: '🎬', n: 'Priming', r: 'Primeiro o contexto, o público e o objetivo; depois a tarefa.', m: '4_priming' },
      ROLE: { e: '🎭', n: 'Role', r: 'A IA assume um papel profissional.', m: '7_role' },
      META: { e: '🧭', n: 'Meta Prompt', r: 'A IA escreve o melhor prompt; o grupo usa esse prompt.', m: '6_meta' },
      COT: { e: '🧠', n: 'Chain of Thought', r: 'Raciocínio em etapas explícitas antes da conclusão.', m: '8_cot' },
      REF: { e: '🔁', n: 'Reflexive', r: 'Primeira versão, depois a IA critica e reescreve.', m: '9_reflexive' },
      RAG: { e: '📚', n: 'RAG', r: 'Responder somente com base nas fontes coladas, citando cada uma.', m: '10_rag' },
      REACT: { e: '🔄', n: 'ReAct', r: 'Ciclos Pensamento → Ação (consultar F_) → Observação.', m: '11_ReAct' }
    },
    p2: {
      SEM: SEM,
      PROMPT: { e: '✍️', n: 'Prompt puro', r: 'Técnicas da Prática 1 numa conversa comum, sem colar nem anexar nada do acervo (F1–F10). Fatos escritos com as palavras do grupo valem.' },
      TUDO: { e: '🗂️', n: 'Tudo junto', r: 'Cole ou anexe o acervo inteiro (arquivo acervo_completo, F1–F10) de uma vez, sem selecionar, e faça o pedido.' },
      SELEC: { e: '🎯', n: 'Contexto selecionado', r: 'Só as fontes necessárias, tratadas se tiverem dados pessoais, com citação obrigatória (F_).' },
      GEM: { e: '📌', n: 'Gem / Projeto', r: 'Instruções persistentes + fontes selecionadas; a tarefa é feita dentro do Gem/Projeto.' },
      RESUMO: { e: '🧾', n: 'Resumo de estado', r: 'Comece com as fontes selecionadas; no meio da tarefa, peça um resumo de estado e termine numa conversa nova só com ele.' },
      PIPE: { e: '🔗', n: 'Pipeline manual', r: 'Etapas fixas, um prompt por etapa; a saída de uma é colada na seguinte. Contexto selecionado, sem Gem.' },
      FERR: { e: '🧰', n: 'Assistente com ferramentas', r: 'Disponibilize os arquivos do acervo, dê só o objetivo e deixe o assistente decidir o que ler. Sem busca na web. Cole no Forms os passos que ele informou.' },
      DUO: { e: '🤝', n: 'Dois agentes', r: 'Triador e Redator em conversas separadas; só a ficha de handoff passa de um para o outro. Contexto selecionado, sem Gem.' }
    }
  };
  var TAREFAS = {
    p1: ['O Ofício à Contratada', 'A Triagem da Ouvidoria', 'A Chuva Explica Tudo?', 'O Parecer da Prorrogação'],
    p2: ['Qual é o prazo?', 'O Lote da Planilha', 'A Manifestação da Rua Modelo', 'Da Entrada ao Encaminhamento']
  };
  var CHAVE = 'painel-praticas-v1';
  var est = { pratica: 'p1', rodada: 1, perm: {}, reveladas: { p1: [], p2: [] }, fp: false, minutos: 20 };
  try { var salvo = JSON.parse(localStorage.getItem(CHAVE)); if (salvo) { for (var k in salvo) est[k] = salvo[k]; } } catch (e) {}
  function salvar() { try { localStorage.setItem(CHAVE, JSON.stringify(est)); } catch (e) {} }
  function $(id) { return document.getElementById(id); }
  function cartaDe(grupo, rodada) {
    var perm = est.perm[est.pratica];
    if (!perm) return null;
    var linha = MATRIZES[est.pratica].matriz[perm[grupo]];
    var cod = linha[rodada - 1];
    var c = BARALHO[est.pratica][cod];
    return { cod: cod, c: c, fp: MATRIZES[est.pratica].falsos[rodada - 1].indexOf(cod) >= 0 };
  }
  function render() {
    document.querySelectorAll('#painel [data-pratica]').forEach(function (b) { b.classList.toggle('ativo', b.dataset.pratica === est.pratica); });
    document.querySelectorAll('#painel [data-rodada]').forEach(function (b) { b.classList.toggle('ativo', +b.dataset.rodada === est.rodada); });
    var sorteado = !!est.perm[est.pratica];
    $('sortear').textContent = sorteado ? '🎲 Refazer o sorteio' : '🎲 Sortear os grupos';
    $('status-sorteio').textContent = sorteado ? 'Sorteio feito.' : 'Ainda não sorteado.';
    $('revelar').disabled = !sorteado;
    $('mostrar-fp').checked = est.fp;
    $('tarefa').textContent = 'Rodada ' + est.rodada + ': ' + TAREFAS[est.pratica][est.rodada - 1];
    var revelada = est.reveladas[est.pratica].indexOf(est.rodada) >= 0;
    var html = '';
    for (var g = 0; g < 10; g++) {
      var x = cartaDe(g, est.rodada);
      if (!x || !revelada) { html += '<div class="carta verso"><div class="grupo">Grupo ' + (g + 1) + '</div>?</div>'; continue; }
      var link = '<div><a href="../cartas_pratica' + (est.pratica === 'p1' ? '1' : '2') + '/#' + x.cod.toLowerCase() + '" target="_blank">📖 como jogar</a></div>';
      var fp = (est.fp && x.fp) ? '<span class="fp">⚠️ falso positivo</span>' : '';
      html += '<div class="carta' + (x.cod === 'SEM' ? ' sem' : '') + '"><div class="grupo">Grupo ' + (g + 1) + '</div><div class="emoji">' + x.c.e + '</div><div class="nome">' + x.c.n + '</div><div>' + x.c.r + '</div>' + link + fp + '</div>';
    }
    $('cartas').innerHTML = html;
    var q = '<table><thead><tr><th>Grupo</th>';
    for (var r = 1; r <= 4; r++) q += '<th>R' + r + ': ' + TAREFAS[est.pratica][r - 1] + '</th>';
    q += '</tr></thead><tbody>';
    for (var gg = 0; gg < 10; gg++) {
      q += '<tr><td>' + (gg + 1) + '</td>';
      for (var rr = 1; rr <= 4; rr++) {
        var y = cartaDe(gg, rr);
        var vis = y && est.reveladas[est.pratica].indexOf(rr) >= 0;
        q += '<td>' + (vis ? y.c.e + ' ' + y.c.n + ((est.fp && y.fp) ? ' ⚠️' : '') : '—') + '</td>';
      }
      q += '</tr>';
    }
    $('quadro').innerHTML = q + '</tbody></table>';
  }
  document.querySelectorAll('#painel [data-pratica]').forEach(function (b) { b.onclick = function () { est.pratica = b.dataset.pratica; salvar(); render(); }; });
  document.querySelectorAll('#painel [data-rodada]').forEach(function (b) { b.onclick = function () { est.rodada = +b.dataset.rodada; salvar(); render(); }; });
  $('sortear').onclick = function () {
    if (est.perm[est.pratica] && !confirm('Refazer o sorteio desta prática? As cartas já reveladas vão mudar.')) return;
    var p = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
    for (var i = p.length - 1; i > 0; i--) { var j = Math.floor(Math.random() * (i + 1)); var t = p[i]; p[i] = p[j]; p[j] = t; }
    est.perm[est.pratica] = p; est.reveladas[est.pratica] = []; salvar(); render();
  };
  $('revelar').onclick = function () {
    if (est.reveladas[est.pratica].indexOf(est.rodada) < 0) est.reveladas[est.pratica].push(est.rodada);
    salvar(); render();
  };
  $('mostrar-fp').onchange = function () { est.fp = this.checked; salvar(); render(); };
  var fimEm = null, restante = est.minutos * 60000, tique = null;
  function mostrar() {
    var ms = fimEm ? Math.max(0, fimEm - Date.now()) : restante;
    var s = Math.ceil(ms / 1000);
    $('relogio').textContent = String(Math.floor(s / 60)).padStart(2, '0') + ':' + String(s % 60).padStart(2, '0');
    if (fimEm && ms <= 0) { clearInterval(tique); fimEm = null; restante = 0; $('relogio').classList.add('fim'); apitar(); }
  }
  function apitar() {
    try {
      var ctx = new (window.AudioContext || window.webkitAudioContext)();
      [0, 0.4, 0.8].forEach(function (t) { var o = ctx.createOscillator(); o.frequency.value = 880; o.connect(ctx.destination); o.start(ctx.currentTime + t); o.stop(ctx.currentTime + t + 0.25); });
    } catch (e) {}
  }
  document.querySelectorAll('#painel [data-min]').forEach(function (b) {
    b.onclick = function () {
      document.querySelectorAll('#painel [data-min]').forEach(function (x) { x.classList.remove('ativo'); });
      b.classList.add('ativo'); est.minutos = +b.dataset.min; salvar();
      clearInterval(tique); fimEm = null; restante = est.minutos * 60000; $('relogio').classList.remove('fim'); mostrar();
    };
  });
  $('iniciar').onclick = function () { if (fimEm || restante <= 0) return; $('relogio').classList.remove('fim'); fimEm = Date.now() + restante; tique = setInterval(mostrar, 250); };
  $('pausar').onclick = function () { if (!fimEm) return; restante = Math.max(0, fimEm - Date.now()); fimEm = null; clearInterval(tique); mostrar(); };
  $('zerar').onclick = function () { clearInterval(tique); fimEm = null; restante = est.minutos * 60000; $('relogio').classList.remove('fim'); mostrar(); };
  document.querySelectorAll('#painel [data-min]').forEach(function (x) { x.classList.toggle('ativo', +x.dataset.min === est.minutos); });
  render(); mostrar();
})();
</script>
</div>
