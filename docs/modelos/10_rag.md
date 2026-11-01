# 🧠 Curso Inteligência Artificial no Serviço Público

> **Autor:** Adriano Marabuco
> **Técnica:** Retrieval-Augmented Generation (RAG)


---

## 🎯 Objetivo da Aula

Ensinar a técnica de **RAG**, que permite à IA **buscar informações relevantes em bases externas (ou internas)** antes de gerar a resposta.
Essa abordagem aumenta a **precisão**, a **atualização** e a **confiabilidade** das respostas, evitando que o modelo “invente” dados (*hallucinations*).

> 💬 É como um servidor que primeiro consulta o processo no SEI e depois redige o parecer.

---

## 📘 Conceito

O **RAG** combina duas etapas principais:

1. 🔎 **Retrieval (Recuperação):** a IA busca documentos ou trechos relevantes em uma base (ex: legislações, atas, contratos, relatórios).
2. 🧠 **Generation (Geração):** o modelo usa essas informações recuperadas para **gerar a resposta final contextualizada**.

Essa técnica cria uma **ponte entre dados e linguagem natural**, ideal para instituições públicas com grandes acervos documentais.

---

## ⚙️ Estrutura do Template Didático

```markdown
# 🎯 Instrução
Sua tarefa é responder à pergunta com base em informações obtidas de {fonte ou base de dados}.  
Primeiro, recupere os trechos relevantes da base (fase de *retrieval*).  
Em seguida, elabore uma resposta completa e contextualizada (fase de *generation*).  
Caso não encontre dados suficientes, informe isso explicitamente.

# 🧩 Estrutura Esperada
1. **Busca das informações relevantes**
2. **Síntese dos dados encontrados**
3. **Resposta gerada com base no conteúdo recuperado**
```

---

## 🧭 Exemplo Prático: Consulta Normativa

```markdown
# 🎯 Instrução
Com base nas normas de contratação pública vigentes, responda:
"É possível prorrogar contratos de manutenção predial além do prazo de 60 meses?"

Primeiro, recupere trechos relevantes da Lei nº 14.133/2021.  
Depois, gere a resposta final explicando a base legal da decisão.
```

**💬 Resultado Esperado (simulado):**

1. **Recuperação:**

   * Art. 107, §4º: admite prorrogação de contratos de serviços contínuos por até 60 meses, prorrogáveis em caráter excepcional por mais 12 meses.
2. **Síntese:**

   * Há limite de 60 meses, com possibilidade de prorrogação justificada.
3. **Resposta final:**

   > Sim. Contratos de manutenção predial contínua podem ser prorrogados além dos 60 meses, desde que haja justificativa técnica e autorização expressa, conforme art. 107, §4º, da Lei 14.133/21.

---

## 📊 Comparativo de Posição Didática

| Técnica                 | Nível                     | Foco Didático                        | Aplicação no Serviço Público                                          | Risco Principal                                     |
| ----------------------- | ------------------------- | ------------------------------------ | --------------------------------------------------------------------- | --------------------------------------------------- |
| **RAG**                 | 🔹 Intermediário-Avançado | Combinar busca e geração de conteúdo | Consultas normativas, sínteses de relatórios, pareceres fundamentados | Depende da qualidade e atualização da base de dados |
| **Chain of Thought**    | 🔸 Avançado               | Raciocínio passo a passo             | Análises complexas e decisões justificadas                            | Textos longos                                       |
| **self-reflexive Prompting** | 🔸 Avançado               | Autoavaliação da resposta            | Revisão e padronização textual                                        | Maior tempo de resposta                             |

---

## 🧩 Dica Extra: Como Aplicar RAG no Contexto Público

| Etapa                       | O que Fazer                                                                                                           | Exemplo Prático                                    |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- |
| **1. Base de Conhecimento** | Criar acervo com leis, editais, contratos e relatórios em formato texto.                                              | Pastas com PDFs normativos convertidos para texto. |
| **2. Indexação**            | Armazenar os documentos em um sistema de busca semântica (como FAISS, ElasticSearch ou ferramentas integradas de IA). | Ex: “Base Legislação MA 2024”                      |
| **3. Recuperação (Prompt)** | “Busque na base as normas sobre contratação temporária de pessoal e explique as restrições legais.”                   | IA retorna trechos e síntese.                      |
| **4. Geração (Resposta)**   | A IA produz a redação final com citações normativas.                                                                  | Parecer resumido pronto para despacho.             |

---

## 📚 Conclusão

O **RAG** é o elo entre **dados institucionais** e **inteligência artificial**.
Ele garante que a IA:

* Fale com **base em evidências reais**,
* Produza respostas **fundamentadas e auditáveis**,
* E respeite o **contexto jurídico e administrativo** do serviço público.

Referências:

- Lewis, P. et al. *Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks.* NeurIPS, 2020.  
  🔗 https://arxiv.org/abs/2005.11401
