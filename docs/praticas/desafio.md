# Desafio Final

<script src="https://cdn.tailwindcss.com"></script>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<style>
    body {
        font-family: 'Inter', sans-serif;
    }

    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap');

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
    
    .data-link {
        color: #3B82F6;
        text-decoration: underline;
    }
    
    .data-link:hover {
        color: #1D4ED8;
    }
</style>

<main class="container mx-auto p-4 md:p-8 max-w-6xl">

<header class="text-center mb-10 md:mb-16">
    <h1 class="text-4xl md:text-5xl font-bold text-blue-800 mb-2">🏆 Aula 6: Gran Finale</h1>
    <p class="text-xl md:text-2xl text-gray-700">A Competição de Engenharia de Prompt</p>
    <p class="text-lg text-gray-500 mt-1">Curso: Inteligência Artificial no Serviço Público</p>
</header>

<section id="desafio" class="mb-12">
    <h2 class="text-3xl font-semibold text-gray-900 mb-4 pb-2 border-b border-gray-300">📜 O Cenário</h2>
    <p class="text-lg text-gray-700 mb-8">
        Bem-vindos, servidores. Hoje, vocês compõem as **Equipes de Resposta Rápida**. O objetivo é simular uma
        crise real da administração pública e resolvê-la utilizando **Engenharia de Prompt Avançada**.
    </p>

    <div class="grid md:grid-cols-2 gap-8 mb-12">
        <div class="bg-white p-6 rounded-lg shadow border-l-4 border-blue-500">
            <h3 class="text-2xl font-semibold text-gray-800 mb-4">🧩 Instruções Gerais</h3>
            <ul class="list-disc list-outside space-y-3 pl-5 text-gray-700">
                <li><span class="font-semibold">Formação:</span> Grupos de 3 a 5 pessoas.</li>
                <li><span class="font-semibold">Ferramentas:</span> LLM de preferência (ChatGPT, Gemini,
                    Claude).</li>
                <li><span class="font-semibold">Tempo:</span> 3 Horas de execução + 1 Hora de apresentações.
                </li>
                <li><span class="font-semibold">Dados:</span> Utilize o <a href="http://dados.recife.pe.gov.br/" target="_blank" class="data-link">Portal de Dados Abertos do Recife</a></li>
            </ul>
        </div>
        <div class="bg-white p-6 rounded-lg shadow border-l-4 border-green-500">
            <h3 class="text-2xl font-semibold text-gray-800 mb-4">🔧 Técnicas Obrigatórias</h3>
            <ul class="list-disc list-outside space-y-3 pl-5 text-gray-700">
                <li><span class="font-semibold">Chain of Thought (CoT):</span> Estruturação do raciocínio.</li>
                <li><span class="font-semibold">RAG/ReAct (Simulado):</span> Uso de dados/leis reais.</li>
                <li><span class="font-semibold">Role Prompting:</span> Persona do gestor público.</li>
                <li><span class="font-semibold">Self-Reflexion:</span> Revisão crítica pela própria IA.</li>
            </ul>
        </div>
    </div>
</section>

