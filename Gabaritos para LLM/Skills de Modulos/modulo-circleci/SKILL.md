---
name: modulo-circleci
description: Use when a tarefa envolve pipelines CircleCI, builds falhando, jobs, workflows, configuracao `.circleci/config.yml`, CLI CircleCI ou Chunk.
---

# Modulo CircleCI

## Proposito

Use este modulo quando a LLM precisar diagnosticar, operar ou melhorar pipelines CircleCI.

Objetivo primario: descobrir por que um pipeline falhou ou como torna-lo mais confiavel.

Objetivo secundario: reduzir desperdicio de CI, melhorar cache, paralelismo, configuracao e qualidade dos logs.

Nao use para: alterar configuracao sem reproduzir ou entender a falha, rerodar jobs indefinidamente, confundir falha de teste com falha de CI.

## Principio Central

CI e evidencia operacional. Logs, workflow, job e configuracao devem ser lidos antes de qualquer correcao.

Regra critica: trate a primeira causa material do job como alvo; nao otimize a pipeline enquanto a falha raiz estiver desconhecida.

## Modelo De Execucao

Estrutura logica: localizar pipeline, ler workflow/job, extrair causa, corrigir ou rerodar, validar.

Estrutura operacional: usar UI, CLI ou Chunk conforme acesso e pedido do usuario.

Modelo mental incorreto: "build vermelho significa problema no CircleCI".

Modelo mental correto: "build vermelho aponta para uma falha especifica em codigo, teste, ambiente ou configuracao".

## Unidade Operacional

A unidade minima e um job ou workflow analisado com evidencia.

Toda unidade deve ter:

- identificador de pipeline, workflow ou job;
- trecho causal do log;
- acao recomendada ou executada;
- resultado de validacao.

## Sistema De Sinais

Use estes sinais como atos operacionais:

- Pipeline: identificar projeto, branch, workflow e job.
- Log: encontrar a primeira mensagem causal confiavel.
- Config: revisar `.circleci/config.yml` quando a causa apontar para orbs, cache, executor ou steps.
- Rerun: repetir job apenas quando houver indicio de flake ou problema externo.
- Otimizar: melhorar desempenho depois que a corretude estiver clara.
- Chunk: usar assistencia CircleCI Chunk quando o pedido envolver esse fluxo.

## Regras De Interpretacao

Os sinais sao evidenciais. Log + Config indica problema provavel de pipeline; Log + teste indica problema do projeto executado dentro da pipeline.

Contradicoes aparentes exigem separacao. Exemplo: falha intermitente + configuracao correta pode indicar flake, dependencia externa ou isolamento ruim.

## Fluxo De Trabalho

1. Identifique o pipeline e o job relevante.
2. Leia o log ate encontrar a primeira causa material.
3. Classifique a falha: codigo, teste, ambiente, dependencia, configuracao ou flake.
4. Escolha acao minima: corrigir, ajustar config, rerodar ou pedir acesso.
5. Valide com job, teste local ou configuracao revisada.

## Exemplo De Uso

Problema: um workflow falha so no CircleCI.

Unidades: localizar job, comparar ambiente local/CI, ler log, ajustar executor ou dependencia, validar novo run.

Objetivo: transformar o vermelho da pipeline em causa e acao verificaveis.

## Condicao De Sucesso

Nao ha vencedor exigido. O sucesso e uma causa comprovada e uma pipeline corrigida, rerodada com criterio ou documentada com proximo passo claro.

