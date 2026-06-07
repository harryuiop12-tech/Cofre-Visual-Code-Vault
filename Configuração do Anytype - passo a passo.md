# Configuração do Anytype - passo a passo

Este guia é operacional. Ele não explica o que registrar na sua vida; ele mostra como configurar as ferramentas do Anytype Desktop para que o sistema funcione.

Use este roteiro na ordem. A ideia é terminar com um Anytype pronto para capturar tarefas, diário, textos importantes, projetos, pessoas e categorias gerais da vida.

## 0. Tradução rápida das ferramentas do Anytype

Antes de configurar, use estes significados práticos:

- `Object`: qualquer item criado no Anytype. Uma tarefa, uma entrada de diário, um projeto, um texto salvo e uma pessoa são objetos.
- `Type`: o tipo de objeto. Exemplo: Tarefa, Diário, Projeto, Recurso, Pessoa.
- `Property`: campo usado para classificar, filtrar ou conectar objetos. Exemplo: Status, Prazo, Área, Link, Projeto relacionado.
- `Template`: modelo salvo dentro de um Type. Ele define a estrutura que aparece quando você cria um novo objeto daquele tipo.
- `Query`: lista automática. Ela busca objetos do seu Graph por Type ou Property.
- `Collection`: lista manual. Ela começa vazia e você adiciona os objetos que quiser.
- `View`: forma de visualizar uma Query ou Collection. Exemplo: Grid, List, Kanban, Calendar, Gallery, Graph.

Regra prática:

- Use `Types` para dizer o que uma coisa é.
- Use `Properties` para dizer como ela deve ser filtrada, ordenada ou conectada.
- Use `Templates` para não reescrever a mesma estrutura.
- Use `Queries` para telas automáticas.
- Use `Collections` para agrupamentos manuais.

## 1. Ajustes iniciais do Space

### 1.1 Nomeie o Space

1. Abra o Anytype Desktop.
2. Na barra lateral, clique em `Settings` no canto superior esquerdo.
3. Entre em `Preferences`.
4. Clique em `Edit info`.
5. Nomeie o Space como `Minha Vida` ou `Sistema Pessoal`.
6. Clique em `Save`.

### 1.2 Crie o painel principal

1. Na barra lateral, clique no botão de criar novo objeto.
2. Crie um objeto do tipo `Page` ou `Document`.
3. Nomeie como `Painel da Vida`.
4. Dentro dele, crie os blocos:

```text
# Painel da Vida

## Captura

## Hoje

## Tarefas

## Diário

## Projetos

## Recursos e Textos

## Pessoas

## Revisão semanal
```

Por enquanto, deixe os blocos vazios. Você vai voltar aqui para inserir Queries e links depois.

### 1.3 Defina a homepage

1. Abra `Settings`.
2. Entre em `Preferences`.
3. Procure a opção de `Homepage`.
4. Escolha um objeto específico.
5. Selecione `Painel da Vida`.

Resultado esperado: sempre que abrir o Space, o Anytype deve começar pelo painel principal.

### 1.4 Defina o tipo padrão de objeto

1. Abra `Settings`.
2. Entre em `Preferences`.
3. Procure `Default object type`.
4. Escolha `Note`, `Page` ou o tipo que você mais usa para captura rápida.

Recomendação: use `Note` para captura rápida, se ele estiver disponível. Depois você transforma ou reclassifica a nota.

## 2. Content Model: criar os Types

Agora você vai criar os tipos principais do sistema.

### 2.1 Abra o Content Model

1. Clique em `Settings`.
2. Entre em `Content Model`.
3. Abra `Object Types`.

### 2.2 Crie ou instale os Types mínimos

Para cada item abaixo:

1. Use a busca da biblioteca de Types.
2. Digite o nome.
3. Se o Anytype já oferecer um Type parecido, você pode instalar.
4. Se não existir, escolha `+ Create type`.

Crie estes Types:

- `Tarefa`
- `Diário`
- `Projeto`
- `Recurso`
- `Pessoa`
- `Área da Vida`
- `Decisão`

Se você preferir usar nomes nativos do Anytype, pode usar `Task`, `Journal`, `Project`, `Bookmark` ou `Human`. Mas escolha um padrão e mantenha.

### 2.3 Configure o layout de cada Type

Abra cada Type e deixe a estrutura simples:

