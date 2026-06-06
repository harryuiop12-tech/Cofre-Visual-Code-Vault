---
name: modulo-latex
description: Use when a tarefa envolve criar, revisar, diagnosticar ou compilar documentos LaTeX, TeX, BibTeX, PDFs academicos ou projetos com Tectonic/TeX Live.
---

# Modulo LaTeX

## Proposito

Use este modulo quando a LLM precisar trabalhar com documentos LaTeX, compilar PDF, diagnosticar erros de TeX ou orientar estrutura de projeto academico.

Objetivo primario: produzir ou recuperar um PDF compilavel a partir de fontes LaTeX.

Objetivo secundario: explicar falhas de compilacao de forma acionavel, sem mascarar erros.

Nao use para: editar PDF final quando a fonte LaTeX e necessaria, instalar runtime sem necessidade, ignorar warnings que afetam o resultado.

## Principio Central

O documento final depende da cadeia fonte, runtime e log. Corrija pela causa indicada pelo compilador, nao por tentativa aleatoria.

Regra critica: sempre diferencie erro de fonte, pacote ausente, runtime inadequado e problema de bibliografia.

## Modelo De Execucao

Estrutura logica: localizar fonte, detectar runtime, compilar, ler log, corrigir, recompilar.

Estrutura operacional: tentar o compilador disponivel mais simples; se falhar por cobertura de pacote, avaliar TeX Live ou outro fallback.

Modelo mental incorreto: "LaTeX falhou, entao o texto esta errado".

Modelo mental correto: "LaTeX falha por uma cadeia especifica que pode ser isolada".

## Unidade Operacional

A unidade minima e uma compilacao ou correcao verificavel.

Toda unidade deve ter:

- arquivo principal identificado;
- comando ou metodo de compilacao definido;
- evidencia no log ou no PDF resultante.

## Sistema De Sinais

Use estes sinais como atos operacionais:

- Fonte: identificar o arquivo raiz e dependencias.
- Runtime: verificar Tectonic, TeX Live, BibTeX/Biber e pacotes.
- Compilar: gerar PDF ou reproduzir erro.
- Log: extrair a primeira falha causal, nao apenas a ultima linha.
- Fallback: trocar compilador ou instalar runtime somente quando justificado.
- Conferir PDF: abrir ou inspecionar o resultado final quando necessario.

## Regras De Interpretacao

Os sinais sao sequenciais, mas podem voltar. Log + Fonte significa corrigir o `.tex`; Log + Runtime significa resolver pacote, engine ou ferramenta.

Contradicoes aparentes sao possiveis. Exemplo: PDF gerado + erro restante significa que houve saida parcial, nao sucesso completo.

## Fluxo De Trabalho

1. Identifique o arquivo principal e a estrutura do projeto.
2. Detecte o runtime disponivel antes de recomendar instalacao.
3. Compile e capture o log.
4. Corrija a primeira causa material encontrada.
5. Recompile ate obter PDF valido ou relatar bloqueio com evidencia.

## Exemplo De Uso

Problema: um artigo nao compila apos adicionar referencias.

Unidades: localizar `main.tex`, verificar bibliografia, rodar compilacao, corrigir engine ou pacote, confirmar PDF.

Objetivo: entregar um PDF correto e uma explicacao curta da causa.

## Condicao De Sucesso

Nao ha vencedor exigido. O sucesso e um documento compilado ou um diagnostico preciso, com log suficiente para provar o estado.

