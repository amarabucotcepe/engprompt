# 🧠 Curso de Engenharia de Prompt para Servidores Públicos

> **Autor:** Adriano Marabuco  
> **Técnica:** Few-Shot Prompting  
  

---
## 🎯 Objetivo da Aula

Ensinar a técnica de **Few-Shot Prompting**, que consiste em fornecer **exemplos guiados** para que o modelo de IA aprenda o **padrão desejado de raciocínio ou resposta**.

Essa técnica é essencial quando queremos que a IA:

* Entenda regras de formatação ou estilo de resposta;
* Replique um padrão de decisão (classificação, análise, síntese, etc.);
* Aprenda a interpretar instruções ambíguas a partir de contextos anteriores.

---

## 📘 Conceito

O *Few-Shot Prompting* parte da ideia de que **exemplos ensinam a IA**.
Ao fornecer **poucos exemplos representativos**, o modelo compreende a lógica, o formato e o estilo desejados — sem precisar de treinamento adicional.

> 🧩 É como mostrar 2 ou 3 modelos de ofício para que o servidor aprenda o padrão de linguagem administrativa.
---

## ⚙️ Estrutura do Template Didático

```markdown
# 🎯 Instrução
Sua tarefa é {tarefa}.  
Retorne o resultado no formato {formato}.

# 🧩 Exemplos
Entrada: <exemplo 1 de entrada>  
Saída esperada: <resposta correspondente>

Entrada: <exemplo 2 de entrada>  
Saída esperada: <resposta correspondente>

Entrada: <exemplo 3 de entrada>  
Saída esperada: <resposta correspondente>

Entrada: {nova entrada que o aluno ou usuário deseja testar}
Resposta: 
```

### 🔍 Boas práticas

* Use **exemplos curtos e variados**, mas sempre dentro do mesmo padrão.
* Inclua **comentários explicativos** quando for usar o template.
* Comece com 2 a 3 exemplos e evolua conforme o modelo precise de mais contexto.
* Evite misturar tipos de resposta (ex: um exemplo analítico e outro descritivo).

---

## 🧭 Exemplo Prático: Classificação de Demandas Públicas

### Contexto

Servidores recebem mensagens de cidadãos via *Ouvidoria Digital* e precisam **classificá-las automaticamente** como:
**elogio**, **reclamação**, **solicitação**, **denúncia** ou **dúvida**.

---

### Template Aplicado

```markdown
# 🎯 Instrução
Sua tarefa é classificar a mensagem do cidadão em uma das seguintes categorias:
- Elogio  
- Reclamação  
- Solicitação  
- Denúncia  
- Dúvida  

Retorne o resultado no formato:  
**Categoria: <nome da categoria>**

# 🧩 Exemplos
Entrada: "Gostaria de parabenizar a equipe pelo atendimento rápido!"  
Saída esperada: Categoria: Elogio

Entrada: "Meu pedido ainda não foi atendido há mais de 30 dias."  
Saída esperada: Categoria: Reclamação

Entrada: "Quero saber como faço para emitir a segunda via do boleto."  
Saída esperada: Categoria: Dúvida

# Simulação:
Entrada: "O servidor da unidade de atendimento está cobrando propina para liberar documentos."
```

**Saída esperada:**

```
Categoria: Denúncia
```
---

## 📚 Referências:
- Brown, T. et al. *Language Models are Few-Shot Learners.* (Base conceitual)  
  🔗 https://arxiv.org/abs/2005.14165