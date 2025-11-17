# 🧠 Curso de Engenharia de Prompt para Servidores Públicos

> **Autor:** Adriano Marabuco
> **Técnica** Reflexive Prompting — Autoavaliação e Revisão da Resposta



## 🪞 3. **Reflexive Prompting** — *Autoavaliação e Revisão da Resposta*

---

### 🎯 Objetivo da Aula

Ensinar a IA a **avaliar e revisar sua própria resposta** antes de apresentá-la.
Essa técnica melhora a qualidade final e reduz erros de coerência e estilo.

> 💬 É como pedir: “leia seu texto e veja se está claro, correto e alinhado com a norma”.

---

### 📘 Conceito

O *Reflexive Prompting* faz o modelo **voltar sobre o próprio raciocínio** e aplicar critérios de revisão (clareza, completude, coerência, tom, etc.).

---

### ⚙️ Estrutura do Template Didático

```markdown
# 🎯 Instrução
Responda à tarefa a seguir.  
Depois, revise sua resposta com base nos seguintes critérios:
- Clareza e objetividade  
- Correção técnica ou normativa  
- Adequação ao público e tom institucional  
- Estrutura e formatação  

Apresente a resposta final com a seção “Revisão e Ajustes” explicando o que foi melhorado.
```

---

### 🧭 Exemplo Prático: Revisão de Justificativa

```markdown
# 🎯 Instrução
Elabore uma justificativa para a ausência de servidor em treinamento e, em seguida, revise sua resposta conforme os critérios propostos.
```

**💬 Resultado Esperado:**

> **Resposta inicial:** O servidor não compareceu devido a compromissos pessoais.
>
> **Revisão e Ajustes:** A justificativa deve manter tom institucional. Ajustado para:
>
> “O servidor não compareceu ao treinamento em razão de imprevistos pessoais devidamente comunicados à chefia imediata, comprometendo-se a participar da próxima turma de capacitação.”

Referências:

- Shinn, N. et al. *Reflexion: Language Agents with Verbal Reinforcement Learning.* arXiv, 2023.  
  🔗 https://arxiv.org/abs/2303.11366  
- Madaan, A. et al. *Self-Refine: Iterative Refinement with Self-Feedback.* 2023.  
  🔗 https://arxiv.org/abs/2303.17651