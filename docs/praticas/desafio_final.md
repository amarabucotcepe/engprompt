# 🧭 Desafio Final (opcional)

<script src="https://cdn.tailwindcss.com"></script>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<style>
    .mission-card.active {
        background-color: #DBEAFE;
        border-color: #2563EB;
        box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
    }

    .chart-container {
        position: relative;
        width: 100%;
        max-width: 400px;
        height: 300px;
        max-height: 400px;
        margin-left: auto;
        margin-right: auto;
    }

    @media (min-width: 768px) {
        .chart-container {
            height: 350px;
        }
    }

    .deliverable-icon {
        font-size: 2.5rem;
        margin-bottom: 1rem;
        display: inline-block;
    }
</style>

<main class="container mx-auto p-4 md:p-8 max-w-6xl">

<header class="text-center mb-10 md:mb-16">
    <p class="text-xl md:text-2xl text-gray-700">Do prompt ao agente, no seu município</p>
    <p class="text-lg text-gray-500 mt-1">Atividade para depois do curso · individual · sem competição</p>
</header>

<section id="proposta" class="mb-12">
    <h2 class="text-3xl font-semibold text-gray-900 mb-4 pb-2 border-b border-gray-300">📜 A Proposta</h2>
    <p class="text-lg text-gray-700 mb-8">
        Este é um <strong>trabalho opcional</strong> para consolidar o curso. Você escolhe uma missão, aplica ao
        <strong>seu município</strong> com dados públicos reais e resolve o problema combinando
        <strong>engenharia de prompt</strong>, <strong>engenharia de contexto</strong> e um
        <strong>fluxo com agentes</strong>, sempre com o humano no circuito. Não há nota de classificação nem
        premiação: o objetivo é você sair com um caso aplicado e um retorno detalhado.
    </p>

    <div class="grid md:grid-cols-2 gap-8 mb-12">
        <div class="bg-white p-6 rounded-lg shadow border-l-4 border-blue-500">
            <h3 class="text-2xl font-semibold text-gray-800 mb-4">🧩 Como funciona</h3>
            <ul class="list-disc list-outside space-y-3 pl-5 text-gray-700">
                <li><span class="font-semibold">Formato:</span> individual (pode trocar ideias com colegas).</li>
                <li><span class="font-semibold">Ferramentas:</span> qualquer assistente com instruções persistentes
                    (Gem no Gemini, Projeto no ChatGPT ou Claude).</li>
                <li><span class="font-semibold">Prazo:</span> definido pelo professor da turma.</li>
                <li><span class="font-semibold">Dados:</span> portal de dados abertos do seu município ou, se não
                    houver, as bases nacionais indicadas em cada missão.</li>
                <li><span class="font-semibold">Retorno:</span> envie pelo formulário para receber feedback
                    automático por e-mail (opcional).</li>
            </ul>
        </div>
        <div class="bg-white p-6 rounded-lg shadow border-l-4 border-green-500">
            <h3 class="text-2xl font-semibold text-gray-800 mb-4">🔧 O que aplicar</h3>
            <ul class="list-disc list-outside space-y-3 pl-5 text-gray-700">
                <li><span class="font-semibold">Prompt:</span> CoT para analisar, Role para as perspectivas,
                    Reflexive para revisar.</li>
                <li><span class="font-semibold">Contexto:</span> fontes selecionadas e citadas, instruções
                    persistentes, dados minimizados.</li>
                <li><span class="font-semibold">Agentes:</span> fluxo em etapas com critério de parada e log de
                    execução.</li>
                <li><span class="font-semibold">Humano no circuito:</span> aprovação antes de qualquer decisão ou
                    comunicação pública.</li>
            </ul>
        </div>
    </div>
</section>

<section id="roteiro" class="mb-12">
    <h2 class="text-3xl font-semibold text-gray-900 mb-4 pb-2 border-b border-gray-300">🗺️ Roteiro sugerido</h2>
    <ol class="list-decimal list-outside pl-6 space-y-2 text-lg text-gray-700">
        <li><strong>Escolha a missão</strong> e confirme que há dados públicos do seu município sobre o tema.</li>
        <li><strong>Levante as fontes:</strong> 3 a 6 bases ou documentos. Anote data de atualização e o que cada um
            responde.</li>
        <li><strong>Monte o pacote de contexto:</strong> instruções persistentes + fontes selecionadas + o que ficou
            de fora e por quê.</li>
        <li><strong>Desenhe o fluxo:</strong> 3 a 6 etapas (ex.: levantar dados → analisar → propor → revisar →
            aprovação humana → comunicar).</li>
        <li><strong>Execute</strong> o fluxo etapa por etapa e registre o log.</li>
        <li><strong>Revise</strong> com um prompt reflexivo e confira os números nas fontes originais.</li>
        <li><strong>Entregue</strong> pelo formulário (se quiser feedback).</li>
    </ol>
