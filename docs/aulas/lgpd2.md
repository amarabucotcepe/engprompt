# 🛡️ Módulo Avançado: Engenharia de Prompt em Conformidade com a LGPD

> **Curso:** Inteligência Artificial no Serviço Público
> **Autor:** Adriano Marabuco
> 

---

## 🎯 Objetivo

Ensinar **como elaborar prompts eficazes, detalhados e específicos** sem violar a **Lei Geral de Proteção de Dados (LGPD)** — garantindo **segurança, anonimização e finalidade legítima** no uso da IA em órgãos públicos.

> 💬 “Não é sobre ocultar informação — é sobre estruturar o contexto de forma responsável e técnica.”

---

## 📘 Conceito-Chave: *Compliance Prompting*

**Compliance Prompting** é a aplicação dos princípios da LGPD **dentro da construção do prompt**.
Ele busca o equilíbrio entre **utilidade** e **conformidade legal**, permitindo que o servidor explore a IA de forma **contextual e segura**.

---

## ⚙️ Princípios do Compliance Prompting

| Princípio                     | Como aplicar no prompt                                                                                                        |
| ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Anonimização ativa**        | Substitua dados reais por marcadores neutros (`[SERVIDOR_X]`, `[CIDADÃO_Y]`) e descreva o perfil funcional, não a identidade. |
| **Contextualização segura**   | Inclua o cenário, o objetivo institucional e o tipo de documento, sem expor informações pessoais.                             |
| **Finalidade explícita**      | Explique à IA o propósito da consulta — ex: “para fins de modelo administrativo” — reduzindo risco de uso indevido.           |
| **Minimização de dados**      | Evite inserir qualquer dado irrelevante para o resultado esperado.                                                            |
| **Rastreabilidade e revisão** | Estruture prompts que permitam auditoria, incluindo metadados e justificativa do uso.                                         |

---

## 🧩 Estrutura Modelo de Prompt com LGPD Compliance

```markdown
# 🎭 Contexto Institucional
Você é {função pública} e deve produzir {tipo de documento}.

# 🧱 Dados Simulados
Use dados fictícios ou anonimizados para fins de exemplo.  
Substitua informações pessoais por placeholders (ex: [SERVIDOR_X], [EMPRESA_Y]).

# 🎯 Finalidade
O objetivo é {propósito legítimo}, respeitando a LGPD e o sigilo administrativo.

# 🧠 Tarefa
Com base em {normas, regulamentos, diretrizes}, elabore {resultado desejado}.

# ⚖️ Conformidade
Não inclua nenhum dado real, pessoal ou sigiloso.  
Explique como o conteúdo gerado pode ser usado de forma ética e segura.
```

---

## 🧭 Exemplos Práticos de Prompts Conformes

### ✅ **Exemplo 1 – Parecer sobre afastamento de servidor**

**Errado:**

> “Elabore um parecer sobre o afastamento do servidor João Silva, CPF 123.456.789-00, lotado na SEFAZ.”

**Correto:**

> “Elabore um modelo de parecer sobre afastamento temporário de servidor público, respeitando a legislação trabalhista e os princípios da administração.
> Use dados fictícios (ex: [SERVIDOR_X]) e descreva as etapas do processo administrativo.”

**🧠 Técnica aplicada:** *Anonimização + Finalidade explícita*

---

### ✅ **Exemplo 2 – Auditoria de contrato**

**Errado:**

> “Analise o contrato nº 345/2023 entre a SEPLAN e a empresa Construtora Delta Ltda.”

**Correto:**

> “Elabore um checklist de verificação de conformidade contratual com base na Lei 14.133/21, considerando contratos de obras públicas.
> Use nomes genéricos (ex: [ÓRGÃO_CONTRATANTE], [EMPRESA_EXECUTORA]) e descreva as cláusulas críticas a avaliar.”

**🧠 Técnica aplicada:** *Contextualização segura + Minimização de dados*

---

### ✅ **Exemplo 3 – Revisão de relatório médico pericial**

**Errado:**

> “Revise o relatório médico do servidor Pedro Costa, CID F32, anexo em PDF.”

**Correto:**

> “Revise um modelo genérico de relatório médico pericial para uso em processos de afastamento por saúde, verificando clareza e conformidade com o formato administrativo.
> Não utilize dados pessoais nem diagnósticos reais.”

**🧠 Técnica aplicada:** *Anonimização ativa + Propósito legítimo*

---

### ✅ **Exemplo 4 – Análise de Ouvidoria**

**Errado:**

> “Classifique as mensagens de Maria Oliveira e Carlos Souza enviadas à ouvidoria.”

**Correto:**

> “Crie um modelo de categorização de manifestações de ouvidoria (elogio, denúncia, sugestão, reclamação) com base em exemplos fictícios.”