- `Tarefa`: layout de página simples ou task, se existir.
- `Diário`: página simples.
- `Projeto`: página simples.
- `Recurso`: página simples ou bookmark, se existir.
- `Pessoa`: perfil simples.
- `Área da Vida`: página simples.
- `Decisão`: página simples.

Não tente deixar perfeito agora. Primeiro faça o modelo funcionar.

## 3. Properties: criar os campos reutilizáveis

Properties são os campos que permitem filtrar, ordenar e conectar seus objetos.

### 3.1 Abra a biblioteca de Properties

1. Clique em `Settings`.
2. Entre em `Content Model`.
3. Abra `Properties`.
4. Clique em `New` para criar uma nova Property quando necessário.

### 3.2 Crie as Properties gerais

Crie estas Properties:

| Property | Tipo no Anytype | Uso |
| --- | --- | --- |
| `Status` | Select | Estado de tarefas, projetos, recursos e decisões |
| `Área` | Object ou Select | Área da vida relacionada |
| `Tema` | Multi-select | Assuntos e categorias |
| `Prazo` | Date | Data limite de uma tarefa |
| `Data` | Date | Data de diário, decisão ou registro |
| `Prioridade` | Select | Alta, Média, Baixa |
| `Energia` | Select | Baixa, Média, Alta |
| `Projeto relacionado` | Object | Conectar tarefa, recurso ou nota a um projeto |
| `Pessoa relacionada` | Object | Conectar objeto a uma pessoa |
| `Link` | URL | Link de artigo, vídeo, documento ou referência |
| `Fonte` | Text ou URL | Origem de uma informação |
| `Tipo de recurso` | Select | Artigo, Livro, Vídeo, Documento, Citação, Prompt |
| `Humor` | Select | Registro emocional no diário |
| `Concluído` | Checkbox | Marcação simples de conclusão, se quiser |

### 3.3 Valores recomendados para Select

Use estes valores para não travar na configuração:

`Status`:

- Capturado
- Próximo
- Em andamento
- Aguardando
- Ativo
- Para ler
- Lendo
- Resumido
- Concluído
- Pausado
- Cancelado
- Arquivado

`Prioridade`:

- Alta
- Média
- Baixa

`Energia`:

- Baixa
- Média
- Alta

`Tipo de recurso`:

- Artigo
- Livro
- Vídeo
- Documento
- Citação
- Prompt
- Referência

`Humor`:

- Bem
- Neutro
- Cansado
- Ansioso
- Triste
- Animado
- Irritado

### 3.4 Adicione Properties aos Types

Para cada Type:

1. Abra `Settings`.
2. Entre em `Content Model`.
3. Abra `Object Types`.
4. Clique no Type.
5. Na área de Properties, clique em `+`.
6. Adicione as Properties correspondentes.

Use esta distribuição:

| Type | Properties |
| --- | --- |
| `Tarefa` | Status, Prazo, Prioridade, Energia, Área, Projeto relacionado, Pessoa relacionada |
| `Diário` | Data, Humor, Energia, Área, Pessoa relacionada, Projeto relacionado, Tema |
| `Projeto` | Status, Área, Prazo, Prioridade, Pessoa relacionada |
| `Recurso` | Status, Tipo de recurso, Tema, Área, Link, Fonte, Projeto relacionado |
| `Pessoa` | Área, Tema, Link |
| `Área da Vida` | Status, Tema |
| `Decisão` | Data, Status, Área, Projeto relacionado, Pessoa relacionada, Prioridade |

### 3.5 Organize as Properties no Type

Dentro de cada Type, organize as Properties assim:

- `Header properties`: coloque Status, Prazo, Prioridade e Data.
- `Panel properties`: coloque Área, Tema, Projeto relacionado, Pessoa relacionada, Link e Fonte.
- `Hidden properties`: deixe apenas o que você quase nunca usa.

Resultado esperado: ao criar uma Tarefa, por exemplo, os campos principais já aparecem no lugar certo.

## 4. Templates: criar modelos de preenchimento

Templates ficam dentro de cada Type. Crie pelo menos um template padrão para cada Type principal.

### 4.1 Caminho principal para criar Template