</section>

<section id="entregaveis" class="mb-16">
    <div class="bg-blue-900 rounded-xl p-8 text-white shadow-lg">
        <h2 class="text-3xl font-bold mb-2 text-center">📦 Entregáveis</h2>
        <p class="text-center text-blue-200 mb-8 text-lg">Quatro artefatos curtos — qualidade importa mais que
            volume.</p>

        <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
            <div class="bg-white/10 p-6 rounded-lg border border-white/20 text-center">
                <span class="deliverable-icon">🧠</span>
                <h3 class="text-xl font-bold mb-2">1. Pacote de Contexto</h3>
                <p class="text-sm text-blue-100 leading-relaxed">
                    Instruções persistentes (até 25 linhas) e lista de fontes com justificativa, incluindo ao menos
                    uma excluída ou tratada.
                </p>
            </div>
            <div class="bg-white/10 p-6 rounded-lg border border-white/20 text-center">
                <span class="deliverable-icon">🔁</span>
                <h3 class="text-xl font-bold mb-2">2. Fluxo e Log</h3>
                <p class="text-sm text-blue-100 leading-relaxed">
                    Desenho do fluxo (3 a 6 etapas, com parada e aprovação humana) e log de um ciclo executado.
                </p>
            </div>
            <div class="bg-white/10 p-6 rounded-lg border border-white/20 text-center">
                <span class="deliverable-icon">📄</span>
                <h3 class="text-xl font-bold mb-2">3. Nota Técnica</h3>
                <p class="text-sm text-blue-100 leading-relaxed">
                    Até 1 página, com diagnóstico baseado nos dados, proposta, riscos e próximos passos — citando as
                    fontes.
                </p>
            </div>
            <div class="bg-white/10 p-6 rounded-lg border border-white/20 text-center">
                <span class="deliverable-icon">📣</span>
                <h3 class="text-xl font-bold mb-2">4. Peça Cidadã</h3>
                <p class="text-sm text-blue-100 leading-relaxed">
                    Post, FAQ, roteiro de áudio ou infográfico explicando a proposta à população em linguagem
                    simples.
                </p>
            </div>
        </div>
    </div>
</section>

<section id="missoes" class="my-12 md:my-16">
    <h2 class="text-3xl font-semibold text-gray-900 mb-4 text-center">📂 Missões</h2>
    <p class="text-lg text-gray-700 text-center mb-8 max-w-2xl mx-auto">
        Escolha uma missão e aplique ao seu município. Clique para ver os detalhes e as fontes de dados sugeridas.
    </p>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 mb-8">
        <button data-mission="1"
            class="mission-card border-2 border-transparent text-left bg-white p-5 rounded-lg shadow-md hover:shadow-lg transition-transform hover:-translate-y-1 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
            <span class="text-2xl block mb-2">🔵</span>
            <h4 class="text-xl font-semibold text-gray-900 mb-1">Missão 01</h4>
            <p class="font-medium text-blue-700">Trânsito Mais Seguro</p>
            <p class="text-sm text-gray-600 mt-2">Intervenções de baixo custo nos pontos mais críticos de acidentes.</p>
        </button>
        <button data-mission="2"
            class="mission-card border-2 border-transparent text-left bg-white p-5 rounded-lg shadow-md hover:shadow-lg transition-transform hover:-translate-y-1 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
            <span class="text-2xl block mb-2">🟢</span>
            <h4 class="text-xl font-semibold text-gray-900 mb-1">Missão 02</h4>
            <p class="font-medium text-blue-700">Combate às Arboviroses</p>
            <p class="text-sm text-gray-600 mt-2">Ação intersetorial Saúde + Limpeza Urbana contra dengue, zika e chikungunya.</p>
        </button>
        <button data-mission="3"
            class="mission-card border-2 border-transparent text-left bg-white p-5 rounded-lg shadow-md hover:shadow-lg transition-transform hover:-translate-y-1 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
            <span class="text-2xl block mb-2">🟠</span>
            <h4 class="text-xl font-semibold text-gray-900 mb-1">Missão 03</h4>
            <p class="font-medium text-blue-700">Período Chuvoso Seguro</p>
            <p class="text-sm text-gray-600 mt-2">Priorizar ações de prevenção com orçamento limitado.</p>
        </button>
        <button data-mission="4"
            class="mission-card border-2 border-transparent text-left bg-white p-5 rounded-lg shadow-md hover:shadow-lg transition-transform hover:-translate-y-1 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
            <span class="text-2xl block mb-2">🟣</span>
            <h4 class="text-xl font-semibold text-gray-900 mb-1">Missão 04</h4>
            <p class="font-medium text-blue-700">Missão Livre</p>
            <p class="text-sm text-gray-600 mt-2">Um problema real da sua área de atuação, com dados públicos.</p>
        </button>
    </div>

    <div id="mission-details"
        class="bg-white p-6 md:p-8 rounded-lg shadow-xl min-h-[300px] flex items-center justify-center transition-all duration-300">
        <p id="mission-placeholder" class="text-center text-gray-500 text-xl">
            Selecione uma missão acima para ver os detalhes.
        </p>
    </div>
