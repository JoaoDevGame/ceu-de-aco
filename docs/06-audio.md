# 6 · Áudio

[← Anterior: Arte e Direção Visual](./05-arte-e-direcao-visual.md) · [🏠 Índice](./README.md) · [Próximo: Arquitetura Técnica →](./07-arquitetura-tecnica.md)

> **Versão do documento:** GDD v0.7.0 · **Data:** 2026-11-04

---

## 6.1 Direção sonora e referências

**[PROPOSTA]** Ficção científica com percussão eletrônica e motivos de metal/energia. Referências específicas **[PENDENTE]**. A música deve **preservar a leitura de alertas da partida**.

---

## 6.2 Lista de SFX e músicas

| ID | Gatilho | Duração | Loop | Volume inicial | Formato |
|---|---|---:|---|---:|---|
| SFX-001 | Ataque básico | <1 s | Não | 0,7 | OGG + M4A fallback |
| SFX-002 | Torre recebe dano | <1 s | Não | 0,8 | OGG + M4A fallback |
| SFX-003 | Torre destruída | 1–2 s | Não | 0,9 | OGG + M4A fallback |
| SFX-004 | Início da morte súbita | 2–3 s | Não | 0,9 | OGG + M4A fallback |
| SFX-005 | Habilidade disponível/acionada | <1 s | Não | 0,6 | OGG + M4A fallback |
| BGM-01 | Menu | 1–3 min | Sim | 0,35 | OGG + M4A fallback |
| BGM-02 | Partida | 1–3 min | Sim | 0,3 | OGG + M4A fallback |
| BGM-03 | História | 1–3 min | Sim | 0,35 | OGG + M4A fallback |

Volumes relativos de teste; **sliders Master/Música/SFX** controlados pelo usuário.

---

## 6.3 Mixagem, ducking e regras de autoplay do navegador

- Desbloquear `AudioContext` **após gesto explícito** do usuário.
- Alertas de gameplay podem baixar a música em **até 6 dB** [PROPOSTA].
- Limitar polifonia; variar pitch levemente em SFX repetidos; respeitar mute e volume salvo.

---

## 6.4 Licenças e créditos

Nenhum áudio final está selecionado. **Registrar autor, licença, comprovante e atribuição** de cada arquivo antes do release. Não usar música de jogos existentes.

---

[← Anterior: Arte e Direção Visual](./05-arte-e-direcao-visual.md) · [🏠 Índice](./README.md) · [Próximo: Arquitetura Técnica →](./07-arquitetura-tecnica.md)
