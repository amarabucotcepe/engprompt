# 🧠 Curso de Engenharia de Prompt para Servidores Públicos

> **Autor:** Adriano Marabuco  
> **Técnica:** Zero-Shot Prompting  
  

---

## 🎯 Objetivo da Aula

Ensinar a técnica de **Zero-Shot Prompting**, usada quando **nenhum exemplo é fornecido à IA** — apenas **uma instrução clara e bem formulada**.
É o método mais direto e rápido, ideal quando:

* A tarefa é simples e inequívoca;
* O usuário quer testar o comportamento natural do modelo;
* Deseja avaliar se a IA compreende corretamente a instrução sem exemplos prévios.

> 💬 É como pedir algo a um servidor sem mostrar um modelo anterior — o resultado depende totalmente da **clareza da instrução**.

---

## 📘 Conceito

“Zero-Shot” significa literalmente **“zero exemplos”**.
Aqui, o sucesso depende da **precisão linguística do comando**: quanto mais específico, contextualizado e orientado for o pedido, mais adequado será o resultado.

> 🧩 Se o *Few-Shot* ensina por exemplo, o *Zero-Shot* ensina por clareza.

---

## ⚙️ Estrutura do Template Didático

```markdown
# 🎯 Instrução
Sua tarefa é {descrição da tarefa com clareza e contexto}.  
Considere {detalhes importantes, critérios, público-alvo, ou restrições}.  
Retorne o resultado no formato {texto, tabela, lista, parecer, resumo, etc.}.
```

### 🔍 Boas práticas

* Seja **específico**: substitua “faça um resumo” por “resuma em até 5 linhas destacando o problema, a causa e a solução”.
* Indique **formato de saída**: o modelo precisa saber se deve gerar texto corrido, lista, tabela etc.
* Adicione **critérios ou papéis** se necessário (ex: “como técnico de planejamento”).
* Evite perguntas ambíguas ou genéricas — *Zero-Shot* não tem contexto de reforço.

---

## 🧭 Exemplo Prático: Geração de Despacho Administrativo

```markdown
# 🎯 Instrução
Elabore um despacho administrativo comunicando que o pagamento de um contrato será realizado após liberação orçamentária pela SEPLAN.  
O texto deve seguir a linguagem formal da administração pública, em até 5 linhas.
```

**💬 Resultado Esperado:**

> Informo que o pagamento referente ao contrato mencionado será efetuado após a liberação orçamentária pela SEPLAN, conforme previsão vigente.
> Encaminhe-se à área financeira para acompanhamento e providências cabíveis.

## 📚 Referências:
- Brown, T. et al. *Language Models are Few-Shot Learners.* NeurIPS, 2020.  
  🔗 https://arxiv.org/abs/2005.14165