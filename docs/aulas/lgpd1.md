# 🛡️ Módulo: LGPD, Ética e Privacidade no Uso de Inteligência Artificial

> **Curso:** Inteligência Artificial no Serviço Público
> **Autor:** Adriano Marabuco
> 

---

## 🎯 Objetivo da Aula

Capacitar os alunos a **utilizar a IA de forma segura, ética e em conformidade com a Lei Geral de Proteção de Dados (LGPD – Lei nº 13.709/2018)**, evitando vazamento de informações pessoais, institucionais ou sigilosas durante o uso de modelos de linguagem e sistemas inteligentes.

> 💬 “Antes de conversar com a IA, o servidor precisa saber **o que pode e o que não pode ser dito**.”

---

## 📘 Conceito Central

A **LGPD** protege os direitos fundamentais de liberdade e privacidade.
No contexto do uso de IA, ela se aplica quando há **tratamento de dados pessoais** — qualquer informação que identifique ou possa identificar uma pessoa.

### 🔹 O que são dados pessoais:

* Nome, CPF, RG, endereço, telefone, e-mail;
* Dados funcionais de servidores ou cidadãos;
* Dados financeiros, contratuais, de saúde, biométricos;
* Fotos, voz ou localização geográfica identificável.

### 🔹 Dados sensíveis:

* Origem racial ou étnica, convicções religiosas, opiniões políticas, saúde, vida sexual, filiação sindical, dados genéticos ou biométricos.

### 🔹 Tratamento de dados:

É **toda operação realizada com dados**, como coleta, armazenamento, uso, transmissão, compartilhamento ou exclusão.

---

## ⚠️ Por que isso importa no uso de IA?

Quando um servidor digita um prompt em uma ferramenta de IA (como ChatGPT, Copilot, Gemini, etc.), ele **pode estar transmitindo dados para fora do ambiente institucional**.
Isso inclui:

* Dados pessoais de cidadãos;
* Informações sigilosas de processos;
* Dados administrativos, fiscais ou financeiros;
* Documentos oficiais e identificadores únicos.

Esses dados podem **ficar registrados em servidores externos**, mesmo que temporariamente — o que configura **tratamento fora do controle do órgão público**.

---

## 🧭 Princípios da LGPD aplicados ao uso de IA

| Princípio             | Aplicação Prática no Uso de IA                                          |
| --------------------- | ----------------------------------------------------------------------- |
| **Finalidade**        | Só use a IA para objetivos institucionais claros e legítimos.           |
| **Necessidade**       | Compartilhe apenas o mínimo de dados necessários para cumprir a tarefa. |
| **Adequação**         | Certifique-se de que o uso é compatível com a função pública.           |
| **Transparência**     | Registre e comunique o uso de IA nos processos, quando cabível.         |
| **Segurança**         | Não insira dados pessoais em plataformas sem garantias de proteção.     |
| **Prevenção**         | Antecipe riscos de vazamento ou uso indevido.                           |
| **Responsabilização** | O servidor é corresponsável pelos dados que envia.                      |

---

## 🧩 Exemplos Práticos

### ❌ Exemplo incorreto:

> “ChatGPT, escreva um parecer sobre o servidor João Silva, CPF 123.456.789-00, que foi afastado por motivo de saúde.”

➡️ **Erro:** vazamento de dados pessoais e de saúde — ambos sensíveis.
➡️ **Violação:** Art. 5º, II e Art. 11 da LGPD.
➡️ **Consequência:** tratamento irregular de dados sensíveis sem base legal.

---

### ✅ Exemplo correto:

> “Elabore um modelo genérico de parecer sobre afastamento de servidor por motivo de saúde, sem mencionar nomes ou dados pessoais.”

➡️ **Ajuste:** contexto preservado, sem identificar a pessoa.
➡️ **Conformidade:** uso legítimo e seguro da IA.

---

## 🧠 Boas Práticas para Prompts Seguros

| Boa Prática                           | Descrição                                                               |
| ------------------------------------- | ----------------------------------------------------------------------- |
| **Anonimize informações**             | Use expressões como “servidor X”, “contratante Y”, “empresa Z”.         |
| **Evite enviar documentos sigilosos** | Não envie PDFs, planilhas ou laudos que contenham dados pessoais.       |
| **Nunca insira dados de cidadãos**    | Substitua nomes e identificadores por placeholders.                     |
| **Descreva o contexto, não o dado**   | Explique a situação, mas não exponha indivíduos.                        |
| **Prefira ambientes controlados**     | Utilize versões corporativas da IA (com contrato de confidencialidade). |
| **Limite o escopo do prompt**         | Especifique o tipo de resposta, evitando exploração indevida.           |
| **Registre usos sensíveis**           | Em análises com dados públicos, mantenha logs e justificativas.         |

