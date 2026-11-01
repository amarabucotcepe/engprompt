# 🧠 Curso Inteligência Artificial no Serviço Público

> **Autor:** Adriano Marabuco
> **Técnica:** Formatting Prompting


---

## 🎯 Objetivo da Aula

Ensinar a técnica de **Formatting Prompting**, que consiste em **controlar o formato da saída da IA** — ou seja, **como** o resultado deve ser apresentado.

Essa técnica é essencial para o serviço público, pois a maioria dos resultados precisam seguir **padrões documentais, tabelas, campos de formulário, planilhas textuais ou modelos oficiais**.

> 💬 “O conteúdo importa, mas o formato comunica.”

---

## 📘 Conceito

O *Formatting Prompting* direciona o modelo para **estruturar a resposta conforme uma moldura definida pelo usuário**.
Isso garante **organização, padronização e facilidade de uso posterior** (por exemplo, copiar direto para um relatório ou planilha).

Pode ser combinado com outras técnicas (como *Few-Shot* ou *Priming*) para criar templates complexos de alta consistência.

---

## ⚙️ Estrutura do Template Didático

```markdown
# 🎯 Instrução
Sua tarefa é {tarefa}.  
Apresente o resultado no formato {especifique o formato de saída desejado}.

# 🧩 Formato esperado
{modelo de estrutura ou moldura, ex: tabela, checklist, campos numerados, etc.}

Exemplo:
| Campo | Descrição | Status |
|-------|------------|---------|
| ... | ... | ... |
```

### 🔍 Boas práticas

* Mostre um **modelo visual de formato** (mesmo que vazio).
* Use símbolos de separação (|, —, *) para tabelas ou listas.
* Combine com instruções de estilo (“use linguagem formal”, “limite a 3 itens”).
* Peça sempre **título + corpo + conclusão**, quando o texto for institucional.

---

## 🧭 Exemplo Prático: Relatório de Ocorrências em Obras

```markdown
# 🎯 Instrução
Liste as principais ocorrências registradas durante a vistoria de obras públicas.  
Apresente o resultado no formato de tabela, com as seguintes colunas:
| Tipo de Ocorrência | Descrição | Ação Recomendada | Prazo para Correção |
```

**💬 Resultado Esperado:**

| Tipo de Ocorrência | Descrição                                     | Ação Recomendada                           | Prazo para Correção |
| ------------------ | --------------------------------------------- | ------------------------------------------ | ------------------- |
| Infiltração        | Vazamento visível em área de cobertura        | Reaplicar manta asfáltica e revisar calhas | 15 dias             |
| Fiação exposta     | Cabo elétrico sem isolamento adequado         | Substituir e instalar conduíte rígido      | 7 dias              |
| Piso danificado    | Cerâmica trincada na área de acesso principal | Substituir peças danificadas               | 10 dias             |

---

## 📚 Referências:

- OpenAI Docs. *Structured Outputs and Formatting Guide.*  
  🔗 https://platform.openai.com/docs/guides/prompt-engineering  
- OpenAI. *JSON mode and structured outputs.*  
  🔗 https://platform.openai.com/docs/guides/structured-output