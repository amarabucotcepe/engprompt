# 🧠 Módulo Complementar: Fluxos de Prompts

**Tema:** Combinação e encadeamento de múltiplos prompts
**Autor:** Adriano Marabuco


---

## 🎯 Objetivo do Módulo

Ensinar os alunos a **construir fluxos de prompts** — sequências lógicas de interações entre humano e IA — para resolver tarefas complexas ou multidimensionais.

> 💬 É o momento em que o servidor deixa de “fazer perguntas” e passa a **projetar conversas inteligentes**.

---

## 📘 Conceito Central

Um **fluxo de prompts** é um *processo conversacional planejado*, composto por **etapas interdependentes**, onde cada resposta da IA serve de **entrada (contexto)** para a próxima tarefa.

Isso permite:

* Dividir tarefas complexas em partes menores e controláveis;
* Garantir coerência entre as etapas (análise → geração → revisão);
* Reutilizar resultados anteriores como base de raciocínio;
* Aumentar a confiabilidade e o controle sobre o resultado final.

---

## 🧩 Exemplo Conceitual — *Pipeline de Prompting*

```
[Prompt 1: Contextualização e Coleta de Dados] 
        ↓
[Prompt 2: Análise e Classificação da Informação]
        ↓
[Prompt 3: Síntese e Redação do Documento Final]
        ↓
[Prompt 4: Revisão e Padronização (self-reflexive ou Meta Prompt)]
```

💡 Cada etapa pode empregar uma técnica diferente:

* Zero-Shot / Instruction no início (para contextualizar);
* Chain of Thought ou Role para análise;
* Formatting ou Priming na redação;
* self-reflexive ou Meta Prompt para revisão final.

---

## 🧭 Exemplo Prático — *Fluxo para Elaboração de Relatório Técnico*

### Etapa 1: Coleta de informações (*Instruction Prompting*)

> “Liste os principais problemas encontrados durante a vistoria de obras do mês de setembro.”

### Etapa 2: Análise técnica (*Chain of Thought*)

> “Analise os problemas listados e classifique-os em estruturais, elétricos e administrativos, explicando as causas.”

### Etapa 3: Geração do relatório (*Formatting + Priming*)

> “Redija um relatório técnico para a diretoria, com linguagem formal, seguindo o formato: Introdução / Diagnóstico / Recomendações.”

### Etapa 4: Revisão e validação (*self-reflexive Prompting*)

> “Revise o relatório anterior, verificando clareza, coerência técnica e tom institucional.”

---

## ⚙️ Estrutura Didática Recomendada para Aula

| Etapa                    | Conteúdo                                                          | Estratégia Didática                       |
| ------------------------ | ----------------------------------------------------------------- | ----------------------------------------- |
| **1. Introdução**        | O que é um fluxo de prompts                                       | Exposição dialogada + diagrama visual     |
| **2. Demonstração**      | Exemplo prático passo a passo (como o acima)                      | Demonstração ao vivo no ChatGPT ou slides |
| **3. Oficina em duplas** | Alunos projetam um fluxo de 3–5 etapas para um caso real do órgão | Trabalho prático guiado                   |
| **4. Revisão coletiva**  | Discussão sobre o que funcionou e o que pode ser ajustado         | Avaliação participativa                   |
| **5. Reflexão final**    | Comparação entre pedir “tudo de uma vez” e dividir em etapas      | Debate e fechamento cognitivo             |

---

## 💡 Dica do Professor

> O segredo dos fluxos de prompts é **ensinar o raciocínio procedural**.
> Mostre aos alunos que a IA pensa melhor **quando a tarefa é bem sequenciada**.
> Estimule-os a usar verbos de ação (“analise”, “sintetize”, “verifique”) e a **encadear etapas com coerência**.
>
> Oriente-os a testar fluxos curtos (3 etapas) antes de construir pipelines maiores.

---

## 🧠 Modelos de Fluxos por Finalidade

| Finalidade                | Estrutura de Fluxo                                             | Técnicas Indicadas               |
| ------------------------- | -------------------------------------------------------------- | -------------------------------- |
| **Análise Técnica**       | Coleta → Raciocínio → Conclusão                                | Instruction + CoT + Formatting   |
| **Redação Oficial**       | Contexto → Redação → Revisão                                   | Priming + Formatting + self-reflexive |
| **Tomada de Decisão**     | Diagnóstico → Avaliação → Escolha → Justificativa              | CoT + Role + ReAct               |
| **Geração de Parecer**    | Leitura de documentos → Interpretação → Conclusão fundamentada | RAG + CoT + Meta Prompt          |
| **Auditoria ou Controle** | Consulta → Verificação → Relatório                             | RAG + ReAct + Formatting         |

---

## 🧰 Atividade Proposta

1. Divida os alunos em grupos e atribua uma tarefa real (ex: elaboração de parecer, relatório ou despacho).
2. Cada grupo deverá **projetar um fluxo de prompts** com 3 a 5 etapas.
3. Teste o fluxo na prática (um aluno digita, outro observa o raciocínio).
4. Registrem as respostas e discutam:

   * Qual etapa mais influenciou o resultado final?
   * O que aconteceria se pulassem uma fase?

---

## 💡 Dica do Professor (pós-atividade)

> Avalie o **grau de dependência entre as etapas** — quanto mais uma resposta servir de base para a próxima, mais o aluno entendeu o conceito de *encadeamento cognitivo*.
>
> Mostre que essa abordagem se aproxima de **fluxos administrativos reais** (coleta de dados → análise → decisão → despacho).
>
> Conclua reforçando: “Engenheiro de Prompt não escreve perguntas — **projeta processos**.”

---

## 📚 Sugestão de Extensão

* Monte um **“Laboratório de Fluxos”**: os alunos podem criar pipelines prontos para o órgão (ex: fluxo para responder demandas de ouvidoria, elaborar relatórios de fiscalização, revisar contratos, etc.).
* Esses fluxos podem ser transformados em **“modelos prontos”** para uso cotidiano no ChatGPT Enterprise ou em sistemas internos.

---

## 🧩 Síntese Visual (para Slide)

```
         [Prompt 1] → [Prompt 2] → [Prompt 3] → [Prompt 4]
           Contexto       Análise       Geração      Revisão
```

> Cada etapa é um **bloco cognitivo**.
> O fluxo inteiro forma um **processo inteligente**.

---

## 🔑 Conclusão

O módulo de **Fluxos de Prompts** transforma o aluno de executor em **arquiteto de interações**.
Ele aprende a:

* Dividir tarefas complexas em etapas lógicas;
* Escolher a técnica ideal para cada fase;
* Garantir que o raciocínio da IA acompanhe o raciocínio humano;
* Produzir resultados **padronizados, verificáveis e reusáveis** no ambiente público.

Referências:

- LangChain Docs. *Chains and Prompt Pipelines.*  
  🔗 https://python.langchain.com/docs/concepts/#chains  
- IBM Developer. *Prompt Chaining com LangChain.*  
  🔗 https://developer.ibm.com/tutorials/langchain-prompt-chaining/