# 🔒 Material do Professor — Correção automática com Google Forms + Gemini

Esta pasta fica **fora do site** (MkDocs publica apenas `docs/`). Ela reúne o que o professor precisa para avaliar as entregas.

| Arquivo | Entrega |
| ------- | ------- |
| [`pratica1_correcao.md`](pratica1_correcao.md) | Prática 1: 4 rodadas em grupo, com sorteio de técnicas |
| [`pratica2_correcao.md`](pratica2_correcao.md) | Prática 2: 4 rodadas em grupo, com sorteio de estratégias de contexto e agentes |
| [`desafio_final_correcao.md`](desafio_final_correcao.md) | Desafio Final (opcional, formativo) |

Cada arquivo traz:
- os campos do formulário e suas variáveis;
- o gabarito de referência;
- o(s) **prompt(s) de correção**;
- as entregas de calibração.

As práticas também trazem a **matriz de rodízio** das cartas e as **fórmulas da planilha** do quadro de resultados. O sorteio e o cronômetro ficam no **Painel do Professor** (`…/praticas/painel/`), e o roteiro de condução, com as surpresas de cada rodada, fica na página **Condução das Práticas** (`…/praticas/conducao/`). As duas estão fora do menu e da busca do site e só abrem pelo endereço direto. Os alunos seguem os **Guias das Cartas** (`cartas_pratica1.md` e `cartas_pratica2.md`, no menu): os moldes de lá foram escritos para que o Prompt B classifique cada carta sozinha. Se mudar um molde, refaça a calibração por carta.

> ⚠️ O repositório é público. Qualquer pessoa que encontrar esta pasta pode ler os gabaritos. Se isso for um problema para a turma, mantenha uma cópia privada (Drive ou repositório privado) e apague daqui.

---

## Visão geral do fluxo

**Práticas 1 e 2 (rodadas em grupo):** dois passos do Gemini, separados para que a avaliação de qualidade seja às cegas.

```text
Google Forms ──► Workspace Studio ──────────────────────────────────────────────────
                 1. Starter: When a form response comes in
                 2. Ask Gemini (Prompt A) → qualidade do PRODUTO, sem saber a carta
                 3. Ask Gemini (Prompt B) → técnicas (P1) ou contexto e fluxo (P2), lendo só o "como fizemos"
                 4. Sheets: Add a row → rodada, grupo, carta e as duas saídas
                 5. Send an email → retorno ao relator do grupo
                 ─────────────────────────────────────────────────────────────────
Planilha ──► aba Cálculos (nota, aderência, minutos) ──► aba Quadro (projetada)
```

**Desafio Final (individual, opcional):** um passo do Gemini, como no fluxo abaixo, sem a parte de cartas.

```text
Starter → Ask Gemini (correção) → Extract (nota) → Sheets: Add a row → Send/Draft an email
```

Faça **um formulário e um fluxo por entrega**: um para a Prática 1, um para a Prática 2 e um para o Desafio Final.

---

## Pré-requisitos

- Conta **Google Workspace de trabalho ou escola** com o **Workspace Studio** e os recursos do **Gemini** liberados pelo administrador. Em contas pessoais, o Studio só está disponível para quem participa do programa *Google Workspace Experiments*.
- Alguns passos podem exigir **aprovação do administrador** de segurança. Teste com antecedência.
- Contas de alunos menores de 18 anos não usam recursos de IA. Isso não afeta o fluxo, porque ele roda na conta do professor.

