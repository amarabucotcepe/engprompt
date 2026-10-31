# 🎓 Prática 1 — Engenharia de Prompt

**Duração:** 4 h (um encontro)
**Formato:** blocos em grupos de 3 a 5 pessoas (não avaliados) + **Desafio Integrador individual**, entregue pelo Google Forms e corrigido automaticamente pelo Gemini.
**Ferramenta:** qualquer assistente de IA generativa (Gemini, ChatGPT, Claude, Copilot).

**Objetivo geral**
Sair do "pedido vago" e chegar a prompts que produzem documentos administrativos confiáveis: estruturados, no tom certo, com raciocínio explícito, revisados e ancorados em fontes.

> ⚠️ **LGPD:** trabalhe somente com os dados fictícios da Ficha do Caso. Não insira nomes reais, CPFs, números de processo, endereços ou qualquer dado pessoal, nem mesmo "para testar".

---

## 🧭 Cronograma

| Tempo | Bloco | Técnicas |
| ----- | ----- | -------- |
| 15 min | Abertura: caso, papéis e regras de LGPD | — |
| 40 min | **A)** Do pedido vago ao prompt estruturado | Zero-Shot → Instruction + Formatting |
| 35 min | **B)** Ensinar pelo exemplo e pela persona | Few-Shot, Priming/Role |
| 40 min | **C)** Raciocínio e autorrevisão | Chain of Thought, Reflexive |
| 30 min | **D)** Respostas ancoradas em fontes | RAG/ReAct simulado, Meta Prompt |
| 10 min | Intervalo | — |
| 55 min | 🎯 **Desafio Integrador** (individual, avaliado) | todas |
| 15 min | Debrief | — |

**Papéis nos grupos (blocos A–D):** redator(a) do prompt · crítico(a) de qualidade · validador(a) LGPD · relator(a). Revezem os papéis a cada bloco.

---

## 📁 Ficha do Caso — "O Contrato dos Buracos"

**Enredo**
A Secretaria de Infraestrutura mantém um contrato de **manutenção corretiva de vias (tapa-buracos)**. Ele vence em **30 dias**. A empresa pediu **prorrogação por 12 meses**, mas o desempenho caiu no último trimestre e as reclamações na Ouvidoria dispararam. O Secretário quer, até o fim do dia, um **parecer técnico** e um **texto curto para explicar a decisão à população**.

Todos os dados abaixo são **fictícios** e servem como fonte para todos os blocos e para o desafio.

**F1 — Extrato do contrato**
- Objeto: serviço contínuo de manutenção corretiva de pavimento, com equipe e material.
- Vigência: 12 meses, encerrando em 30 dias. Valor anual: R$ 2.400.000,00.
- Cláusula 5.2: o edital **prevê a prorrogação**, nos termos da lei.
- Instrumento de Medição de Resultado (IMR):
  - Meta: 90% das ordens de serviço atendidas em até 72 h.
  - Penalidade: abaixo de 80%, aplica-se uma glosa de 5% na fatura do mês.

**F2 — Relatório do fiscal do contrato (últimos 6 meses)**

| Mês | Jan | Fev | Mar | Abr | Mai | Jun |
| --- | --- | --- | --- | --- | --- | --- |
| % OS em até 72 h | 92% | 91% | 88% | 74% | 71% | 79% |

- Média do semestre: 82,5%. Houve glosa em abril, maio e junho.
- A empresa alega chuvas acima da média em abril e maio e atraso do fornecedor de massa asfáltica.
- O fiscal confirma as chuvas pelo boletim da Defesa Civil. Registra, porém, que **em junho, sem chuvas relevantes, o índice ficou em 79%**.

**F3 — Pesquisa de preços (Setor de Compras)**
- Preço contratado: R$ 118/m². Mediana de mercado (3 orçamentos + painel de preços): R$ 126/m².
- O preço contratado está **6,3% abaixo do mercado**.
- Uma nova licitação levaria **cerca de 5 meses** para ser concluída.

**F4 — Ouvidoria**
- Manifestações sobre buracos: 140 no 1º trimestre e 310 no 2º trimestre (**+121%**).

**F5 — Base legal (Lei nº 14.133/2021, art. 107)**
> "Os contratos de serviços e fornecimentos contínuos poderão ser prorrogados sucessivamente, respeitada a vigência máxima decenal, desde que haja previsão em edital e que a autoridade competente ateste que as condições e os preços permanecem vantajosos para a Administração, permitida a negociação com o contratado ou a extinção contratual sem ônus para qualquer das partes."

---

## 🧩 A) Do pedido vago ao prompt estruturado — **"O Ofício à Contratada"** (40 min)

**Desafio**
Antes de decidir, a Secretaria precisa **notificar a empresa** sobre a queda de desempenho e pedir uma manifestação formal em 5 dias úteis.

