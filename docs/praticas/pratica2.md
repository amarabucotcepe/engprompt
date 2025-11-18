Perfeito, Adriano 👏 — agora avançamos para a **Aula 5 – Exercitando Prompts Avançados**, mantendo o mesmo padrão didático da Aula 4, mas com **maior complexidade, storytelling mais rico e foco em raciocínio, papéis institucionais e autorreflexão**.

Cada dinâmica (Chain of Thought, Role Prompting, self-reflexive Prompting e RAG/ReAct combinados) dura cerca de **60 minutos**, permitindo debate e análise crítica.
Ao final, o professor pode aplicar as **rubricas automatizadas** com IA avaliadora.

---

# 🎓 Aula 5 — Exercitando Prompts Avançados

**Tempo total sugerido:** 4h (1h por técnica)

**Objetivo geral:**
Desenvolver a capacidade de usar técnicas avançadas de prompting para **raciocinar, justificar, revisar e agir com base em informações externas**, simulando situações complexas da administração pública.

**Papéis nos grupos:**

1. **Redator de prompt**,
2. **Analista de coerência**,
3. **Revisor de conformidade (LGPD e ética)**,
4. **Apresentador**.

---

## 🧩 1) Chain of Thought — **“A Decisão sobre o Fornecimento de Medicamentos”**

**Enredo (realista e sensível)**
A Secretaria de Saúde recebeu uma solicitação de um cidadão pedindo um medicamento que **não está na lista do SUS**. O servidor precisa **decidir se recomenda a compra excepcional** e **justificar sua decisão** com base em critérios técnicos, legais e de equidade.

**Desafio**
Construir um prompt que leve a IA a **raciocinar passo a passo** (Chain of Thought) antes de emitir o parecer final.

**Objetivo didático**
Aprender a estruturar prompts que levem a IA a **explicitar o raciocínio intermediário**, melhorando transparência e auditabilidade.

**Etapas resumidas**

* Professor narra o caso (5 min).
* Grupos criam prompt CoT (ex: “Pense passo a passo antes de responder…”).
* Geram 2 respostas: com e sem CoT → comparam diferenças.
* Apresentam e discutem impacto do raciocínio explícito.

**Prompt de avaliação da IA**

```text
Avalie o parecer produzido conforme:
1. Clareza do raciocínio passo a passo (0–3)
2. Fundamentação técnica e legal (0–3)
3. Coerência da decisão final (0–2)
4. Neutralidade e responsabilidade ética (0–2)
Explique em 3 linhas o motivo da nota.
```

---

## 🧩 2) Role Prompting — **“A Reunião do Comitê de Crise”**

**Enredo**
Após uma enchente, um Comitê de Crise precisa tomar decisões rápidas sobre abrigos temporários e distribuição de cestas básicas.
O grupo deve simular **diferentes papéis**: coordenador da defesa civil, gestor financeiro, secretário de assistência social, e assessor jurídico.

**Desafio**
Criar prompts que definam papéis institucionais distintos, gerando perspectivas diferentes sobre a mesma decisão.

**Objetivo didático**
Aprender a controlar *voz, prioridade e responsabilidade* da resposta, conforme o papel assumido.

**Exemplo de prompt base**

```
Você é o [papel].  
Contexto: enchente afetou 300 famílias em 4 bairros.  
Tarefa: opinar sobre a prioridade imediata.  
Fale em 5 linhas, mantendo coerência com seu cargo e atribuições legais.
```

**Atividade**

* Cada grupo usa 2 papéis diferentes e compara as saídas.
* Depois criam **um prompt “síntese”**, conciliando perspectivas (usando CoT se quiserem).

**Prompt de avaliação da IA**

```text
Avalie a coerência dos papéis e da decisão final:
1. Fidelidade ao papel institucional (0–3)
2. Clareza e objetividade das falas (0–3)
3. Coerência na integração dos pontos de vista (0–2)
4. Respeito a princípios éticos e administrativos (0–2)
Forneça nota total e justificativa breve.
```

