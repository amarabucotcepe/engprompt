# 🧠 Curso Inteligência Artificial no Serviço Público

> **Autor:** Adriano Marabuco
> **Técnica** Chain of Thought (CoT) — Raciocínio Passo a Passo


---

## 🔷 Introdução ao Módulo

Os **prompts avançados** são usados quando desejamos que a IA **raciocine, avalie, simule papéis institucionais ou reflita sobre a própria resposta**.
Essas técnicas ampliam a autonomia do modelo e trazem resultados de nível analítico e estratégico — ideais para **pareceres técnicos, decisões complexas, sínteses administrativas e treinamentos internos**.

---

## 🧩 1. **Chain of Thought (CoT)** — *Raciocínio Passo a Passo*

---

### 🎯 Objetivo da Aula

Ensinar a IA a **explicar o raciocínio** antes de apresentar a resposta final.
Essa técnica melhora a **transparência**, a **coerência** e a **precisão** em tarefas analíticas e decisórias.

> 💬 É como pedir ao servidor: “explique o raciocínio antes de chegar à conclusão”.

---

### 📘 Conceito

No *Chain of Thought Prompting*, o modelo é instruído a **pensar em etapas** — primeiro analisar, depois concluir.
O resultado é uma resposta mais estruturada e confiável.

---

### ⚙️ Estrutura do Template Didático

```markdown
# 🎯 Instrução
Sua tarefa é {tarefa analítica}.  
Pense passo a passo antes de responder.  
Explique cada etapa do seu raciocínio e, ao final, apresente a conclusão em um parágrafo separado com o título “Conclusão:”.

# 🧩 Exemplo de Estrutura Esperada
1. Análise inicial dos fatos
2. Interpretação normativa ou técnica
3. Comparação de alternativas
4. Conclusão final
```

---

### 🧭 Exemplo Prático: Análise de Pedido de Aditivo Contratual

```markdown
# 🎯 Instrução
Analise se o pedido de aditivo contratual apresentado pela empresa é justificável.  
Pense passo a passo antes de responder e finalize com uma conclusão.
```

**💬 Resultado Esperado:**

1. O contrato original previa prazo de 90 dias para execução.
2. A empresa justificou o atraso em função de chuvas intensas, comprovadas por boletins meteorológicos.
3. O fiscal do contrato atestou a paralisação temporária e recomendou prorrogação.
   **Conclusão:** O pedido de aditivo é justificável, pois as condições climáticas configuram caso fortuito, amparado pela Lei 14.133/21, art. 124.

Referências:

- Wei, J. et al. *Chain-of-Thought Prompting Elicits Reasoning in Large Language Models.* NeurIPS, 2022.  
  🔗 https://arxiv.org/abs/2201.11903  
- Kojima, T. et al. *Large Language Models are Zero-Shot Reasoners.* ACL, 2022.  
  🔗 https://arxiv.org/abs/2205.11916