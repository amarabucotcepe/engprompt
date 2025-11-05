# 🎓 Aula 4 — Exercitando Prompts Básicos (versão com storytelling + avaliação)

Cada dinâmica mantém 1 h de duração e estrutura comum (apresentação → execução → avaliação).
Os casos agora trazem **enredo, personagens e contexto administrativo**, tornando a atividade mais envolvente.

---

## 🧩 1) Zero-Shot — **“O Ofício da Semana do Servidor”**

**Enredo**
A Secretaria de Gestão Pública está preparando a **Semana do Servidor**.
Por motivos de ajuste orçamentário, será preciso **adiar a premiação anual**, e a assessoria de comunicação precisa redigir um ofício curto aos setores sem causar mal-estar.

**Desafio**
Gerar um **ofício de até 5 linhas**, tom institucional, objetivo, sem culpas ou justificativas técnicas.
Usar **apenas uma instrução direta (zero-shot)**.

**Objetivo didático**
Mostrar que pequenas escolhas de palavras mudam o tom e a clareza quando não há contexto.

**Prompt de avaliação da IA**

```text
Avalie o texto produzido pelo grupo conforme os critérios:
1. Clareza da mensagem (0–2)
2. Adequação de tom institucional (0–3)
3. Conformidade com o pedido (5 linhas máx.) (0–3)
4. Correção gramatical (0–2)
Explique em 2 linhas o motivo das notas.
```

---

## 🧩 2) Instruction — **“O Checklist do Pregão Fantasma”**

**Enredo**
A Divisão de Compras recebeu um alerta do TCU: um processo de pregão foi suspenso por erro de habilitação.
Para evitar reincidência, o setor precisa criar um **checklist de habilitação** para serviços continuados, claro e padronizado.

**Desafio**
Produzir um prompt que gere um checklist com seções bem definidas e formato de tabela (Instruction Prompting).

**Objetivo didático**
Compreender como instruções detalhadas controlam estrutura e formatação da resposta.

**Prompt de avaliação da IA**

```text
Avalie o checklist segundo:
1. Cobertura das quatro seções obrigatórias (0–2)
2. Clareza e precisão dos itens (0–3)
3. Formatação em tabela e legibilidade (0–3)
4. Ausência de dados pessoais e adequação LGPD (0–2)
Dê uma nota final de 0 a 10 e comente brevemente.
```

---

## 🧩 3) Few-Shot — **“A Ouvidoria Digital da Cidadania”**

**Enredo**
A Ouvidoria Digital recebe centenas de mensagens por semana.
O coordenador quer automatizar a triagem das manifestações: **Elogio**, **Reclamação**, **Denúncia**, **Sugestão**.
Os alunos devem fornecer bons exemplos de cada categoria para treinar a IA.

**Desafio**
Criar um prompt Few-Shot com 4 exemplos claros e equilibrados, testar em novas mensagens e avaliar a acurácia.

**Objetivo didático**
Evidenciar a importância da diversidade e clareza dos exemplos para evitar enviesamento.

**Prompt de avaliação da IA**

```text
Avalie o conjunto de exemplos e a classificação obtida:
1. Cobertura equilibrada das categorias (0–3)
2. Clareza e neutralidade dos exemplos (0–3)
3. Taxa de acerto nas mensagens-teste (0–3)
4. Explicação de eventuais erros (0–1)
Apresente a nota total e um comentário de melhoria.
```

---

## 🧩 4) Priming — **“O Gestor e o Pedido de Prorrogação”**

**Enredo**
O Contrato de Manutenção Predial do Centro Administrativo está para vencer.
A empresa solicita **prorrogação por 12 meses**, alegando que houve chuvas excepcionais e atraso no fornecimento de materiais.
O gestor precisa emitir um **parecer de até 10 linhas**, técnico e formal, sem ultrapassar suas competências.

**Desafio**
Redigir o prompt com priming forte (definindo papel, público, objetivo, tom) e gerar o parecer.

**Objetivo didático**
Aprender a controlar voz institucional e alinhamento ao papel funcional.

**Prompt de avaliação da IA**

```text
Avalie o parecer considerando:
1. Tom institucional e respeito à hierarquia (0–3)
2. Clareza e objetividade (0–3)
3. Fundamentação técnica adequada (0–2)
4. Conformidade com papel e limites do gestor (0–2)
Forneça justificativa resumida e nota de 0 a 10.
```

---

## 🧭 Fluxo didático geral (por caso)

| Etapa                       | Duração | Atividade                                               |
| --------------------------- | ------- | ------------------------------------------------------- |
| Apresentação + storytelling | 10 min  | Professor narra o caso e relembra a técnica             |
| Execução em grupos          | 35 min  | Criação do prompt, geração de resposta, ajuste          |
| Avaliação + discussão       | 15 min  | Apresentação rápida, avaliação pela IA e pelo professor |

---

## 🪄 Dica do Professor

> Durante a apresentação, atue como “cliente interno” solicitando a tarefa, para aumentar a imersão dos alunos.
> No debate, compare as respostas da IA com redações reais da administração pública, mostrando onde a IA é útil e onde precisa de supervisão humana.
