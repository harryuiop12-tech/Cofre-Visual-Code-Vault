---
name: modulo-data-analytics
description: Use when a tarefa exige analise de dados, metricas, diagnostico quantitativo, dashboards, relatorios, KPIs, validacao de dados ou visualizacao analitica.
---

# Modulo Data Analytics

## Proposito

Use este modulo quando a LLM precisar produzir analise quantitativa confiavel, diagnosticar metricas, criar dashboards, relatorios, KPIs ou validar dados.

Objetivo primario: transformar dados e pergunta de negocio em conclusao sustentada por evidencia.

Objetivo secundario: tornar fontes, definicoes, metodos, incertezas e limitacoes explicitos.

Nao use para: inventar numeros, ignorar granularidade, confundir correlacao com causa ou entregar grafico bonito sem validacao.

## Principio Central

Conclusao analitica precisa de fonte, definicao e metodo. Sem isso, o resultado e hipotese, nao achado.

Regra critica: valide a confiabilidade dos dados antes de usar a analise para orientar decisao.

## Modelo De Execucao

Estrutura logica: entender pergunta, localizar fonte, validar dados, analisar, visualizar, explicar.

Estrutura operacional: escolher a rota adequada entre qualidade de dados, diagnostico de metricas, KPI, dashboard, relatorio, mercado ou visualizacao.

Modelo mental incorreto: "analise e calcular qualquer numero disponivel".

Modelo mental correto: "analise e responder uma pergunta com dados adequados e incerteza calibrada".

## Unidade Operacional

A unidade minima e um achado analitico verificavel.

Todo achado deve ter:

- pergunta ou decisao associada;
- fonte e recorte temporal;
- definicao da metrica;
- calculo ou consulta revisavel;
- caveat quando houver limitacao.

## Sistema De Sinais

Use estes sinais como atos operacionais:

- Contexto: entender negocio, pergunta e criterio de decisao.
- Fonte: identificar tabelas, arquivos, planilhas ou datasets.
- Qualidade: checar grain, nulos, duplicatas, freshness e joins.
- Analise: calcular metricas e comparacoes no nivel correto.
- Visual: escolher grafico que responda a pergunta.
- Handoff: entregar relatorio, dashboard ou recomendacao com caveats.

## Regras De Interpretacao

Os sinais sao dependentes do risco. Uma exploracao rapida pode exigir menos validacao; um relatorio executivo exige metodologia, fontes e QA mais fortes.

Contradicoes aparentes devem virar caveats. Exemplo: dado forte + definicao incerta significa responder com condicao, nao com certeza.

## Fluxo De Trabalho

1. Reescreva a pergunta como decisao, diagnostico ou monitoramento.
2. Localize e descreva as fontes disponiveis.
3. Valide se os dados suportam a pergunta.
4. Execute a analise no grao correto.
5. Entregue achados, visualizacoes e limitacoes proporcionais ao uso.

## Exemplo De Uso

Problema: a receita caiu e o usuario quer entender por que.

Unidades: confirmar definicao de receita, comparar periodo, segmentar drivers, validar dados, apresentar explicacao calibrada.

Objetivo: separar movimento real, mudanca de definicao, problema de dados e driver de negocio.

## Condicao De Sucesso

Nao ha vencedor exigido. O sucesso e uma resposta analitica que ajuda decisao, com evidencia rastreavel e incerteza declarada.