1. Abra `Settings`.
2. Entre em `Content Model`.
3. Abra `Object Types`.
4. Clique no Type desejado.
5. Clique em `Templates` no topo.
6. Clique em `+`.
7. Nomeie o template.
8. Adicione texto, blocos e Properties.
9. O Anytype salva automaticamente.

### 4.2 Template para Tarefa

Type: `Tarefa`

Nome do template: `Tarefa padrão`

Conteúdo:

```text
## Resultado esperado

## Próxima ação

## Contexto

## Observações
```

Properties padrão:

- Status: Capturado
- Prioridade: Média
- Energia: Média

Defina este template como o padrão do Type `Tarefa`.

### 4.3 Template para Diário

Type: `Diário`

Nome do template: `Diário diário`

Conteúdo:

```text
## O que aconteceu hoje?

## Como eu me senti?

## O que ficou pendente?

## O que eu quero lembrar?
```

Properties padrão:

- Data: hoje, se o Anytype permitir preencher no momento da criação.

Defina como template padrão do Type `Diário`.

### 4.4 Template para Projeto

Type: `Projeto`

Nome do template: `Projeto padrão`

Conteúdo:

```text
## Resultado desejado

## Por que isso importa?

## Próximas ações

## Recursos relacionados

## Decisões

## Registro de progresso
```

Properties padrão:

- Status: Ativo ou Capturado
- Prioridade: Média

Defina este template como o padrão do Type `Projeto`.

### 4.5 Template para Recurso

Type: `Recurso`

Nome do template: `Recurso padrão`

Conteúdo:

```text
## Resumo

## Ideias principais

## Trechos importantes

## Como posso usar isso?

## Links relacionados
```

Properties padrão:

- Status: Capturado
- Tipo de recurso: Referência

Defina este template como o padrão do Type `Recurso`.

### 4.6 Template para Pessoa

Type: `Pessoa`

Nome do template: `Pessoa padrão`

Conteúdo:

```text
## Quem é?

## Contexto

## Informações importantes

## Último contato

## Próximo contato
```

Defina este template como o padrão do Type `Pessoa`.

### 4.7 Template para Decisão

Type: `Decisão`

Nome do template: `Decisão padrão`

Conteúdo:

```text
## Decisão

## Contexto

## Opções consideradas

## Motivo da escolha

## Riscos

## Quando revisar
```

Defina este template como o padrão do Type `Decisão`.

## 5. Queries: criar telas automáticas

Queries são suas telas principais. Elas puxam objetos automaticamente do Graph.

### 5.1 Como criar uma Query

Você pode criar de dois jeitos:

- Pela barra lateral: use o botão de criar e escolha `Query`.
- Dentro do editor: digite `/` e escolha `Query`.

Ao criar, escolha:

- `Query by Type`, quando quiser listar todos os objetos de um Type.
- `Query by Property`, quando quiser listar objetos que tenham uma Property específica.

### 5.2 Query: Hoje

Objetivo: mostrar o que precisa de atenção agora.

1. Crie uma Query chamada `Hoje`.
2. Escolha `Query by Type`.
3. Selecione `Tarefa`.
4. Adicione as Properties visíveis: Status, Prazo, Prioridade, Área, Projeto relacionado.
5. Adicione filtro:
   - Prazo é hoje ou antes de hoje.
   - Status não é Concluído.
   - Status não é Cancelado.
6. Ordene por:
   - Prazo crescente.
   - Prioridade.

View recomendada: `List` ou `Grid`.

### 5.3 Query: Todas as Tarefas

1. Crie uma Query chamada `Todas as Tarefas`.
2. Escolha `Query by Type`.
3. Selecione `Tarefa`.
4. Mostre: Status, Prazo, Prioridade, Energia, Área, Projeto relacionado.
5. Crie views dentro da mesma Query:
   - `Lista`: todas as tarefas.
   - `Kanban`: agrupada por Status.
   - `Calendário`: usando Prazo.

Observação: Kanban e Calendar são recursos de desktop.

### 5.4 Query: Diário

1. Crie uma Query chamada `Diário`.
2. Escolha `Query by Type`.
3. Selecione `Diário`.
4. Mostre: Data, Humor, Energia, Área, Tema.
5. Ordene por Data decrescente.
6. Crie views:
   - `Lista`: leitura rápida.
   - `Calendário`: visão por data.

### 5.5 Query: Projetos Ativos

