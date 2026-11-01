# 🃏 Guia das Cartas — Prática 1

Abra a seção da carta que o seu grupo tirou e siga o passo a passo. Os tempos somam **20 minutos**, o tempo de execução da rodada. A teoria de cada técnica está em **Modelos**, no menu do site; aqui está só **como jogar a carta**.

!!! abstract "📏 Regras para todas as cartas"

    - 🆕 **Conversa nova a cada rodada.** Nada do que foi feito na rodada anterior entra na conversa.
    - 📋 **Copie o enunciado da rodada exatamente como está** e cole as fontes que ele pede (F1, F2…). Os moldes abaixo indicam onde: `[ENUNCIADO DA RODADA]` e `[FONTES]`.
    - 🃏 **Use só a técnica da sua carta.** Os moldes já estão montados para isso: acrescentar papel, regras, exemplos ou estrutura que o molde não pede conta como outra técnica.
    - 🔄 **Não gostou da resposta?** Pode pedir para a IA gerar de novo (botão de refazer), sem mudar o prompt.
    - ✋ **Entreguem o texto que a IA produziu.** Só vale corrigir erro de digitação ou de formatação ao colar. Reescrever à mão mistura o trabalho do grupo com o da técnica.

!!! info "📨 Como preencher o \"Como fizemos\""

    Cole os prompts **na ordem**, trocando o que é igual para todos por marcadores:

    - o enunciado colado vira `[ENUNCIADO DA RODADA]`;
    - as fontes coladas viram `[FONTES: F1, F2]` (diga quais).

    Exemplo:

    ```text
    Mensagem 1:
    Você é assessor(a) técnico(a) de contratos da Secretaria de Infraestrutura...
    [ENUNCIADO DA RODADA]
    [FONTES: F1, F2]
    ```

    **Sem IA:** descreva o passo a passo do trabalho manual (quem fez o quê).

---

## 🚫 Sem IA { #sem }

**Em uma frase:** o grupo faz o trabalho como faria hoje, **sem nenhuma IA**. É a linha de base da comparação.

**⏱️ Passo a passo**

1. **(2 min)** Escolham onde escrever: papel, Bloco de Notas ou um editor **sem** recursos de IA. No Gmail e no Google Docs, não usem "Ajude-me a escrever" nem aceitem sugestões automáticas.
2. **(5 min)** Leiam o enunciado e as fontes que ele pede. Uma pessoa destaca os números e fatos que vão ser usados.
3. **(9 min)** Uma pessoa redige; as outras conferem cada dado com a fonte enquanto o texto avança.
4. **(4 min)** Revisão final (limite de linhas, dados, tom) e entrega.

**🚫 Não vale:** nenhum assistente de IA, tradutor com IA, corretor com IA ou sugestão automática de texto. Calculadora e editor de texto simples podem.

**📨 No "Como fizemos":** o passo a passo manual. Exemplo: *"Lemos F1 e F2 em papel; Ana marcou os números; João redigiu no Bloco de Notas; Maria conferiu os dados; 18 min."*

---

## 0️⃣ Zero-Shot { #zs }

**Em uma frase:** um pedido direto, **só a tarefa e os dados**, sem mais nada.

**⏱️ Passo a passo**

1. **(3 min)** Abram uma conversa nova e colem o molde abaixo, com o enunciado e as fontes.
2. **(2 min)** Enviem. Não acrescentem nenhuma frase ao molde.
3. **(10 min)** Leiam a resposta com atenção. Se estiver fraca, peçam para **gerar de novo** (no máximo 2 vezes), sem mudar o prompt, e escolham a melhor.
4. **(5 min)** Entreguem a resposta escolhida.

**📋 Molde**

```text
[ENUNCIADO DA RODADA]

[FONTES]
```

**🚫 Não faça:** dar papel à IA, listar regras, definir formato, dar exemplos ou pedir raciocínio. Qualquer um desses vira outra técnica.

