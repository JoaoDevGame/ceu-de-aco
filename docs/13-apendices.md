# 13 · Apêndices

[← Anterior: Pendências e Riscos](./12-pendencias-e-riscos.md) · [🏠 Índice](./README.md)

> **Versão do documento:** GDD v0.7.0 · **Data:** 2026-11-04

---

## A. Glossário

| Termo | Definição |
|---|---|
| GDD | Documento que descreve jogo, regras e implementação. |
| Core loop | Ciclo repetido de decisões e ações do jogador. |
| MVP | Menor versão que testa a proposta. |
| HP | Pontos de vida. |
| Morte súbita | Estado após 30 min sem vencedor: defesas explodem e bases ficam com 1 HP. |
| Servidor autoritativo | Servidor valida o estado final; cliente envia intenções e renderiza. |
| Bot | Jogador controlado por IA para teste ou preenchimento de vaga, se aprovado. |
| FSM | Máquina de estados finitos. |
| DoD / DoR | Definition of Done / Definition of Ready. |
| ADR | Registro de decisão arquitetural. |

---

## B. Referências e inspirações

- ***Sonic*** foi mencionado pelo usuário **somente** como exemplo de animação/comportamento de personagem parado; **não copiar** assets, personagens, música ou elementos protegidos.
- Phaser: <https://docs.phaser.io/> · <https://phaser.io/examples>
- Template React + Phaser: <https://github.com/phaserjs/template-react-ts>
- Game Programming Patterns: <https://gameprogrammingpatterns.com>
- WCAG 2.2: <https://www.w3.org/TR/WCAG22/>
- Game Accessibility Guidelines: <https://gameaccessibilityguidelines.com/>
- Classificação Indicativa (Brasil): <https://www.gov.br/mj/pt-br/assuntos/seus-direitos/classificacao>
- LGPD: Lei nº 13.709/2018.

---

## C. Créditos e licenças de terceiros

**Nenhum asset de produção foi selecionado.**

Antes do release, manter inventário com **nome, autor, URL, licença, data de obtenção e atribuição** para cada sprite, fonte, música, efeito sonoro e biblioteca. **Não usar conteúdo de terceiros sem licença compatível.**

### Modelo de registro

| Asset | Autor | URL | Licença | Obtido em | Atribuição exigida |
|---|---|---|---|---|---|
| _(preencher)_ | | | | | |

---

## D. Relatório de Auditoria do GDD

### Completude
- ✔ 13 seções do template presentes; itens desconhecidos estão identificados como [PENDENTE] ou "Não aplicável".
- ✔ Elevator pitch abaixo de 50 palavras; quatro pilares propostos.
- ✔ Core loop micro/macro/meta e diagrama incluídos.
- ✔ Vitória, derrota, respawn proposto, desconexão e morte súbita descritos.
- ✔ Fluxo cobre boot, preload, menu, história, lobby, partida, pausa/configurações, erro e resultado.

### Consistência
- ✔ Valores confirmados repetidos consistentemente: torre defesa 25.000 HP em 5 segmentos de 5.000; torre principal 45.000 HP em barra contínua; bases em 1 HP na morte súbita.
- ✔ Ataques automáticos de torres incluídos como regra; alvo/prioridade permanecem identificados como pendentes.
- ✔ Seleção de personagem por cada um dos seis jogadores registrada; regra de duplicatas/timeout fica pendente.
- ✔ Chefe de 300 m, aviso aos 4:30, surgimento proposto aos 5 min e ataque por proximidade rastreados. Recompensa pelo golpe final auditada: +15% velocidade e +5% dano por 90 s.
- ✔ IDs de mecânicas, requisitos, tarefas e testes são rastreados na matriz.
- ✔ Propostas e pendências não foram apresentadas como decisões confirmadas.
- ⚠ Escopo e cronograma dependem de equipe, horas e confirmação do MVP online; risco registrado em RSK-01.

### Técnica React + Phaser
- ✔ Responsabilidades React/Phaser/servidor separadas; contrato de eventos documentado.
- ✔ Ciclo de vida Phaser/React, StrictMode, assinaturas e dados serializáveis especificados.
- ✔ Performance, assets, escala, testes, rede e deploy descritos.
- ⚠ Prova de rede autoritativa e escolha de provedor ainda não executadas; registradas como trabalho pendente.

### Conformidade e inclusão
- ✔ Classificação, LGPD, licenças, acessibilidade, segurança e menores abordados.
- ✔ Monetização não aplicável ao hobby/MVP; sem dark patterns ou anúncios propostos.
- ⚠ ClassInd, política/termos e revisão de privacidade precisam ser finalizados antes de beta público.

### Produção
- ✔ Milestones, backlog MoSCoW, estimativas relativas, DoR/DoD e riscos incluídos.
- ⚠ Calendário e orçamento não aprovados; faltam equipe, horas semanais, prazo e provedor de servidor.

---

## Resultado da auditoria

> GDD implementável como **rascunho de planejamento**, condicionado à resolução das pendências da [Seção 12](./12-pendencias-e-riscos.md) antes de produção online aberta. **Faça playtest e prova técnica antes de congelar balanceamento.**

---

[← Anterior: Pendências e Riscos](./12-pendencias-e-riscos.md) · [🏠 Índice](./README.md)