1. Crie uma Query chamada `Projetos Ativos`.
2. Escolha `Query by Type`.
3. Selecione `Projeto`.
4. Mostre: Status, Área, Prazo, Prioridade.
5. Filtre:
   - Status é Ativo ou Em andamento.
6. View recomendada:
   - `Grid` para visão geral.
   - `Kanban` por Status se você tiver muitos projetos.

### 5.6 Query: Recursos e Textos

1. Crie uma Query chamada `Recursos e Textos`.
2. Escolha `Query by Type`.
3. Selecione `Recurso`.
4. Mostre: Status, Tipo de recurso, Tema, Área, Link, Fonte.
5. Crie views:
   - `Para ler`: filtro Status é Capturado ou Para ler.
   - `Biblioteca`: filtro Status é Resumido ou Arquivado.
   - `Por tema`: agrupe ou ordene por Tema.

### 5.7 Query: Pessoas

1. Crie uma Query chamada `Pessoas`.
2. Escolha `Query by Type`.
3. Selecione `Pessoa`.
4. Mostre: Área, Tema, Link.
5. View recomendada: `Grid` ou `Gallery`.

### 5.8 Query: Decisões

1. Crie uma Query chamada `Decisões`.
2. Escolha `Query by Type`.
3. Selecione `Decisão`.
4. Mostre: Data, Status, Área, Projeto relacionado, Prioridade.
5. Ordene por Data decrescente.

## 6. Collections: quando usar

Use Collections apenas para listas manuais, quando você quer escolher exatamente o que entra.

Não use Collection para:

- Todas as tarefas.
- Todo o diário.
- Todos os recursos.
- Todos os projetos.

Para isso, use Queries.

### 6.1 Collection: Arquivo Pessoal

1. Crie uma Collection chamada `Arquivo Pessoal`.
2. Adicione manualmente objetos que você quer guardar juntos:
   - documentos pessoais;
   - decisões importantes;
   - recursos essenciais;
   - páginas de referência.

### 6.2 Collection: Materiais de um Tema

Exemplo: `Materiais - Saúde`, `Materiais - Estudos`, `Materiais - Finanças`.

1. Crie uma Collection com o nome do tema.
2. Adicione manualmente recursos, projetos, decisões e notas relevantes.

Regra: se a lista deve se atualizar sozinha, crie uma Query. Se a lista é uma seleção manual, crie uma Collection.

## 7. Views: como configurar cada tela

### 7.1 View List

Use para:

- Hoje
- Diário
- Decisões
- Capturas recentes

Configuração:

- Mostre poucas Properties.
- Ordene por Data ou Prazo.
- Use filtros simples.

### 7.2 View Grid

Use para:

- Projetos
- Recursos
- Pessoas
- Áreas da Vida

Configuração:

- Mostre Status, Área e Prioridade quando fizer sentido.
- Evite campos demais na grade.

### 7.3 View Kanban

Use para:

- Tarefas por Status.
- Projetos por Status.
- Recursos por Status de leitura.

Configuração:

- Agrupe por `Status`.
- Mantenha os status simples.

### 7.4 View Calendar

Use para:

- Tarefas com Prazo.
- Diário por Data.
- Decisões por Data.

Configuração:

- Tarefas usam a Property `Prazo`.
- Diário e Decisões usam a Property `Data`.

### 7.5 View Graph

Use para explorar conexões:

- Projeto ligado a tarefas.
- Pessoa ligada a decisões.
- Recurso ligado a temas.

Não use Graph como tela principal de trabalho. Use como mapa para investigar conexões.

## 8. Colocar tudo no Painel da Vida

Agora volte ao objeto `Painel da Vida`.

### 8.1 Inserir atalhos e Queries

Dentro do painel, adicione links ou inline Queries:

```text
## Captura
- Link para criar nova Tarefa
- Link para criar novo Diário
- Link para criar novo Recurso

## Hoje
- Inline Query: Hoje

## Tarefas
- Link para Todas as Tarefas

## Diário
- Link para Diário

## Projetos
- Link para Projetos Ativos

## Recursos e Textos
- Link para Recursos e Textos

## Pessoas
- Link para Pessoas

## Revisão semanal
- Link para Todas as Tarefas
- Link para Projetos Ativos
- Link para Recursos e Textos
- Link para Decisões
```

Para inserir uma Query dentro de uma página:

1. Clique no local desejado.
2. Digite `/`.
3. Procure `Query`.
4. Escolha a Query existente ou crie uma nova.

### 8.2 Adicionar atalhos na Sidebar

Na barra lateral, deixe fácil acesso a:

- `Painel da Vida`
- `Hoje`
- `Todas as Tarefas`
- `Diário`
- `Projetos Ativos`
- `Recursos e Textos`

Se o Anytype oferecer Widgets na sua versão:

1. Abra o menu de widgets da Sidebar.
2. Adicione as Queries principais.
3. Coloque `Hoje` e `Painel da Vida` no topo.

## 9. Fluxo de manutenção

### 9.1 Capturar rápido

Quando algo surgir:

1. Crie um objeto rápido.
2. Escolha o Type certo se souber.
3. Se não souber, crie como Note ou Page.
4. Depois transforme em Tarefa, Recurso, Diário ou Projeto.

### 9.2 Reclassificar sem medo

Se um objeto estiver no Type errado:

1. Abra o objeto.
2. Abra o menu de propriedades ou configuração do objeto.
3. Altere o `Object Type`.
4. Preencha as Properties do novo Type.

### 9.3 Revisar semanalmente

Uma vez por semana:

1. Abra `Hoje`.
2. Abra `Todas as Tarefas`.
3. Filtre tarefas vencidas e sem projeto.
4. Abra `Projetos Ativos`.
5. Verifique se todo projeto ativo tem próxima ação.
6. Abra `Recursos e Textos`.
7. Arquive ou resuma o que já foi usado.
8. Abra `Decisões`.
9. Revise decisões que precisam ser revisitadas.

### 9.4 Evitar bagunça

Use estas regras:

- Não crie uma Property nova se uma existente já resolve.
- Não crie Collection para algo que deveria atualizar automaticamente.
- Não crie Type novo para uma diferença pequena; use Property.
- Não coloque campos demais no Header.
- Não deixe tudo com Status `Capturado`.
- Revise Queries antes de criar novas.

## 10. Configuração mínima para começar hoje

Se quiser configurar em uma sessão curta, faça só isto:

1. Criar `Painel da Vida`.
2. Definir `Painel da Vida` como homepage.
3. Criar Types: `Tarefa`, `Diário`, `Projeto`, `Recurso`, `Pessoa`.
4. Criar Properties: `Status`, `Área`, `Prazo`, `Data`, `Prioridade`, `Projeto relacionado`, `Link`, `Tema`.
5. Adicionar Properties aos Types.
6. Criar templates padrão para Tarefa, Diário, Projeto e Recurso.
7. Criar Queries: `Hoje`, `Todas as Tarefas`, `Diário`, `Projetos Ativos`, `Recursos e Textos`.
8. Colocar links para essas Queries no `Painel da Vida`.

Depois disso, comece a usar. Ajuste só depois de uma semana.

## 11. Checklist final

Marque quando terminar:

- [ ] Space nomeado.
- [ ] `Painel da Vida` criado.
- [ ] Homepage apontando para `Painel da Vida`.
- [ ] Type padrão definido para captura rápida.
- [ ] Types principais criados.
- [ ] Properties gerais criadas.
- [ ] Properties adicionadas aos Types certos.
- [ ] Templates padrão criados.
- [ ] Query `Hoje` criada.
- [ ] Query `Todas as Tarefas` criada.
- [ ] Query `Diário` criada.
- [ ] Query `Projetos Ativos` criada.
- [ ] Query `Recursos e Textos` criada.
- [ ] Collections manuais criadas apenas se forem necessárias.
- [ ] Views configuradas.
- [ ] Atalhos adicionados no `Painel da Vida`.
- [ ] Atalhos ou widgets adicionados na Sidebar.

## 12. Fontes usadas

Este roteiro foi baseado na documentação oficial do Anytype:

- Objects: https://doc.anytype.io/anytype-docs/getting-started/object-editor
- Properties: https://doc.anytype.io/anytype-docs/getting-started/types/relations
- Templates: https://doc.anytype.io/anytype-docs/getting-started/types/templates
- Queries: https://doc.anytype.io/anytype-docs/getting-started/sets
- Collections: https://doc.anytype.io/anytype-docs/getting-started/sets/collections
- Space Settings: https://doc.anytype.io/anytype-docs/advanced/settings/space-settings
