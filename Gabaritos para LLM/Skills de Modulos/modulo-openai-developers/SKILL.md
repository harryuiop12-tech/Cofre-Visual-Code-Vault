---
name: modulo-openai-developers
description: Use when a tarefa envolve OpenAI API, Agents SDK, ChatGPT Apps SDK, MCP apps, chaves de API, troubleshooting, avaliacao ou submissao de apps.
---

# Modulo OpenAI Developers

## Proposito

Use este modulo quando a LLM precisar construir, configurar, depurar ou avaliar software baseado em produtos OpenAI.

Objetivo primario: transformar uma ideia de app, agente, integracao ou automacao OpenAI em implementacao correta e segura.

Objetivo secundario: usar documentacao atual, proteger credenciais e diferenciar problema de codigo, modelo, quota, permissao ou rede.

Nao use para: expor chaves, inventar comportamento de API, ignorar documentacao oficial ou tratar erro de credencial como bug de codigo.

## Principio Central

Integrações OpenAI dependem de contrato atual, credencial correta e caminho de produto adequado.

Regra critica: para informacao instavel de API, confirme na documentacao oficial antes de orientar implementacao.

## Modelo De Execucao

Estrutura logica: definir produto, confirmar docs, preparar credenciais, implementar, testar, avaliar.

Estrutura operacional: escolher entre API direta, Agents SDK, ChatGPT Apps SDK, MCP app, troubleshooting ou submissao.

Modelo mental incorreto: "qualquer tarefa com IA e so chamar um modelo".

Modelo mental correto: "cada produto OpenAI tem contrato, ferramenta, seguranca e fluxo de validacao proprios".

## Unidade Operacional

A unidade minima e uma integracao OpenAI verificavel.

Toda unidade deve ter:

- caso de uso e superficie escolhida;
- modelo ou SDK justificado;
- destino seguro para credenciais;
- teste ou avaliacao de funcionamento;
- tratamento de erro esperado.

## Sistema De Sinais

Use estes sinais como atos operacionais:

- Produto: escolher API, Agents SDK, Apps SDK ou outro caminho.
- Docs: consultar fonte oficial quando a regra pode ter mudado.
- Credencial: localizar, criar ou solicitar chave sem expor segredo.
- Construir: implementar o menor fluxo funcional.
- Troubleshoot: classificar falha por rede, auth, quota, rate limit, modelo ou codigo.
- Avaliar: testar comportamento, outputs e casos negativos.
- Submeter: preparar artefato de review quando for app ChatGPT.

## Regras De Interpretacao

Os sinais sao dependentes do produto. Docs + Construir significa seguir contrato oficial; Credencial + Troubleshoot significa verificar ambiente sem revelar chave.

Contradicoes aparentes devem favorecer seguranca. Exemplo: usuario pede rapidez + nova API instavel significa checar docs antes de codar.

## Fluxo De Trabalho

1. Identifique a superficie OpenAI correta para o objetivo.
2. Confirme documentacao oficial quando houver risco de mudanca.
3. Trate credenciais como segredo e configure destino local seguro.
4. Implemente o menor caminho funcional.
5. Teste, diagnostique falhas e registre limites ou proximos passos.

## Exemplo De Uso

Problema: o usuario quer criar um agente que usa ferramentas e depois avaliar respostas.

Unidades: escolher Agents SDK, configurar chave, montar agente, criar execucao, adicionar avaliacao simples, testar falhas.

Objetivo: entregar prototipo verificavel sem vazar credenciais nem depender de API presumida.

## Condicao De Sucesso

Nao ha vencedor exigido. O sucesso e uma integracao OpenAI funcional, segura e alinhada ao produto correto, com erros diagnosticaveis.