---

## 🧪 Few-Shot { #fs }

**Em uma frase:** antes da tarefa, mostre de **2 a 4 exemplos** de entrada → saída. A IA aprende o padrão pelos exemplos.

**⏱️ Passo a passo**

1. **(8 min)** Escrevam de 2 a 4 exemplos **inventados pelo grupo**, do mesmo tipo da tarefa: um pedido curto e a resposta que vocês considerariam ideal. Os exemplos **não podem** ser itens da própria tarefa.
2. **(3 min)** Montem o prompt com o molde e enviem.
3. **(6 min)** Leiam a resposta. Se ela copiou um erro dos exemplos, corrijam o **exemplo** e enviem de novo em conversa nova.
4. **(3 min)** Entreguem.

**📋 Molde**

```text
Veja exemplos do que espero.

Exemplo 1
Entrada: [pedido inventado pelo grupo]
Saída: [resposta ideal]

Exemplo 2
Entrada: [pedido inventado pelo grupo]
Saída: [resposta ideal]

Agora faça o mesmo para o caso abaixo.

[ENUNCIADO DA RODADA]

[FONTES]
```

**🚫 Não faça:** escrever regras ("nunca", "sempre", "não use"), dar papel à IA, descrever o formato com seções ou pedir "pense passo a passo". O padrão tem que vir **só** dos exemplos.

**💡 Atenção:** a IA copia tudo dos exemplos, inclusive os defeitos. Exemplos ruins geram respostas ruins.

---

## 📐 Instruction { #ins }

**Em uma frase:** a tarefa mais uma **lista de regras** do que fazer e do que não fazer.

**⏱️ Passo a passo**

1. **(7 min)** Em grupo, escrevam de **3 a 6 regras**, pensando no que o produto precisa ter e no que ele **não pode** ter (tom, cuidados, limites). Uma regra por linha, numeradas.
2. **(3 min)** Montem o prompt com o molde e enviem.
3. **(7 min)** Confiram a resposta regra por regra. Se uma regra foi descumprida, deixem-na mais clara e enviem de novo em conversa nova.
4. **(3 min)** Entreguem.

**📋 Molde**

```text
[ENUNCIADO DA RODADA]

[FONTES]

Siga estas regras:
1. Não invente nomes, números, leis ou cláusulas.
2. Não inclua dados pessoais.
3. [regra do grupo]
4. [regra do grupo]
```

**🚫 Não faça:** desenhar seções ou modelo de saída (é Formatting), dar exemplos, dar papel à IA, pedir raciocínio, nem escrever "use somente as fontes" ou "cite a fonte" (é RAG).

---

## 🧾 Formatting { #fmt }

**Em uma frase:** você define a **estrutura exata da saída**: seções, ordem, tabela, tamanho.

**⏱️ Passo a passo**

1. **(6 min)** Leiam o enunciado e desenhem a "forma" do produto: quais seções ou colunas, em que ordem, e quanto cada uma ocupa. Exemplos de forma: um documento com título e seções nomeadas; uma tabela com colunas definidas.
2. **(3 min)** Montem o prompt com o molde e enviem.
3. **(7 min)** Confiram se a resposta seguiu a forma. Se não seguiu, deixem o modelo mais explícito e enviem de novo em conversa nova.
4. **(4 min)** Entreguem.

**📋 Molde**

```text
[ENUNCIADO DA RODADA]

[FONTES]

Apresente a resposta exatamente neste formato:

[NOME DA SEÇÃO 1]: [o que vai aqui, em até N linhas]
[NOME DA SEÇÃO 2]: [o que vai aqui]
[NOME DA SEÇÃO 3]: [o que vai aqui]

(ou uma tabela com as colunas: [coluna] | [coluna] | [coluna])
```

**🚫 Não faça:** lista de regras de conteúdo (é Instruction), exemplos preenchidos (é Few-Shot), papel ou pedido de raciocínio.

---

