
# 🎓 Aula 4 — Exercitando Prompts Básicos

**Configuração geral (para qualquer dinâmica)**

* **Turmas em grupos de 4–6**.
* **Papéis no grupo:**

  1. Facilitador(a) do caso, 2) Redator(a) do prompt, 3) Validador(a) LGPD, 4) Crítico(a) de qualidade, 5) Apresentador(a).
* **Materiais:** 1 computador por grupo (acesso ao modelo), folha de anotações do prompt, modelo de entrega (1 página).
* **Entregáveis (ao final):** (a) **Prompt usado**, (b) **Resposta da IA**, (c) **Justificativa curta** (5–8 linhas) do que funcionou e o que mudariam.
* **Rubrica comum (0–10):**

  * Clareza do objetivo (0–2)
  * Aderência à técnica (0–3)
  * Qualidade do resultado (0–3)
  * Conformidade LGPD (0–2)

> ⚠️ **LGPD:** não inserir nomes reais, CPFs, prontuários, números de processo ou qualquer dado pessoal/sensível. Use apenas dados **fictícios** ou **placeholders**.

---

## 1) Dinâmica Zero-Shot — “Ofício em 5 linhas” (60 min)

**Objetivo didático**
Perceber forças e limites de instruções **mínimas** (sem exemplos), e como pequenos ajustes de linguagem influenciam a saída.

**Caso (Administração/Contratos)**
A diretoria precisa comunicar **atraso no pagamento** por “contingenciamento orçamentário”. Solicita-se um **ofício de 5 linhas**, tom **institucional**, sem culpas nem detalhes técnicos.

**Roteiro (min a min)**

* **0–8 min (professor):** apresenta o caso e reforça regra de **Zero-Shot** (não usar exemplos, nem listas de regras detalhadas).
* **8–35 min (grupos):**

  1. Redigir **1 prompt zero-shot** (máx. 2 frases).
  2. Rodar 2–3 variações mínimas (trocar 1 palavra, ordem, sinônimos).
  3. Escolher a **melhor saída** e registrar por que.
* **35–50 min (professor + grupos):** leitura rápida de 2 respostas por grupos; comentários sobre clareza/variabilidade.
* **50–60 min (professor):** síntese do aprendizado (quando **não** usar zero-shot; perigos de ambiguidade).

**Template (exemplo de ponto de partida)**

> “Elabore um ofício institucional, com **até 5 linhas**, informando **atraso no pagamento** por **contingenciamento orçamentário**. Linguagem **formal** e **objetiva**.”

**Critérios específicos**

* É **zero-shot** de verdade (sem listas de regras/exemplos)?
* O texto final cabe em 5 linhas e tem tom institucional?

---

## 2) Dinâmica Instruction — “Checklist de licitação” (60 min)

**Objetivo didático**
Praticar **regras claras**, **critérios** e **formato de saída** (controle sobre o resultado).

**Caso (Licitações/Lei 14.133/21)**
Preparar um **checklist** para **análise de habilitação** em pregão eletrônico de serviços continuados.

**Roteiro**

* **0–10 min (professor):** apresenta escopo e lembra: **Instruction** = especificar **o que** e **como** (critérios + formato).
* **10–38 min (grupos):**

  1. Escrever prompt com 3 blocos: **tarefa**, **regras**, **formato**.
  2. Gerar saída; ajustar **somente via instrução** (não colar exemplos).
* **38–55 min (plenária):** comparação rápida entre checklists; feedback do professor.
* **55–60 min:** fechamento (boas práticas de instrução e de formatação).

**Template sugerido**

```
Sua tarefa é criar um CHECKLIST de habilitação para pregão eletrônico de serviços continuados.
Regras:
1) Itens em linguagem administrativa e objetiva.
2) Organizar por seções: Documentação jurídica; Regularidade fiscal; Qualificação técnica; Qualificação econômico-financeira.
3) Para cada item, inclua: Nome do item | Descrição | Evidência aceita | Risco se ausente.
Formato: tabela com 4 colunas. Não invente normas; mantenha genérico.
```

**Critérios específicos**

* Cobertura dos **blocos certos** (jurídica, fiscal, técnica, econômico-financeira).
* **Formato** realmente entregue em **tabela** com as 4 colunas.

