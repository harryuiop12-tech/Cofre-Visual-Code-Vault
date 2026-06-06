# Guia do Usuário — `[to-RusH:_(>Hatsu#Roku<)]`

> Protocolo Roku Hatsu: 6 modos de operação cognitiva inspirados nos 6 tipos de Hatsu de Hunter x Hunter. Cada modo aplica uma **forma diferente de pensar** sobre o mesmo material — não é um estilo de escrita, é uma operação mental.

---

## 1. O que é esta skill (em uma frase)

Você fornece um material (uma frase, um texto, uma ideia) e escolhe **como** quer que ele seja processado, invocando um dos 6 Hatsus. Cada Hatsu faz algo cognitivamente distinto:

| Hatsu | Operação | O que ele faz com o seu material |
|-------|----------|----------------------------------|
| **Reforço** | Melhorar | Otimiza e fortalece o que já existe, sem mudar a natureza |
| **Transformação** | Converter | Muda a forma/linguagem, preservando o conteúdo central |
| **Emissão** | Buscar | Vai buscar informação externa real para complementar |
| **Materialização** | Criar | Cria uma estrutura concreta e usável do zero (tabela, card, checklist) |
| **Manipulação** | Controlar | Aplica regras e restrições explícitas que você define |
| **Especialização** | Inferir | Deduz o que está implícito: pressupostos, padrões, lacunas |

---

## 2. Como invocar (a sintaxe)

Toda invocação começa com `Hatsu:` seguida do(s) modo(s) e, opcionalmente, da quantidade de variações.

### 2.1 Um único modo
```
Hatsu: Reforço
"seu texto aqui"
```

### 2.2 Pedindo várias variações — `(min-max)`
O número entre parênteses define **quantos resultados** você quer (entre o mínimo e o máximo).
```
[(Hatsu: Transformação).(3-7)]
"seu texto aqui"
```
> Isso pede de 3 a 7 versões transformadas. Se você não indicar quantidade, o padrão é 1.

### 2.3 Vários modos em PARALELO — vírgula `,`
Cada modo opera **independentemente** sobre o mesmo material. As respostas não se misturam.
```
Hatsu: Reforço, Emissão, Especialização
"seu texto aqui"
```

### 2.4 Todos os 6 de uma vez — `Roku`
Atalho para ver o material sob as 6 lentes ao mesmo tempo (em paralelo).
```
Hatsu: Roku
"seu texto aqui"
```

### 2.5 Modos em SÉRIE — seta `>`
A saída de um modo vira a **entrada** do próximo (uma cadeia ordenada).
```
Hatsu: Emissão > Materialização > Reforço
"seu texto aqui"
```
> Lê-se: busque dados externos → monte uma estrutura com eles → otimize essa estrutura.

### 2.6 Combinação avançada — série + paralelo + quantidade
```
Hatsu: Emissão > [Materialização, Reforço].(3)
"seu texto aqui"
```
> Busca externa primeiro; a partir dessa saída, ramifica em paralelo (Materialização e Reforço), com 3 variações cada.

### Resumo dos operadores

| Símbolo | Significado |
|---------|-------------|
| `,` | Paralelo — modos independentes, não se cruzam |
| `>` | Série — a saída de um alimenta o próximo |
| `[ ]` | Agrupa um ramo paralelo dentro de uma série |
| `.(min-max)` | Quantidade de variações desejada |
| `Roku` | Os 6 modos de uma vez |

---

## 3. O que você pode pedir em cada modo

### 🔵 Reforço — "deixe mais forte sem mudar o que é"
- Corrigir ortografia/pontuação mantendo o tom.
- Deixar um texto mais claro, mais conciso ou mais firme.
- Amplificar a força de um pedido, convite ou argumento já existente.

**Exemplo:** `Hatsu: Reforço` → "Cara, queria muito ir no cinema com você semana que vem. Bora?"

> Não faz: criar conteúdo novo, mudar o formato, traduzir, ou adivinhar intenções.

---

### 🟢 Transformação — "mude a forma, mantenha a essência"
- Mudar o registro (informal ↔ formal).
- Traduzir para outro idioma.
- Converter para outro canal (texto → roteiro de áudio, frase → verso, texto → formato telegráfico).
- Mudar a perspectiva (direto ↔ indireto).

**Exemplo:** `Hatsu: Transformação` → "Olá! Gostaria de saber se você teria interesse em irmos ao cinema na próxima semana."

> Não faz: adicionar/remover informação, apenas polir mantendo o mesmo formato.

---

