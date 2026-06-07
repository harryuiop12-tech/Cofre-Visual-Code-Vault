---
name: modulo-hexa-kill
description: Use when a tarefa exige aplicar o protocolo HEXAKILL para comparar abordagens independentes, elos, pings, calls e consequencias de uma mesma situacao.
---

# Modulo HEXA KILL

## Proposito

Use este modulo quando a LLM precisar aplicar o protocolo HEXAKILL: comparar multiplas abordagens independentes para a mesma situacao, usando elos, calls e pings como linguagem operacional.

Objetivo primario: mapear consequencias, custos, privilegios, riscos, gatilhos e criterios de uso de cada abordagem.

Objetivo secundario: revelar trade-offs, pressupostos ocultos, efeitos colaterais e contextos em que cada abordagem fica melhor ou pior.

Nao use para: defender uma abordagem, atacar outra, forcar consenso, criar uma resposta unica ou eleger vencedor universal.

## Principio Central

Cada ELO nasce da mesma situacao original, mas deve permanecer independente dos outros elos.

Regra critica: nenhum ELO deve ser gerado como resposta, correcao ou evolucao causal de outro ELO. Se um elo influencia o seguinte, o processo deixou de ser HEXAKILL puro e virou protocolo serial.

Importancia: critica.

## Modelo De Execucao

Estrutura logica: paralela. Todos os elos derivam da mesma origem e ficam lado a lado para comparacao.

Estrutura operacional: sequencial. Os elos podem ser apresentados um por mensagem, com meta-prompts entre eles, desde que a independencia analitica seja preservada.

Modelo mental incorreto: "ELO 01 influencia ELO 02, que melhora ELO 03, que corrige ELO 04".

Modelo mental correto: "Situacao original -> ELO 01, ELO 02, ELO 03, ELO 04, ELO 05, ELO 06".

## Unidade Operacional

A unidade minima e um ELO: uma ramificacao analitica independente.

Todo ELO deve:

- derivar da mesma situacao original;
- ser analisavel isoladamente;
- nao depender das conclusoes de outros elos;
- representar uma abordagem, perspectiva, intervencao, hipotese ou exploracao distinta;
- registrar consequencias, vantagens, desvantagens e criterio de uso.

## Quantidade

O formato padrao e 6 elos: ELO 01/06 ate ELO 06/06.

O numero e flexivel quando o usuario adaptar o protocolo. A essencia nao e a cardinalidade seis; a essencia e a comparacao paralela.

## Sistema De Progressao

Use calls/announcers como sinal narrativo e estrutural de progresso:

- First Blood: primeira perspectiva obtida.
- Double Kill: duas perspectivas em comparacao.
- Triple Kill: tres vetores ativos.
- Quadra Kill: quatro vetores ativos.
- Penta Kill: cinco vetores ativos.
- Hexakill: matriz completa ou espaco suficientemente explorado.

Regra critica: announcer nao significa vitoria. Ele indica estagio da analise.

## Sistema De Pings

Os pings sao atos comunicacionais, nao enfeites nem tags esteticas. Eles funcionam como no League of Legends: sinalizam intencao, prioridade, risco, movimento, lacuna ou pressao dentro da conversa.

Use estes pings como sinais-base:

- Assist Me: pedido de ajuda, convergencia, suporte ou foco.
- Caution: risco, aviso, perigo ou vies possivel.
- On My Way: movimento, transicao, aproximacao ou proxima etapa.
- Retreat: recuo, reducao de compromisso ou retirada de uma linha.
- All In: comprometimento maximo ou analise sem economia.
- Hold: pausa, estabilizacao ou espera.
- Push: pressao, avancar uma linha ou aumentar intensidade.
- Target: prioridade, foco ou alvo analitico principal.
- Enemy Vision: area observada, informacao exposta ou visibilidade conhecida.
- Missing: fator desconhecido, ausencia, incerteza ou lacuna nao explicada.
- Need Vision: necessidade de informacao, contexto ou discriminacao adicional.
- Generic Ping: chamada geral de atencao.

## Regras De Interpretacao Dos Pings

Os pings sao interpretativos, contextuais, subjetivos, meta-comunicacionais e faticos. Eles podem falar da mensagem, do processo, do objeto analisado ou da relacao entre interlocutores.

Nao assuma significado universal fixo. O significado-base orienta, mas o contexto decide a interpretacao final.

Contradicoes sao permitidas quando geram sentido util. Exemplos:

- All In + Retreat: compromisso maximo com recuo ou abandono completo de uma linha.
- Need Vision + Target: existe lacuna informacional sobre o ponto prioritario.
- Push + Hold: manter posicao enquanto aumenta pressao em outra dimensao.

Evite spam de pings. Muitos sinais reduzem valor comunicativo.

## Filosofia De Analise

O HEXAKILL e diagnostico, analitico e observacional.

A pergunta central nao e "qual abordagem vence?", mas "o que acontece quando esta abordagem e aplicada?".

Compare:

- quando a abordagem melhora ou piora a situacao;
- quais custos ela cria;
- quais pressupostos ocultos ela exige;
- quais reacoes ela provoca;
- quais contextos favorecem ou punem seu uso.

## Gabarito De ELO

Ao preencher um ELO, adapte os nomes ao caso, mas preserve a funcao dos campos:

- Abordagem: qual estrategia, perspectiva ou intervencao esta sendo analisada.
- Gatilho Pressionado: que mecanismo, tensao ou resposta a abordagem ativa.
- Replica Provavel: que reacao o interlocutor, sistema ou ambiente tende a produzir.
- Efeito Operacional: como a abordagem altera UX, relacao, decisao, fluxo ou agencia.
- Desvantagem: custo, risco, dano, perda ou fragilidade da abordagem.
- Privilegio: beneficio, contexto favoravel ou vantagem real da abordagem.
- Criterio De Escolha: quando vale usar, evitar ou reservar a abordagem.

Preenchimento ideal e completo. Se houver incerteza, use inferencia de baixa confianca, hipotese fraca ou estimativa provisoria, mas nao deixe o campo vazio quando ele for necessario para comparar.

## Meta-Prompts Entre Elos

Meta-prompts podem existir entre elos. Eles podem ajustar foco futuro, por exemplo:

- "foque mais no impacto emocional";
- "compare em contexto clinico e em contexto de LLM";
- "analise autonomia e confianca";
- "observe efeitos de longo prazo".

Restricao: meta-prompts podem alterar o enquadramento dos proximos elos, mas nao podem transformar um elo em dependencia causal do anterior.

## Fluxo De Trabalho

1. Defina a situacao original que todos os elos devem compartilhar.
2. Combine ou receba as abordagens que serao comparadas.
3. Para cada ELO, anuncie o estagio quando fizer sentido e aplique pings funcionais no inicio ou durante a resposta.
4. Preencha o gabarito do ELO com foco em consequencias, nao em defesa ou ataque.
5. Ao final, compare o mapa resultante: custos, vantagens, riscos, contextos e criterios de escolha.

## Exemplo De Uso

Problema: como um psiquiatra ou uma IA deve lidar com um usuario muito tangencial e prolixo.

Unidades: limitar palavras, fazer perguntas fechadas, interromper e redirecionar, resumir e confirmar, extrair tema principal, forcar respostas estruturadas.

Objetivo: comparar consequencias de cada intervencao sem pressupor vencedor universal.

## Condicao De Sucesso

Vencedor nao e exigido.

O sucesso e um mapa de entendimento: onde cada abordagem brilha, onde falha, quais custos cria, quais beneficios entrega, quais gatilhos ativa e em quais condicoes deve ou nao ser usada.

