# 🎓 Prática 1 — Engenharia de Prompt

| ⏱️ Duração | 👥 Formato | 🧰 Ferramenta |
| ---------- | ---------- | ------------- |
| 4 h (um encontro) | **4 rodadas cronometradas em grupo**: todos os grupos fazem a mesma tarefa, cada um com uma técnica sorteada. Entrega pelo Google Forms, com correção automática pelo Gemini | qualquer assistente de IA generativa (Gemini, ChatGPT, Claude, Copilot) |

!!! abstract "🎯 Objetivo geral"

    Descobrir, com dados da própria turma, **quanto a IA acrescenta ao trabalho e quanto as técnicas acrescentam à IA**. Cada rodada compara o mesmo trabalho feito **sem IA**, com IA usada "de qualquer jeito" e com técnicas de prompt.

!!! warning "⚠️ LGPD"

    Trabalhe somente com os dados fictícios da Ficha do Caso. Não insira nomes reais, CPFs, números de processo, endereços ou qualquer dado pessoal, nem mesmo "para testar".

---

## 🧭 Cronograma

| Tempo | Momento |
| ----- | ------- |
| 20 min | Abertura: regras do jogo, Ficha do Caso e formação dos grupos |
| 45 min | 🧩 **Rodada 1:** O Ofício à Contratada |
| 45 min | 🧩 **Rodada 2:** A Triagem da Ouvidoria |
| 10 min | Intervalo |
| 45 min | 🧩 **Rodada 3:** A Chuva Explica Tudo? |
| 45 min | 🧩 **Rodada 4:** O Parecer da Prorrogação |
| 30 min | 🏁 Quadro final |

---

## 🎲 Como funciona o jogo

**Cada rodada (45 min)**

| ⏱️ | Momento | O que acontece |
| -- | ------- | -------------- |
| 5 min | 🃏 Carta | O professor revela a carta de cada grupo. Leia a tarefa e a seção da sua carta no [Guia das Cartas](cartas_pratica1.md). |
| 20 min | 🛠️ Execução | Tempo fixo, igual para todos. Quem terminar antes já pode entregar: o horário de entrega também conta como resultado. |
| 5 min | 📨 Entrega | **Um envio por grupo** no Google Forms (link do professor). |
| 15 min | 🔍 Revelação | Três saídas aparecem **sem identificação**: a turma vota na melhor e **tenta adivinhar a técnica** de cada uma. Depois o professor mostra o quadro da rodada: carta, nota e tempo de cada grupo. |

**👥 Papéis no grupo**, revezando a cada rodada:

✍️ redator(a) do prompt · 🔍 crítico(a) de qualidade · 🛡️ validador(a) LGPD · 📣 relator(a), que faz a entrega no Forms

**🃏 Regras das cartas**

- ✅ Todos os grupos usam **as mesmas fontes** e fazem **a mesma tarefa**. Só a técnica muda.
- ✅ Em toda rodada, **um grupo tira "Sem IA"**: é a linha de base da comparação.
- ✅ O rodízio garante que nenhum grupo repete técnica e que só aparecem técnicas que têm relação com a tarefa. Algumas cartas **parecem** servir e não servem tão bem: descobrir isso também faz parte do jogo.
- ⚠️ **Use a técnica da sua carta.** Misturar outras técnicas não é proibido, mas o Gemini identifica as técnicas pelo seu prompt e isso reduz a pontuação de aderência.

**📊 Nota da rodada (por grupo)**

| Parte | Pontos | Quem avalia |
| ----- | ------ | ----------- |
| Qualidade do produto | 0–8 | Gemini, **às cegas**: ele lê só o produto final, sem saber a carta nem se houve IA |
| Aderência à carta | 0–2 | Comparação entre a carta sorteada e as técnicas que o Gemini identificou no "como fizemos" |

!!! tip "🃏 Passo a passo de cada carta"

    O [Guia das Cartas da Prática 1](cartas_pratica1.md) tem, para cada carta, o passo a passo com tempos, o molde pronto para colar e o que **não** fazer para não misturar técnicas. Abra a seção da sua carta assim que ela for revelada.

