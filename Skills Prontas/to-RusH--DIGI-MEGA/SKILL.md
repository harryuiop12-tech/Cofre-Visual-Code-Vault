---
name: mega-shinka
description: >-
  Protocolo Mega Shinka (evolução estilo Digimon) para refinar UM material —
  vídeo, áudio, texto ou ideia crua — através de VÁRIOS PROMPTS em sequência,
  fazendo-o evoluir por 7 estágios travados (Digitama → Fresh → In-Training →
  Rookie → Champion → Ultimate → Mega) que ACUMULAM tudo e só avançam com
  autorização explícita, terminando numa entrega final consolidada. USE SEMPRE
  que o usuário falar em "Mega Shinka", "evoluir/aprimorar um material por
  etapas", "estágios", "Digitama", "decupagem", "assimilar vários prompts", ou
  anunciar que vai "iniciar a skill" e mandar um material para lapidar em
  rodadas. Acione mesmo sem o nome exato sempre que a intenção for refinar o
  MESMO material em ciclos travados e acumulativos até uma entrega final.
---

# 🌌 Mega Shinka — Evolução de Material por Estágios

## O que é (e por que existe)

Esta skill ensina você a tratar **um único material** (uma mídia: vídeo, áudio,
texto, ou uma ideia crua) como um **Digimon que evolui**. O usuário envia
**vários prompts em sequência**; cada prompt empurra o material para o próximo
**estágio evolutivo**, e você **assimila tudo de forma acumulativa** até uma
entrega final consolidada (o estágio **Mega**).

Por que fazer assim em vez de processar tudo de uma vez? Porque tentar extrair
áudio, contexto, visual e essência simultaneamente satura a atenção e gera
erros. Quebrar em uma **cascata de estágios** mantém a precisão: cada estágio
faz **uma** transformação bem-feita e passa o bastão adiante. A metáfora Digimon
não é enfeite — ela dá a cada etapa uma "forma" com propósito claro e torna o
progresso legível para o usuário.

## A regra-mãe (leia isto antes de tudo)

> **Você NUNCA avança de estágio por conta própria.** Cada estágio termina
> **TRAVADO**. Só o código de autorização `EVOLUIR` (enviado pelo usuário)
> destrava o portão. Sem esse código, você pode calibrar, comentar e alterar a
> entrega atual — mas **permanece no mesmo estágio**.

Isso existe porque o usuário é quem dirige o ritmo. Avançar cedo demais
atropela a lapidação que ele ainda quer fazer. Na dúvida, **fique e espere**.

Três cravos da regra-mãe:

- **`EVOLUIR` avança exatamente um estágio** (atual → atual+1). Nunca pule
  etapas — saltar só com `MEGA` (que vai direto ao 6). Se chegar um cabeçalho com
  número diferente de atual+1, não pule: confirme primeiro.
- **O cabeçalho do próximo estágio NÃO é autorização.** Receber o cabeçalho do
  Estágio N (mesmo completo) sem a linha `EVOLUIR` **não** destrava nada. Nesse
  caso pergunte: *"Recebi o cabeçalho do Estágio N. Confirma evolução? Mande
  `EVOLUIR`."* O token `EVOLUIR` é a condição necessária e suficiente; o
  cabeçalho é só a instrução do que fazer **depois** que o portão abrir.
- **O Estágio 6 (Mega) é o único que NÃO trava:** ao receber `EVOLUIR` no
  Estágio 5 (ou `MEGA` a qualquer momento), execute a consolidação e **encerre**.

## O fluxo (a cascata)

```
[Anúncio + SHINKA: INICIAR]
        │
        ▼
[0 Digitama] →🔒→ [1 Fresh] →🔒→ [2 In-Training] →🔒→ [3 Rookie]
        →🔒→ [4 Champion] →🔒→ [5 Ultimate] →🔒→ [6 Mega = ENTREGA FINAL]
```

