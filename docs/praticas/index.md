# 🧭 Trilha de Práticas

As práticas são **dois encontros presenciais de 4 horas**. Elas levam você do prompt bem escrito até um fluxo de trabalho com agentes de IA. Depois do curso, há um **Desafio Final opcional**, para aplicar tudo ao seu município.

```text
Prática 1 ─────────────────►  Prática 2 ──────────────────────────►  Desafio Final
Engenharia de Prompt          Contexto + Fluxos com Agentes           (opcional, em casa)
"como pedir"                  "o que a IA vê" + "como ela trabalha"   "no meu município"
```

| Etapa | Duração | Foco | Avaliação |
| ----- | ------- | ---- | --------- |
| [Prática 1 — Engenharia de Prompt](pratica1_engenharia_de_prompt.md) | 4 h | 4 rodadas com sorteio de técnicas (Zero-Shot, Few-Shot, Instruction, Formatting, Priming, Role, Meta Prompt, CoT, Reflexive, RAG, ReAct) contra um grupo **sem IA** | Nota por grupo em cada rodada (Forms + Gemini) |
| [Prática 2 — Contexto e Agentes](pratica2_contexto_e_agentes.md) | 4 h | 4 rodadas com sorteio de estratégias: prompt puro × contexto (fontes, Gem/Projeto, resumo de estado) × agentes (pipeline, ferramentas, dois agentes) | Nota por grupo em cada rodada (Forms + Gemini) |
| [Desafio Final (opcional)](desafio_final.md) | em casa | Missão aplicada ao seu município, com dados públicos | Retorno formativo opcional (Forms + Gemini) |

---

## 🎲 Como funciona cada prática

Cada prática é um **experimento**: a turma descobre, com os próprios resultados, quanto a IA acrescenta ao trabalho e quanto cada técnica acrescenta à IA.

1. **Rodadas cronometradas em grupo.** São 4 rodadas por encontro. Em cada uma, **todos os grupos fazem a mesma tarefa** em 20 minutos, cada um com uma **carta sorteada**: uma técnica ou estratégia. Um grupo por rodada tira a carta **"Sem IA"** e faz o trabalho à mão: é a linha de base da comparação.
2. **Rodízio.** A cada rodada as cartas mudam de grupo. Assim, o resultado de uma técnica não depende de qual grupo a usou.
3. **Entrega pelo Google Forms.** Um envio por grupo, com o produto final e o relato de **como o grupo fez**.
4. **Correção automática em duas partes.**
    - **Qualidade (0–8):** o Gemini lê só o produto, **às cegas**: não sabe a carta nem se houve IA.
    - **Aderência à carta (0–2):** o Gemini identifica as técnicas pelo relato, sem saber a carta, e a planilha compara com a carta sorteada.
5. **Revelação.** Três saídas aparecem sem identificação, a turma vota na melhor e tenta adivinhar a técnica. Depois vem o quadro da rodada: carta, nota e tempo de cada grupo. No fim do dia, o quadro mostra a média de cada técnica contra o "Sem IA".

> 💡 A correção é, ela mesma, um **fluxo com agente**: formulário → Gemini → planilha → e-mail, com o professor no circuito. Na Prática 2 você vai analisar esse fluxo por dentro.

---

## 📏 Rubrica-base

A nota de cada rodada soma **10 pontos** (8 de qualidade + 2 de aderência à carta), e a rubrica de qualidade tem sempre um critério de **LGPD e ética**. Os critérios são escritos para serem **verificáveis**, por exemplo "usa dados de ≥ 2 fontes" ou "há aprovação humana antes do envio". Assim, a correção automática fica consistente e você sabe exatamente o que é esperado.

---

## 🛡️ Regras de ouro

- **Dados fictícios ou agregados, sempre.** Nunca cole nomes, CPFs, endereços, prontuários ou números de processo reais.
- **A IA recomenda; quem decide é a autoridade competente.**
- **Toda informação precisa ter origem.** Se não há fonte, a resposta certa é "não consta".
- **Quem assina responde.** Revisão humana antes de qualquer comunicação externa.

---

## 📚 Para revisar antes das práticas

- [Modelos de prompt](../modelos/0_zero_shot.md) e [Cheatsheet das técnicas](../modelos/Cheatsheet_Tecnicas_de_Prompt_Completo.md)
- [Fluxos de prompts](../aulas/fluxos.md) (base para a Prática 2)
- [LGPD e Compliance Prompting](../aulas/lgpd2.md)
