# 📚 Documentação — Céu de Aço

Índice central da documentação do projeto. Todo o conteúdo deriva do **GDD v0.7.0** e está dividido em arquivos por seção para facilitar leitura, revisão e histórico no GitHub.

> **Status do projeto:** Rascunho para validação · **Versão do GDD:** `0.7.0` · **Última atualização:** 2026-11-04

---

## Como ler esta documentação

Legendas usadas em todo o texto (mantidas do GDD):

| Marca | Significado |
|---|---|
| **[DECIDIDO]** | Regra confirmada pelo usuário. Não alterar sem nova decisão explícita. |
| **[PROPOSTA]** | Valor/regra inicial para prototipagem e playtest. Não é balanceamento aprovado. |
| **[SUPOSIÇÃO]** | Premissa derivada do brief. Precisa ser validada. |
| **[PENDENTE]** | Informação ausente. Bloqueia produção final do item relacionado. |

---

## Índice de documentos

| # | Documento | Conteúdo |
|---|---|---|
| 01 | [Visão Geral](./01-visao-geral.md) | Elevator pitch, conceito, gênero, pilares, USP, referências, escopo MoSCoW |
| 02 | [Gameplay](./02-gameplay.md) | Core loop, mecânicas (MEC), controles, câmera, física, vitória/derrota, economia, balanceamento |
| 03 | [Conteúdo do Jogo](./03-conteudo-do-jogo.md) | Personagens, entidades, chefes, itens, níveis, level design, narrativa |
| 04 | [Interface e UX/UI](./04-interface-ux-ui.md) | Fluxo de telas, wireframes, HUD, menus, feedback, acessibilidade, i18n |
| 05 | [Arte e Direção Visual](./05-arte-e-direcao-visual.md) | Estilo, paleta, specs técnicas, lista de assets, animações e VFX, nomenclatura |
| 06 | [Áudio](./06-audio.md) | Direção sonora, SFX/BGM, mixagem, autoplay, licenças |
| 07 | [Arquitetura Técnica](./07-arquitetura-tecnica.md) | React + Phaser, stack, pastas, cenas, EventBus, estado, rede, performance, ADRs |
| 08 | [Monetização e Live Ops](./08-monetizacao-e-live-ops.md) | Modelo de negócio, itens, anúncios, roadmap pós-lançamento |
| 09 | [Produção e Gestão](./09-producao-e-gestao.md) | RACI, milestones, backlog, cronograma, DoR/DoD, riscos, orçamento |
| 10 | [Qualidade, Testes e Lançamento](./10-qualidade-testes-e-lancamento.md) | QA, matriz de navegadores, casos de teste, playtest, KPIs, checklist |
| 11 | [Requisitos Consolidados](./11-requisitos-consolidados.md) | REQ-F, REQ-NF e matriz de rastreabilidade |
| 12 | [Pendências e Riscos](./12-pendencias-e-riscos.md) | Decidido, suposições e 11 perguntas abertas |
| 13 | [Apêndices](./13-apendices.md) | Glossário, referências, licenças, relatório de auditoria |
| — | [CHANGELOG](./CHANGELOG.md) | Histórico de versões do GDD |
| — | [GDD Completo](./gdd-completo.md) | Documento único com todas as seções (para leitura linear/export) |

---

## Documentos relacionados na raiz

- [README principal](../README.md) — apresentação do projeto, stack e roadmap resumido.

---

## Convenções de manutenção

1. **Uma decisão por linha de histórico.** Toda alteração de regra confirmada gera entrada no [CHANGELOG](./CHANGELOG.md) e atualização do rodapé de versão do arquivo afetado.
2. **Nunca promover [PROPOSTA] a [DECIDIDO]** sem confirmação explícita registrada.
3. **IDs estáveis.** `MEC-###`, `ENT-###`, `ITM-###`, `LVL-##`, `AST-###`, `SFX-###`, `BGM-##`, `EVT-###`, `REQ-F-###`, `REQ-NF-###`, `BKL-###`, `TST-###`, `RSK-##`, `ADR-##` não devem ser renumerados; itens removidos ficam marcados como obsoletos.
4. **Rastreabilidade obrigatória.** Toda mecânica nova precisa entrar na [matriz de rastreabilidade](./11-requisitos-consolidados.md#113-matriz-de-rastreabilidade).
5. **Textos de UI sempre por chave de i18n** (`menu.play_online`, `match.sudden_death`, `tower.hp`) — nunca strings literais no código.