Referência oficial: [Guide to Starters & Steps in Workspace Studio](https://support.google.com/workspace-studio/answer/16765661).

> Os nomes das opções abaixo seguem a documentação do Google em inglês. Na interface em português, os rótulos podem mudar um pouco.

---

## Passo a passo

### 1. Criar o formulário
1. Crie o Google Forms com **exatamente** os campos listados na seção 1 do arquivo de correção da entrega. Use os mesmos títulos de pergunta para facilitar o mapeamento das variáveis.
2. Em **Configurações → Respostas**, ajuste:
   - **Desative "Restringir a usuários de [sua organização]".** Em contas Workspace essa opção costuma vir ligada, e servidores de outras prefeituras não conseguem nem abrir o formulário.
   - **Coletar endereços de e-mail → "Entrada do respondente".** É o padrão recomendado para turmas de várias prefeituras, já que muitos servidores usam e-mail institucional fora do Google. A opção *Verificado* obriga a fazer login com uma conta Google. O lado ruim da *Entrada do respondente* é que, se o aluno digitar o e-mail errado, o feedback não chega. Por isso, avise a turma.
3. Marque como obrigatórios todos os campos que entram na rubrica.
4. Na descrição do formulário, inclua o aviso de transparência:

   ```text
   Sua entrega será analisada automaticamente pelo Gemini com a rubrica publicada
   na página da prática, e você receberá o retorno por e-mail. O professor revisa
   os casos de dúvida. Não inclua dados pessoais reais (seus ou de terceiros).
   Para contestar a nota, responda ao e-mail de retorno.
   ```

5. Crie a planilha de controle:
   - **Práticas:** abas `Respostas`, `Inícios`, `Cálculos` e `Quadro`, exatamente como na seção "Planilha e fórmulas" do arquivo de correção.
   - **Desafio Final:** uma aba com as colunas abaixo.

   | Data/hora | Nome | E-mail | Nota | Feedback | Revisado pelo professor |
   | --------- | ---- | ------ | ---- | -------- | ----------------------- |

### 2. Criar o fluxo no Workspace Studio

**Práticas (rodadas)**
1. **Starter:** `When a form response comes in` → selecione o formulário da prática.
2. **Step `Ask Gemini` (Prompt A — Qualidade):** cole o Prompt A e insira só as variáveis `{{rodada}}` e `{{produto}}`.
3. **Step `Ask Gemini` (Prompt B — Classificação):** cole o Prompt B e insira só a variável `{{como}}`.
4. **Step `Sheets › Add a row`** na aba `Respostas`: data da resposta, Rodada, Grupo, Carta sorteada, saída do passo 2 e saída do passo 3. Não use o Extract: a aba `Cálculos` tira a nota e a classificação das saídas com fórmulas. As colunas da P2 são diferentes das da P1 (contexto e fluxo em vez de técnicas): siga a seção "Planilha e fórmulas" de cada arquivo.
5. **Step `Send an email`** para o e-mail do respondente. Assunto: `Retorno – Prática 1, Rodada ` (ou `Prática 2`) + variável Rodada. Corpo: saída do passo 2, uma linha em branco, saída do passo 3 e o rodapé abaixo. Nas rodadas, prefira o envio automático: o retorno faz parte da revelação.
6. Ative o fluxo.

> ⏱️ **Latência:** são 10 envios por rodada, cada um com dois passos do Gemini. Não há garantia de que tudo termine em 5 minutos. Por isso a revelação começa pela **vitrine com voto cego**, que não depende das notas; enquanto a turma vota, a planilha se completa. Meça o tempo real na calibração.

**Desafio Final**
1. **Starter:** `When a form response comes in` → selecione o formulário.
2. **Step `Ask Gemini`:**
   - cole o **prompt de correção** (seção 3 do arquivo de correção);
   - substitua cada `{{variável}}` pelo chip da resposta correspondente, com **+ Variables** → pergunta do formulário. Faça isso inclusive com o `{{nome}}` que aparece no formato de saída;
   - formato de saída: **texto**.
3. **Step `Extract`:**
   - entrada: a resposta do passo *Ask Gemini*;
   - item personalizado: `nota_total`, com a descrição *"número que aparece após 'NOTA_TOTAL:', de 0 a 10"*.

   **Plano B:** se o Extract não aparecer como variável no passo seguinte, pule esta etapa. Grave só o feedback completo (coluna E) e calcule a nota na coluna D da planilha com a fórmula `=REGEXEXTRACT(E2;"NOTA_TOTAL:\s*(\d+)")`.
4. **Step `Sheets › Add a row`:** na planilha de controle, mapeie as colunas para as variáveis:
   - **Data/hora:** data da resposta;
   - **Nome:** resposta do campo nome;
   - **E-mail:** e-mail do respondente;
   - **Nota:** `nota_total`;
   - **Feedback:** saída do *Ask Gemini*.

   Deixe a coluna **Revisado pelo professor** vazia.
5. **Envio ao aluno:** escolha um dos dois steps.
   - **`Send an email`**: envio automático.
     - **To:** variável *e-mail do respondente*.
     - **Assunto:** `Retorno – Desafio Final`.
     - **Corpo:** saída do *Ask Gemini*, seguida do rodapé:

       ```text
       —
       Correção automática feita pelo Gemini com a rubrica da prática.
       Discorda de algum ponto? Responda este e-mail que o professor revisa.
       ```

   - **`Draft an email`**: o rascunho fica para o professor revisar e enviar. É a opção com **humano no circuito**, recomendada na primeira turma ou no Desafio Final.
6. Ative o fluxo.

### 3. Testar antes da aula (obrigatório)
Use os testes de **calibração** de cada arquivo de correção. Nas práticas, confira também se a aba `Cálculos` calcula a aderência e os minutos, e se o `Quadro` atualiza. No Desafio Final:

- [ ] Envie a entrega **fraca** e confira se a nota ficou na faixa esperada.
- [ ] Envie a entrega **forte** e confira se a nota ficou na faixa esperada.
- [ ] Envie o **teste de injeção**, nas duas variantes ("ignore a rubrica" e "fechar o delimitador"). A nota **não** pode subir.
- [ ] Envie uma entrega **de uma conta de fora do seu domínio**, como um Gmail pessoal ou o e-mail de outra prefeitura. Confirme que o formulário abre e que o **e-mail de retorno chega**. A política do administrador pode bloquear o envio de e-mails para domínios externos.
- [ ] Confirme que o e-mail chegou com o formato correto, começando por `NOTA_TOTAL:`.
- [ ] Confirme que a planilha recebeu a linha e que a coluna **Nota** tem só o número.
- [ ] Envie a mesma entrega **duas vezes**. Se as notas diferirem em mais de 1 ponto, deixe os descritores da rubrica mais objetivos.

Se alguma nota sair fora da faixa, ajuste primeiro os **descritores da rubrica** no prompt. Evite acrescentar regras soltas.

---

## Durante e depois da aula

- **Revisão por amostragem.** Filtre na planilha:
  - notas ≤ 4;
  - notas 10;
  - qualquer feedback que mencione LGPD com 0 ponto.

  Revise esses casos e marque **Revisado pelo professor**.
- **Contestações.** Respostas ao e-mail chegam ao professor. Se corrigir uma nota, registre o motivo na planilha. Esse histórico ajuda a calibrar o prompt para a próxima turma.
- **Uso didático.** A planilha é o **log do agente**. Na Prática 2, ela é material da rodada sobre agentes: mostre como o fluxo de correção decide, registra e onde o professor entra.
- **Privacidade.** As entregas são processadas pelo Gemini dentro do Workspace da instituição. Guarde a planilha só pelo tempo necessário ao curso e não reutilize as entregas para outros fins sem consentimento.
