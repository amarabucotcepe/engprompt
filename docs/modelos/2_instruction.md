# 🧠 Curso de Engenharia de Prompt para Servidores Públicos

> **Autor:** Adriano Marabuco  
> **Técnica:** Instruction Prompting  
  

---

## 🎯 Objetivo da Aula

Ensinar a técnica de **Instruction Prompting**, usada para **dar instruções completas e detalhadas** à IA.
Ela permite ao servidor definir com clareza **o que deve ser feito, como, com que tom e em qual formato**.

> 💬 É como redigir um memorando para um colega: quanto mais específico o pedido, menor o risco de interpretação errada.

---

## 📘 Conceito

Enquanto o *Zero-Shot* foca em “**o que pedir**”, o *Instruction Prompting* ensina “**como pedir bem**”.

A técnica consiste em **estruturar a instrução em múltiplas partes**, como:

* **Objetivo da tarefa**
* **Contexto** (quando e por que)
* **Critérios ou restrições**
* **Formato esperado de resposta**

Essa técnica forma a base para tarefas complexas, pois ensina o modelo a seguir **regras explícitas** e **limites operacionais**, algo essencial no serviço público.

---

## ⚙️ Estrutura do Template Didático

```markdown
# 🎯 Instrução
Sua tarefa é {tarefa principal}.  
Considere o seguinte contexto: {informações ou situação real}.  
Siga estas regras:
1. {Regra 1 – restrição, critério, formato}
2. {Regra 2 – tom, tamanho, referências}
3. {Regra 3 – o que evitar}
Retorne o resultado no formato {texto, tabela, lista, minuta, etc.}.
```

### 🔍 Boas práticas

* Seja **explícito** sobre o formato e o público.
* Liste as regras numeradas (a IA entende melhor).
* Indique o **papel ou o contexto institucional** se relevante.
* Evite ordens vagas como “seja breve” — especifique: “use até 5 linhas”.

---

## 🧭 Exemplo Prático: Redação de Justificativa Administrativa

```markdown
# 🎯 Instrução
Sua tarefa é redigir uma justificativa formal para o atraso no envio de relatórios de campo.  
Considere o seguinte contexto: a equipe teve dificuldades logísticas devido às fortes chuvas na região.  
Siga estas regras:
1. O texto deve ter até 6 linhas.  
2. Use tom formal e impessoal.  
3. Evite expressões subjetivas como “lamentamos” ou “infelizmente”.  
Retorne o resultado no formato de parágrafo administrativo.
```

**💬 Resultado Esperado:**

> Em razão das fortes chuvas ocorridas na região de atuação, houve impossibilidade de deslocamento das equipes de campo, ocasionando atraso no envio dos relatórios. As atividades foram retomadas tão logo as condições permitiram, e os documentos encontram-se em fase final de consolidação.

## Referências:

- Ouyang, L. et al. *Training language models to follow instructions with human feedback (InstructGPT).* NeurIPS, 2022.  
  🔗 https://arxiv.org/abs/2203.02155