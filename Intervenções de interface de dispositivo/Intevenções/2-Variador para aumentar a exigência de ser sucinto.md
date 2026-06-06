## 2. `>RESUMIR>` — Variador para **aumentar a exigência de ser sucinto**

**Natureza:** Controle contínuo (variador / slider).  
**O que acontece quando acionado:**  
Cada vez que o usuário envia `>RESUMIR>`, é como girar um knob no sentido “mais resumido”. O nível de concisão exigido **aumenta** para todas as próximas respostas. Internamente, um parâmetro de “sucintude” sobe um degrau (ou porcentagem). Quanto mais vezes você acionar, mais extremo o resumo:

- 1 acionamento: respostas mais diretas, menos exemplos.
- Vários acionamentos acumulados: posso chegar a uma linha por resposta, apenas o núcleo.
- O estado é mantido até que você use o variador oposto (`<RESUMIR<`) ou outros comandos.

**Efeito no parâmetro “tamanho do texto”:**  
Encolhimento progressivo e contínuo do comprimento das respostas seguintes, calibrado pelo número de acionamentos.

---
