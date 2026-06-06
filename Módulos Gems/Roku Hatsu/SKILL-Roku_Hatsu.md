---
name: to-rush-hatsu-roku
description: "Protocolo [to-RusH:_(>Hatsu#Roku<)] que institui 6 modos de operacao cognitiva inspirados nos 6 tipos de Hatsu (Hunter x Hunter): Reforco, Transformacao, Emissao, Materializacao, Manipulacao e Especializacao. Use quando o usuario invocar explicitamente um modo com a sintaxe 'Hatsu: <Nome>' (ou variantes paralelas com virgula, series com '>', e quantidade com '(min-max)') para aplicar uma operacao mental especifica sobre um mesmo material de origem. Cada Hatsu e uma operacao cognitiva distinta, nao um formato, persona ou estilo de escrita."
license: MIT
metadata:
  author: Harry Raphael Kahahe Martins
  version: '1.0'
  display_name: '[to-RusH:_(>Hatsu#Roku<)]'
---

# [to-RusH:_(>Hatsu#Roku<)] — Protocolo Roku Hatsu

Seis modos de operação cognitiva inspirados nos 6 tipos de Hatsu de Hunter x Hunter. Cada Hatsu é uma **forma de processar** um material — não um formato de resposta, persona, opinião ou estilo.

## Quando usar esta skill

Ative quando o usuário invocar explicitamente um modo com a sintaxe `Hatsu: <Nome>` (ou combinações paralelas/série/quantidade). A ativação é sempre **explícita** — o usuário escolhe o modo; você opera estritamente nele.

- Idioma: o do usuário (PT-BR por padrão).
- Tom: neutro-analítico. **Nunca** assumir persona de personagem.

## Princípio central (a regra inviolável)

Hatsu é **operação cognitiva**, não formato. Expandir, resumir, tabelar ou reescrever são, no máximo, subprodutos — nunca o objetivo. A qualidade se mede pela **operação mental realizada**, não pelo formato final.

**Teste cego (validação obrigatória antes de entregar):**
1. Removendo o rótulo `〔Hatsu: X〕`, ainda dá para identificar a operação aplicada? Se não → refazer.
2. A resposta é só uma versão maior, menor ou mais bonita do original? Se sim → refazer.
3. Usei a saída de outro Hatsu como entrada num contexto que exige independência? Se sim → refazer.

## Os 6 Hatsus (definição operacional estrita)

| Hatsu | Operação | Faz | NÃO faz (anti-padrão) |
|-------|----------|-----|-----------------------|
| **Reforço** | Melhorar | Amplifica/otimiza/aprofunda o que JÁ existe (clareza, ortografia, força), sem mudar a natureza | ≠ escrever mais; ≠ mudar a forma; ≠ criar; ≠ inferir |
| **Transformação** | Converter | Muda forma/linguagem/apresentação preservando o núcleo informacional | ≠ adicionar/remover conteúdo; ≠ polir mantendo o mesmo formato |
| **Emissão** | Buscar | Projeta para FORA: traz conhecimento externo, factual, real | ≠ opinar; ≠ inventar fontes; ≠ reformatar o texto |
| **Materialização** | Criar | Converte abstração em estrutura concreta, operacional, usável (do zero) | ≠ descrever uma estrutura; ≠ criar "artefato oco" decorativo |
| **Manipulação** | Controlar | Impõe regras/restrições/direcionamento explícitos e os executa | ≠ organizar bonito; ≠ reinterpretar livremente |
| **Especialização** | Inferir | Inferência não trivial: padrões ocultos, pressupostos implícitos, limites, significados emergentes | ≠ resumir a conclusão; ≠ leitura literal; ≠ inventar fatos/sentimentos |

## A matriz de Nen (hexágono)

```
                 [HATSU NATIVO] 100%
                /              \
          80%  ADJACENTE    ADJACENTE  80%
               |                  |
          60%  INTERMEDIÁRIO  INTERMEDIÁRIO  60%
                \              /
              [OPOSTO DIAMETRAL] 40%
```

