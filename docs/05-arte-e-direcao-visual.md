# 5 · Arte e Direção Visual

[← Anterior: Interface e UX/UI](./04-interface-ux-ui.md) · [🏠 Índice](./README.md) · [Próximo: Áudio →](./06-audio.md)

> **Versão do documento:** GDD v0.7.0 · **Data:** 2026-11-04

---

## 5.1 Estilo, referências e moodboard (descrição)

**[PROPOSTA]** 2D top-down de ficção científica, **silhuetas claras e leitura de batalha antes de detalhes**. Contraste entre metal, energia e biomas espaciais. Personagens podem combinar traços de animais e máquinas conforme pedido.

> **[PENDENTE]** Referências visuais específicas e paleta final.
> **Não usar** personagens, logos ou assets de *Sonic*.

---

## 5.2 Paleta de cores (hex) e tipografia

| Uso | Hex |
|---|---|
| Azul espacial (fundo) | `#101B36` |
| Aço (estruturas) | `#75849A` |
| Ciano aliado | `#43D9E6` |
| Âmbar adversário | `#F5A742` |
| Alerta | `#F15B64` |
| Texto | `#F4F6FA` |

Paleta provisória — **verificar contraste em fundos reais** (alvo WCAG 2.2 AA).

**Tipografia provisória:** sans-serif legível para UI; licença e família **[PENDENTE]**.

---

## 5.3 Especificações técnicas: resolução base, tiles/sprites, FPS de animação, formatos, atlas

| Item | Especificação |
|---|---|
| Resolução lógica | 1280×720, `Scale.FIT`, `CENTER_BOTH`, paisagem |
| Tiles | 64×64 px sugerido |
| Sprites | Dimensionados para legibilidade na câmera; **pixel art ainda não escolhida** |
| Animações | 8–12 FPS [PROPOSTA] |
| Render | 60 FPS desktop |
| Formato | PNG para sprites com transparência; WebP para fundos/UI quando suportado |
| Atlas | Até 2048×2048 (foco mobile futuro) |

---

## 5.4 Lista de assets visuais

| ID | Nome | Dimensões | Frames | Prioridade | Status | Origem/licença |
|---|---|---:|---:|---|---|---|
| AST-001 | Piloto base | A definir | 6 estados | Must | Placeholder | Pendente; criar/adquirir com licença registrada. |
| AST-002 | Tanque | A definir | 3 estados | Must | Placeholder | Pendente. |
| AST-003 | Avião | A definir | 3 estados | Must | Placeholder | Pendente. |
| AST-004 | Torre de defesa | A definir | 2 estados | Must | Placeholder | Pendente. |
| AST-005 | Torre principal | A definir | 3 estados | Must | Placeholder | Pendente. |
| AST-006 | Arena e tiles | 1280×720 lógica | — | Must | Blockout | Tiled; origem/licença pendente. |
| AST-007 | Efeitos de tiro/explosão | A definir | 4–8 | Should | Não iniciado | Pendente. |
| AST-008 | Ícones da UI | 32–64 px | — | Must | Não iniciado | Criar original/licença pendente. |

---

## 5.5 Animações e VFX

Idle (inclui sentar/olhar ao redor), movimento, ataque, dano, habilidade, destruição e respawn. **Explosões têm duração curta e não obscurecem telegraphs.** Redução de movimento desliga shake e reduz partículas.

---

## 5.6 Convenções de nomenclatura e pastas

| Prefixo | Uso |
|---|---|
| `spr_pilot_*`, `spr_tank_*`, `spr_aircraft_*`, `spr_tower_*` | Sprites/atlas |
| `bg_*` | Fundos |
| `ui_*` | Interface |
| `tm_*` | Tilemaps |
| `sfx_*`, `bgm_*` | Áudio |

Regras: **snake_case**; arquivos por atlas; licenças em `assets/licenses/`. Pasta recomendada em [7.3](./07-arquitetura-tecnica.md#73-estrutura-de-pastas-do-projeto).

---

[← Anterior: Interface e UX/UI](./04-interface-ux-ui.md) · [🏠 Índice](./README.md) · [Próximo: Áudio →](./06-audio.md)