??? info "🃏 O baralho: resumo das cartas"

    | Carta | Em uma linha | Passo a passo | Teoria |
    | ----- | ------------ | ------------- | ------ |
    | 🚫 **Sem IA** | Nenhuma IA de nenhum tipo, inclusive Gemini no Gmail/Docs, Copilot no Word, sugestão automática de texto e tradutores com IA. Vale usar as fontes, um editor de texto simples e a calculadora. | [abrir](cartas_pratica1.md#sem) | — |
    | 0️⃣ **Zero-Shot** | Um pedido direto, sem exemplos nem estrutura: a tarefa e os dados. | [abrir](cartas_pratica1.md#zs) | [modelo](../modelos/0_zero_shot.md) |
    | 🧪 **Few-Shot** | Antes da tarefa, mostre de 2 a 4 exemplos de entrada → saída esperada. | [abrir](cartas_pratica1.md#fs) | [modelo](../modelos/1_few_shot.md) |
    | 📐 **Instruction** | Tarefa + regras explícitas do que fazer e do que não fazer. | [abrir](cartas_pratica1.md#ins) | [modelo](../modelos/2_instruction.md) |
    | 🧾 **Formatting** | Defina a estrutura exata da saída: seções, ordem, tamanho. | [abrir](cartas_pratica1.md#fmt) | [modelo](../modelos/3_formatting.md) |
    | 🎬 **Priming** | Prepare o terreno numa primeira mensagem (contexto, público, objetivo) e só depois peça a tarefa. | [abrir](cartas_pratica1.md#pri) | [modelo](../modelos/4_priming.md) |
    | 🎭 **Role** | Dê à IA um papel profissional, como auditor(a) ou assessor(a) jurídico(a). | [abrir](cartas_pratica1.md#role) | [modelo](../modelos/7_role.md) |
    | 🧭 **Meta Prompt** | Peça à IA que escreva o melhor prompt para a tarefa e então use esse prompt. | [abrir](cartas_pratica1.md#meta) | [modelo](../modelos/6_meta.md) |
    | 🧠 **Chain of Thought** | Peça raciocínio em etapas explícitas antes da conclusão. | [abrir](cartas_pratica1.md#cot) | [modelo](../modelos/8_cot.md) |
    | 🔁 **Reflexive** | Gere uma primeira versão e peça à IA que a critique e reescreva. | [abrir](cartas_pratica1.md#ref) | [modelo](../modelos/9_reflexive.md) |
    | 📚 **RAG** | Cole as fontes e exija resposta **somente** com base nelas, citando a fonte de cada informação. | [abrir](cartas_pratica1.md#rag) | [modelo](../modelos/10_rag.md) |
    | 🔄 **ReAct** | Peça ciclos **Pensamento → Ação ("consultar F_") → Observação** até concluir. | [abrir](cartas_pratica1.md#react) | [modelo](../modelos/11_ReAct.md) |

??? info "📨 O que o Forms pede em toda rodada"

    | Campo | Orientação |
    | ----- | ---------- |
    | E-mail | do(a) relator(a); o feedback do grupo chega nele |
    | Rodada | 1 a 4 |
    | Grupo | 1 a 10 |
    | Carta sorteada | a carta do grupo nesta rodada |
    | Como fizemos | os prompts, na ordem em que foram usados, trocando o enunciado colado por `[ENUNCIADO DA RODADA]` e as fontes coladas por `[FONTES: F1, F2]` (veja o [guia](cartas_pratica1.md)). **Sem IA:** descreva o passo a passo do trabalho manual |
    | Produto final | o texto entregue, exatamente como ficou |
    | Declaração LGPD | "Declaramos que não inserimos dados pessoais reais" |

---

## 📁 Ficha do Caso — "O Contrato dos Buracos"

!!! quote "📖 Enredo"

    A Secretaria de Infraestrutura mantém um contrato de **manutenção corretiva de vias (tapa-buracos)**. Ele vence em **30 dias**. A empresa pediu **prorrogação por 12 meses**, mas o desempenho caiu no último trimestre e as reclamações na Ouvidoria dispararam. O Secretário quer, até o fim do dia, um **parecer técnico** e um **texto curto para explicar a decisão à população**.

Todos os dados abaixo são **fictícios** e servem como fonte para todos os blocos e para o desafio.

### 📄 F1 — Extrato do contrato

| Item | Dado |
| ---- | ---- |
| Objeto | serviço contínuo de manutenção corretiva de pavimento, com equipe e material |
| Vigência | 12 meses, encerrando em **30 dias** |
| Valor anual | R$ 2.400.000,00 |
| Cláusula 5.2 | o edital **prevê a prorrogação**, nos termos da lei |
| Meta do IMR (Instrumento de Medição de Resultado) | 90% das ordens de serviço atendidas em até 72 h |
| Penalidade do IMR | abaixo de 80%, aplica-se uma glosa de 5% na fatura do mês |

### 📈 F2 — Relatório do fiscal do contrato (últimos 6 meses)

<div style="position:relative;max-width:680px;height:320px;margin:1rem 0">
<canvas id="grafico-imr" role="img" aria-label="Percentual de ordens de serviço atendidas em até 72 horas: janeiro 92%, fevereiro 91%, março 88%, abril 74%, maio 71%, junho 79%. Meta de 90%; abaixo de 80% há glosa."></canvas>
</div>
<script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.1/dist/chart.umd.min.js"></script>
<script>
(function () {
  var v = [92, 91, 88, 74, 71, 79];
  var cor = v.map(function (x) { return x >= 90 ? '#2e7d32' : (x >= 80 ? '#f9a825' : '#c62828'); });
  var rotulos = {
    id: 'rotulos',
    afterDatasetsDraw: function (c) {
      var ctx = c.ctx;
      ctx.save();
      ctx.font = 'bold 13px sans-serif';
      ctx.textAlign = 'center';
      ctx.fillStyle = '#333';
      c.getDatasetMeta(0).data.forEach(function (barra, i) { ctx.fillText(v[i] + '%', barra.x, barra.y - 6); });
      ctx.restore();
    }
  };
  new Chart(document.getElementById('grafico-imr'), {
    data: {
      labels: ['Jan', 'Fev', 'Mar', 'Abr ☔', 'Mai ☔', 'Jun'],
      datasets: [
        { type: 'bar', label: '% de OS atendidas em até 72 h', data: v, backgroundColor: cor, order: 2 },
        { type: 'line', label: 'Meta do IMR (90%)', data: [90, 90, 90, 90, 90, 90], borderColor: '#2e7d32', borderDash: [6, 4], borderWidth: 2, pointRadius: 0, order: 1 },
        { type: 'line', label: 'Limite da glosa (80%)', data: [80, 80, 80, 80, 80, 80], borderColor: '#c62828', borderDash: [6, 4], borderWidth: 2, pointRadius: 0, order: 1 }
      ]
    },
    options: {
      maintainAspectRatio: false,
      scales: { y: { min: 60, max: 100, ticks: { callback: function (x) { return x + '%'; } } } },
      plugins: {
        title: { display: true, text: '% de ordens de serviço atendidas em até 72 h' },
        legend: { position: 'bottom', labels: { filter: function (item) { return item.datasetIndex > 0; } } }
      }
    },
    plugins: [rotulos]
  });
})();
</script>

🟩 meta atingida · 🟨 abaixo da meta · 🟥 glosa aplicada · ☔ chuva acima da média

??? note "📄 Ver os dados em tabela"

    | Mês | Jan | Fev | Mar | Abr | Mai | Jun |
    | --- | --- | --- | --- | --- | --- | --- |
    | % OS em até 72 h | 92% | 91% | 88% | 74% | 71% | 79% |

- 📊 Média do semestre: 82,5%. Houve glosa em abril, maio e junho.
- 🏢 A empresa alega chuvas acima da média em abril e maio e atraso do fornecedor de massa asfáltica.
- 🔎 O fiscal confirma as chuvas pelo boletim da Defesa Civil. Registra, porém, que **em junho, sem chuvas relevantes, o índice ficou em 79%**.

### 💰 F3 — Pesquisa de preços (Setor de Compras)

| Preço contratado | Mediana de mercado | Diferença | Nova licitação |
| ---------------- | ------------------ | --------- | -------------- |
| R$ 118/m² | R$ 126/m² (3 orçamentos + painel de preços) | **6,3% abaixo do mercado** | levaria **cerca de 5 meses** para ser concluída |

### 📣 F4 — Ouvidoria

| Manifestações sobre buracos | 1º trimestre | 2º trimestre | Variação |
| --------------------------- | ------------ | ------------ | -------- |
| total | 140 | 310 | **+121%** |

### ⚖️ F5 — Base legal (Lei nº 14.133/2021, art. 107)

> "Os contratos de serviços e fornecimentos contínuos poderão ser prorrogados sucessivamente, respeitada a vigência máxima decenal, desde que haja previsão em edital e que a autoridade competente ateste que as condições e os preços permanecem vantajosos para a Administração, permitida a negociação com o contratado ou a extinção contratual sem ônus para qualquer das partes."

---

## 🧩 Rodada 1 — **"O Ofício à Contratada"** (redação)

**🎯 Objetivo:** Comparar o mesmo documento oficial escrito à mão, com IA sem técnica e com cada técnica, e ver o que muda em **fidelidade aos dados, estrutura e tom**.

??? example "🛠️ Tarefa"

    **🚩 Tarefa (igual para todos)**

    Antes de decidir sobre a prorrogação, a Secretaria precisa **notificar a empresa** sobre a queda de desempenho e pedir uma **manifestação formal em 5 dias úteis**. Redija o ofício com base em **F1 e F2**, em até 15 linhas.

    **⚖️ Qualidade (0–8)**

    | Critério | Pontos |
    | -------- | ------ |
    | Fidelidade aos dados | 0–2 |
    | Estrutura e tom | 0–2 |
    | Pedido e prazo | 0–2 |
    | LGPD e ética | 0–2 |

---

## 🧩 Rodada 2 — **"A Triagem da Ouvidoria"** (classificação)

**🎯 Objetivo:** Ver se a IA classifica melhor e mais rápido que uma pessoa, e qual técnica torna o **critério de classificação** mais consistente.

??? example "🛠️ Tarefa"

    **🚩 Tarefa (igual para todos)**

    Classifique as 8 manifestações abaixo em **Elogio**, **Reclamação**, **Denúncia** ou **Sugestão**, com uma justificativa de uma linha para cada. Sinalize as que precisam de encaminhamento.

    ```text
    1. "Tem um buraco enorme na rua da escola há três semanas, já caiu moto lá."
    2. "A equipe que tapou o buraco na minha rua foi rápida e deixou tudo limpo. Parabéns."
    3. "Vi o caminhão da empresa descarregando asfalto numa obra particular no sábado."
    4. "Poderiam avisar pelo aplicativo quando o reparo da rua for agendado?"
    5. "Consertaram o buraco, mas dois dias depois abriu de novo. Dinheiro jogado fora."
    6. "Sugiro priorizar as ruas que têm linha de ônibus."
    7. "Um homem dizendo ser da prefeitura cobrou 'taxa' para incluir a rua na lista."
    8. "Atendimento excelente da central, me deram o protocolo na hora."
    ```

    **⚖️ Qualidade (0–8)**

    | Critério | Pontos |
    | -------- | ------ |
    | Acerto da classificação | 0–4 |
    | Critério consistente | 0–2 |
    | LGPD e ética | 0–2 |

---

## 🧩 Rodada 3 — **"A Chuva Explica Tudo?"** (análise)

**🎯 Objetivo:** Comparar análises de uma decisão administrativa e descobrir qual técnica produz uma conclusão que você consegue **defender diante de um órgão de controle**.

??? example "🛠️ Tarefa"

    **🚩 Tarefa (igual para todos)**

    A empresa pede que as glosas de abril, maio e junho sejam canceladas por causa das chuvas. Com base em **F1 e F2**, diga se a justificativa vale para **cada mês** e por quê, em até 12 linhas.

    **⚖️ Qualidade (0–8)**

    | Critério | Pontos |
    | -------- | ------ |
    | Conclusão por mês | 0–3 |
    | Uso das fontes | 0–2 |
    | Raciocínio verificável | 0–1 |
    | LGPD e ética | 0–2 |

---

## 🧩 Rodada 4 — **"O Parecer da Prorrogação"** (síntese com fontes)

**🎯 Objetivo:** Fechar o caso com a tarefa mais complexa do dia e ver se a vantagem das técnicas **cresce quando o trabalho exige juntar várias fontes**.

??? example "🛠️ Tarefa"

    **🚩 Tarefa (igual para todos)**

    Com base **somente** na Ficha do Caso (F1 a F5), produza:

    1. **Parecer técnico** (até 15 linhas) ao Secretário, com uma **recomendação explícita**: prorrogar, prorrogar com condições ou não prorrogar. Inclua justificativa, riscos e próximos passos.
    2. **Resumo cidadão** (até 5 linhas) explicando a decisão à população, sem jargão.

    Não existe uma única resposta certa: a avaliação olha a **fundamentação** e a **coerência**.

    **⚖️ Qualidade (0–8)**

    | Critério | Pontos |
    | -------- | ------ |
    | Fundamentação nas fontes | 0–2 |
    | Recomendação, riscos e próximos passos | 0–2 |
    | Resumo cidadão | 0–2 |
    | LGPD e ética | 0–2 |

---

## 🏁 Quadro final (30 min)

O professor projeta o quadro do dia: a **média de qualidade por carta** nas 4 rodadas, com a linha "Sem IA" em destaque.
