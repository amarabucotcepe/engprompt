# 🧠 Módulo: Recursos e Multimodalidade na Engenharia de Prompt

> **Curso:** Engenharia de Prompt para Servidores Públicos
> **Autor:** Adriano Marabuco
> **Revisão Didática:** Prof. ChatGPT (IA Educacional)

---

## 🎯 Objetivo da Aula

Ensinar aos alunos que a IA não deve ser usada isoladamente.
O servidor moderno **combina recursos externos e modalidades de entrada** (texto, imagem, planilha, áudio, etc.) para **aumentar a precisão, contextualização e aplicabilidade prática** das respostas geradas.

> 💬 “A IA não é apenas uma ferramenta de texto — é um agente de integração de conhecimento.”

---

## 📘 Conceito Central

### 🔹 Recursos Externos

São elementos *fora do modelo*, mas que podem ser usados para complementar a resposta:

* Arquivos (PDFs, DOCXs, planilhas, imagens)
* Bases normativas, bancos de dados e APIs
* Ferramentas conectadas (calculadoras, tradutores, buscadores)
* Internet e repositórios institucionais

### 🔹 Multimodalidade

É a capacidade da IA de **interpretar e gerar múltiplos tipos de mídia**, como:

* 🖼️ Imagens (plantas, mapas, diagramas, relatórios fotográficos)
* 📄 Documentos e tabelas
* 🎧 Áudios e transcrições
* 📊 Gráficos e visualizações de dados
* 🗺️ Mapas e geoinformações

A combinação desses elementos transforma o modelo em **assistente cognitivo completo**.

---

## ⚙️ Estrutura Didática Recomendada

| Etapa                  | Tema                                                 | Estratégia Didática                               |
| ---------------------- | ---------------------------------------------------- | ------------------------------------------------- |
| **1. Introdução**      | Conceito de recursos e multimodalidade               | Exposição dialogada com exemplos reais            |
| **2. Demonstração**    | Exemplo prático com arquivo e imagem                 | IA analisando relatório fotográfico               |
| **3. Oficina prática** | Atividade com arquivos reais (PDF, planilha, imagem) | Grupos testando prompts multimodais               |
| **4. Integração**      | Conectar com outras técnicas (RAG, ReAct)            | Mostrando como essas técnicas usam dados externos |
| **5. Reflexão final**  | Discussão sobre limitações e boas práticas           | Debate guiado                                     |

---

## 🧩 Estrutura de Prompt Multimodal

```markdown
# 🎯 Instrução Multimodal
Você é {função}.  
Analise o(s) recurso(s) a seguir:  
- Arquivo: {nome ou tipo de arquivo}  
- Imagem: {descrição do conteúdo visual}  
- Planilha: {título ou campo de dados}  

Tarefa: {objetivo principal}.  
Explique o raciocínio, integre dados visuais e textuais, e gere o resultado no formato {texto/tabela/relatório}.
```

---

## 🧭 Exemplos Práticos

### 🏗️ Exemplo 1 — Análise Fotográfica Técnica

**Cenário:** Engenheiro da fiscalização envia 5 fotos da fachada de um prédio com rachaduras.

**Prompt:**

> “Analise as imagens anexadas e identifique indícios de patologias estruturais. Classifique os danos (baixo, médio, alto risco) e sugira medidas corretivas. Elabore um resumo técnico.”

**Resultado esperado:**

* Descrição visual detalhada
* Correlação com norma técnica (ex: NBR 15575)
* Tabela: *Local / Tipo de dano / Grau de risco / Ação recomendada*

---

### 📊 Exemplo 2 — Interpretação de Planilha

**Cenário:** Servidor de planejamento anexa planilha com metas e execução orçamentária.

**Prompt:**

> “Analise a planilha de execução orçamentária anexa e calcule o percentual de cumprimento de metas. Gere um gráfico de barras e um resumo textual destacando as três unidades com menor execução.”

**Resultado esperado:**

* Cálculos automáticos
* Visualização gráfica
* Síntese em texto executivo

---

### 📄 Exemplo 3 — Documento + Imagem

**Cenário:** Analista combina um PDF (relatório técnico) e uma imagem (foto de campo).

**Prompt:**

> “Com base no relatório técnico em PDF e nas imagens anexas, identifique discrepâncias entre o texto e a realidade fotografada. Liste inconsistências e proponha recomendações para o gestor.”

**Resultado esperado:**

* Confronto entre descrição e evidência visual
* Relatório final com recomendações fundamentadas

---

### 🔍 Exemplo 4 — Uso Combinado (RAG + Multimodal)

**Cenário:** Auditor deseja gerar relatório com base em norma (Lei 14.133/21) e documentos internos.

**Prompt:**

> “Busque nos arquivos anexos e na base normativa aplicável os dispositivos que regulam prorrogação contratual. Analise as imagens do relatório fotográfico e explique se as condições atendem ao previsto na legislação.”

**Resultado esperado:**

* Busca contextual (RAG)
* Interpretação visual (Multimodal)
* Conclusão jurídica fundamentada

---

## 🧰 Atividade Prática de Sala

1. Divida os alunos em grupos de 3.
2. Cada grupo recebe:

   * Um arquivo (PDF ou planilha)
   * Uma imagem (foto ou mapa)
3. Desafio: criar um prompt multimodal para gerar **relatório técnico integrado**.
4. Apresentar:

   * O prompt usado
   * A resposta obtida
   * Como os recursos externos influenciaram o resultado

---

## 💡 Dica do Professor

> “A multimodalidade transforma a IA em parceiro de campo, não apenas de gabinete.”
> Mostre aos alunos que:
>
> * A IA **interpreta imagens e documentos** com precisão contextual.
> * Combinar formatos diferentes **melhora a consistência técnica**.
> * O servidor pode usar multimodalidade para **validar, comparar e auditar** informações.

> Enfatize também os limites: a IA **não substitui laudos técnicos nem medições físicas** — ela **auxilia na interpretação** e **organização de evidências**.

---

## ⚠️ Boas Práticas e Cuidados

| Cuidados                        | Justificativa                                      |
| ------------------------------- | -------------------------------------------------- |
| Sempre citar fontes e anexos    | Transparência institucional                        |
| Explicitar formato de saída     | Evita erros de formatação                          |
| Controlar volume de dados       | Arquivos grandes podem gerar respostas incompletas |
| Pedir justificativas explícitas | Garante rastreabilidade do raciocínio              |
| Revisar informações sensíveis   | Imagens podem conter dados pessoais                |

---

## 🧭 Integração Didática

| Módulo                | Aplicação                                      |
| --------------------- | ---------------------------------------------- |
| **RAG**               | Consulta e citação de fontes externas          |
| **ReAct**             | Ações baseadas em evidências multimodais       |
| **Fluxos de Prompts** | Encadear análise de texto + imagem + relatório |
| **Experimentação**    | Testar diferentes combinações de formatos      |

---

## 🧩 Reflexão Final

> “A multimodalidade é o elo entre a IA e o mundo real.
> Ela permite que o servidor enxergue, compare e decida —
> com base em **fatos, imagens e dados**, e não apenas palavras.”

---

Referências:
- OpenAI. *GPT-4 Technical Report (Multimodal Capabilities).*  
  🔗 https://arxiv.org/abs/2303.08774  
- Google DeepMind. *Gemini: A Family of Highly Capable Multimodal Models.*  
  🔗 https://arxiv.org/abs/2312.11805