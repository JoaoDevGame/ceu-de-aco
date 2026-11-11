<div align="center">

# 🚀 Céu de Aço

**Jogo 2D de estratégia espacial 3v3 em tempo real — React + Phaser + TypeScript**

**Status:** rascunho para validação · **GDD:** v0.7.0 · **Plataforma:** desktop web

<sub>Documentação completa em [<code>docs/</code>](./docs/README.md)</sub>

</div>

---

## 📖 Sobre o projeto

*Céu de Aço* é um jogo de estratégia espacial 2D jogável no navegador, em que **equipes de três jogadores** coordenam personagens, tanques, aviões e torres para destruir a base inimiga. As partidas duram **até 30 minutos**; se o relógio chegar ao fim sem vencedor, entra em vigor a **morte súbita**: todas as torres de defesa explodem e as torres principais de ambos os lados ficam com **1 HP** — o primeiro ataque válido à base decide o jogo.

Antes da partida, cada um dos seis jogadores escolhe **um personagem da lista**. O jogo terá ainda unidades terrestres e aéreas, personagens com traços inspirados em animais e máquinas, além de **modo história e lore**.

> ⚠️ **Este repositório está na fase de documentação (GDD).** Não há código de jogo implementado. As regras marcadas como *[PROPOSTA]* ou *[PENDENTE]* ainda podem mudar.

---

## 🎯 Pilares de design

1. **Estratégia com escolhas** — mais de uma composição deve poder vencer.
2. **Trabalho em equipe** — cada integrante do 3v3 contribui; a partida não deve ser decidida por uma pessoa.
3. **Combate legível** — vida, alcance, perigo e estado da base são claros, inclusive para novos jogadores.
4. **Mundo original de aço e estrelas** — identidade própria, sem copiar personagens ou marcas existentes.

*Status: [PROPOSTA] — a confirmar na próxima revisão.*

---

## 💻 Plataforma alvo

| Item | Valor |
|---|---|
| Plataforma | Desktop web (paisagem) |
| Controles | Teclado e mouse |
| Stack | React + Phaser + TypeScript + Vite |
| Servidor | Node.js + TypeScript autoritativo (WebSocket / Colyseus a validar) |
| Resolução lógica | 1280×720, `Scale.FIT` + `CENTER_BOTH` |
| Meta de render | 60 FPS |
| Público | Fãs de estratégia e ficção científica — ClassInd 10 [SUPOSIÇÃO] |
| Modelo | Portfólio/hobby, sem monetização no MVP |

Mobile, gamepad e chat de voz/texto estão **fora do MVP**.

---

## 🗂️ Estrutura da documentação

Todos os documentos ficam em [`docs/`](./docs/README.md):

| Documento | O que cobre |
|---|---|
| [01 · Visão Geral](./docs/01-visao-geral.md) | Pitch, conceito, pilares, USP, escopo MoSCoW |
| [02 · Gameplay](./docs/02-gameplay.md) | Core loop, MEC-001 a MEC-013, controles, economia, balanceamento |
| [03 · Conteúdo do Jogo](./docs/03-conteudo-do-jogo.md) | Personagens, entidades, itens, níveis, level design, narrativa |
| [04 · Interface e UX/UI](./docs/04-interface-ux-ui.md) | Fluxo de telas, wireframes, HUD, acessibilidade, i18n |
| [05 · Arte e Direção Visual](./docs/05-arte-e-direcao-visual.md) | Estilo, paleta, specs, assets, VFX |
| [06 · Áudio](./docs/06-audio.md) | Direção sonora, SFX/BGM, mixagem, licenças |
| [07 · Arquitetura Técnica](./docs/07-arquitetura-tecnica.md) | React ↔ Phaser, EventBus, servidor autoritativo, ADRs |
| [08 · Monetização e Live Ops](./docs/08-monetizacao-e-live-ops.md) | Modelo de negócio (não aplicável ao MVP) |
| [09 · Produção e Gestão](./docs/09-producao-e-gestao.md) | RACI, milestones, backlog, riscos |
| [10 · Qualidade e Testes](./docs/10-qualidade-testes-e-lancamento.md) | QA, casos de teste, playtest, KPIs, checklist |
| [11 · Requisitos](./docs/11-requisitos-consolidados.md) | REQ-F e REQ-NF com rastreabilidade |
| [12 · Pendências e Riscos](./docs/12-pendencias-e-riscos.md) | O que está decidido e o que falta decidir |
| [13 · Apêndices](./docs/13-apendices.md) | Glossário, referências, auditoria |
| [CHANGELOG](./docs/CHANGELOG.md) | Histórico de versões do GDD |
| [GDD Completo](./docs/gdd-completo.md) | Todas as seções em arquivo único |

---

## 📊 Regras-chave já confirmadas

| Regra | Valor |
|---|---|
| Formato | 3v3 (seis jogadores por partida) |
| Limite de partida | 30 minutos |
| HP torre de defesa | 25.000 (5 segmentos de 5.000) |
| HP torre principal | 45.000 (barra contínua) |
| Morte súbita | Defesas explodem; bases com 1 HP; primeiro ataque decide |
| Chefe neutro | Aviso aos 4:30, surge no centro aos 5:00; altura canônica 300 m |
| Recompensa do chefe | Equipe do golpe final: +15% velocidade e +5% dano por 90 s, sem acúmulo |
| Seleção pré-partida | Cada jogador escolhe um personagem da lista |

Detalhes, valores de teste e o que ainda está pendente: [`docs/02-gameplay.md`](./docs/02-gameplay.md) e [`docs/12-pendencias-e-riscos.md`](./docs/12-pendencias-e-riscos.md).

---

## 🛣️ Roadmap resumido

| Milestone | Foco | Critério de saída |
|---|---|---|
| **Protótipo** | Arena blockout contra bots: movimento, ataque, HP, torres, timer, morte súbita | Partida offline reproduzível; regra principal validada em playtest |
| **Vertical Slice** | Arena polida, prólogo, bot, prova de rede 1v1 e sessão 3v3 controlada | Servidor autoritativo calculando HP, timer e resultado |
| **Alpha** | Lobby, seleção de personagem, unidades, economia, 3v3 fechado | Partida completa com reconexão básica; sem bugs bloqueadores |
| **Beta** | Testes externos, balanceamento, acessibilidade, privacidade, carga | Crash-free ≥99%; sem falha crítica de segurança |
| **Release** | Build web, servidor monitorado, termos, créditos, suporte | Checklist da seção 10 concluído |

Prazos e equipe: **[PENDENTE]**. O cronograma do GDD é apenas cenário ilustrativo.

---

## 🤝 Como contribuir

- Discussões de design devem citar o **ID** do item (`MEC-003`, `REQ-F-014`, `RSK-02`…).
- Alterações em regras confirmadas exigem decisão explícita e entrada no [CHANGELOG](./docs/CHANGELOG.md).
- Nada entra como "decidido" sem registro em [`docs/12-pendencias-e-riscos.md`](./docs/12-pendencias-e-riscos.md).
- Assets de terceiros: registrar autor, URL, licença e data em [`docs/13-apendices.md`](./docs/13-apendices.md#c-créditos-e-licenças-de-terceiros) **antes** do commit.

---

## 📄 Licença

A definir. Nenhum asset de produção foi selecionado; todo conteúdo de terceiros precisa de licença compatível e atribuição antes do release.

Não usar personagens, arte, música ou marcas de jogos existentes (ex.: *Sonic* foi citado apenas como referência de **animação de idle**).

---

<div align="center">

**Céu de Aço** · GDD v0.7.0 · 2026-11-04 · projeto de portfólio/hobby

</div>