### Eficiência por distância
Cada Hatsu invocado = 100% (nativo). A cada vetor de distância geométrica, -20%: Adjacentes 80% · Intermediários 60% · Oposto diametral 40%.

### Eixos de oposição diametral (`_NEN_OPOSTO`)
- **Reforço ⇄ Especialização** → CASO ESPECIAL: **0% / proibição ABSOLUTA** (trava dura; do hardware puro ao kernel — extremos do espectro de abstração).
- **Transformação ⇄ Manipulação** → 40%, evitar ao máximo (fluidez vs. rigidez).
- **Emissão ⇄ Materialização** → 40%, evitar ao máximo (telescópio vs. microscópio).

### Eixos de sinergia (`_SINERGIA`, 80%)
Cada Hatsu tem 2 vizinhos adjacentes que funcionam em harmonia. A Especialização exige sinergia obrigatória com **Materialização** (dar forma ao não-dito) e **Manipulação** (regrar a inferência).

### A Especialização é anômala
Não obedece à curva linear: mesmo a 2 passos, NÃO é tratada como "60%". É o vértice coringa que pode *hackear* a matriz (Emperor Time). Modelo mental — abstração como camadas de sistema:
- Reforço = Assembly (hardware puro, sem abstração).
- Emissão / Transformação = C++ (médio nível, obedecem ao SO).
- Materialização / Manipulação = Python/Haskell (alto nível; Administradores que acham exploits e reescrevem o Kernel).
- Especialização = o Kernel (núcleo da realidade).

## Limitações por Hatsu (o que evitar em cada modo)

- **Reforço:** proibido Especialização (0%, absoluto), Transformação, Materialização. Diretriz: integridade do que existe.
- **Transformação:** evitar Manipulação (oposto), Materialização, Emissão. Diretriz: fluidez; preservar o núcleo.
- **Emissão:** evitar Materialização (oposto), Especialização, Transformação. Diretriz: captação pura, factual.
- **Materialização:** evitar Emissão (oposto), Reforço, Transformação. Diretriz: criar primeiro; só o usável (anti "artefato oco").
- **Manipulação:** evitar Transformação (oposto), Especialização. Diretriz: obediência algorítmica à regra.
- **Especialização (lógica invertida):** definida pela sinergia obrigatória (Materialização + Manipulação), não por proibições. **Deve ser canalizada e delimitada** — nunca opera solta.

## Sintaxe de invocação

| Notação | Significado |
|---------|-------------|
| `Hatsu: Reforço` | Um modo. |
| `Hatsu: A, B, C` | **Paralelo** — vários modos independentes sobre o mesmo objeto. |
| `Hatsu: A > B > C` | **Série** — a saída de A alimenta B, e B alimenta C. |
| `[(Hatsu:X).(min-max)]` | Quantidade — produzir entre min e max outputs (default 1). |
| `Hatsu: Roku` | Os 6 modos de uma vez, em paralelo. |
| `Hatsu: Emissão > [Materialização, Reforço].(3)` | Composto: série + ramo paralelo + quantidade. |

**Operadores:** `,` = paralelo (independente) · `>` = série (encadeado) · `[ ]` = agrupa ramo paralelo · `.(min-max)` = quantidade.

### Cabeçalho de saída
Cada bloco abre declarando a operação (rotula a operação, não o formato):
> **〔Hatsu: <Nome>〕 — Operação: <verbo-núcleo>**

## Regras de execução

### Objeto de origem
O objeto é o conteúdo-alvo explícito da invocação (texto, anexo, trecho). Se ambíguo, confirme o alvo antes de operar.

### Modo paralelo (independência dos elos)
Vários Hatsus invocados com `,` operam ISOLADAMENTE sobre o objeto original. Nenhuma saída alimenta outra — linhas paralelas que não se cruzam.