### 🟡 Emissão — "vá buscar o que falta lá fora"
- Buscar dados externos reais (o que está em cartaz, preços, horários, fatos, lançamentos).
- Trazer contexto factual que complementa o material.

**Exemplo:** `Hatsu: Emissão` → busca os filmes em cartaz e horários da semana para o convite virar um plano real.

> Regra de ouro: **nunca inventa fontes.** Se houver dados concretos (cidade, fonte), faz a busca de verdade; se não, mostra "vetores de busca" para você acionar e avisa a limitação.

---

### 🟠 Materialização — "transforme a ideia em algo concreto e usável"
- Criar tabelas, checklists, formulários, cards, enquetes, matrizes de decisão.
- Estruturar uma intenção abstrata em uma ferramenta utilizável.

**Exemplo:** `Hatsu: Materialização` → uma enquete de disponibilidade com dias e turnos para marcar com o amigo.

> Não faz: estruturas decorativas e inúteis ("artefatos ocos"). Só cria o que tem propósito prático.

---

### 🔴 Manipulação — "aplique estas regras"
- Reescrever sob restrições explícitas que você define: limite de palavras, sem gírias, sem acentos, terminar em pergunta sim/não, tom não-insistente, prazo de resposta, formato fixo.

**Exemplo:** `Hatsu: Manipulação` com regra "máx. 5 palavras" → "Cinema semana que vem?"

> Você define a regra; o modo a executa com precisão. Não reinterpreta livremente nem adivinha intenções.

---

### 🟣 Especialização — "me diga o que está implícito"
- Identificar pressupostos não ditos, padrões ocultos, significados emergentes.
- Apontar lacunas a resolver.
- Fazer autocrítica (o que NÃO dá para concluir a partir do material).

**Exemplo:** `Hatsu: Especialização` → "O 'anima?' transfere a decisão e suaviza o convite; 'semana que vem' indica data negociável; há intimidade pelo uso de 'Cara'/'contigo'."

> Importante: este modo é **delimitado e ancorado**. Ele infere a partir de evidências do material — nunca inventa fatos ou sentimentos de terceiros. Você pode (e deve) dizer o escopo: "infira só sobre o tom", "infira só as lacunas práticas".

---

## 4. Regras importantes de comportamento

- **Mesma origem:** no modo paralelo, todos os Hatsus operam sobre o material original; nenhum usa a saída do outro.
- **Série é a exceção:** só quando você usa `>`, a saída de um alimenta o próximo. A ordem importa (`A > B` ≠ `B > A`).
- **Mistura de opostos = aviso:** se você pedir algo que combina modos incompatíveis (ex: "Reforço, mas infira o sentimento"), a skill avisa e oferece fazer em **etapas separadas** em vez de misturar.
- **Combinações que fluem bem** (sinergia): `Emissão > Materialização`, `Materialização > Reforço`, `Especialização > Materialização > Manipulação`.
- **Combinação proibida:** Reforço + Especialização ao mesmo tempo (são opostos extremos). A skill sempre sugere separar em passos.

---

## 5. Receituário rápido (copie e adapte)

| Você quer... | Peça assim |
|--------------|-----------|
| Melhorar um texto sem mudá-lo | `Hatsu: Reforço` |
| Versão formal de uma mensagem | `Hatsu: Transformação` |
| 5 versões diferentes de um convite | `[(Hatsu: Transformação).(5)]` |
| Buscar dados reais para um plano | `Hatsu: Emissão` |
| Montar uma tabela/checklist | `Hatsu: Materialização` |
| Reescrever com regras suas | `Hatsu: Manipulação` (diga a regra) |
| Entender o que está implícito | `Hatsu: Especialização` (diga o escopo) |
| Ver tudo de uma vez | `Hatsu: Roku` |
| Comparar 3 lentes lado a lado | `Hatsu: Reforço, Emissão, Especialização` |
| Buscar e depois estruturar | `Hatsu: Emissão > Materialização` |
| Inferir, dar forma e regrar | `Hatsu: Especialização > Materialização > Manipulação` |

---

## 6. Modelo de mensagem completa

```
Hatsu: Emissão > [Materialização, Reforço].(3)

"Cara eu queria ir contigo no cinema semana que vem, anima?"
```

Isso diz: busque dados externos sobre o convite, e a partir disso gere — em paralelo — 3 estruturas concretas (Materialização) e 3 versões otimizadas (Reforço).

---

*Skill: `to-rush-hatsu-roku` · Protocolo `[to-RusH:_(>Hatsu#Roku<)]` · v1.0*