**Objetivo didático**
Ver na prática o que acontece quando o prompt melhora em camadas: do **Zero-Shot** (só a tarefa) para o **Instruction** (tarefa + regras), e depois para o **Formatting** (estrutura da saída definida).

**Etapas**
1. **Zero-Shot (10 min):** escreva o pedido em **uma frase só**, sem regras nem exemplos. Gere a resposta e anote o que ficou genérico, inventado ou fora do tom.
2. **Instruction (15 min):** reescreva o prompt em 3 blocos (**Tarefa**, **Regras**, **Formato**). Regras de exemplo: usar apenas os dados de F1 e F2, não atribuir culpa, fixar o prazo de resposta.
3. **Formatting (10 min):** exija uma estrutura fixa, por exemplo: cabeçalho, 3 parágrafos com função definida, e o fecho. Inclua um limite de tamanho.
4. **Comparação (5 min):** coloque as 3 versões lado a lado. O que mudou de uma para outra?

**Template de partida (Instruction + Formatting)**

```text
TAREFA: Redija um ofício da Secretaria de Infraestrutura à empresa contratada
notificando a queda de desempenho no contrato de manutenção de vias.

REGRAS:
1. Use somente os dados abaixo; não invente números, nomes ou normas.
2. Tom institucional, objetivo, sem adjetivos ou acusações.
3. Solicite manifestação formal em até 5 dias úteis.

FORMATO:
- Assunto (1 linha)
- Parágrafo 1: contexto do contrato e da meta do IMR
- Parágrafo 2: resultados de abr–jun e glosas aplicadas
- Parágrafo 3: solicitação e prazo
- Máximo de 15 linhas.

DADOS: [cole aqui F1 e F2]
```

---

## 🧩 B) Ensinar pelo exemplo e pela persona — **"A Ouvidoria e as Duas Vozes"** (35 min)

### B1 · Few-Shot: triagem da Ouvidoria (20 min)

**Desafio**
Monte um prompt com **4 exemplos**, um por categoria (**Elogio**, **Reclamação**, **Denúncia** e **Sugestão**), e teste nas 8 mensagens abaixo. A meta é acertar **7 de 8**.

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

**Pergunte-se:** os seus exemplos são parecidos demais com as mensagens de teste? Algum deles induz um viés, como "toda crítica é reclamação"? Quando o modelo errar, troque o exemplo, não a mensagem.

### B2 · Priming/Role: mesma pergunta, duas vozes (15 min)

**Desafio**
Faça a mesma pergunta (*"Devemos prorrogar o contrato?"*) a duas personas, informando papel, público, objetivo e tom:
1. **Gestor(a) do contrato**, que olha para desempenho e continuidade do serviço;
2. **Assessor(a) da Secretaria de Finanças**, que olha para preço, risco e orçamento.

Compare as respostas. O que cada uma prioriza? Algum argumento só aparece em uma delas?

```text
Você é [PAPEL] na Prefeitura. Público: Secretário de Infraestrutura.
Objetivo: opinar sobre a prorrogação do contrato de manutenção de vias.
Tom: técnico-formal, até 8 linhas, sem extrapolar suas atribuições.
Dados: [F1, F2, F3]
```

---

## 🧩 C) Raciocínio e autorrevisão — **"A Chuva Explica Tudo?"** (40 min)

**Desafio**
A empresa pede que as glosas de abril, maio e junho sejam canceladas por causa das chuvas. Use as fontes F1 e F2 para decidir se a justificativa vale para **cada mês**.

**Etapas**
1. **Sem CoT (5 min):** peça só a conclusão e anote a resposta.
2. **Com CoT (15 min):** peça que a IA raciocine em etapas explícitas:
   1. o que o contrato exige;
   2. o que aconteceu em cada mês;
   3. se a causa alegada explica o resultado;
   4. a conclusão por mês.
3. **Reflexive (15 min):** peça que a IA **critique a própria análise**. Ela usou algum dado que não está nas fontes? Tratou junho como abril? A conclusão é coerente com as etapas? Depois, peça a versão corrigida com a lista de mudanças.
4. **Comparação (5 min):** a resposta com CoT chegou à mesma conclusão que a resposta sem CoT? Qual das duas você conseguiria **defender diante de um órgão de controle**?

**Prompt reflexivo de apoio**

```text
Revise a análise acima como um auditor interno:
1. Aponte até 3 problemas (dado inventado, salto lógico, conclusão incoerente).
2. Reescreva a análise corrigida.
3. Liste em tópicos o que mudou e por quê.
```

---

## 🧩 D) Respostas ancoradas em fontes — **"Mostre de Onde Veio"** (30 min)