---

## 🧩 3) self-reflexive Prompting — **“O Relatório que se Corrige”**

**Enredo**
O Controlador Interno solicita um **relatório de acompanhamento de metas ambientais** (redução de consumo de energia elétrica nos prédios públicos).
O servidor gera a primeira versão com IA, mas agora deve criar um prompt que **peça à própria IA para revisar e aperfeiçoar o texto**, justificando as alterações — *como se fosse um revisor interno*.

**Desafio**
Usar *self-reflexive prompting* (autoavaliação + autocorreção da IA).

**Objetivo didático**
Aprender a implementar ciclos de revisão, melhorando precisão e estilo.

**Etapas**

1. Gerar um relatório inicial (5–7 linhas).
2. Usar prompt reflexivo, como:

   ```
   Releia o texto acima e identifique 3 pontos que podem ser aprimorados
   em clareza, concisão ou objetividade.  
   Depois reescreva o texto corrigido e explique as mudanças.
   ```
3. Comparar versões e apresentar ganhos qualitativos.

**Prompt de avaliação da IA**

```text
Avalie a revisão reflexiva considerando:
1. Clareza e pertinência das autocríticas (0–3)
2. Melhoria efetiva do texto (0–3)
3. Conformidade com o formato institucional (0–2)
4. Rigor técnico e gramatical (0–2)
Retorne nota e breve justificativa.
```

---

## 🧩 4) RAG + ReAct — **“O Parecer Inteligente com Base em Leis e Dados”**

**Enredo**
Um órgão público precisa emitir um parecer sobre **uso de drones em obras públicas**, verificando se há base legal e boas práticas técnicas.
Os alunos devem simular o uso de **RAG (busca + geração)**: primeiro **pesquisando informações legais** (reais ou simuladas) e depois **raciocinando e agindo (ReAct)** para produzir o parecer.

**Desafio**
Construir um fluxo de prompts encadeados:

1. Busca de informações legais (ex: NBRs, Lei 14.133/2021, ANAC).
2. Raciocínio estruturado (CoT).
3. Produção do parecer técnico final.

**Objetivo didático**
Mostrar como a IA pode **raciocinar e agir com base em fontes**, unindo RAG e ReAct em processos decisórios do setor público.

**Prompt exemplo**

```
1. Busque normas brasileiras ou leis que tratem do uso de drones em obras públicas.
2. Resuma em 5 linhas os pontos principais.
3. A partir dessas informações, elabore um parecer técnico de 10 linhas
sobre a viabilidade e os cuidados administrativos.
```

**Prompt de avaliação da IA**

```text
Avalie o parecer gerado conforme:
1. Qualidade e relevância das informações recuperadas (0–3)
2. Clareza do raciocínio e encadeamento (0–3)
3. Fundamentação técnica e legal (0–2)
4. Originalidade e responsabilidade na conclusão (0–2)
Inclua nota final e comentário curto.
```

---

## 📊 Avaliação geral da aula

| Critério                         | Peso | Descrição                                                          |
| -------------------------------- | ---- | ------------------------------------------------------------------ |
| Aplicação correta da técnica     | 0–3  | O prompt segue o padrão proposto (CoT, Role, self-reflexive, RAG/ReAct) |
| Clareza e completude da resposta | 0–3  | O produto é claro, objetivo e consistente                          |
| Ética e LGPD                     | 0–2  | Nenhum dado pessoal ou decisão antiética                           |
| Reflexão crítica do grupo        | 0–2  | Os alunos explicam o que aprenderam ou ajustariam                  |

---

## 🧠 Dica do Professor

> Combine grupos para formar “duplas de revisão”: um grupo aplica sua técnica e o outro atua como avaliador com base nos prompts de avaliação.
> Isso promove pensamento crítico e simula a prática de auditoria e revisão institucional.

