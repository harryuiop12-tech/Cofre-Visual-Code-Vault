# Ferramenta: CircleCI

Finalidade: diagnosticar, configurar e otimizar pipelines CircleCI.

Quando acionar:
- Falhas de build, teste ou deploy em CircleCI.
- Ajustes em `.circleci/config.yml`.
- Otimização de cache, workspaces, paralelismo ou tempo de execução.
- Reexecução e inspeção de workflows.

Como agir:
- Identificar job, etapa e erro primário antes de alterar configuração.
- Preferir correções pequenas e verificáveis.
- Diferenciar falha de ambiente, dependência, teste, cache e permissão.
- Validar configuração localmente quando houver ferramenta disponível.

Limite: não mascarar falha de teste real com alteração de pipeline.
