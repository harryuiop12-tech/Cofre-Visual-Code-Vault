---
name: modulo-superpowers
description: Use when a tarefa exige aplicar metodos disciplinados de engenharia, como planejamento, TDD, debugging sistematico, reviews, verificacao ou execucao de planos.
---

# Modulo Superpowers

## Proposito

Use este modulo quando a LLM precisar escolher e seguir um metodo de trabalho, nao apenas responder diretamente. Ele organiza tarefas de desenvolvimento em protocolos de raciocinio, execucao e verificacao.

Objetivo primario: impedir acao improvisada em tarefas que exigem rigor.

Objetivo secundario: tornar o processo auditavel, com evidencias antes de conclusoes.

Nao use para: tarefas triviais que nao precisam de metodo, substituir a instrucao do usuario, transformar todo pedido simples em burocracia.

## Principio Central

O metodo certo vem antes da execucao. Se uma tarefa pede depuracao, use debugging; se pede implementacao, use plano e teste; se pede conclusao, verifique antes de afirmar.

Regra critica: nao pule a habilidade de processo aplicavel so porque a resposta parece obvia.

## Modelo De Execucao

Estrutura logica: selecionar protocolo, seguir passos, registrar evidencia, concluir.

Estrutura operacional: carregar a habilidade relevante, executar o fluxo dela e manter o usuario informado.

Modelo mental incorreto: "Superpowers e um conjunto decorativo de boas praticas".

Modelo mental correto: "Superpowers e um roteador de disciplina operacional".

## Unidade Operacional

A unidade minima e uma decisao de processo aplicada a uma tarefa concreta.

Toda unidade deve ter:

- gatilho que justifique o metodo;
- passos obrigatorios conhecidos;
- evidencia de que a tarefa avancou ou foi bloqueada.

## Sistema De Sinais

Use estes sinais como atos operacionais:

- Skill Check: identificar qual habilidade ou metodo se aplica.
- Plano: decompor antes de executar quando ha multiplos passos.
- Teste Primeiro: escrever ou definir verificacao antes da mudanca quando for bugfix ou feature.
- Debugging: investigar causa antes de propor correcao.
- Evidencia: rodar verificacao antes de declarar pronto.
- Review: procurar riscos, regressao e lacunas antes de finalizar.

## Regras De Interpretacao

Os sinais sao obrigatorios quando o gatilho existe. "Teste Primeiro" pode significar teste automatizado, caso manual ou verificacao reproduzivel, dependendo do contexto.

Contradicoes aparentes devem ser resolvidas pela prioridade do trabalho. Exemplo: Plano + Debugging significa primeiro entender a falha, depois planejar a correcao.

## Fluxo De Trabalho

1. Classifique a tarefa: criar, corrigir, investigar, revisar, executar plano ou finalizar.
2. Escolha a habilidade de processo correspondente.
3. Siga o fluxo da habilidade sem reduzir etapas criticas.
4. Atualize o usuario quando houver progresso, risco ou mudanca de rota.
5. Finalize somente com verificacao proporcional ao risco.

## Exemplo De Uso

Problema: uma alteracao quebrou testes e o usuario pede correcao.

Unidades: reproduzir falha, isolar causa, definir teste, corrigir, verificar.

Objetivo: corrigir a causa real, nao apenas fazer a falha desaparecer.

## Condicao De Sucesso

Nao ha vencedor exigido. O sucesso e uma tarefa conduzida pelo metodo adequado, com evidencia clara e sem pular etapas que protegem qualidade.

