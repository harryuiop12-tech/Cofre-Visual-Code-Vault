---
name: modulo-computador
description: Use when a tarefa exige controlar, inspecionar ou operar aplicativos Windows, janelas, interfaces locais, arquivos visuais ou fluxos de desktop.
---

# Modulo Computador

## Proposito

Use este modulo quando a LLM precisar agir sobre o computador do usuario, observar uma interface, operar janelas, inspecionar imagens locais ou coordenar uma tarefa em aplicativo grafico.

Objetivo primario: transformar uma intencao do usuario em acoes locais verificaveis.

Objetivo secundario: reduzir erro operacional, evitar cliques cegos e confirmar o estado real antes de declarar sucesso.

Nao use para: simular acesso que nao existe, assumir conteudo de tela sem observar, automatizar acoes destrutivas sem confirmacao explicita.

## Principio Central

A tela e o estado local sao a fonte de verdade. Antes de agir, observe; depois de agir, verifique.

Regra critica: nunca trate uma intencao como concluida apenas porque o comando foi enviado. A conclusao depende do estado observado.

## Modelo De Execucao

Estrutura logica: observar, interpretar, agir, verificar.

Estrutura operacional: passos curtos, com pausa para reavaliar quando a interface muda.

Modelo mental incorreto: "clicar ate parecer que funcionou".

Modelo mental correto: "confirmar contexto, executar a menor acao util e conferir o resultado".

## Unidade Operacional

A unidade minima e uma acao de desktop verificavel.

Toda acao deve ter:

- alvo claro, como janela, botao, campo, menu, arquivo ou imagem;
- criterio de sucesso observavel;
- plano de recuperacao se a interface nao responder como esperado.

## Sistema De Sinais

Use estes sinais como atos operacionais:

- Observar: capturar o estado atual antes de decidir.
- Focar: selecionar a janela, area ou objeto correto.
- Agir: executar uma interacao curta e reversivel quando possivel.
- Conferir: validar se o resultado apareceu na tela ou no arquivo.
- Escalar: pedir confirmacao antes de risco alto, como apagar, enviar, comprar ou alterar conta.

## Regras De Interpretacao

Os sinais sao contextuais. "Agir" em um editor de texto pode ser digitar; em um navegador pode ser clicar; em um explorador de arquivos pode ser abrir ou selecionar.

Contradicoes aparentes sao permitidas quando refletem cautela util. Exemplo: Agir + Escalar significa preparar a acao, mas aguardar confirmacao antes do ponto irreversivel.

## Fluxo De Trabalho

1. Entenda o objetivo final em termos de resultado visivel ou arquivo produzido.
2. Observe o estado atual da tela ou do arquivo relevante.
3. Identifique a menor sequencia de interacoes necessaria.
4. Execute uma etapa por vez, reavaliando se a interface mudar.
5. Verifique o resultado final por evidencia observavel.

## Exemplo De Uso

Problema: o usuario quer abrir um aplicativo, localizar uma opcao e exportar um arquivo.

Unidades: abrir aplicativo, navegar ate a opcao, acionar exportacao, conferir arquivo gerado.

Objetivo: concluir a operacao com evidencia local, sem depender de suposicao sobre a interface.

## Condicao De Sucesso

Nao ha vencedor exigido. O sucesso e o estado local corresponder ao pedido do usuario, com verificacao concreta e sem efeitos colaterais indevidos.