**🧠 Técnica aplicada:** *Generalização de contexto + Simulação controlada*

---

## 🧰 Técnicas Específicas de Prompt Seguro

| Técnica                         | Descrição                                                   | Aplicação Prática                                                            |
| ------------------------------- | ----------------------------------------------------------- | ---------------------------------------------------------------------------- |
| **Placeholder Prompting**       | Substitui nomes e identificadores por códigos ou etiquetas. | “[CIDADÃO_1], [SERVIDOR_2], [EMPRESA_X]”                                     |
| **Synthetic Context Prompting** | Cria situações verossímeis com dados simulados.             | “Considere um cenário hipotético em que um contrato público é aditivado.”    |
| **Purpose Framing**             | Explicita o objetivo legítimo do uso.                       | “Para fins de treinamento e padronização de relatórios.”                     |
| **Privacy Reminder Loop**       | Reforça a conformidade em cada etapa do fluxo.              | “Antes de prosseguir, confirme que não há dados pessoais nesta análise.”     |
| **Compliance Meta Prompt**      | Pede que a IA valide se o prompt está em conformidade.      | “Verifique se este prompt viola algum princípio da LGPD e explique por quê.” |

---

## ⚖️ Template de Verificação de Conformidade

```markdown
# 🔍 Checagem LGPD
Analise o prompt abaixo e verifique se ele contém risco de violar a LGPD.  
Classifique como:
- SEGURO: sem dados pessoais ou sensíveis  
- MODERADO: contexto potencialmente identificável  
- CRÍTICO: contém dados pessoais, sensíveis ou sigilosos  

Explique brevemente o motivo e sugira ajustes.

Prompt analisado: "{texto}"
```

➡️ Essa técnica cria **uma camada de autocontrole** dentro do próprio fluxo de prompts (*Meta Compliance*).

---

## 🧠 Boas Práticas para Prompts Eficazes e Seguros

| Prática                                                   | Benefício                                                      |
| --------------------------------------------------------- | -------------------------------------------------------------- |
| Especifique o contexto institucional, não o indivíduo     | Mantém riqueza de informação sem violar privacidade            |
| Estruture o raciocínio com dados genéricos, mas realistas | Garante utilidade sem risco jurídico                           |
| Use perguntas orientadas à norma, não à pessoa            | Direciona a IA para o conhecimento técnico                     |
| Solicite citações normativas e justificativas             | Aumenta precisão e responsabilidade                            |
| Valide a saída antes de compartilhar                      | Evita respostas que contenham dados simulados realistas demais |

---

## 💬 Atividade Proposta

1. Selecione 3 prompts que você usaria no seu trabalho real.
2. Reescreva-os aplicando **técnicas de Compliance Prompting** (anonimização, finalidade, framing).
3. Use o **template de checagem LGPD** para validar a conformidade.
4. Compare resultados com colegas e discuta:

   * O prompt ficou menos eficaz?
   * Ou se tornou mais claro e auditável?

---

## 💡 Dica do Professor

> “A eficiência não está em pedir mais, mas em pedir certo.”
>
> Ensine os alunos que prompts bem projetados **preservam o contexto técnico** sem violar a privacidade.
> Mostre que **um bom prompt de compliance** é aquele que:
>
> * Explica o *porquê* da tarefa,
> * Define o *escopo* dos dados,
> * E documenta o *uso legítimo* da IA.

---

## 🧭 Integração Didática

| Módulo Posterior               | Relação com Compliance Prompting                              |
| ------------------------------ | ------------------------------------------------------------- |
| **Fluxos de Prompts**          | Introduz checkpoints de privacidade em cada etapa.            |
| **RAG**                        | Define o que pode ser buscado e citado em conformidade legal. |
| **ReAct**                      | Aplica validação antes de executar ações externas.            |
| **Experimentação**             | Permite testar diferentes níveis de anonimização e eficácia.  |
| **Recursos e Multimodalidade** | Controla o envio e análise de arquivos e imagens.             |

---

## 🧩 Reflexão Final

> “A IA não viola a LGPD — quem viola é o usuário mal instruído.”
>
> O engenheiro de prompt ético **conhece a lei, domina a técnica e desenha a conversa com responsabilidade.**


Referências:

Autoridade Nacional de Proteção de Dados (ANPD). Guia de Boas Práticas e Governança de Dados. 2023.

CNJ. Recomendações sobre o Uso Ético de Inteligência Artificial no Setor Público. 2022.

OpenAI. Responsible AI Use and Data Privacy Principles. 2024.

European Data Protection Board. Guidelines on AI and Data Protection. 2023.

ENAP. Ética e Governança no Uso de Inteligência Artificial no Setor Público. Brasília, 2023.