## 🎬 Priming { #pri }

**Em uma frase:** primeiro você **prepara o terreno** numa mensagem só de contexto; a tarefa vem **depois**, em outra mensagem.

**⏱️ Passo a passo**

1. **(6 min)** Preencham a mensagem 1: quem vocês são, para quem é o texto, qual o objetivo e a situação em 2 ou 3 linhas.
2. **(1 min)** Enviem a mensagem 1 e esperem a IA confirmar.
3. **(2 min)** Enviem a mensagem 2, com o enunciado e as fontes.
4. **(7 min)** Leiam a resposta; se estiver fraca, gerem de novo.
5. **(4 min)** Entreguem.

**📋 Molde: mensagem 1** (sem a tarefa)

```text
Daqui a pouco vou pedir um trabalho. Antes, o contexto:
- Quem somos: [setor da prefeitura]
- Para quem é o texto: [destinatário]
- Objetivo do texto: [o que ele precisa conseguir]
- Situação: [resumo do caso em 2 ou 3 linhas]
Responda apenas "entendi" e aguarde.
```

**📋 Molde: mensagem 2**

```text
[ENUNCIADO DA RODADA]

[FONTES]
```

**🚫 Não faça:** escrever "você é…" (é Role), listar regras, definir formato ou dar exemplos. "Quem somos" descreve o **grupo**, não a IA.

---

## 🎭 Role { #role }

**Em uma frase:** a IA assume um **papel profissional** — o de quem faria esse trabalho de verdade.

**⏱️ Passo a passo**

1. **(4 min)** Decidam quem, na prefeitura, faria este trabalho. Descrevam o papel em 1 ou 2 linhas: cargo, experiência e responsabilidade.
2. **(2 min)** Montem o prompt com o molde e enviem.
3. **(10 min)** Leiam a resposta. Se o tom não convencer, ajustem **só a descrição do papel** e enviem de novo em conversa nova.
4. **(4 min)** Entreguem.

**📋 Molde**

```text
Você é [cargo], com [experiência relevante], responsável por [responsabilidade].

[ENUNCIADO DA RODADA]

[FONTES]
```

**🚫 Não faça:** listar regras, definir seções de saída, dar exemplos ou pedir raciocínio. Todo o efeito tem que vir do papel.

---

## 🧭 Meta Prompt { #meta }

**Em uma frase:** você pede à IA que **escreva o melhor prompt** para a tarefa e depois usa esse prompt.

**⏱️ Passo a passo**

1. **(2 min)** Enviem a mensagem 1 (molde), com o enunciado e **sem** as fontes.
2. **(3 min)** Leiam o prompt que a IA escreveu. **Não editem**: só preencham o que ela deixou entre colchetes, se houver.
3. **(2 min)** Abram uma **conversa nova**, colem o prompt gerado e, embaixo, as fontes. Enviem.
4. **(9 min)** Leiam a resposta; se estiver fraca, gerem de novo.
5. **(4 min)** Entreguem.

**📋 Molde: mensagem 1**

```text
Escreva o melhor prompt possível para que uma IA faça a tarefa abaixo. O prompt
deve estar completo e pronto para usar. Não execute a tarefa: escreva só o prompt.

TAREFA:
[ENUNCIADO DA RODADA]
```

**📨 No "Como fizemos":** cole a mensagem 1 e, depois, o prompt que a IA gerou **entre estes marcadores**:

```text
PROMPT GERADO PELA IA <<<
(cole aqui)
>>>
[FONTES: F1, F2]
```

**🚫 Não faça:** acrescentar ao prompt gerado regras, papel ou exemplos escritos pelo grupo.

---

## 🧠 Chain of Thought { #cot }

**Em uma frase:** você pede que a IA **raciocine em etapas** antes de concluir.

**⏱️ Passo a passo**

