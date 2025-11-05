
# 🧩 Cheatsheet – Técnicas de Engenharia de Prompt

- **Curso:** Engenharia de Prompt para Servidores Públicos  
- **Autor:** Adriano Marabuco  
- **Versão Didática:** Prof. ChatGPT (IA Educacional)

---

## 🧱 PROMPTS BÁSICOS

| Técnica | O que é | Quando Usar | Estrutura Base | Exemplo de Aplicação Pública |
|----------|----------|--------------|----------------|------------------------------|
| **Zero-Shot** | Instrução direta, sem exemplos | Tarefas simples e objetivas | `Sua tarefa é {tarefa}. Retorne no formato {formato}.` | Gerar despacho curto comunicando atraso no pagamento. |
| **Instruction** | Instrução detalhada com regras | Quando há critérios, restrições ou público específico | `Sua tarefa é {tarefa}. Considere {contexto}.` | Justificativa formal com até 6 linhas e tom impessoal. |
| **Few-Shot** | Ensinando por exemplo | Quando há padrão ou modelo de resposta | `Exemplo 1: entrada → saída / Exemplo 2: entrada → saída / Agora gere a saída.` | Classificação de manifestações de ouvidoria. |
| **Formatting** | Controle da forma da resposta | Quando é necessário padronizar formato | `Apresente o resultado no formato: {modelo}.` | Gerar relatório com colunas: Causa / Consequência / Ação. |
| **Priming** | Condicionamento do papel e tom | Quando é necessário ajustar o estilo de escrita | `Você é {função}. Seu objetivo é {meta}. Use tom {formal/técnico}.` | “Você é analista da SEFAZ. Redija parecer sobre aditivo contratual.” |

---

## ⚙️ PROMPTS AVANÇADOS

| Técnica | O que é | Quando Usar | Estrutura Base | Exemplo de Aplicação Pública |
|----------|----------|--------------|----------------|------------------------------|
| **Chain of Thought (CoT)** | Ensina a IA a raciocinar passo a passo | Em decisões complexas ou pareceres administrativos | `Pense passo a passo antes de responder. Explique o raciocínio e finalize com Conclusão.` | Parecer técnico com análise e justificativa legal. |
| **Role Prompting** | Simula papéis institucionais | Quando é preciso adotar diferentes pontos de vista | `Você é {cargo}. Seu público é {grupo}. Sua tarefa é {ação}.` | Redigir relatório sob o ponto de vista do auditor. |
| **Reflexive Prompting** | Autoavaliação da resposta | Quando é preciso revisar e melhorar resultados | `Responda. Depois revise conforme critérios: clareza, coerência, tom.` | Revisar texto de despacho para linguagem oficial. |
| **Meta Prompting** | Avaliar ou otimizar um prompt | Quando se quer ensinar ou corrigir prompts | `Analise o prompt: {texto}. Liste melhorias e reescreva versão otimizada.` | Melhorar prompt de relatório padronizado do órgão. |
| **RAG (Retrieval-Augmented Generation)** | Busca + geração | Quando há necessidade de citar documentos, leis ou relatórios | `Busque nas fontes {X}. Recupere, sintetize e gere resposta final.` | Consultar leis e gerar parecer fundamentado. |
| **ReAct (Reason + Act)** | Pensar e agir em ciclos | Quando é preciso alternar entre raciocínio e ação | `Raciocínio: … / Ação: … / Observação: … / Conclusão: …` | Verificar contratos, consultar norma e emitir decisão. |

---

## 🔁 PROMPTS COMPLEMENTARES

| Técnica | Propósito | Aplicação |
|----------|------------|-----------|
| **Fluxos de Prompts** | Combinar múltiplos prompts em sequência lógica | Ex: Coleta → Análise → Geração → Revisão |
| **Experimentação de Prompts** | Testar, comparar e otimizar versões | Criar 3 variações do mesmo prompt e avaliar resultados |
| **Recursos Externos** | Integrar arquivos, bases, buscas e APIs | Enriquecer o contexto e validar respostas |

---

## 🧭 ESCOLHENDO A TÉCNICA CERTA

| Situação | Técnica Ideal |
|-----------|----------------|
| Precisa de resposta rápida e direta | Zero-Shot |
| Quer controlar formato e regras | Instruction ou Formatting |
| Deseja replicar padrão existente | Few-Shot |
| Quer ajustar o tom e papel | Priming ou Role |
| Precisa justificar decisão | Chain of Thought |
| Quer revisar e melhorar texto | Reflexive |
| Quer aprimorar um prompt existente | Meta |
| Precisa citar leis ou dados externos | RAG |
| Precisa agir e pensar em etapas | ReAct |
| Quer combinar tudo em processo completo | Fluxo de Prompts |
| Quer testar e medir resultados | Experimentação |
| Precisa validar com arquivos e fontes | Recursos Externos |

---

## 💡 Dicas Gerais do Professor

1. **Comece simples:** use *Zero-Shot* para testar o comportamento inicial.  
2. **Adicione estrutura:** com *Instruction* e *Formatting*, ganhe controle.  
3. **Refine pelo contexto:** use *Priming* ou *Role* para adequar o tom.  
4. **Pense em processos:** combine técnicas em fluxos lógicos.  
5. **Valide e experimente:** teste múltiplas versões e registre resultados.  
6. **Sempre cite fontes:** use *RAG* e *Recursos Externos* para basear respostas em fatos.  
7. **Reflita e melhore:** finalize com *Reflexive* ou *Meta Prompting*.

---

## 🧩 Estrutura Mestre – Prompt Profissional Completo

```markdown
# 🎭 Contexto e Papel
Você é {função/cargo}.  
Seu objetivo é {meta institucional}.  
Público-alvo: {tipo de leitor}.

# 🎯 Instrução
Sua tarefa é {tarefa principal}.  
Considere {regras, contexto ou documentos}.  
Use o tom {formal/técnico/consultivo}.  
Retorne o resultado no formato {tabela, texto, ofício, relatório, etc.}.

# 🧩 Etapas (se necessário)
1. Raciocine passo a passo.  
2. Consulte fontes (RAG) ou aja (ReAct).  
3. Gere a resposta.  
4. Revise o texto conforme critérios institucionais (Reflexive).

# 🔁 Melhoria Contínua
Explique como o prompt poderia ser otimizado (Meta Prompting).
```

---

## 🧠 Frase Final

> “A força da IA está no prompt, mas o poder do servidor público está em saber **planejar, testar e combinar** prompts com propósito.”

---