**Desafio**
Responder com segurança: *"A lei permite prorrogar este contrato? Em quais condições?"*

**Etapas**
1. **Sem fonte (5 min):** faça a pergunta sem colar nada. Anote os artigos, prazos ou condições que a IA citar e verifique se estão certos.
2. **RAG simulado (10 min):** cole F1, F3 e F5 e exija:
   - responder **somente** com base nas fontes coladas;
   - **citar a fonte** (F1, F3 ou F5) em cada afirmação;
   - dizer *"não consta nas fontes"* quando faltar informação.
3. **ReAct leve (5 min):** peça que a IA alterne **Pensamento → Ação ("consultar F_") → Observação** até concluir.
4. **Meta Prompt (10 min):** peça que a IA **escreva para você o prompt ideal** do parecer final, aplicando o que funcionou nos blocos A a D. Guarde esse prompt, porque ele é um bom ponto de partida para o desafio.

**Pergunte-se:** o que melhorou a resposta foi a forma de perguntar **ou as informações que você entregou**? Essa é a ponte para a Prática 2, sobre **engenharia de contexto**.

---

## 🎯 Desafio Integrador — **"O Parecer da Prorrogação"** (55 min · individual · avaliado)

**Enunciado**
Com base **somente** na Ficha do Caso (F1 a F5), produza com a IA:
1. **Parecer técnico** (até 15 linhas) ao Secretário, com uma **recomendação explícita**: prorrogar, prorrogar com condições ou não prorrogar. A recomendação deve vir com justificativa, riscos e próximos passos.
2. **Resumo cidadão** (até 5 linhas) explicando a decisão à população, sem jargão.

**Regras**
- Combine **pelo menos 4 técnicas** vistas hoje, e faça com que elas apareçam de fato no seu prompt.
- Faça **pelo menos uma rodada de autorrevisão** (Reflexive) antes da versão final.
- Não existe uma única resposta certa. A avaliação olha a **fundamentação nas fontes** e a **coerência**.

**Entrega pelo Google Forms** (link fornecido pelo professor)

| Campo | Tipo | Orientação |
| ----- | ---- | ---------- |
| E-mail | coletado automaticamente | o feedback será enviado para ele |
| Nome completo | resposta curta | — |
| Órgão / Secretaria | resposta curta | opcional |
| Técnicas utilizadas | caixas de seleção | Zero-Shot, Instruction, Formatting, Few-Shot, Priming/Role, CoT, Reflexive, RAG/ReAct, Meta Prompt |
| Prompt(s) utilizado(s) | parágrafo | cole o prompt principal e o prompt de revisão (até ~4.000 caracteres) |
| Parecer técnico final | parágrafo | até 15 linhas |
| Resumo cidadão | parágrafo | até 5 linhas |
| Reflexão | parágrafo | 5 a 8 linhas: o que mudou após a autorrevisão e o que você faria diferente |
| Declaração LGPD | caixa de seleção | "Declaro que não inseri dados pessoais reais" |

**Como sua entrega será avaliada (10 pontos)**
A correção é feita pelo Gemini, com base nesta rubrica, e você recebe por e-mail a nota por critério e sugestões de melhoria. O professor revisa os casos de dúvida.

| Critério | Pontos | O que é observado |
| -------- | ------ | ----------------- |
| Uso das técnicas | 0–3 | ≥ 4 técnicas reconhecíveis no prompt, coerentes com as que foram declaradas |
| Fundamentação nas fontes | 0–2 | O parecer usa dados de ≥ 2 fontes (F1–F5) e não inventa números ou normas |
| Qualidade do parecer e do resumo | 0–2 | Recomendação explícita com riscos e próximos passos; resumo ≤ 5 linhas, sem jargão |
| Autorrevisão | 0–1 | A reflexão cita ≥ 1 mudança concreta feita após a revisão |
| LGPD e ética | 0–2 | Sem dados pessoais; a decisão final fica com a autoridade competente |

---

## 🗣️ Debrief (15 min)

- Qual técnica fez **mais diferença** no resultado? Qual quase não mudou nada?
- Onde a IA **inventou** algo, e qual técnica ajudou a evitar isso?
- Quem **assina** o parecer? Que tipo de revisão humana é indispensável antes disso?

---

## 💡 Dica do Professor

> Faça o papel do **Secretário** na abertura e no debrief e cobre a decisão: "prorrogo ou não?". Isso desloca a conversa de "o texto ficou bonito" para "o texto me ajuda a decidir com segurança".
> Durante os blocos, anote no quadro os **erros comuns** que aparecerem, por exemplo: dado inventado no Zero-Shot, exemplos enviesados no Few-Shot ou CoT que parece raciocinar mas não usa as fontes. Esses erros alimentam o debrief e preparam a Prática 2.
