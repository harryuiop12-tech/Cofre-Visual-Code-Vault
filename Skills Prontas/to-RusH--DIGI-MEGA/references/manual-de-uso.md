# 📖 Manual de Uso Completo — `to-RusH--DIGI-MEGA` (Mega Shinka)

> Documento de referência exaustivo da skill. O `SKILL.md` é o **motor** (as
> regras que a IA segue). Este manual é o **guia do usuário**: explica, no
> detalhe, como você opera a skill, todos os comandos, todos os estágios, todos
> os caminhos possíveis e **tudo o que pode acontecer** em cada um deles —
> incluindo dois passo-a-passo completos (um genérico e um específico).
>
> Leitura rápida? Vá direto à seção **2 (ciclo em 30 segundos)** e à **8
> (exemplo específico)**. Quer dominar tudo? Leia na ordem.

---

## Índice

1. [O que é a skill e quando usá-la](#1-o-que-é-a-skill-e-quando-usá-la)
2. [O ciclo em 30 segundos](#2-o-ciclo-em-30-segundos)
3. [Anatomia de uma rodada (o que você manda × o que a IA devolve)](#3-anatomia-de-uma-rodada)
4. [Referência completa dos comandos](#4-referência-completa-dos-comandos)
5. [Os 7 estágios, destrinchados](#5-os-7-estágios-destrinchados)
6. [Todos os caminhos: tudo que pode acontecer](#6-todos-os-caminhos-tudo-que-pode-acontecer)
7. [Exemplo GENÉRICO completo (de ponta a ponta)](#7-exemplo-genérico-completo)
8. [Exemplo ESPECÍFICO completo (caso real de mídia)](#8-exemplo-específico-completo)
9. [Erros comuns, armadilhas e FAQ](#9-erros-comuns-armadilhas-e-faq)
10. [Folha de cola (cheat sheet)](#10-folha-de-cola)

---

## 1. O que é a skill e quando usá-la

A `to-RusH--DIGI-MEGA` faz uma IA **refinar um único material em rodadas**, como
um Digimon que **evolui por estágios**. Em vez de pedir tudo de uma vez, você
manda **vários prompts em sequência**; cada um empurra o material para o próximo
estágio, a IA **acumula** o que já foi feito, e **só avança quando você
autoriza**. No fim, o estágio **Mega** funde tudo numa entrega final.

**Use quando** você quer:

- Transformar uma mídia (vídeo, áudio, texto, ideia crua) com controle fino,
  etapa por etapa.
- Lapidar um resultado aos poucos, podendo revisar cada fase antes de seguir.
- Garantir que nada se perca no caminho (tudo fica registrado no *ledger*).
- Decupar/transcrever mídia com precisão (caso clássico).

**Não use quando** você só quer uma resposta única e rápida — aí é melhor um
pedido normal, sem o ritual de estágios.

---

## 2. O ciclo em 30 segundos

```
Você: SHINKA: INICIAR + diz o objetivo
  └─ IA entra em modo Mega Shinka e pede o material.
Você: (cola o material bruto)          → vira o DIGITAMA (Estágio 0)
  └─ IA ingere, mostra o ledger e TRAVA 🔒.
Você: EVOLUIR (+ cabeçalho do estágio)  → sobe um estágio
  └─ IA trabalha o estágio e TRAVA 🔒 de novo.
        ↑ (repete: EVOLUIR para subir; CALIBRAR/ALTERAR/COMENTAR para lapidar
           sem subir; STATUS para ver tudo; RETROCEDER para voltar)
Você: EVOLUIR no Estágio 5  → IA gera o MEGA (Estágio 6) e ENCERRA. 🐉
```

**Regra de ouro:** a IA **nunca** avança sozinha. O portão de cada estágio só
abre com `EVOLUIR` (ou `MEGA`). Tudo o mais lapida, mas mantém você no estágio.

---

## 3. Anatomia de uma rodada

Cada vez que você está num estágio, a interação tem duas metades.

### 3.1 O que VOCÊ manda

Um dos comandos (seção 4). Para **avançar**, o ideal é mandar `EVOLUIR` seguido
do **cabeçalho do próximo estágio**, que diz à IA como tratar aquela fase:

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

Você **não precisa** preencher todos os campos: o que faltar, a IA completa com
os **padrões do estágio** (seção 5). Mas preencher dá controle total.

### 3.2 O que a IA DEVOLVE

Sempre na mesma estrutura, para você nunca se perder:

```
🧬 [cabeçalho com os 7 sinais — sempre completo]

──────── TRABALHO ────────
[a entrega deste estágio]

──────── 📒 ASSIMILAÇÃO ACUMULADA ────────
[o ledger: 1 linha-resumo por estágio + revisões]

──────── 🔒 TRAVA {N}/6 ────────
✅ Estágio concluído. Não vou avançar sozinho.
→ EVOLUIR para subir · CALIBRAR/COMENTAR/ALTERAR para lapidar · STATUS · RETROCEDER · MEGA · ABORTAR
```

O **único estágio que não termina em trava é o Mega (6)** — ele entrega e
encerra.

**Garantia de não-perda:** toda calibragem, comentário ou alteração que mude
conteúdo é gravada como **subitem de revisão** no bloco `📒 ASSIMILAÇÃO
ACUMULADA` (que neste manual chamamos informalmente de *ledger*) — nunca fica só
na resposta. É por isso que um `RETROCEDER` nunca perde o que você lapidou.

### 3.3 Os 7 sinais (o cabeçalho), um por um

| # | Sinal | O que responde |
|---|---|---|
| 1 | ▶ **QUANDO COMEÇA** | o que disparou este estágio (qual comando/mensagem) |
| 2 | 🔢 **ORDEM** | a posição na cascata (ex.: 3 de 6) |
| 3 | 🧠 **INTERPRETAR** | se é execução literal ou se a IA pode/deve interpretar |
| 4 | ❓ **PERGUNTAR** | se a IA pode te fazer perguntas (proibido/só se bloquear/livre) |
| 5 | 💡 **SUGERIR** | se a IA pode sugerir melhorias (proibido/só se solicitado/livre) |
| 6 | 🏁 **TÉRMINO PREVISTO** | a condição de saída — você já sabe quando acaba |
| 7 | ✅ **CONCLUSÃO** | o marco concreto que indica que **acabou de fato** |

**Você não precisa preencher todos.** O que faltar, a IA completa com os padrões
do estágio (seção 5). Os dois sinais que **não** estão na tabela de padrões têm
preenchimento fixo: **(1) QUANDO COMEÇA** = o comando que abriu o estágio; **(7)
CONCLUSÃO** = o mesmo texto do TÉRMINO PREVISTO. O cabeçalho **nunca** sai com
menos de 7 linhas.

---

## 4. Referência completa dos comandos

Para cada comando: **o que faz**, **sintaxe**, **avança ou não**, **exemplo** e
— o mais importante para "todos os caminhos" — **o que acontece se você usar
fora de hora**.

### 4.1 `SHINKA: INICIAR` — ligar a skill
- **Faz:** entra no modo Mega Shinka. A IA confirma e avisa que o **próximo**
  conteúdo será o Digitama. Ela **não** começa a transformar nada ainda.
- **Variações aceitas:** "vou iniciar a skill", "iniciar Mega Shinka", "iniciar
  to-RusH--DIGI-MEGA".
- **Boas práticas:** já diga o **objetivo** e a **entrega final desejada**.
- **Se usado fora de hora:** se já estiver numa sessão, a IA pergunta se você
  quer reiniciar (descartando o progresso) ou continuar.

### 4.2 *(o material)* — o Digitama
- **Faz:** o conteúdo que você manda logo após o INICIAR vira o **Estágio 0
  (Digitama)** — o material bruto. A IA ingere, ecoa e trava.
- **Sintaxe:** texto livre, link, transcrição colada, descrição da ideia.
- **Se mandado antes do INICIAR:** a IA trata como conversa normal, **não** como
  Digitama, até você ligar a skill.

### 4.3 `EVOLUIR` — autorizar o avanço (o destravador)
- **Faz:** **único** comando que abre o portão. Sobe **exatamente um** estágio
  (atual → atual+1).
- **Sintaxe:** `EVOLUIR` isolado na primeira linha (idealmente + cabeçalho do
  próximo estágio).
- **No Estágio 5 → 6:** `EVOLUIR` faz a IA **gerar o Mega e encerrar**.
- **Se o número do cabeçalho não for atual+1:** a IA **não pula** — pergunta se
  você confirma ir para atual+1. Não existe pulo para um estágio intermediário:
  `EVOLUIR` sobe sempre +1, e o único salto possível é `MEGA`, que vai **direto
  ao 6 (entrega final) e encerra**.
- **Se mandado sem nada mais:** a IA avança usando os **padrões** do próximo
  estágio.
- **Se a palavra "evoluir" aparecer dentro de um texto/argumento:** **não conta**
  como comando (ver 4.x "reconhecimento").

### 4.4 `CALIBRAR: <ajuste>` — lapidar a entrega atual (sem subir)
- **Faz:** refaz/ajusta a entrega do **estágio atual** conforme seu pedido.
  Reentrega na estrutura completa (7 sinais + trabalho + ledger + trava).
- **Não avança.**
- **Exemplo:** `CALIBRAR: encurta a transcrição e tira as gírias`.
- **Se o argumento pedir para avançar** ("CALIBRAR: pode seguir"): a IA **não
  avança** — lembra que avanço só com `EVOLUIR`.

### 4.5 `COMENTAR: <nota>` — anotar sem mudar o conteúdo
- **Faz:** registra uma observação do autor. Ela vira uma tag `@(<nota>)@`
  anexada ao ponto relevante e entra no ledger. **Não** altera o conteúdo.
- **Não avança.**
- **Exemplo:** `COMENTAR: aqui o apresentador improvisou, não estava no roteiro`.

### 4.6 `ALTERAR <alvo>: <mudança>` — corrigir algo específico (inclusive no passado)
- **Faz:** modifica um ponto específico de uma entrega — do estágio atual **ou
  de um anterior**. Registra no ledger o "antes → depois", para a acumulação não
  se perder.
- **Não avança.**
- **Exemplo:** `ALTERAR estágio 2: o timestamp de início é 00:14, não 00:11`.
- **Diferença de CALIBRAR:** `CALIBRAR` mexe na entrega **atual** em geral;
  `ALTERAR` faz uma mudança **pontual e rastreável**, podendo mirar o passado.

### 4.7 `STATUS` — ver onde você está
- **Faz:** imprime o **ledger completo** + estágio atual + se está travado.
- **Não avança.** Pode ser mandado a qualquer momento.

### 4.8 `RETROCEDER <N>` — de-evolução (退化)
- **Faz:** reabre o **Estágio N**. As entregas dos estágios posteriores ficam
  **suspensas** (não apagadas) até serem reprocessadas.
- **Depois de retroceder:** `EVOLUIR` reprocessa **um por vez** (N→N+1),
  refazendo cada estágio à luz da mudança (a entrega suspensa vira rascunho).
- **Exemplo:** `RETROCEDER 1` (voltar à triagem porque o idioma estava errado).
- **Bordas:** `RETROCEDER 0` reabre o próprio Digitama (raro, mas válido).
  `RETROCEDER` para o estágio atual ou para um número inexistente faz a IA pedir
  um N válido.

### 4.9 `MEGA` / `ASSIMILAR TUDO` — forçar a consolidação final
- **Faz:** pula direto para o **Estágio 6** e consolida tudo o que houver, depois
  encerra.
- **Avança (salto) para o 6.**
- **Se chamado cedo (antes do Estágio 4):** a IA **confirma antes**, avisando que
  consolidaria material ainda cru.

### 4.10 `ABORTAR` — encerrar sem consolidar
- **Faz:** encerra o protocolo **sem** gerar o Mega. O que foi feito fica no
  histórico, mas não há entrega final consolidada.
- **Sempre confirmado isoladamente** (é destrutivo).

### 4.11 Reconhecimento de comando (anti-engano) — importante
- Um código **só vale como comando** quando aparece **isolado no início da
  mensagem** (primeira linha, sozinho ou seguido só do próprio argumento).
- A mesma palavra dentro do material, de uma nota ou do texto de um
  `CALIBRAR/COMENTAR/ALTERAR` é **conteúdo, não comando** — não destrava nem
  encerra.

### 4.12 Vários códigos numa mensagem
- Ordem de execução: **lapidação primeiro** (`ALTERAR`→`COMENTAR`→`CALIBRAR`),
  **movimento depois** (`RETROCEDER`/`EVOLUIR`/`MEGA`).
- **Só um código de movimento por mensagem.** Dois (ex.: `MEGA`+`ABORTAR`) →
  a IA não executa nenhum e pergunta qual vale.
- `CALIBRAR: x` + `EVOLUIR` = aplica a calibragem **e depois** evolui.

---

## 5. Os 7 estágios, destrinchados

Para cada estágio: **o que entra**, **o que sai**, os **padrões de permissão** e
**como sobrescrever**. Lembre: os padrões são ponto de partida — seu cabeçalho
manda.

| # | Forma | Decupagem | Japonês | Estado-alvo |
|---|---|---|---|---|
| 0 | **Digitama** | 00 BRUTO | デジタマ | dado cru, intocado |
| 1 | **Fresh** | 01 AMPLO | 幼年期 | limpo de ruído; triagem (tipo/tom/linguagem) |
| 2 | **In-Training** | 02 FOCO | 幼年期・発展 | contextualizado; variáveis, métricas, timestamps |
| 3 | **Rookie** | 03 VISUAL | 成長期・開花 | funcional; utilidade primária / contexto imagético |
| 4 | **Champion** | 04 ESSÊNCIA | 成熟期・結実 | blindado; essência, o "porquê", restrições |
| 5 | **Ultimate** | 05 CALIBRE | 完全体・結晶 | purificado; pente-fino, contradições caçadas |
| 6 | **Mega** | 06 ASSIMILADO | 究極体・超越 / とっておき | compilado; entrega final, tudo consolidado |

**Padrões de permissão:**

| Estágio | Interpretar | Perguntar | Sugerir | Término padrão |
|---|---|---|---|---|
| 0 Digitama | literal (só ingerir) | só se ilegível | proibido | material recebido e ecoado |
| 1 Fresh | leve | só se bloquear | proibido | triagem feita |
| 2 In-Training | média | só se bloquear | só se solicitado | contexto + métricas mapeados |
| 3 Rookie | média | só se bloquear | só se solicitado | função/cenas descritas |
| 4 Champion | alta | livre (focada) | sim (restrições/riscos) | essência + restrições definidas |
| 5 Ultimate | alta | livre | sim (melhorias) | sem redundância/contradição |
| 6 Mega | total | só p/ confirmar formato | sim | entrega final produzida |

**Lendo a tabela:** cedo a IA é **fiel e literal** (preserva o material); tarde
ela é **interpretativa e otimizadora** (lapida). É de propósito — você não quer
a IA "melhorando" o material cru antes de ele estar mapeado.

**Como sobrescrever:** basta pôr o campo no cabeçalho. Ex.: quer que a IA já
sugira no Estágio 1? Mande `💡 SUGERIR: livre`. Quer proibir perguntas no
Estágio 4? Mande `❓ PERGUNTAR: proibido`.

> Nota: o cabeçalho de cada estágio também inclui o **nome japonês** da forma
> (ex.: Mega = 究極体・超越 / とっておき) — é só sabor, não muda nada.

### 5.1 Tags padronizadas (para mídia)

A IA conhece um conjunto de tags para anotar mídia sem bagunçar a formatação —
úteis sobretudo na decupagem/transcrição (o caso-âncora da skill). Você pode
pedir que sejam usadas; elas aparecem nas entregas dos estágios 3–6.

| Elemento | Sintaxe | Exemplo |
|---|---|---|
| Trilha sonora | `[Música: <estilo/letra>]` | `[Música: pop agitada ao fundo]` |
| Efeito sonoro | `[Efeito: <ruído>]` | `[Efeito: porta batendo]` |
| Silêncio/pausa | `[Pausa: <segundos>s]` | `[Pausa: 3s]` |
| Nota do autor | `@(<comentário>)@` | `@(improvisou aqui)@` |
| Quebra de linha | `<br>` | `vamos lá<br>na rua comigo` |

A tag `@(...)@` é exatamente o que o comando `COMENTAR:` gera.

---

## 6. Todos os caminhos: tudo que pode acontecer

Esta é a seção "exaustiva". Pense no protocolo como uma **máquina de estados**.
A qualquer momento você está num **estado**, e cada **comando** leva a um
**resultado**. Abaixo, o que acontece com cada comando em cada estado.

### 6.1 Estados possíveis
- **A — Fora da skill** (ainda não deu INICIAR).
- **B — Ligada, esperando o Digitama** (deu INICIAR, ainda não mandou material).
- **C — Travado num estágio 0–5** (entrega feita, aguardando você).
- **D — Reprocessando** (depois de um RETROCEDER, subindo de novo).
- **E — Encerrado** (Mega entregue, ou ABORTAR).

> Nota de fidelidade: o motor garante explicitamente o ritual de travas, o
> avanço só por `EVOLUIR`/`MEGA`, o roteamento via `RETROCEDER` após o Mega e a
> confirmação isolada do `ABORTAR`. As células dos estados **D** e **E** abaixo
> descrevem o **comportamento esperado e coerente** nesses casos (ex.: reiniciar
> com um novo `INICIAR`), não uma garantia rígida do motor.

### 6.2 O que cada comando faz em cada estado

| Comando \ Estado | A (fora) | B (espera Digitama) | C (travado 0–5) | E (encerrado) |
|---|---|---|---|---|
| `SHINKA: INICIAR` | liga a skill | já ligada (segue esperando) | pergunta se reinicia | inicia uma **nova** sessão |
| *(material)* | conversa normal | vira o Digitama (estágio 0) | tratado como conteúdo p/ o estágio atual | conversa normal |
| `EVOLUIR` | nada (não há o que evoluir) | nada (mande o material antes) | **sobe +1**; no 5→gera Mega e encerra | nada (use RETROCEDER) |
| `CALIBRAR:` | — | — | refaz o estágio atual, **trava** | — (sugere RETROCEDER) |
| `COMENTAR:` | — | — | anota `@()@`, **trava** | — |
| `ALTERAR:` | — | — | muda ponto (atual/passado), **trava** | — (sugere RETROCEDER) |
| `STATUS` | — | mostra estado vazio | mostra ledger + estágio | mostra ledger final |
| `RETROCEDER N` | — | — | volta ao N, suspende posteriores | **reabre** o N |
| `MEGA` | — | — | consolida (confirma se < estágio 4) | nada (já encerrado) |
| `ABORTAR` | — | encerra (nada feito) | confirma e encerra sem Mega | nada |

### 6.3 Casos de borda e o que a IA faz

- **Você manda só o cabeçalho do próximo estágio, sem `EVOLUIR`.** → A IA **não
  sobe**. Ela pergunta: "Recebi o cabeçalho do Estágio N. Confirma evolução?
  Mande `EVOLUIR`." (O cabeçalho é instrução, não autorização.)
- **Você escreve algo ambíguo** ("pode seguir?", "tá bom"). → A IA **não assume**
  que é EVOLUIR; pede o código.
- **Você manda `EVOLUIR` pedindo pular do 1 para o 4.** → A IA **não pula** (não
  há salto para estágio intermediário); oferece ir para o 2, ou usar `MEGA` para
  ir **direto ao 6 e encerrar**.
- **Você manda `CALIBRAR`/`COMENTAR`/`ALTERAR` (ou qualquer entrada) que
  contradiz um fato de um estágio anterior** (ex.: o idioma). → A IA **sinaliza o
  conflito** e pergunta se você quer `ALTERAR` o estágio passado (propagando no
  ledger) ou tratar como exceção local.
- **Você manda dois comandos de movimento** (ex.: `MEGA` + `ABORTAR`, ou até
  **dois `EVOLUIR`**). → A IA **não executa nenhum** e pergunta qual vale.
- **Você dá `MEGA` no Estágio 1.** → A IA **confirma**: "consolidar agora pega
  material ainda cru — confirma forçar ou prefere evoluir estágio a estágio?"
- **Você edita depois do Mega.** → A IA **roteia**: "protocolo encerrado; para
  editar mande `RETROCEDER <N>`." Não reedita o Mega às cegas.
- **Você dá `TÉRMINO PREVISTO` vago** ("quando estiver bom"). → A IA adota o
  **término padrão** do estágio e avisa qual usou. (Evita loop sem fim.)
- **A palavra de um comando aparece dentro do material** (ex.: o texto bruto
  contém "EVOLUIR"). → É **conteúdo**, não comando; nada é destravado.
- **Você manda um Digitama vazio, cortado ou ilegível.** → É o **único** caso em
  que a IA pergunta no Estágio 0 (PERGUNTAR = "só se ilegível"): ela pede o
  material legível antes de ecoar e travar.
- **Material muito grande** (transcrição de horas, texto enorme). → O ritual não
  muda: o conteúdo completo fica no bloco TRABALHO e o ledger mantém **1
  linha-resumo** por estágio.
- **Você manda `EVOLUIR` + cabeçalho de um estágio anterior ao atual.** → A IA
  **não regride por `EVOLUIR`**; confirma e sugere `RETROCEDER <N>` para voltar.
- **Você manda `CALIBRAR: pode seguir`** (pedido de avanço dentro de um comando
  que não avança). → A IA responde *"Para evoluir, mande `EVOLUIR` isolado."* e
  **continua travada**.

---

## 7. Exemplo GENÉRICO completo

**Objetivo:** demonstrar a mecânica com um material simples (um parágrafo de
ideias soltas) virando um **plano de ação enxuto**. Mostra: INICIAR → Digitama →
todos os estágios → um CALIBRAR → um STATUS → Mega.

> Notação: **`>>`** = o que você manda. **`🤖`** = resposta da IA (resumida no
> formato real).

---

**`>>`**
```
SHINKA: INICIAR
Objetivo: organizar minhas ideias soltas sobre começar a correr.
Entrega final desejada: um plano de ação em 3 passos.
```
**🤖** Modo `to-RusH--DIGI-MEGA` ativo. 🥚 Mande o material bruto (Digitama) no
próximo prompt. Ainda não vou transformar nada.

---

**`>>`**
```
Quero começar a correr mas não tenho tênis bom, durmo tarde, e me empolgo e
paro na primeira semana sempre. Acho que de manhã seria melhor. Tenho medo de
lesão.
```
**🤖**
```
🧬 ESTÁGIO 0 — Digitama / 00 BRUTO / デジタマ
1) ▶ QUANDO COMEÇA: você enviou o material após o INICIAR
2) 🔢 ORDEM: 0 de 6
3) 🧠 INTERPRETAR: literal (só ingerir)
4) ❓ PERGUNTAR: só se ilegível
5) 💡 SUGERIR: proibido
6) 🏁 TÉRMINO PREVISTO: material recebido e ecoado
7) ✅ CONCLUSÃO: ledger criado com o bruto

──────── TRABALHO ────────
Material recebido na íntegra (sem alterar): "Quero começar a correr… medo de lesão."

──────── 📒 ASSIMILAÇÃO ACUMULADA ────────
- 0 Digitama: brain-dump sobre começar a correr (tênis, sono, recaída, manhã, medo de lesão)

──────── 🔒 TRAVA 0/6 ────────
✅ Digitama ingerido. Não vou avançar sozinho.
→ EVOLUIR para a triagem · CALIBRAR/COMENTAR/ALTERAR · STATUS · RETROCEDER · MEGA · ABORTAR
```

---

**`>>`** `EVOLUIR`
**🤖**
```
🧬 ESTÁGIO 1 — Fresh / 01 AMPLO / 幼年期
1) ▶ QUANDO COMEÇA: você mandou EVOLUIR
2) 🔢 ORDEM: 1 de 6   3) 🧠 INTERPRETAR: leve   4) ❓ PERGUNTAR: só se bloquear
5) 💡 SUGERIR: proibido   6) 🏁 TÉRMINO PREVISTO: triagem feita   7) ✅ CONCLUSÃO: tipo/tom classificados

──────── TRABALHO ────────
Tipo: desabafo + intenção de meta pessoal. Tom: ansioso, motivado mas inseguro.
Tema central: começar a correr de forma sustentável.

──────── 📒 ASSIMILAÇÃO ACUMULADA ────────
- 0 Digitama: brain-dump sobre correr
- 1 Fresh: meta pessoal; tom ansioso/motivado; foco em sustentabilidade

──────── 🔒 TRAVA 1/6 ────────
✅ Triagem feita. EVOLUIR para mapear o contexto.
```

---

**`>>`** `EVOLUIR`
**🤖** *(Estágio 2 — In-Training: extrai as variáveis ocultas)*
```
──────── TRABALHO ────────
Variáveis: (a) equipamento ausente (tênis), (b) higiene de sono (dorme tarde),
(c) histórico de recaída (para na 1ª semana), (d) janela preferida (manhã),
(e) restrição/risco (medo de lesão).
[…ledger somando a linha do Estágio 2…] 🔒 TRAVA 2/6
```

---

**`>>`** `STATUS`
**🤖**
```
📒 REGISTRO DE ASSIMILAÇÃO (completo)
- 0 Digitama: brain-dump sobre correr
- 1 Fresh: meta pessoal; tom ansioso; foco sustentabilidade
- 2 In-Training: 5 variáveis (tênis, sono, recaída, manhã, lesão)
Estágio atual: 2 · Estado: 🔒 TRAVADO
```

---

**`>>`** `EVOLUIR` → **🤖** *(Estágio 3 — Rookie: utilidade primária)*
```
TRABALHO: a função do material é "virar um plano que evite recaída e lesão".
🔒 TRAVA 3/6
```

**`>>`** `EVOLUIR` → **🤖** *(Estágio 4 — Champion: essência + restrições)*
```
TRABALHO:
Essência ("porquê"): a pessoa não falha por preguiça, e sim por começar forte
demais e se machucar/cansar → recai.
Restrições (Armor): nada de volume alto na semana 1; respeitar sono; calçado
mínimo viável antes de começar.
💡 SUGESTÃO (permitida neste estágio): incluir progressão gradual.
🔒 TRAVA 4/6
```

---

**`>>`**
```
CALIBRAR: deixa a essência em 1 frase só, bem direta.
```
**🤖**
```
🧬 ESTÁGIO 4 — Champion (recalibrado)
[…7 sinais…]
──────── TRABALHO ────────
Essência: "Você não falha por falta de vontade — falha por começar rápido
demais; o plano tem que ser propositalmente devagar."
Restrições: sem volume alto na semana 1; respeitar sono; tênis mínimo antes de iniciar.
──────── 📒 LEDGER ──────── (revisão registrada: Champion → essência condensada em 1 frase)
🔒 TRAVA 4/6  (continuo no estágio 4)
```

---

**`>>`**
```
COMENTAR: lembrar que essa pessoa já tentou app de corrida e largou.
```
**🤖**
```
🧬 ESTÁGIO 4 — Champion (comentário anexado)
[…7 sinais inalterados…]
──────── TRABALHO ────────
[conteúdo inalterado]  @(autor: já tentou app de corrida e largou — evitar depender de app)@
──────── 📒 ASSIMILAÇÃO ACUMULADA ────────
[…]  (revisão: COMENTAR anexado ao Champion)
🔒 TRAVA 4/6  (continuo no estágio 4; o conteúdo não muda, só a nota)
```

---

**`>>`** `EVOLUIR` → **🤖** *(Estágio 5 — Ultimate: pente-fino)*
```
TRABALHO: removidas redundâncias; checada contradição (manhã × dormir tarde →
resolver o sono é pré-requisito, não detalhe). Plano enxugado e coerente.
🔒 TRAVA 5/6
```

---

**`>>`** `EVOLUIR`
**🤖**
```
🧬 ESTÁGIO 6 — Mega / 06 ASSIMILADO / とっておき
[…7 sinais; INTERPRETAR: total…]

──────── TRABALHO (ENTREGA FINAL) ────────
PLANO DE AÇÃO — "Começar a correr sem recair" (3 passos)
1. Pré-requisito (semana 0): ajustar o sono (dormir 30 min mais cedo) e comprar
   um tênis mínimo viável. Sem isso, não começa.
2. Semana 1–2: caminhar/trotar 20 min, 3×/semana, de manhã. Devagar de propósito.
3. Regra anti-recaída: se sentir dor, reduz — nunca zera. Progressão de 10%/semana.

✔ Fidelidade · ✔ Acumulação (incl. calibragem da essência) · ✔ Coerência · ✔ Formato (3 passos)

──────── 📒 LEDGER FINAL ────────
[0→6 consolidados]

PROTOCOLO ENCERRADO no Mega. Para editar algo, mande RETROCEDER <N>.
```

---

## 8. Exemplo ESPECÍFICO completo

**Caso real:** transformar um **vlog do YouTube** numa **tabela de transcrição
decupada** (o uso clássico da skill). Mostra material concreto, timestamps,
tags de mídia, um `ALTERAR` no passado, um `RETROCEDER` e o Mega em formato de
tabela.

---

**`>>`**
```
SHINKA: INICIAR
Objetivo: decupar meu vlog "Café da manhã na fazenda" para legendas.
Entrega final desejada: tabela Markdown | ORDEM | TEMPO | FALANTE | TEXTO |.
```
**🤖** Modo ativo. 🥚 Mande o material bruto (transcrição corrida ou o conteúdo
do vídeo) como Digitama.

---

**`>>`**
```
[00:00] oi gente bom dia hoje to aqui na fazenda da minha vó
[00:06] (som de galo) vamo ver o que tem de café
[00:12] Vó: senta menino, tem bolo de fubá quentinho
[00:18] nossa que cheiro bom... gente isso aqui é vida
```
**🤖**
```
🧬 ESTÁGIO 0 — Digitama / 00 BRUTO / デジタマ
1) ▶ QUANDO COMEÇA: você enviou o material após o INICIAR
2) 🔢 ORDEM: 0 de 6
3) 🧠 INTERPRETAR: literal (só ingerir)
4) ❓ PERGUNTAR: só se ilegível
5) 💡 SUGERIR: proibido
6) 🏁 TÉRMINO PREVISTO: material recebido e ecoado
7) ✅ CONCLUSÃO: material recebido e ecoado (= término previsto)

──────── TRABALHO ────────
Transcrição bruta recebida na íntegra, 4 falas, com marcações de tempo cruas.

──────── 📒 ASSIMILAÇÃO ACUMULADA ────────
- 0 Digitama: vlog "Café na fazenda", ~18s, fala informal + 1 efeito (galo) + 2 falantes

🔒 TRAVA 0/6
```

---

**`>>`** `EVOLUIR` (Estágio 1 — Fresh: triagem)
**🤖**
```
TRABALHO:
Tipo: vlog cotidiano. Tom: afetivo, coloquial, regional. Idioma: português (BR).
Falantes detectados: Narrador (autor) e "Vó".
🔒 TRAVA 1/6
```

---

**`>>`** `EVOLUIR` (Estágio 2 — In-Training: timestamps e métricas)
**🤖**
```
TRABALHO (sincronização):
| ORDEM | TEMPO | FALANTE | (texto vem depois) |
| 1 | 00:00–00:06 | Narrador |
| 2 | 00:06–00:12 | Narrador |
| 3 | 00:12–00:18 | Vó |
| 4 | 00:18–00:24 | Narrador |
🔒 TRAVA 2/6
```

---

**`>>`**
```
ALTERAR estágio 2: a fala 2 começa em 00:07, não 00:06 (tem um corte).
```
**🤖**
```
[…recalibra o Estágio 2…]
| 2 | 00:07–00:12 | Narrador |
──────── 📒 LEDGER ──────── (revisão: Estágio 2, fala 2 início 00:06 → 00:07)
🔒 TRAVA 2/6  (continuo no estágio 2)
```

---

**`>>`** `EVOLUIR` (Estágio 3 — Rookie: contexto imagético/sonoro)
**🤖**
```
TRABALHO: anotações de cena —
- Fala 2: [Efeito: galo cantando ao fundo]
- Fala 3: Vó entra em quadro, oferece bolo (gesto de chamar para sentar)
🔒 TRAVA 3/6
```

---

**`>>`** `EVOLUIR` (Estágio 4 — Champion: essência + restrições de fidelidade)
**🤖**
```
TRABALHO:
Essência: registrar o afeto do momento, preservando a fala regional (não
"corrigir" o português coloquial — fidelidade literal é a restrição-mãe).
Restrição: manter "to", "vamo", "vó" como ditos; marcar efeitos com [Efeito:].
🔒 TRAVA 4/6
```

---

**`>>`**
```
RETROCEDER 1
```
**🤖**
```
Retrocedendo ao Estágio 1 (Fresh). Estágios 2–4 ficam SUSPENSOS (não apagados)
até reprocessar. Reabrindo a triagem agora. Mande sua mudança e depois EVOLUIR
para reprocessar 2→3→4 à luz dela.
```
*(Você percebeu que faltou marcar um terceiro falante que aparece depois; ajusta
na triagem e reevolui — a IA reaplica 2, 3 e 4 reaproveitando o que estava
suspenso como rascunho.)*

---

**`>>`** `EVOLUIR` ×3 *(de 1 a 4, reprocessando 2, 3 e 4)* → e o **4º** `EVOLUIR` abre o Estágio 5 — Ultimate
**🤖**
```
TRABALHO: pente-fino — padronização dos nomes (sempre "Vó" e "Narrador"),
timestamps sem sobreposição, tags `[Efeito:]` consistentes, nenhuma fala perdida.
🔒 TRAVA 5/6
```

---

**`>>`** `EVOLUIR`
**🤖**
```
🧬 ESTÁGIO 6 — Mega / 06 ASSIMILADO / とっておき
──────── TRABALHO (ENTREGA FINAL) ────────
| ORDEM | TEMPO | FALANTE | TEXTO |
| :---: | :---: | :--- | :--- |
| 1 | 00:00–00:07 | Narrador | oi gente bom dia, hoje to aqui na fazenda da minha vó |
| 2 | 00:07–00:12 | Narrador | [Efeito: galo cantando] vamo ver o que tem de café |
| 3 | 00:12–00:18 | Vó | senta menino, tem bolo de fubá quentinho |
| 4 | 00:18–00:24 | Narrador | nossa que cheiro bom... gente, isso aqui é vida @(afeto, momento-chave)@ |

✔ Fidelidade literal · ✔ Tudo acumulado (incl. ALTERAR 00:07 e o retrocesso) · ✔ Coerência · ✔ Formato pedido

PROTOCOLO ENCERRADO. Para editar, RETROCEDER <N>.
```

---

## 9. Erros comuns, armadilhas e FAQ

- **"Mandei o cabeçalho do estágio e ela não avançou."** É de propósito:
  cabeçalho **não** é autorização. Mande `EVOLUIR` (pode ser junto do cabeçalho).
- **"Quero mudar algo de duas etapas atrás."** Use `ALTERAR estágio N: …` — ele
  mira o passado e registra a revisão. `CALIBRAR` é para a etapa atual.
- **"A IA está sugerindo coisas e eu não quero."** Ponha `💡 SUGERIR: proibido`
  no cabeçalho do estágio (ou diga no INICIAR que prefere sem sugestões).
- **"Quero ir direto ao resultado final."** Use `MEGA` — mas se o material ainda
  estiver cru, a IA vai confirmar antes (o Mega fica melhor com os estágios
  feitos).
- **"Perdi o fio."** Mande `STATUS` a qualquer hora.
- **"Comecei errado."** `ABORTAR` encerra sem consolidar; `SHINKA: INICIAR` de
  novo começa uma nova sessão.
- **"Posso pular um estágio que não faz sentido pro meu material?"** Pode dar um
  cabeçalho com `TAREFA: nada a fazer aqui, só repassar` — a IA registra e trava;
  você evolui. (Os estágios são um trilho, mas você decide o peso de cada um.)

---

## 10. Folha de cola

```
LIGAR ........ SHINKA: INICIAR  (+ objetivo + entrega desejada)
DIGITAMA ..... (cole o material bruto)
SUBIR ........ EVOLUIR   (+ cabeçalho opcional do próximo estágio)
LAPIDAR ...... CALIBRAR: …   COMENTAR: …   ALTERAR estágio N: …
VER .......... STATUS
VOLTAR ....... RETROCEDER N
FECHAR ....... EVOLUIR no estágio 5  |  MEGA (forçar)  |  ABORTAR (sem entrega)

ESTÁGIOS: 0 Digitama → 1 Fresh → 2 In-Training → 3 Rookie → 4 Champion → 5 Ultimate → 6 Mega
PORTÃO: só EVOLUIR (ou MEGA) destrava. Tudo o mais mantém você no estágio.
SINAIS: ▶ começa · 🔢 ordem · 🧠 interpretar · ❓ perguntar · 💡 sugerir · 🏁 término · ✅ conclusão
```