</section>

<section id="avaliacao" class="my-12 md:my-16">
    <h2 class="text-3xl font-semibold text-gray-900 mb-4 text-center">💬 Como será o retorno</h2>
    <p class="text-lg text-gray-700 text-center mb-8 max-w-3xl mx-auto">
        Se você enviar pelo formulário, o Gemini analisa a entrega com a rubrica abaixo e devolve por e-mail uma
        avaliação por critério com sugestões de melhoria. É um retorno <strong>formativo</strong>: serve para você
        evoluir, não para classificar.
    </p>

    <div class="grid md:grid-cols-2 gap-8 md:gap-12 items-center">
        <div class="bg-white p-6 rounded-lg shadow">
            <h3 class="text-2xl font-semibold text-blue-700 mb-4 text-center">Peso dos critérios</h3>
            <div class="chart-container">
                <canvas id="rubricChart"></canvas>
            </div>
        </div>

        <div>
            <h3 class="text-2xl font-semibold text-blue-700 mb-4">Rubrica (10 pontos)</h3>
            <div class="overflow-x-auto">
                <table class="w-full text-left min-w-[400px]">
                    <thead class="bg-gray-100 border-b border-gray-300">
                        <tr>
                            <th class="p-3 font-semibold text-gray-700">Critério</th>
                            <th class="p-3 font-semibold text-gray-700 text-center">Peso</th>
                            <th class="p-3 font-semibold text-gray-700">O que é observado</th>
                        </tr>
                    </thead>
                    <tbody class="divide-y divide-gray-200">
                        <tr>
                            <td class="p-3 font-medium">Contexto e fontes</td>
                            <td class="p-3 text-center">2</td>
                            <td class="p-3 text-sm text-gray-600">Instruções completas; ≥ 3 fontes públicas com
                                justificativa e data; ≥ 1 excluída ou tratada.</td>
                        </tr>
                        <tr>
                            <td class="p-3 font-medium">Fluxo e humano no circuito</td>
                            <td class="p-3 text-center">2</td>
                            <td class="p-3 text-sm text-gray-600">3 a 6 etapas com parada; aprovação humana antes
                                de decisão ou comunicação; log coerente.</td>
                        </tr>
                        <tr>
                            <td class="p-3 font-medium">Nota técnica fundamentada</td>
                            <td class="p-3 text-center">2</td>
                            <td class="p-3 text-sm text-gray-600">Diagnóstico com dados citados; proposta, riscos e
                                próximos passos.</td>
                        </tr>
                        <tr>
                            <td class="p-3 font-medium">Comunicação cidadã</td>
                            <td class="p-3 text-center">2</td>
                            <td class="p-3 text-sm text-gray-600">Linguagem simples, sem jargão, coerente com a nota
                                técnica.</td>
                        </tr>
                        <tr>
                            <td class="p-3 font-medium">Ética e LGPD</td>
                            <td class="p-3 text-center">2</td>
                            <td class="p-3 text-sm text-gray-600">Apenas dados agregados/públicos; nenhum dado
                                pessoal; proposta justa.</td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <p class="text-sm text-gray-500 mt-4">
                ⚠️ Mesmo em bases públicas, use somente dados <strong>agregados</strong> (por bairro, mês, tipo). Não
                cole registros individuais no assistente.
            </p>
        </div>
    </div>