<section id="entregaveis" class="mb-16">
    <div class="bg-blue-900 rounded-xl p-8 text-white shadow-lg">
        <h2 class="text-3xl font-bold mb-2 text-center">📦 Entregáveis do Projeto</h2>
        <p class="text-center text-blue-200 mb-8 text-lg">Cada equipe deve submeter os seguintes três artefatos
            ao final do tempo:</p>

        <div class="grid md:grid-cols-3 gap-6">
            <div
                class="bg-white/10 backdrop-blur-sm p-6 rounded-lg border border-white/20 hover:bg-white/20 transition text-center">
                <span class="deliverable-icon">🎤</span>
                <h3 class="text-xl font-bold mb-2">1. Apresentação (Pitch)</h3>
                <p class="text-sm text-blue-100 leading-relaxed">
                    Uma defesa oral de <strong>5 minutos</strong> simulando uma reunião com o
                    Secretário/Prefeito. Deve convencer a autoridade de que a solução é viável, legal e
                    eficiente.
                </p>
            </div>

            <div
                class="bg-white/10 backdrop-blur-sm p-6 rounded-lg border border-white/20 hover:bg-white/20 transition text-center">
                <span class="deliverable-icon">🌐</span>
                <h3 class="text-xl font-bold mb-2">2. Site ou Infográfico</h3>
                <p class="text-sm text-blue-100 leading-relaxed">
                    Um artefato visual (mockup de site, dashboard ou infográfico) focado na <strong>Comunicação
                        Cidadã</strong>. Como vocês explicariam essa solução para a sociedade?
                </p>
            </div>

            <div
                class="bg-white/10 backdrop-blur-sm p-6 rounded-lg border border-white/20 hover:bg-white/20 transition text-center">
                <span class="deliverable-icon">📄</span>
                <h3 class="text-xl font-bold mb-2">3. Relatório Técnico</h3>
                <p class="text-sm text-blue-100 leading-relaxed">
                    Documento formal contendo:
                    <br>• <strong>Parecer Técnico</strong> (Solução detalhada).
                    <br>• <strong>Log de Prompts</strong> (Histórico da conversa com a IA, destacando as
                    técnicas usadas).
                </p>
            </div>
        </div>
    </div>
</section>

<section id="missoes" class="my-12 md:my-16">
    <h2 class="text-3xl font-semibold text-gray-900 mb-4 text-center">📂 Painel de Missões</h2>
    <p class="text-lg text-gray-700 text-center mb-8 max-w-2xl mx-auto">
        O professor distribuirá uma missão para cada grupo ou permitirá a escolha. Clique para ver os detalhes.
    </p>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
        <button id="btn-missao-1" data-mission="1"
            class="mission-card border-2 border-transparent text-left bg-white p-5 rounded-lg shadow-md hover:shadow-lg transition-transform hover:-translate-y-1 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
            <span class="text-2xl block mb-2">🔵</span>
            <h4 class="text-xl font-semibold text-gray-900 mb-1">Missão 01</h4>
            <p class="font-medium text-blue-700">Operação Trânsito Zero</p>
            <p class="text-sm text-gray-600 mt-2">Plano de "Urbanismo Tático" de baixo custo para reduzir
                acidentes com ciclistas.</p>
        </button>
        <button id="btn-missao-2" data-mission="2"
            class="mission-card border-2 border-transparent text-left bg-white p-5 rounded-lg shadow-md hover:shadow-lg transition-transform hover:-translate-y-1 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
            <span class="text-2xl block mb-2">🟢</span>
            <h4 class="text-xl font-semibold text-gray-900 mb-1">Missão 02</h4>
            <p class="font-medium text-blue-700">Guerra às Arboviroses</p>
            <p class="text-sm text-gray-600 mt-2">Ação conjunta de Saúde e Limpeza Urbana contra surto de
                Dengue/Zika.</p>
        </button>
        <button id="btn-missao-3" data-mission="3"
            class="mission-card border-2 border-transparent text-left bg-white p-5 rounded-lg shadow-md hover:shadow-lg transition-transform hover:-translate-y-1 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
            <span class="text-2xl block mb-2">🟠</span>
            <h4 class="text-xl font-semibold text-gray-900 mb-1">Missão 03</h4>
            <p class="font-medium text-blue-700">Inverno Seguro</p>
            <p class="text-sm text-gray-600 mt-2">Priorização de obras de contenção com orçamento limitado e
                risco de chuvas.</p>
        </button>
    </div>

    <div id="mission-details"
        class="bg-white p-6 md:p-8 rounded-lg shadow-xl min-h-[300px] flex items-center justify-center transition-all duration-300">
        <p id="mission-placeholder" class="text-center text-gray-500 text-xl">
            Selecione uma missão acima para ver os detalhes e dados necessários.
        </p>
    </div>