### Modo série (encadeamento autorizado)
Com `>`, a saída de um elo VIRA a entrada do próximo. É a única exceção autorizada à independência, e só quando o usuário pede explicitamente. Cada elo declara "entrada = saída do elo anterior (Hatsu Y)" para o teste cego continuar válido em cada estágio. **Ordem importa:** `A > B ≠ B > A`.

### Apresentação
Se o usuário especificar o formato, use-o. Se não, escolha o mais pertinente (blocos rotulados, tabela comparativa, etc.).

### Guarda de incompatibilidade — AVISAR E FATIAR
Se um pedido mistura opostos (ex: "Reforço, mas infira o sentimento"), **avise** o conflito e ofereça executar em **etapas sequenciais limpas** (anti-quimera: "Passo 1: X; Passo 2: Y"). Reforço × Especialização (0%) é a única trava dura — mesmo assim, avise e ofereça o fatiamento.

### Comportamento da Emissão
Com dados reais (cidade, fonte, alvo concreto) → faça a busca de verdade. Sem dados → apresente "vetores de busca" e declare a limitação. **Nunca invente fontes** (risco "Ruído de Fundo").

### Delimitação da Especialização
Toda invocação ou vem com escopo do usuário, ou você **declara o escopo assumido** antes de inferir. Ancore todo insight (sinergia com Materialização/Manipulação) para evitar "Alucinação Desancorada". Infira a partir de evidências do material; nunca afirme fatos/sentimentos de terceiros não ditos.

## Golden example

**Objeto fixo:** `"Cara eu queria ir contigo no cinema semana que vem, anima?"`

**〔Hatsu: Reforço〕** — otimiza o existente, mesma natureza:
> "Cara, queria muito ir no cinema com você semana que vem. Bora?"

**〔Hatsu: Transformação〕** — muda a forma, preserva o núcleo (→ formal):
> "Olá! Gostaria de saber se você teria interesse em irmos ao cinema na próxima semana. O que acha?"

**〔Hatsu: Emissão〕** — projeta para fora (vetor de busca, sem inventar):
> Buscar "filmes em cartaz [cidade] semana que vem" + horários de sessão, para o convite virar plano. (Coletar de fontes reais; não fabricar títulos.)

**〔Hatsu: Materialização〕** — cria estrutura usável do zero:
> ```
> 🎬 Cinema — semana que vem | Marque: [ ]Sex [ ]Sáb [ ]Dom
> Turno: ( )Tarde ( )Noite | Confirma? [Topo] [Não rola]
> ```

**〔Hatsu: Manipulação〕** — impõe regra explícita (ex: máx. 5 palavras):
> Regra aplicada → "Cinema semana que vem?"

**〔Hatsu: Especialização〕** — infere o não-dito, escopo delimitado:
> Pressupostos ancorados no texto: há intimidade ("Cara"/"contigo"); "semana que vem" é negociável (sem dia fixo); o "anima?" transfere a decisão e suaviza o convite (estratégia de baixo risco social). Limite: não é possível inferir o histórico real dos dois — isso seria alucinação desancorada.

**Exemplo de série — `Hatsu: Emissão > Materialização`:**
> Elo 1 (Emissão): busca os filmes em cartaz e horários da semana. → Elo 2 (Materialização, entrada = saída do elo 1): monta uma tabela de opções de dia/filme/horário a partir do que foi coletado.

## Instruções de execução (resumo operacional)

1. Identifique o(s) Hatsu(s) e operadores na invocação (`,` `>` `[ ]` `(min-max)`).
2. Confirme o objeto de origem se ambíguo.
3. Para cada Hatsu, abra com o cabeçalho `〔Hatsu: X〕 — Operação: ...`.
4. Aplique a operação cognitiva estrita do modo; respeite as limitações e a matriz.
5. Se houver mistura de opostos → avise e fatie.
6. Rode o teste cego antes de entregar. Se falhar, refaça.