</section>

<footer class="text-center mt-12 md:mt-16 pt-8 border-t border-gray-300 pb-8">
    <p class="text-lg italic text-gray-700 max-w-2xl mx-auto">
        "A tecnologia não resolve problemas públicos sozinha; ela precisa da inteligência humana para guiá-la."
    </p>
    <p class="mt-4 font-bold text-2xl text-blue-800">
        Bom trabalho!
    </p>
</footer>

</main>

<script>
    document.addEventListener('DOMContentLoaded', () => {

        const missions = {
            "1": {
                title: "🔵 Missão 01: Trânsito Mais Seguro",
                context: "Os acidentes com pedestres, ciclistas e motociclistas aumentaram no seu município. O órgão de trânsito precisa de um plano de intervenções rápidas e de baixo custo (sinalização, travessias, redução de velocidade) para os pontos mais críticos.",
                dataLinks: [
                    { name: "Portal Brasileiro de Dados Abertos — busque pelo seu município (acidentes, vias, infrações)", url: "https://dados.gov.br" },
                    { name: "Óbitos por acidentes de transporte — DATASUS (TabNet/SIM)", url: "https://datasus.saude.gov.br/informacoes-de-saude-tabnet/" },
                    { name: "Frota de veículos e população — IBGE Cidades", url: "https://cidades.ibge.gov.br" }
                ],
                challenge: [
                    "<strong>Diagnóstico:</strong> identificar onde e com quem os acidentes se concentram (local, horário, tipo de vítima).",
                    "<strong>Proposta:</strong> 3 a 5 intervenções priorizadas, com custo relativo e justificativa.",
                    "<strong>Peça cidadã:</strong> post para redes sociais explicando a mudança e o motivo."
                ],
                focus: "Contexto: selecionar só as variáveis agregadas necessárias. Fluxo: agente Analista → agente Redator, com aprovação do gestor de trânsito antes da publicação."
            },
            "2": {
                title: "🟢 Missão 02: Combate às Arboviroses",
                context: "Os casos de dengue, zika e chikungunya estão subindo. A Saúde suspeita de relação com o acúmulo de resíduos em áreas vulneráveis e propõe um mutirão intersetorial com a Limpeza Urbana.",
                dataLinks: [
                    { name: "InfoDengue — situação por município", url: "https://info.dengue.mat.br" },
                    { name: "Notificações de agravos — DATASUS (TabNet/SINAN)", url: "https://datasus.saude.gov.br/informacoes-de-saude-tabnet/" },
                    { name: "Saneamento e coleta de lixo — IBGE Cidades", url: "https://cidades.ibge.gov.br" },
                    { name: "Portal Brasileiro de Dados Abertos — busque pelo seu município (coleta, ocorrências)", url: "https://dados.gov.br" }
                ],
                challenge: [
                    "<strong>Correlação:</strong> cruzar evolução dos casos com indicadores de coleta e saneamento por área.",
                    "<strong>Ação:</strong> plano de um \"Dia D\" intersetorial (locais, equipes, cronograma).",
                    "<strong>Peça cidadã:</strong> roteiro de áudio de 30 segundos para carro de som ou rádio comunitária."
                ],
                focus: "Contexto: dados de saúde só agregados (nunca registros individuais). Fluxo com dois papéis (Saúde e Limpeza Urbana) e handoff estruturado."
            },
            "3": {
                title: "🟠 Missão 03: Período Chuvoso Seguro",
                context: "A previsão indica chuvas acima da média e o orçamento é limitado. O Prefeito precisa decidir quais ações de prevenção priorizar, dando atenção a áreas com escolas e unidades de saúde.",
                dataLinks: [
                    { name: "S2iD — histórico de desastres e decretos", url: "https://s2id.mi.gov.br" },
                    { name: "Cemaden — monitoramento e áreas de risco", url: "https://www.gov.br/cemaden" },
                    { name: "Estabelecimentos de saúde — CNES", url: "https://cnes.datasus.gov.br" },
                    { name: "Portal Brasileiro de Dados Abertos — busque pelo seu município (defesa civil, obras, escolas)", url: "https://dados.gov.br" }
                ],
                challenge: [
                    "<strong>Priorização:</strong> matriz de decisão cruzando histórico de ocorrências e equipamentos públicos críticos.",
                    "<strong>Justificativa:</strong> nota técnica com critérios transparentes para a ordem de prioridade.",
                    "<strong>Peça cidadã:</strong> FAQ para o site da Prefeitura (o que fazer, a quem ligar)."
                ],
                focus: "Fluxo com agentes de papéis distintos (técnico, jurídico, financeiro) e um ponto de aprovação humana antes da priorização final."
            },
            "4": {
                title: "🟣 Missão 04: Missão Livre",
                context: "Escolha um problema real da sua área de atuação (educação, assistência social, arrecadação, meio ambiente, atendimento ao cidadão…) para o qual existam dados públicos do seu município.",
                dataLinks: [
                    { name: "Portal Brasileiro de Dados Abertos", url: "https://dados.gov.br" },
                    { name: "IBGE Cidades — indicadores municipais", url: "https://cidades.ibge.gov.br" }
                ],
                challenge: [
                    "<strong>Problema:</strong> descreva o problema e por que ele importa para a população.",
                    "<strong>Análise e proposta:</strong> diagnóstico baseado em dados e proposta com riscos e próximos passos.",
                    "<strong>Peça cidadã:</strong> formato à sua escolha, adequado ao público."
                ],
                focus: "Mesmos entregáveis e rubrica das demais missões. Prefira um processo que você realmente poderia levar ao seu setor."
            }
        };

        const missionButtons = document.querySelectorAll('.mission-card');
        const detailsContainer = document.getElementById('mission-details');

        missionButtons.forEach(button => {
            button.addEventListener('click', () => {
                const data = missions[button.dataset.mission];

                missionButtons.forEach(btn => btn.classList.remove('active', 'border-blue-500'));
                button.classList.add('active', 'border-blue-500');

                const dataLinksHtml = `
                    <h4 class="text-lg font-semibold text-gray-800 mt-4 mb-2">📊 Fontes de dados sugeridas:</h4>
                    <div class="space-y-2">
                        ${data.dataLinks.map(item => `
                            <div class="flex items-center">
                                <span class="text-blue-500 mr-2">🔗</span>
                                <a href="${item.url}" target="_blank" class="text-blue-600 hover:text-blue-800 hover:underline">${item.name}</a>
                            </div>
                        `).join('')}
                    </div>
                    <p class="text-sm text-gray-500 mt-3">Comece pelo portal de dados abertos ou de transparência do seu município; use as bases nacionais quando não houver dado local.</p>
                `;

                detailsContainer.innerHTML = `
                    <div class="w-full">
                        <h3 class="text-3xl font-bold text-blue-800 mb-3">${data.title}</h3>
                        <p class="text-lg text-gray-700 mb-4">${data.context}</p>
                        <hr class="my-4">
                        <h4 class="text-xl font-semibold text-gray-800 mb-3">🎯 O Desafio:</h4>
                        <ol class="list-decimal list-outside pl-5 space-y-2 text-gray-700 mb-4">
                            ${data.challenge.map(item => `<li>${item}</li>`).join('')}
                        </ol>
                        ${dataLinksHtml}
                        <div class="mt-6 bg-blue-50 p-4 rounded-lg">
                            <h4 class="text-lg font-semibold text-blue-700 mb-1">🔍 Contexto e agentes nesta missão:</h4>
                            <p class="text-blue-900">${data.focus}</p>
                        </div>
                    </div>
                `;
            });
        });

        const ctx = document.getElementById('rubricChart').getContext('2d');
        new Chart(ctx, {
            type: 'doughnut',
            data: {
                labels: [
                    'Contexto e fontes (2)',
                    'Fluxo e humano no circuito (2)',
                    'Nota técnica fundamentada (2)',
                    'Comunicação cidadã (2)',
                    'Ética e LGPD (2)'
                ],
                datasets: [{
                    label: 'Peso',
                    data: [2, 2, 2, 2, 2],
                    backgroundColor: ['#1D4ED8', '#2563EB', '#3B82F6', '#60A5FA', '#93C5FD'],
                    borderColor: '#FFFFFF',
                    borderWidth: 3
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: {
                        position: 'bottom',
                        labels: { font: { size: 12 }, boxWidth: 20, padding: 15 }
                    },
                    tooltip: {
                        callbacks: {
                            label: (context) => `${context.label}: ${context.parsed} pontos`
                        }
                    }
                }
            }
        });
    });
</script>
