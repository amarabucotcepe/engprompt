# 🧠 Curso Inteligência Artificial no Serviço Público

> **Autor:** Adriano Marabuco
> **Técnica** Role Prompting — Interpretação de Papéis


## 🎭 2. **Role Prompting** — *Interpretação de Papéis*

---

### 🎯 Objetivo da Aula

Ensinar a IA a **adotar um papel profissional ou institucional específico**, ajustando linguagem, foco e responsabilidade.

> 💬 É como dizer: “fale como se fosse um auditor, ou como se fosse o gestor financeiro”.

---

### 📘 Conceito

O *Role Prompting* utiliza o comando de **simulação de papéis** para gerar respostas compatíveis com o contexto organizacional.
É essencial para treinar, revisar e simular processos administrativos.

---

### ⚙️ Estrutura do Template Didático

```markdown
# 🎭 Contexto de Papel
Você é {cargo ou função}.  
Seu público-alvo é {tipo de leitor}.  
Seu objetivo é {missão da tarefa}.  
Use um tom {formal/instrutivo/técnico/consultivo}.

# 🧩 Tarefa
{descrição da tarefa}.
Retorne a resposta no formato {parecer, ofício, minuta, relatório, etc.}.
```

---

### 🧭 Exemplo Prático: Papel de Gestor de Contrato

```markdown
# 🎭 Contexto de Papel
Você é gestor de contrato no setor de Engenharia da SEFAZ-MA.  
Seu objetivo é elaborar uma comunicação à empresa contratada sobre o atraso na entrega dos serviços.  
Use um tom formal e objetivo.

# 🧩 Tarefa
Elabore o texto da notificação.
```

**💬 Resultado Esperado:**

> Prezados,
> Constatou-se atraso na execução dos serviços previstos no Contrato nº 27/2024. Solicitamos a imediata regularização do cronograma, sob pena de aplicação das penalidades cabíveis.
> Atenciosamente,
> Gestão de Contratos – SEFAZ-MA

Referências:

- Jakesch, M. et al. *Co-Writing with Opinionated Language Models Affects Users’ Views.* CHI, 2023.  
  🔗 https://arxiv.org/abs/2304.00583  
- OpenAI Docs. *System and Role Prompts.*  
  🔗 https://platform.openai.com/docs/guides/prompt-engineering