1. **(3 min)** Montem o prompt com o molde e enviem.
2. **(8 min)** Leiam o raciocínio: cada etapa usa um dado correto da fonte? A conclusão decorre das etapas?
3. **(5 min)** Se o raciocínio tiver um erro, gerem de novo. O **produto final** é a resposta no formato e no tamanho que o enunciado pede; o raciocínio completo vai no "Como fizemos".
4. **(4 min)** Entreguem.

**📋 Molde**

```text
[ENUNCIADO DA RODADA]

[FONTES]

Antes de responder, pense passo a passo: primeiro identifique os dados das fontes
que importam para a tarefa, depois analise o que cada um indica e só então chegue
à conclusão. Mostre o raciocínio e, no fim, a resposta final.
```

**🚫 Não faça:** transformar as etapas numa lista numerada de regras (vira Instruction), dar papel, exemplos ou um modelo de saída com seções.

---

## 🔁 Reflexive { #ref }

**Em uma frase:** a IA faz uma primeira versão, **critica a própria resposta** e reescreve.

**⏱️ Passo a passo**

1. **(3 min)** Enviem a mensagem 1, com o enunciado e as fontes.
2. **(2 min)** Na **mesma conversa**, enviem a mensagem 2.
3. **(10 min)** Comparem a primeira versão com a reescrita. A crítica encontrou problemas reais?
4. **(5 min)** Entreguem a **versão reescrita**.

**📋 Molde: mensagem 1**

```text
[ENUNCIADO DA RODADA]

[FONTES]
```

**📋 Molde: mensagem 2**

```text
Agora critique a sua resposta: aponte dados errados ou inventados, trechos que não
respondem ao que foi pedido e problemas de clareza ou de tom. Depois reescreva a
resposta corrigindo tudo o que apontou.
```

**🚫 Não faça:** "revise como um especialista" (é Role), listar regras ou definir formato.

---

## 📚 RAG { #rag }

**Em uma frase:** a IA responde **somente com base nas fontes** que você colou e **cita** de onde tirou cada informação.

**⏱️ Passo a passo**

1. **(4 min)** Colem as fontes que o enunciado pede, cada uma com o rótulo dela ([F1], [F2]…).
2. **(2 min)** Montem o prompt com o molde e enviem.
3. **(10 min)** Confiram as citações: cada informação aponta para a fonte certa? Apareceu algo sem fonte?
4. **(4 min)** Entreguem.

**📋 Molde**

```text
Responda usando SOMENTE as fontes abaixo. Cite a fonte (F1, F2…) de cada
informação. Se algo não estiver nas fontes, escreva "não consta nas fontes".

FONTES
[F1] (cole)
[F2] (cole)

TAREFA
[ENUNCIADO DA RODADA]
```

**🚫 Não faça:** dar papel, acrescentar lista de regras, definir seções ou dar exemplos.

---

## 🔄 ReAct { #react }

**Em uma frase:** a IA trabalha em **ciclos**: pensa no que precisa, consulta uma fonte, observa o que encontrou e repete até concluir.

**⏱️ Passo a passo**

1. **(4 min)** Montem o prompt com o molde, com as fontes rotuladas, e enviem.
2. **(9 min)** Acompanhem os ciclos: cada "Ação" consulta uma fonte que existe? A "Observação" repete o que a fonte diz de verdade?
3. **(3 min)** O **produto final** é só a **Resposta final**, no formato e no tamanho que o enunciado pede. Os ciclos vão no "Como fizemos".
4. **(4 min)** Entreguem.

**📋 Molde**

```text
Resolva a tarefa em ciclos. Em cada ciclo, escreva:
Pensamento: o que preciso descobrir agora
Ação: consultar [F_]
Observação: o que a fonte diz
Repita os ciclos até ter tudo de que precisa. Então escreva "Resposta final:" e a
resposta.

FONTES
[F1] (cole)
[F2] (cole)

TAREFA
[ENUNCIADO DA RODADA]
```

**🚫 Não faça:** dar papel, acrescentar lista de regras ou exemplos.