---

## 3) Dinâmica Few-Shot — “Classificar Ouvidoria” (60 min)

**Objetivo didático**
Treinar **exemplos bem escolhidos** para induzir padrão de resposta (**in-context learning**).

**Caso (Ouvidoria/Cidadão)**
Classificar manifestações em: **Elogio, Reclamação, Denúncia, Sugestão**.

**Roteiro**

* **0–10 min (professor):** explica que **a qualidade e a diversidade dos exemplos** determinam a generalização.
* **10–40 min (grupos):**

  1. Construir **3–4 exemplos** (entrada → rótulo) **equilibrados** (um por classe).
  2. Testar em **5 novas mensagens** dadas pelo professor (ou ficha).
  3. Se erro > 1, **aprimorar exemplos** (trocar, encurtar/alongar).
* **40–55 min:** discutir quais exemplos mais ajudaram/atrapalharam e **por quê**.
* **55–60 min:** fechamento (princípios para escolher exemplos).

**Template de Few-Shot**

```
Classifique a manifestação do cidadão em {Elogio, Reclamação, Denúncia, Sugestão}.

Exemplos:
- "A equipe me atendeu muito bem e resolveu rápido." → Elogio
- "Falta remédio no posto há duas semanas." → Reclamação
- "O servidor X pediu vantagem para agilizar meu processo." → Denúncia
- "Poderiam ampliar o horário de atendimento?" → Sugestão

Agora classifique:
"{NOVA MENSAGEM}"
Retorne apenas o rótulo.
```

**Critérios específicos**

* Exemplos **cobrem todas as classes** e são **claros, curtos e típicos**.
* **Acurácia** nas 5 mensagens de teste (meta ≥ 4/5).

---

## 4) Dinâmica Priming — “Parecer como Gestor de Contrato” (60 min)

**Objetivo didático**
Praticar **papel institucional, tom e foco** para alinhar a resposta ao contexto do órgão.

**Caso (Gestão de Contratos)**
Escrever **parecer breve** sobre **pedido de prorrogação** de contrato de manutenção predial. Deve soar como **gestor de contrato**; tom **técnico-formal**; sem citar artigos específicos (evitar erro factual).

**Roteiro**

* **0–8 min (professor):** priming = **definir papel, público, objetivo e tom**.
* **8–38 min (grupos):**

  1. Construir prompt com bloco de **contexto de papel** + **tarefa** + **formato** (10 linhas).
  2. Gerar saída; ajustar **apenas o contexto/tonalidade**.
* **38–55 min:** leitura de 2 respostas por grupo; foco no **tom** e **responsabilidade** do parecer.
* **55–60 min:** lições: diferença de escrever “como eu” vs. “como gestor”.

**Template de Priming**

```
Você é gestor de contrato em órgão público. Público-alvo: diretoria técnica.
Objetivo: emitir parecer de até 10 linhas sobre pedido de prorrogação de contrato de manutenção predial.
Use tom técnico-formal, linguagem administrativa, foco em critérios objetivos (escopo, cronograma, desempenho, justificativa).
Tarefa: redigir o parecer.
```

**Critérios específicos**

* Tom realmente **institucional** (sem coloquialismos, sem adjetivação).
* Parecer com **foco decisório** (recomenda, condiciona, registra riscos).

---

## Planejamento do Professor (1 página por dinâmica)

* **Apresentação (8–10 min)**: mostrar caso, reforçar **a técnica** (o que **pode** e o que **não pode**).
* **Execução (30–38 min)**: grupos criam o prompt, rodam 2–3 iterações, escolhem saída.
* **Avaliação (12–20 min)**: apresentações rápidas + aplicação da **rubrica**.
* **Debrief (5 min)**: pontos fortes/fracos da técnica, quando usar/evitar.

---

## Dicas práticas

* **Tempo**: use um cronômetro visível (p. ex., 10-30-20).
* **LGPD**: nomeie um **Validador LGPD** em cada grupo.
* **Quadro**: anote “erros comuns” que surgirem (ex.: ambiguidades em zero-shot; formatação quebrada em instruction; exemplos enviesados em few-shot; tom inadequado em priming).
* **Reuso**: peça que salvem **prompt + resposta** para montar o **repositório do curso**.