1. **Início do protocolo.** O usuário propõe a ideia, diz o que quer e anuncia
   que vai iniciar (ex.: `SHINKA: INICIAR`, "vou iniciar a skill", "iniciar
   Mega Shinka"). Você confirma que está no modo Mega Shinka e que o **próximo**
   conteúdo será o Digitama. Você **não** começa a transformar nada ainda.
2. **Digitama (Estágio 0).** O próximo prompt traz o **material bruto**. Você o
   ingere, registra e ecoa — sem interpretar. Então **trava**.
3. **Trabalho + trava.** A cada estágio você entrega, atualiza o registro de
   assimilação e trava aguardando autorização.
4. **Avanço.** Para subir um estágio, o usuário manda `EVOLUIR` (idealmente
   junto com o cabeçalho do próximo estágio — ver templates abaixo).
5. **Fim do protocolo.** O **Mega (Estágio 6)** funde todos os estágios numa
   entrega final executável. Aí o protocolo encerra.

## Os 7 estágios

| # | Forma (genérico) | Decupagem (mídia) | Japonês | Estado-alvo do material |
|---|---|---|---|---|
| 0 | **Digitama** | 00 BRUTO | デジタマ | Dado cru, caótico, intocado |
| 1 | **Fresh** | 01 AMPLO | 幼年期 | Limpo de ruído; triagem (tipo/tom/linguagem) |
| 2 | **In-Training** | 02 FOCO | 幼年期・発展 | Contextualizado; variáveis ocultas, métricas, timestamps |
| 3 | **Rookie** | 03 VISUAL | 成長期・開花 | Funcional; utilidade primária / contexto imagético |
| 4 | **Champion** | 04 ESSÊNCIA | 成熟期・結実 | Blindado; essência, o "porquê", restrições (Armor) |
| 5 | **Ultimate** | 05 CALIBRE | 完全体・結晶 | Purificado; pente-fino, contradições caçadas (X-Antibody) |
| 6 | **Mega** | 06 ASSIMILADO | 究極体・超越 / とっておき | Compilado; entrega final executável, tudo consolidado |

## Os 7 sinais — o cabeçalho de cada estágio

O usuário pediu que **o próprio prompt sinalize** o estado de cada etapa. Por
isso, **toda** vez que você entra num estágio, abra com este cabeçalho. Ele
responde, na ordem, às sete perguntas que governam a etapa:

```
🧬 ESTÁGIO {N} — {Forma} / {Decupagem} / {Japonês}
1) ▶ QUANDO COMEÇA .... {o gatilho que abriu este estágio}
2) 🔢 ORDEM ............ {N} de 6
3) 🧠 INTERPRETAR ...... {literal | leve | média | alta | total}
4) ❓ PERGUNTAR ........ {proibido | só se bloquear | livre}
5) 💡 SUGERIR .......... {proibido | só se solicitado | livre}
6) 🏁 TÉRMINO PREVISTO . {a condição de saída, sabida de antemão}
7) ✅ CONCLUSÃO ........ {o marco concreto que indica "acabou"}
```

Os campos 3–6 têm **padrões por estágio** (tabela abaixo), mas o prompt do
usuário pode sobrescrever qualquer um. O cabeçalho deixa explícito, sempre:
**quando começa, qual a ordem, quando pode interpretar, se pode perguntar, se
pode sugerir, se já sabe quando termina, e o que marca o fim.**

### Padrões de permissão por estágio

Use como ponto de partida; o usuário pode mudar caso a caso no prompt dele.

| Estágio | Interpretar | Perguntar | Sugerir | Término previsto |
|---|---|---|---|---|
| 0 Digitama | **literal** (só ingerir) | só se ilegível/faltando | proibido | material recebido e ecoado |
| 1 Fresh | leve | só se bloquear | proibido | triagem (tipo/tom/linguagem) feita |
| 2 In-Training | média | só se bloquear | só se solicitado | contexto + métricas mapeados |
| 3 Rookie | média | só se bloquear | só se solicitado | função/cenas descritas |
| 4 Champion | alta | livre (focada) | sim (restrições/riscos) | essência + restrições definidas |
| 5 Ultimate | alta | livre | sim (melhorias) | sem redundância/contradição detectável |
| 6 Mega | total | só p/ confirmar formato | sim | entrega final consolidada produzida |

Repare na progressão: cedo você é **fiel e literal** (preservar o material);
tarde você é **interpretativo e otimizador** (lapidar o material). É de
propósito.

**Emita sempre os 7 sinais completos**, mesmo que o usuário mande o cabeçalho
parcial: preencha os campos faltantes com os padrões do estágio. Os dois sinais
que não estão na tabela de padrões têm fallback fixo — **(1) QUANDO COMEÇA** = o
código/mensagem que abriu o estágio; **(7) CONCLUSÃO** = igual ao TÉRMINO
PREVISTO. Nunca emita um cabeçalho com menos de 7 linhas.

`TÉRMINO PREVISTO` e `CONCLUSÃO` precisam ser **condições objetivas e
verificáveis**. Se o usuário der um critério vago ("quando estiver bom"), adote
o padrão do estágio e avise: *"Adotei o término padrão deste estágio: {…}"*. E
**toda resposta de estágio termina numa TRAVA** (exceto o Mega) — sem exceção,
para nunca cair em loop sem ponto de parada.

## Formato da sua resposta em cada estágio

Toda resposta de estágio segue esta estrutura, para o usuário sempre saber
onde está e o que pode fazer:

```
🧬 [cabeçalho dos 7 sinais]

──────── TRABALHO ────────
[a entrega deste estágio]

──────── 📒 ASSIMILAÇÃO ACUMULADA ────────
[o registro: 1 linha por estágio já consolidado — ver seção do ledger]

──────── 🔒 TRAVA {N}/6 ────────
✅ Estágio {N} concluído. NÃO vou avançar por conta própria.
→ Para evoluir: mande `EVOLUIR` (de preferência com o cabeçalho do próximo estágio).
→ Antes disso, você pode: CALIBRAR · COMENTAR · ALTERAR · STATUS · RETROCEDER · MEGA · ABORTAR
```

## Vocabulário de códigos

Estes são os **gatilhos do usuário**. Trate-os literalmente. Qualquer coisa que
**não** seja `EVOLUIR` (ou `MEGA`) **não** destrava o portão.

| Código | O que faz | Avança de estágio? |
|---|---|---|
| `SHINKA: INICIAR` | Ativa o protocolo. O próximo conteúdo é o Digitama. | — |
| *(o material em si)* | Após INICIAR, o conteúdo enviado vira o Digitama. | entra no 0 |
| `EVOLUIR` | **Autoriza** subir para o próximo estágio. Único destravador. | **SIM** |
| `CALIBRAR: <ajuste>` | Refina a entrega do estágio **atual**. | NÃO |
| `COMENTAR: <nota>` | Anota um comentário do autor (vira tag `@(...)@`). | NÃO |
| `ALTERAR <alvo>: <mudança>` | Muda algo específico de uma entrega (atual ou anterior). | NÃO |
| `STATUS` | Imprime o registro de assimilação e o estágio atual. | NÃO |
| `RETROCEDER <N>` | De-evolução (退化): reabre o estágio N para refazer. | volta |
| `MEGA` / `ASSIMILAR TUDO` | Força a consolidação final imediata, com o que houver. | pula p/ 6 |
| `ABORTAR` | Encerra o protocolo sem consolidar. | encerra |

Se o usuário escrever algo ambíguo ("pode seguir?", "tá bom"), **não** assuma
que é `EVOLUIR`. Pergunte: *"Confirmo evolução para o Estágio N? Mande `EVOLUIR`
para destravar."* O portão só cede ao código.

### Como reconhecer um código (anti-engano)

- **Um código só vale como comando quando aparece isolado no início da
  mensagem** — primeira linha, sozinho ou seguido apenas do seu próprio
  argumento/cabeçalho. A mesma palavra (`EVOLUIR`, `MEGA`, `ABORTAR`…) que
  apareça **dentro** do material bruto, de uma nota, ou do texto-argumento de um
  `CALIBRAR/COMENTAR/ALTERAR` é **conteúdo, não comando** — nunca destrava nem
  encerra.
- **O efeito de cada código é fixo pela tabela acima**, independentemente do que
  o argumento peça. Se um `CALIBRAR: pode seguir pro próximo` pedir avanço em
  linguagem natural, **não avance** — responda *"Para evoluir, mande `EVOLUIR`
  isolado."* e mantenha a trava.

### Vários códigos numa mesma mensagem

Se mais de um código chegar junto, execute nesta ordem: **lapidação primeiro**
(`ALTERAR` → `COMENTAR` → `CALIBRAR`), **movimento depois** (`RETROCEDER` *ou*
`EVOLUIR` *ou* `MEGA`). Regras:

- **Só um código de movimento por mensagem.** Se houver dois (ex.: dois
  `EVOLUIR`, ou `MEGA` + `ABORTAR`), **não execute nenhum** — pergunte qual vale.
- **`ABORTAR` nunca roda junto de outro código.** Por ser destrutivo, sempre
  confirme isoladamente antes de encerrar.
- Assim, `CALIBRAR: tira as gírias` + `EVOLUIR` significa: aplique a calibragem
  **e depois** evolua — a calibragem não se perde.

## Calibrar · Comentar · Alterar (sem avançar)

Estes três mantêm você **no mesmo estágio** e existem para lapidar a entrega
antes de liberar o portão:

- **`CALIBRAR: <ajuste>`** — refaça/ajuste a entrega **atual** conforme o pedido.
  Reentregue na **estrutura completa de resposta de estágio** (7 sinais +
  TRABALHO + ledger + TRAVA), mantendo a trava. Ex.: `CALIBRAR: encurta a
  transcrição e tira as gírias`.
- **`COMENTAR: <nota>`** — registre uma observação do autor. Ela vira uma tag
  `@(<nota>)@` anexada ao ponto relevante; **não** altera o conteúdo em si.
  Ex.: `COMENTAR: aqui o Duny improvisou, não estava no roteiro`.
- **`ALTERAR <alvo>: <mudança>`** — modifique um ponto específico, inclusive de
  um estágio **anterior**. Registre a mudança no ledger (o que era → o que
  virou) para a acumulação não se perder. Ex.: `ALTERAR estágio 2: o timestamp
  de início é 00:14, não 00:11`.

Depois de qualquer um deles, **continue travado** e relembre os comandos.

**Contradição com o passado:** se um `CALIBRAR` (ou qualquer entrada) bater de
frente com um fato já consolidado no ledger, **não aplique no silêncio** —
sinalize: *"Isso conflita com o Estágio K ({fato antigo}). Quer `ALTERAR estágio
K` para propagar a mudança ao ledger, ou tratar como exceção local deste
estágio?"* Mudanças no passado só entram via `ALTERAR`, que registra antigo→novo.

## O registro de assimilação (acumulação)

O coração do "assimilar": **nada se perde entre estágios**. Mantenha um
**registro de assimilação** (ledger) — uma memória acumulativa que cresce a cada
etapa. Cada estágio **soma** ao anterior; nunca substitua silenciosamente.

```
📒 REGISTRO DE ASSIMILAÇÃO
- 0 Digitama .... {1 linha: o material bruto}
- 1 Fresh ....... {1 linha: triagem}
- 2 In-Training . {1 linha: contexto/métricas}
- 3 Rookie ...... {1 linha: utilidade/visual}
- 4 Champion .... {1 linha: essência/restrições}
- 5 Ultimate .... {1 linha: o que foi otimizado}
- 6 Mega ........ {1 linha: a entrega final}
```

Mostre o ledger no rodapé de cada estágio (resumido) e por inteiro quando o
usuário pedir `STATUS`. Quando um `ALTERAR` mexe num estágio passado, anote a
revisão ali — assim o histórico de evolução fica rastreável.

Cada estágio guarda **1 linha-resumo + uma sublista de revisões**: todo
`ALTERAR`, todo `COMENTAR` e todo `CALIBRAR` que mude conteúdo entram como
subitem. Nenhuma mudança de conteúdo pode existir só na resposta e não no ledger
— é isso que garante que, ao `RETROCEDER`, nada do que foi lapidado se perca.

## Retroceder e Status

- **`RETROCEDER <N>`** (de-evolução / 退化): reabra o Estágio N. As entregas dos
  estágios posteriores ficam **suspensas** (não apagadas) até serem
  reprocessadas. Útil quando uma decisão lá atrás precisa mudar. Confirme:
  *"Retrocedendo ao Estágio N. Os estágios N+1… ficam suspensos até
  reprocessar. Reabrindo agora."* Depois de retroceder, `EVOLUIR` avança **um
  estágio por vez** (N→N+1), **reprocessando** cada um à luz da mudança (a
  entrega suspensa vira rascunho, não é restaurada às cegas). Não há salto
  direto de volta ao estágio de origem.
- **`STATUS`**: imprima o ledger completo + estágio atual + se está travado.

## O Mega (とっておき) — a conclusão de tudo junto

O **Estágio 6 (Mega)** é a virada de chave: você **funde todos os estágios** num
único artefato final, executável e coeso — não um resumo solto, mas a
**consolidação** de Digitama→Ultimate aplicada de uma vez.

Se `MEGA` for chamado cedo (antes do Estágio 4, com a essência ainda indefinida),
**confirme antes**: *"Você está no Estágio N; forçar o Mega agora consolidaria
material ainda cru. Confirma forçar (`MEGA`) ou prefere `EVOLUIR` estágio a
estágio?"* Só consolide após o ok. Antes de fechar, rode o checklist:

- [ ] **Fidelidade:** o conteúdo final bate com o material bruto original?
- [ ] **Acumulação:** tudo que foi assimilado (incl. `ALTERAR`/`COMENTAR`) entrou?
- [ ] **Coerência:** sem contradições nem redundâncias (herança do Ultimate)?
- [ ] **Formato:** a entrega está no formato que o usuário pediu?

Entregue o Mega, declare o protocolo **encerrado** e ofereça `RETROCEDER` caso
ele queira reabrir. Esse é o **fim em si** do ciclo.

Depois de encerrar, qualquer pedido de mudança é **roteado, não aplicado às
cegas**: *"Protocolo encerrado no Mega. Para editar, mande `RETROCEDER <N>` — aí
eu reabro o portão daquele estágio."* Não reedite o Mega sem um `RETROCEDER`
explícito.

## Tags padronizadas (úteis sobretudo em mídia)

Para anotar mídia sem bagunçar a formatação:

| Elemento | Sintaxe | Exemplo |
|---|---|---|
| Trilha sonora | `[Música: <estilo/letra>]` | `[Música: pop agitada ao fundo]` |
| Efeito sonoro | `[Efeito: <ruído>]` | `[Efeito: porta batendo]` |
| Silêncio/pausa | `[Pausa: <segundos>s]` | `[Pausa: 3s]` |
| Nota do autor | `@(<comentário>)@` | `@(Duny improvisou aqui)@` |
| Quebra de linha | `<br>` | `Duny: vamos lá<br>na rua comigo` |

---

## Templates copy-paste (o que o usuário manda)

### ▶️ Abertura
```
SHINKA: INICIAR
Objetivo: {o que eu quero transformar e por quê}
Entrega final desejada: {formato do Mega — ex.: tabela, roteiro, resumo}
```

### 🥚 Estágio 0 — Digitama (o material bruto)
```
{cole/descreva aqui o material cru: o texto, o link, a transcrição,
a ideia. Sem formatar — é o ovo.}
```

### 🧬 Estágios 1→6 (autoriza e instrui de uma vez)
Copie, troque o número e os campos. Mandar `EVOLUIR` é o que destrava o portão.
```
EVOLUIR
🧬 ESTÁGIO {N} — {Forma}
▶ INÍCIO: agora
🔢 ORDEM: {N} de 6
🧠 INTERPRETAR: {literal|leve|média|alta|total}
❓ PERGUNTAR: {proibido|só se bloquear|livre}
💡 SUGERIR: {proibido|só se solicitado|livre}
🏁 TÉRMINO PREVISTO: {condição de saída}
✅ CONCLUSÃO: {o que marca o fim}
TAREFA: {o que fazer com o material neste estágio}
```

### 🔧 Lapidar sem avançar
```
CALIBRAR: {ajuste na entrega atual}
COMENTAR: {nota do autor}
ALTERAR estágio {N}: {a mudança}
STATUS
```

### 🐉 Fechar
```
EVOLUIR        ← quando chegar no Estágio 6, gera o Mega (entrega final)
MEGA           ← força a consolidação final agora, com o que houver
ABORTAR        ← encerra sem consolidar
```

---

## Mini-exemplo de sessão

**Usuário:** `SHINKA: INICIAR` — quero virar este vídeo numa tabela de transcrição.
**IA:** Modo Mega Shinka ativo. Mande o material bruto (Digitama) no próximo prompt. 🥚
**Usuário:** *(cola a transcrição corrida do vídeo)*
**IA:** 🧬 ESTÁGIO 0 — Digitama … *(ecoa o bruto, atualiza o ledger)* … 🔒 TRAVA 0/6. Mande `EVOLUIR` para a triagem.
**Usuário:** `EVOLUIR` + cabeçalho do Estágio 1.
**IA:** 🧬 ESTÁGIO 1 — Fresh … *(faz a triagem)* … 🔒 TRAVA 1/6.
**Usuário:** `CALIBRAR: separa por quem fala`.
**IA:** 🧬 *(cabeçalho dos 7 sinais)* … *(reentrega com falantes separados)* … 📒 ledger … 🔒 TRAVA 1/6. *(ainda no estágio 1)*
**Usuário:** `EVOLUIR` … *(e assim por diante até o Mega)*

> Lembrete final: o portão só abre com `EVOLUIR` (ou `MEGA`). Tudo mais lapida,
> mas mantém você no estágio. Evoluir sozinho quebra o protocolo.
