# 🧠 Curso de Engenharia de Prompt para Servidores Públicos

> **Autor:** Adriano Marabuco
> **Técnica:** ReAct Prompting (*Reason + Act*)


---

## 🎯 Objetivo da Aula

Ensinar a técnica de **ReAct Prompting**, usada para instruir a IA a **raciocinar e agir iterativamente**, alternando entre o pensamento e a execução de ações lógicas, consultas ou inferências, até chegar à resposta final.

> 💬 É como treinar um servidor experiente: ele pensa sobre o problema, consulta fontes, analisa e só depois toma a decisão.

---

## 📘 Conceito

O **ReAct (Reason + Act)** combina **duas capacidades da IA em um ciclo**:

1. 🧩 **Reason (Raciocinar):** o modelo explica seu pensamento, analisa hipóteses e identifica lacunas.
2. ⚙️ **Act (Agir):** o modelo executa uma ação — como consultar dados, filtrar opções ou realizar um cálculo.

Esse ciclo continua até que a IA alcance uma conclusão confiável.
É amplamente usado em sistemas *agentes inteligentes*, *assistentes analíticos* e *chatbots administrativos*.

---

## ⚙️ Estrutura do Template Didático

```markdown
# 🎯 Instrução
Resolva a tarefa a seguir utilizando o método ReAct (Reason + Act).  
Siga este formato:

**Raciocínio:** descreva seu pensamento lógico ou análise inicial.  
**Ação:** execute uma ação ou decisão parcial com base no raciocínio.  
**Observação:** descreva o resultado obtido.  
Repita esse ciclo quantas vezes for necessário até chegar à resposta final.  
Finalize com **Conclusão:** apresentando o resultado definitivo.
```

---

## 🧭 Exemplo Prático: Verificação de Regularidade Contratual

```markdown
# 🎯 Instrução
Verifique se o contrato nº 25/2024 da SEFAZ-MA pode ser renovado, considerando que a execução atual está atrasada em 30 dias.  
Utilize o método ReAct (Reason + Act).
```

**💬 Resultado Esperado:**

**Raciocínio:** O contrato pode ser renovado apenas se não houver descumprimento grave. O atraso de 30 dias precisa ser justificado.
**Ação:** Consultar cláusulas do contrato e verificar se há justificativa formal registrada.
**Observação:** A justificativa foi apresentada pelo gestor, alegando atraso na entrega de materiais por motivo de força maior.
**Raciocínio:** Com base nisso, a prorrogação pode ser aceita conforme a Lei 14.133/21, art. 107, §4º.
**Ação:** Redigir parecer favorável com recomendação de novo cronograma.
**Conclusão:** O contrato nº 25/2024 pode ser renovado, desde que o novo cronograma seja formalmente aprovado e o gestor mantenha registro da justificativa no processo.

---

## 📊 Comparativo Didático

| Técnica                    | Foco Cognitivo              | Quando Usar                                                   | Vantagem                                      | Risco                                           |
| -------------------------- | --------------------------- | ------------------------------------------------------------- | --------------------------------------------- | ----------------------------------------------- |
| **ReAct (Reason + Act)**   | 🧩 Pensar e agir em ciclos  | Tarefas complexas com necessidade de raciocínio e verificação | Permite decisões mais seguras e fundamentadas | Pode gerar respostas extensas se mal delimitada |
| **Chain of Thought (CoT)** | 🧠 Raciocínio passo a passo | Quando é preciso justificar uma conclusão                     | Explicações transparentes e coerentes         | Tende a ser linear, sem ajustes intermediários  |
| **RAG**                    | 🔎 Busca e geração          | Quando há base documental externa                             | Usa dados reais e reduz erros factuais        | Depende da qualidade das fontes                 |
| **Reflexive Prompting**    | 🪞 Autoavaliação            | Quando é necessário revisar ou aprimorar respostas            | Melhora a consistência textual                | Requer tempo adicional                          |
| **Meta Prompting**         | 🔁 Metacognição             | Quando se deseja avaliar e aprimorar prompts                  | Gera aprendizado institucional                | Requer domínio das demais técnicas              |

---

## 🧩 Dica Extra — Estrutura Visual para Ensinar o Ciclo ReAct

| Etapa                   | Ação da IA                     | Analogia com Servidor Público          |
| ----------------------- | ------------------------------ | -------------------------------------- |
| **Reason (Raciocinar)** | Analisa a situação e hipóteses | Leitura do processo ou da demanda      |
| **Act (Agir)**          | Executa uma ação parcial       | Consulta norma, calcula, solicita dado |
| **Observe (Observar)**  | Interpreta o resultado da ação | Avalia retorno, parecer ou documento   |
| **Loop**                | Repete até consolidar resposta | Consolidação de informação             |
| **Conclusão**           | Emite parecer final            | Redige despacho ou relatório           |

---

## 🧩 Aplicações Práticas no Setor Público

| Área                         | Aplicação                                 | Exemplo                                          |
| ---------------------------- | ----------------------------------------- | ------------------------------------------------ |
| **Licitações e Contratos**   | Análise de pedidos, aditivos e renovações | Avaliar justificativas legais com base em etapas |
| **Fiscalização de Obras**    | Verificação iterativa de conformidades    | Checar se fotos e relatórios coincidem           |
| **Planejamento e Orçamento** | Avaliação de cenários e estimativas       | Simular alternativas de despesa                  |
| **Controle Interno**         | Auditorias baseadas em evidências         | Cruzar dados e gerar pareceres progressivos      |

---

## 🧭 Conclusão

O **ReAct Prompting** é um passo além do *Chain of Thought*:
ele ensina a IA não apenas a **pensar**, mas também a **agir com consciência e controle**, tornando-a uma verdadeira **assistente pública cognitiva** — capaz de analisar, consultar e decidir com base em fatos e raciocínio.

Referências:

- Yao, S. et al. *ReAct: Synergizing Reasoning and Acting in Language Models.* ICLR, 2023.  
  🔗 https://arxiv.org/abs/2210.03629  
  🔗 https://react-lm.github.io/