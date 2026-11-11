# 3 · Conteúdo do Jogo

[← Anterior: Gameplay](./02-gameplay.md) · [🏠 Índice](./README.md) · [Próximo: Interface e UX/UI →](./04-interface-ux-ui.md)

> **Versão do documento:** GDD v0.7.0 · **Data:** 2026-11-04

---

## 3.1 Personagem(ns) jogável(is): atributos, habilidades, estados, animações

Cada um dos **seis jogadores escolhe um personagem de uma lista antes da partida**; três escolhas para cada equipe, com o mesmo processo para o time inimigo. **[PROPOSTA]** O jogador controla o personagem escolhido. Tipos de traço podem ser **animal, mecânico ou híbrido**, afetando visual e habilidade.

> **[PENDENTE]** Lista final, tamanho do elenco e regra de repetição de personagem.

### Estados do personagem

| Estado | Descrição | Transição |
|---|---|---|
| `idle` | Parado; pode sentar/olhar ao redor após atraso cosmético [tempo pendente]. | Input válido → `move`. |
| `move` | Movimento e orientação para cursor/alvo. | Sem input → `idle`; ataque → `attack`. |
| `attack` | Animação e solicitação validada pelo servidor. | Fim da animação → `move`/`idle`. |
| `ability` | Habilidade única com cooldown. | Cooldown/efeito concluído → estado anterior. |
| `damaged` | Feedback visual breve; não bloquear controle excessivamente. | Após hit feedback → `move`/`idle`. |
| `defeated` | Aguarda respawn proposto de 8 s. | Respawn validado → `move`. |

**Animações mínimas:** idle, move, attack, ability, hit, defeated/respawn. A animação de espera **nunca** deve bloquear input ou conceder vantagem.

---

## 3.2 Inimigos / NPCs / Chefes: comportamento (FSM/Behavior), stats, telegraph

### Entidades

- **ENT-002 — Torre principal:** objetivo de cada equipe; **45.000 HP**; ataca inimigos automaticamente, **um por vez** [interpretação a confirmar]; barra de HP **contínua**. Estado validado pelo servidor.
- **ENT-003 — Torre de defesa:** **25.000 HP** cada, divididos em **5 segmentos de 5.000 HP**; quantidade/posicionamento [SUPOSIÇÃO: 2 por lado]. Ataca um inimigo válido por vez [interpretação a confirmar]. **Tipos de alvo e prioridade [PENDENTE].**
- **ENT-004 — Tanque:** unidade terrestre, lenta e resistente [PROPOSTA].
- **ENT-005 — Avião:** unidade aérea, rápida e menos resistente [PROPOSTA].
- **ENT-006 — NPCs:** unidades de rota/objetivo controladas por IA simples; comportamento exato [PENDENTE].
- **ENT-007 — Chefe neutro:** criatura gigante de **300 m**; aviso aos **4:30** e surgimento proposto aos **5:00** no centro da arena; ataca quem se aproxima. Escala visual adaptada para não cobrir HUD/arena. A equipe do jogador que acerta o **golpe final** ganha **+15% velocidade e +5% dano por 90 s**. HP, raio e dano do chefe continuam pendentes.

### FSM de unidade básica [PROPOSTA]

```text
Spawn → MoveToObjective → AcquireTarget → Telegraph → Attack → Recover → MoveToObjective
   └── (morte) ──> Defeated → Respawn/Remove
```

Ataques de alto dano devem ter **telegraph visual e sonoro** antes do impacto.

---

## 3.3 Itens, power-ups e coletáveis

| ID | Item | Descrição | Estado |
|---|---|---|---|
| ITM-001 | Créditos de equipe | Recurso abstrato para compras; saldo autoritativo. | Definido |
| ITM-002 | Upgrade de unidade | Altera um atributo dentro de limites; sem bônus oculto. | Definido |
| ITM-003 | Reparo | [PROPOSTA], custo e limite pendentes; **não pode reparar a base durante morte súbita**. | Pendente |

### Recompensa do chefe

A equipe que derrota o chefe recebe um **bônus coletivo de 90 s**: velocidade aumentada e um pouco mais de dano.

> **[DECIDIDO]** O servidor identifica a equipe do jogador que desfere o **golpe final** e concede **+15% velocidade** e **+5% dano** por **90 s**, **uma única vez**, sem acúmulo.

**Power-ups temporários:** não aplicáveis no primeiro protótipo — manter escopo simples.

---

## 3.4 Níveis / Mundos / Fases: lista, objetivo, novidades, duração estimada

| ID | Conteúdo | Objetivo | Duração |
|---|---|---|---|
| LVL-01 | Arena competitiva inicial | Testar 3v3, bases, torres, tanque/avião, chefe neutro aos 5 min e morte súbita. | Até 30 min + morte súbita; duração média a medir. |
| LVL-02 | Missão de prólogo | Ensinar controles contra bots e apresentar contexto da guerra/lore. | 5–8 min [PROPOSTA]. |
| LVL-03 | Cenário de teste de rede | Validar movimento, dano, reconexão e sincronização com poucos jogadores. | 5–10 min por rodada [PROPOSTA]. |

Uma **arena única** é suficiente para o primeiro lançamento de teste. Mapas adicionais ficam fora do MVP.

---

## 3.5 Level design: princípios, ritmo, teaching moments, ferramentas (Tiled)

- **Simetria inicial** entre os lados; distâncias equivalentes entre spawn, torres e base.
- Linhas de ataque e áreas de cobertura devem ser **legíveis**; não esconder ataque letal atrás de efeitos.
- **Tutorial:** apresentar movimento → ataque → torre → unidade → base → morte súbita.
- Arena construída em **Tiled** com camadas `ground`, `collision`, `structures`, `spawn`, `objectives`, `decor`; testar espelhamento dos lados.

---

## 3.6 Narrativa e personagens: sinopse, tom, diálogos, estrutura

O usuário confirmou **modo de história e lore**, mas ainda não forneceu trama, facções, nomes ou tom.

> **[PENDENTE — definir antes de produzir diálogo/arte final].**

**Proposta:** prólogo curto apresenta a guerra espacial e ensina controles; lore é entregue por cenas breves e registros opcionais. **Evitar exposition durante combate competitivo.**

---

[← Anterior: Gameplay](./02-gameplay.md) · [🏠 Índice](./README.md) · [Próximo: Interface e UX/UI →](./04-interface-ux-ui.md)