</section>

<section id="avaliacao" class="my-12 md:my-16">
    <h2 class="text-3xl font-semibold text-gray-900 mb-4 text-center">⚖️ Avaliação e Premiação</h2>
    <p class="text-lg text-gray-700 text-center mb-8 max-w-3xl mx-auto">
        A sua performance será avaliada por uma combinação de jurados humanos (Professor) e inteligência
        artificial (IA-Jurado).
    </p>

    <div class="grid md:grid-cols-2 gap-8 md:gap-12 items-center">
        <div class="bg-white p-6 rounded-lg shadow">
            <h3 class="text-2xl font-semibold text-blue-700 mb-4 text-center">Composição da Nota</h3>
            <div class="chart-container">
                <canvas id="rubricChart"></canvas>
            </div>
        </div>

        <div class="space-y-8">
            <div>
                <h3 class="text-2xl font-semibold text-blue-700 mb-4">Rubrica de Avaliação</h3>
                <div class="overflow-x-auto">
                    <table class="w-full text-left min-w-[400px]">
                        <thead class="bg-gray-100 border-b border-gray-300">
                            <tr>
                                <th class="p-3 font-semibold text-gray-700">Critério</th>
                                <th class="p-3 font-semibold text-gray-700 text-center">Peso</th>
                                <th class="p-3 font-semibold text-gray-700">O que será observado?</th>
                            </tr>
                        </thead>
                        <tbody class="divide-y divide-gray-200">
                            <tr class="hover:bg-gray-50">
                                <td class="p-3 font-medium">Domínio Técnico</td>
                                <td class="p-3 text-center">3.0</td>
                                <td class="p-3 text-sm text-gray-600">Uso correto e combinado das técnicas (CoT,
                                    etc).</td>
                            </tr>
                            <tr class="hover:bg-gray-50">
                                <td class="p-3 font-medium">Aplicabilidade</td>
                                <td class="p-3 text-center">2.0</td>
                                <td class="p-3 text-sm text-gray-600">A solução é viável e faz sentido com os
                                    dados?</td>
                            </tr>
                            <tr class="hover:bg-gray-50">
                                <td class="p-3 font-medium">Clareza/Comunicação</td>
                                <td class="p-3 text-center">2.0</td>
                                <td class="p-3 text-sm text-gray-600">Qualidade do Relatório e do
                                    Infográfico/Site.</td>
                            </tr>
                            <tr class="hover:bg-gray-50">
                                <td class="p-3 font-medium">Ética e LGPD</td>
                                <td class="p-3 text-center">2.0</td>
                                <td class="p-3 text-sm text-gray-600">Cuidado com dados sensíveis; solução
                                    justa.</td>
                            </tr>
                            <tr class="hover:bg-gray-50">
                                <td class="p-3 font-medium">Criatividade</td>
                                <td class="p-3 text-center">1.0</td>
                                <td class="p-3 text-sm text-gray-600">Originalidade na abordagem do problema.
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>

            <div>
                <h3 class="text-2xl font-semibold text-blue-700 mb-4">🏅 Premiação Simbólica</h3>
                <ul class="space-y-3">
                    <li class="flex items-center text-lg"><span class="text-2xl mr-3">🥇</span><span
                            class="font-semibold">Prêmio Prompt Dourado:</span>&nbsp;Melhor nota global.</li>
                    <li class="flex items-center text-lg"><span class="text-2xl mr-3">🥈</span><span
                            class="font-semibold">Prêmio IA Ética:</span>&nbsp;Melhor conformidade e
                        responsabilidade.</li>
                    <li class="flex items-center text-lg"><span class="text-2xl mr-3">🥉</span><span
                            class="font-semibold">Prêmio Inovação Cidadã:</span>&nbsp;Melhor site/infográfico.
                    </li>
                </ul>
            </div>
        </div>
    </div>