---

## 🔐 Ferramentas e Ambientes Seguros

| Ambiente                                                | Recomendação                                                   |
| ------------------------------------------------------- | -------------------------------------------------------------- |
| **ChatGPT (versão pública)**                            | Evite inserir qualquer dado pessoal ou institucional sensível. |
| **ChatGPT Enterprise / Copilot Gov / IA institucional** | Preferencial: dados tratados com confidencialidade contratual. |
| **Ambientes locais (on-premise)**                       | Ideais para processar informações de cidadãos ou servidores.   |
| **Ambientes de treinamento (sandbox)**                  | Use apenas dados fictícios e exemplos genéricos.               |

---

## 💬 Atividade Proposta

1. Liste 5 exemplos de prompts usados no trabalho cotidiano.
2. Identifique se há risco de exposição de dados pessoais.
3. Reescreva o prompt aplicando **anonimização e princípios da LGPD**.
4. Apresente ao grupo e discuta as adaptações necessárias.

---

## 💡 Dica do Professor

> “A LGPD não impede o uso de IA — ela exige responsabilidade.”
> Ensine aos alunos que **privacidade é parte da ética profissional**, e que o bom servidor:
>
> * Evita dados identificáveis;
> * Escreve prompts neutros;
> * Usa apenas o necessário para o propósito institucional.
>
> Mostre exemplos de boas e más práticas e discuta **o impacto reputacional** de vazamentos em órgãos públicos.

---

## 🧭 Integração com os Módulos Seguintes

| Módulo                         | Impacto da LGPD                                 |
| ------------------------------ | ----------------------------------------------- |
| **Fluxos de Prompts**          | Definir etapas seguras de manipulação de dados. |
| **Técnicas de Prompt**         | Evitar prompts com conteúdo sensível.           |
| **Recursos e Multimodalidade** | Controlar envio de arquivos e imagens pessoais. |
| **Experimentação**             | Garantir anonimização em testes e exemplos.     |

---

## ⚠️ Erros Comuns a Evitar

* Inserir dados de cidadãos, processos administrativos ou informações médicas.
* Copiar e colar e-mails internos ou planilhas de controle.
* Gerar relatórios com nomes ou cargos identificáveis.
* Usar IA pública para revisar contratos, pareceres ou laudos reais.
* Compartilhar prints de respostas de IA contendo dados sensíveis.

---

## 📚 Referências e Apoio

* **Lei Geral de Proteção de Dados Pessoais (Lei nº 13.709/2018)**
* **Guia de Boas Práticas da ANPD (Autoridade Nacional de Proteção de Dados)**
* **Enunciado CNJ nº 531** — sobre proteção de dados em atos judiciais
* **Portarias internas e normativas de segurança da informação (Ex: GSI/PR, ENAP)**

---

## 🧩 Reflexão Final

> “Usar IA com ética é proteger pessoas, reputações e instituições.”
>
> A inteligência artificial só é inteligente quando **respeita a privacidade, a legalidade e a confiança pública**.

---

Referências:
- Autoridade Nacional de Proteção de Dados (ANPD). *Guia de Boas Práticas e Governança de Dados.*  
  🔗 https://www.gov.br/anpd/pt-br/assuntos/guia-de-boas-praticas  
- CNJ. *Recomendações sobre o Uso Ético de Inteligência Artificial no Setor Público.*  
  🔗 https://atos.cnj.jus.br/atos/detalhar/atos-normativos?documento=3648  
- OpenAI. *Responsible AI Use and Data Privacy Principles.*  
  🔗 https://openai.com/safety  
- European Data Protection Board. *Guidelines on Artificial Intelligence and Data Protection.*  
  🔗 https://edpb.europa.eu/system/files/2023-05/edpb_guidelines_ai_en.pdf  
- ENAP. *Ética e Governança no Uso de Inteligência Artificial no Setor Público.* Brasília, 2023.  
  🔗 https://repositorio.enap.gov.br/handle/1/6882