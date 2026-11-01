# 🧠 Curso Inteligência Artificial no Serviço Público

> **Autor:** Adriano Marabuco

# Recursos e Referências

## 📚 Aula 0 - Inteligência Artificial

* **Foundation Models:** BOMMASANI, Rishi et al. *On the opportunities and risks of foundation models*. arXiv preprint, 2021.
    * 🔗 [Ler no arXiv](https://arxiv.org/abs/2108.07258)
* **Stochastic Parrots:** BENDER, Emily M. et al. *On the dangers of stochastic parrots: Can language models be too big?*. ACM FAccT, 2021.
    * 🔗 [Ler na ACM Digital Library](https://dl.acm.org/doi/10.1145/3442188.3445922)
* **Transfer Learning:** PAN, Sinno Jialin; YANG, Qiang. *A survey on transfer learning*. IEEE Transactions on knowledge and data engineering, 2009.
    * 🔗 [Ler no IEEE Xplore](https://ieeexplore.ieee.org/document/5288526)
* **Diffusion Models:** SOHL-DICKSTEIN, Jascha et al. *Deep unsupervised learning using nonequilibrium thermodynamics*. ICML, 2015.
    * 🔗 [Ler no arXiv](https://arxiv.org/abs/1503.03585)
* **Riscos e Alucinações:** LI, Zihao. *The dark side of chatgpt: Legal and ethical challenges from stochastic parrots and hallucination*. arXiv preprint, 2023.
    * 🔗 [Ler no arXiv](https://arxiv.org/abs/2304.14347)
* **Janela de Contexto:** LIU, Nelson F. et al. *Lost in the middle: How language models use long contexts*. arXiv preprint, 2023.
    * 🔗 [Ler no arXiv](https://arxiv.org/abs/2307.03172)
* **Impacto Cognitivo:** KOSMYNA, Nataliya et al. *Your brain on ChatGPT: Accumulation of cognitive debt when using an AI assistant for essay writing task*. arXiv preprint, 2025.
    * 🔗 [Verificar no arXiv](https://arxiv.org/abs/2506.08872) *(Nota: Citado nos slides como material de 2025)*


## Aula 1 LGPD

## 📜 Legislação e Guias Técnicos

Documentos oficiais e guias orientadores sobre a aplicação da lei e o uso de IA.

* **Lei Geral de Proteção de Dados (LGPD):** Lei nº 13.709/2018.
    * *Artigos citados:* Art. 1º (Fundamentos), Art. 3º (Aplicação), Art. 5º (Definições), Art. 6º (Princípios), Art. 42-43 (Responsabilidade), Art. 52 (Sanções).
* **IA Generativa e a LGPD (ANPD):** Documento técnico sobre o tratamento de dados pessoais em sistemas de IA.
    * 🔗 [Ler Radar Tecnológico ANPD (PDF)](https://www.gov.br/anpd/pt-br/centrais-de-conteudo/documentos-tecnicos-orientativos/radar_tecnologico_ia_generativa_anpd.pdf/view)
* **Cartilha de Segurança (CERT.br):** Fascículo sobre Vazamento de Dados.
    * 🔗 [Ler Fascículo (PDF)](https://cartilha.cert.br/fasciculos/vazamento-de-dados/fasciculo-vazamento-de-dados.pdf)

## Aula 2 Engenharia de Prompts

## 📚 Referências Bibliográficas (Papers)

Artigos acadêmicos fundamentais que embasam as técnicas de *Prompt Engineering* discutidas em aula.

* **Zero-Shot Learning:**
    * KOJIMA, Takeshi et al. *Large language models are zero-shot reasoners*. [cite_start]NeurIPS, 2022. [cite: 639]
    * LAROCHELLE, Hugo et al. *Zero-data learning of new tasks*. [cite_start]AAAI, 2008. [cite: 641]
* **Few-Shot Learning:**
    * BROWN, Tom et al. *Language models are few-shot learners*. [cite_start]NeurIPS, 2020. [cite: 662]
* **Instruction Following:**
    * OUYANG, Long et al. *Training language models to follow instructions with human feedback*. [cite_start]NeurIPS, 2022. [cite: 683]
* **Meta Prompting:**
    * REYNOLDS, Laria; MCDONELL, Kyle. *Prompt programming for large language models: Beyond the few-shot paradigm*. [cite_start]CHI, 2021. [cite: 703]
    * ZHOU, Yongchao et al. *Large language models are human-level prompt engineers*. [cite_start]ICLR, 2022. [cite: 705]
* **Chain of Thought (CoT):**
    * WEI, Jason et al. *Chain-of-thought prompting elicits reasoning in large language models*. [cite_start]NeurIPS, 2022. [cite: 714]
* **Self-Refine (Reflexão):**
    * MADAAN, Aman et al. *Self-refine: Iterative refinement with self-feedback*. [cite_start]NeurIPS, 2023. [cite: 724]
* **Role-Play:**
    * KONG, Aobo et al. [cite_start]*Better zero-shot reasoning with role-play prompting*. arXiv, 2023. [cite: 734]
* **RAG (Retrieval-Augmented Generation):**
    * LEWIS, Patrick et al. *Retrieval-augmented generation for knowledge-intensive nlp tasks*. [cite_start]NeurIPS, 2020. [cite: 742]
* **ReAct (Reason + Act):**
    * YAO, Shunyu et al. *React: Synergizing reasoning and acting in language models*. [cite_start]ICLR, 2022. [cite: 751]
* **Engenharia de IA:**
    * HUYEN, Chip. *AI Engineering: Building Applications with Foundation Models*. [cite_start]O'Reilly Media. [cite: 531]

## 📘 Guias Oficiais e Documentação

Materiais técnicos das principais desenvolvedoras de LLMs.

### Google (Gemini)
* **Estratégias de Prompting:** Documentação oficial da API do Gemini.
    * [cite_start]🔗 [Ler Documentação](https://ai.google.dev/gemini-api/docs/prompting-strategies?hl=pt-br) [cite: 532]
* **Prompting Guide 101:** Guia para Google Workspace.
    * [cite_start]🔗 [Baixar PDF](https://services.google.com/fh/files/misc/gemini-for-google-workspace-prompting-guide-101.pdf) [cite: 545]

### Anthropic (Claude)
* **Modelos e Variáveis:** Guia sobre templates de prompts.
    * [cite_start]🔗 [Ler Guia](https://docs.claude.com/en/docs/build-with-claude/prompt-engineering/prompt-templates-and-variables) [cite: 555]
* **Chain of Thought:** Exemplos práticos.
    * [cite_start]🔗 [Ver Exemplos](https://docs.claude.com/en/docs/build-with-claude/prompt-engineering/chain-of-thought#example-writing-donor-emails-guided-cot) [cite: 717]

### OpenAI
* **Prompt Engineering Guide:** Guia oficial de boas práticas.
    * [cite_start]🔗 [Ler Guia](https://platform.openai.com/docs/guides/prompt-engineering) [cite: 569]

### Outros
* **Markdown Guide (GitHub):** Sintaxe para formatação de textos.
    * [cite_start]🔗 [Acessar Guia](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) [cite: 584]

## 🗃️ Repositórios de Prompts

Bibliotecas de prompts prontos para uso e inspiração.

* [cite_start]**Google Gallery:** [ai.google.dev/gemini-api/prompts](https://ai.google.dev/gemini-api/prompts?hl=pt-br) [cite: 622]
* [cite_start]**Anthropic Prompt Library:** [docs.claude.com/en/resources/prompt-library](https://docs.claude.com/en/resources/prompt-library/library) [cite: 624]
* [cite_start]**OpenAI Prompt Pack:** [academy.openai.com](https://academy.openai.com/public/clubs/work-users-ynjqu/resources/chatgpt-for-any-role) [cite: 623]
* [cite_start]**Repositório Nacional (TCU/TCE):** [cines.tcerr.tc.br/appiagen](https://cines.tcerr.tc.br/appiagen/) [cite: 625]

## 📰 Leituras Complementares

* **Artigo:** "ChatGPT cria ou destrói trabalho?" por Silvio Meira.
    * [cite_start]🔗 [Ler artigo](https://silvio.meira.com/chatgpt-cria-ou-destroi-trabalho/) [cite: 511]

### Recursos e Repositórios

* **Galeria Google:**
    * [https://ai.google.dev/gemini-api/prompts?hl=pt-br](https://ai.google.dev/gemini-api/prompts?hl=pt-br) [cite: 115]
* **Prompt Pack OpenAI:**
    * [https://academy.openai.com/public/clubs/work-users-ynjqu/resources/chatgpt-for-any-role](https://academy.openai.com/public/clubs/work-users-ynjqu/resources/chatgpt-for-any-role) [cite: 116]
* **Prompt Library (Claude):**
    * [https://docs.claude.com/en/resources/prompt-library/library](https://docs.claude.com/en/resources/prompt-library/library) [cite: 117]
* **Repositório Nacional de Prompts:**
    * [https://cines.tcerr.tc.br/appiagen/](https://cines.tcerr.tc.br/appiagen/) [cite: 118]