</section>

<footer class="text-center mt-12 md:mt-16 pt-8 border-t border-gray-300 pb-8">
    <p class="text-lg italic text-gray-700 max-w-2xl mx-auto">
        "A tecnologia não resolve problemas públicos sozinha; ela precisa da inteligência humana para guiá-la."
    </p>
    <p class="mt-4 font-bold text-2xl text-blue-800">
        Boa sorte, servidores!
    </p>
</footer>

</main>

<script>
    document.addEventListener('DOMContentLoaded', () => {

        const missions = {
            "1": {
                title: "🔵 Missão 01: Operação Trânsito Zero",
                context: "Aumento drástico de acidentes com ciclistas e pedestres. A CTTU precisa de um plano de 'Urbanismo Tático' (baixo custo/alto impacto) para apresentar ao Conselho Municipal.",
                dataLinks: [
                    { name: "Acidentes de trânsito com vítimas", url: "http://dados.recife.pe.gov.br/dataset/acidentes-de-transito-com-vitimas" },
                    { name: "Ciclovias, ciclofaixas e estações de bikes", url: "http://dados.recife.pe.gov.br/dataset/ciclovias-ciclofaixas-estacoes-de-aluguel-de-bikes-e-rotas" },
                    { name: "Velocidade das vias", url: "http://dados.recife.pe.gov.br/dataset/velocidade-das-vias-quantitativo-por-velocidade-media" },
                    { name: "Registro de infrações de trânsito", url: "http://dados.recife.pe.gov.br/dataset/registro-das-infracoes-de-transito" }
                ],
                challenge: [
                    "<strong>Diagnóstico:</strong> Analisar dados de acidentes cruzando com locais de excesso de velocidade e infraestrutura cicloviária.",
                    "<strong>Solução:</strong> Propor intervenções físicas rápidas e de baixo custo (sinalização, redutores, pintura).",
                    "<strong>Entrega:</strong> Nota Técnica justificando redução de velocidade + Post para Redes Sociais."
                ],
                focus: "<em>Data Analysis Prompting</em> com <em>Chain of Thought</em> para análise espacial e priorização."
            },
            "2": {
                title: "🟢 Missão 02: Guerra às Arboviroses",
                context: "Risco iminente de surto de Dengue/Zika. O Secretário de Saúde suspeita que o problema está no acúmulo de lixo em áreas vulneráveis e pede uma ação conjunta com a Emlurb (Limpeza Urbana).",
                dataLinks: [
                    { name: "Casos de dengue, zika e chikungunya", url: "http://dados.recife.pe.gov.br/dataset/casos-de-dengue-zika-e-chikungunya" },
                    { name: "Vigilância de zoonoses", url: "http://dados.recife.pe.gov.br/dataset/vigilancia-de-zoonoses" },
                    { name: "Destinação de resíduos sólidos", url: "http://dados.recife.pe.gov.br/dataset/destinacao-de-residuos-solidos" },
                    { name: "Favelas, cortiços e loteamentos irregulares", url: "http://dados.recife.pe.gov.br/dataset/relacao-das-favelas-corticos-e-loteamentos-irregulares" }
                ],
                challenge: [
                    "<strong>Correlação:</strong> Usar a IA para identificar sobreposição geográfica (casos de doença × coleta de lixo × áreas vulneráveis).",
                    "<strong>Ação:</strong> Planejar um 'Dia D' intersetorial (Saúde + Limpeza Urbana).",
                    "<strong>Entrega:</strong> Plano de Ação Intersetorial + Roteiro para Carro de Som (linguagem popular)."
                ],
                focus: "<em>Chain of Thought</em> para planejamento logístico e <em>Style Transfer</em> (técnico para popular)."
            },
            "3": {
                title: "🟠 Missão 03: Inverno Seguro",
                context: "Previsão de chuvas fortes. Orçamento limitado. O Prefeito precisa decidir quais obras de contenção priorizar para evitar tragédias, focando em áreas com escolas e postos de saúde.",
                dataLinks: [
                    { name: "Registro de atendimentos da Defesa Civil", url: "http://dados.recife.pe.gov.br/dataset/registro-de-atendimentos-da-defesa-civil" },
                    { name: "Obras públicas", url: "http://dados.recife.pe.gov.br/dataset/obras-publicas" },
                    { name: "Unidades educacionais no município", url: "http://dados.recife.pe.gov.br/dataset/unidades-educacionais-no-municipio" },
                    { name: "Equipamentos de saúde", url: "http://dados.recife.pe.gov.br/dataset/equipamentos-de-saude" }
                ],
                challenge: [
                    "<strong>Priorização:</strong> Criar uma 'Matriz de Decisão' cruzando histórico de riscos com presença de equipamentos públicos críticos.",
                    "<strong>Justificativa:</strong> Redigir justificativa legal/orçamentária para priorização das obras.",
                    "<strong>Entrega:</strong> Matriz de Priorização + FAQ (Perguntas Frequentes) para o site da Prefeitura."
                ],
                focus: "<em>Role Prompting</em> (Jurídico/Financeiro) e <em>Logical Prompting</em> para decisões baseadas em critérios."
            }
        };

        const missionButtons = document.querySelectorAll('.mission-card');
        const detailsContainer = document.getElementById('mission-details');
        const placeholder = document.getElementById('mission-placeholder');

        missionButtons.forEach(button => {
            button.addEventListener('click', () => {
                const missionId = button.dataset.mission;
                const data = missions[missionId];

                missionButtons.forEach(btn => btn.classList.remove('active', 'border-blue-500'));
                button.classList.add('active', 'border-blue-500');

                if (placeholder) {
                    placeholder.style.display = 'none';
                }

                let dataLinksHtml = '';
                if (data.dataLinks) {
                    dataLinksHtml = `
                        <h4 class="text-lg font-semibold text-gray-800 mt-4 mb-2">📊 Dados de Referência (Portal de Dados Abertos do Recife):</h4>
                        <div class="space-y-2">
                            ${data.dataLinks.map(item => `
                                <div class="flex items-center">
                                    <span class="text-blue-500 mr-2">🔗</span>
                                    <a href="${item.url}" target="_blank" class="text-blue-600 hover:text-blue-800 hover:underline">
                                        ${item.name}
                                    </a>
                                </div>
                            `).join('')}
                        </div>
                    `;
                }

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
                            <h4 class="text-lg font-semibold text-blue-700 mb-1">🔍 Técnica em Foco:</h4>
                            <p class="text-blue-900">${data.focus}</p>
                        </div>
                    </div>
                `;
            });
        });

        const ctx = document.getElementById('rubricChart').getContext('2d');
        const rubricChart = new Chart(ctx, {
            type: 'doughnut',
            data: {
                labels: [
                    'Domínio Técnico (3.0)',
                    'Aplicabilidade (2.0)',
                    'Clareza/Comunicação (2.0)',
                    'Ética e LGPD (2.0)',
                    'Criatividade (1.0)'
                ],
                datasets: [{
                    label: 'Peso na Nota',
                    data: [3, 2, 2, 2, 1],
                    backgroundColor: [
                        '#1D4ED8',
                        '#2563EB',
                        '#3B82F6',
                        '#60A5FA',
                        '#93C5FD'
                    ],
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
                        labels: {
                            font: {
                                size: 12
                            },
                            boxWidth: 20,
                            padding: 15
                        }
                    },
                    tooltip: {
                        callbacks: {
                            label: function (context) {
                                let label = context.label || '';
                                if (label) {
                                    label += ': ';
                                }
                                if (context.parsed !== null) {
                                    label += context.parsed.toFixed(1) + ' pontos';
                                }
                                return label;
                            }
                        }
                    }
                }
            }
        });
    });
</script>
