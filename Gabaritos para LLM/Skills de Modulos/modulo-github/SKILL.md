---
name: modulo-github
description: Use when a tarefa envolve repositorios GitHub, issues, pull requests, reviews, checks, branches, commits, publicacao ou triagem de contexto remoto.
---

# Modulo GitHub

## Proposito

Use este modulo quando a LLM precisar orientar ou executar trabalho relacionado ao GitHub: entender PRs, issues, reviews, CI, branches, commits e publicacao.

Objetivo primario: transformar estado local e remoto em uma decisao segura de engenharia.

Objetivo secundario: preservar historico, escopo e contexto de review sem sobrescrever trabalho de terceiros.

Nao use para: alterar historico destrutivamente sem pedido claro, publicar segredos, assumir estado remoto sem consultar evidencia.

## Principio Central

GitHub e uma superficie de colaboracao. Toda acao deve respeitar escopo, autoria, comentarios pendentes e verificacoes remotas.

Regra critica: antes de corrigir, publicar ou responder, descubra qual branch, PR, issue ou check esta em jogo.

## Modelo De Execucao

Estrutura logica: orientar contexto, inspecionar estado, decidir acao, executar, validar remoto.

Estrutura operacional: usar conector GitHub quando disponivel para metadados e `gh`/git local para lacunas praticas.

Modelo mental incorreto: "GitHub e so um lugar para dar push".

Modelo mental correto: "GitHub e o registro compartilhado de revisao, automacao e decisao".

## Unidade Operacional

A unidade minima e uma operacao GitHub verificavel.

Toda unidade deve ter:

- alvo claro, como repo, issue, PR, branch, comentario ou check;
- estado inicial observado;
- resultado confirmado localmente ou no remoto.

## Sistema De Sinais

Use estes sinais como atos operacionais:

- Orientar: identificar repo, branch, PR, issue e objetivo.
- Ler Review: reunir comentarios, requested changes e contexto inline.
- Corrigir: alterar apenas o escopo necessario.
- CI: inspecionar checks, logs e causa provavel antes de mudar codigo.
- Publicar: commit, push ou PR somente com escopo confirmado.
- Responder: deixar comentario claro quando a evidencia sustenta a resposta.

## Regras De Interpretacao

Os sinais sao contextuais. CI pode apontar para GitHub Actions, CircleCI ou outro provedor; Orientar vem antes de qualquer acao remota relevante.

Contradicoes aparentes devem ser resolvidas por seguranca. Exemplo: Publicar + Review significa preparar commit, mas checar pendencias antes de enviar.

## Fluxo De Trabalho

1. Identifique o repositorio, branch e alvo remoto.
2. Compare estado local, remoto e solicitacao do usuario.
3. Leia comentarios, checks ou issues quando forem parte da tarefa.
4. Execute a menor acao necessaria: responder, corrigir, commit, push ou abrir PR.
5. Valide que o remoto mostra o resultado esperado.

## Exemplo De Uso

Problema: o usuario pede para resolver comentarios de um PR.

Unidades: localizar PR, ler threads, separar feedback acionavel, corrigir, testar, responder ou atualizar PR.

Objetivo: fechar o ciclo de review sem apagar trabalho nao relacionado.

## Condicao De Sucesso

Nao ha vencedor exigido. O sucesso e o alvo GitHub refletir a mudanca ou resposta pretendida, com escopo claro e verificacao remota quando aplicavel.

