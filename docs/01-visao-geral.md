# 1 · Visão Geral

[🏠 Índice](./README.md) · [Próximo: Gameplay →](./02-gameplay.md)

> **Versão do documento:** GDD v0.7.0 · **Data:** 2026-11-04 · **Status:** Rascunho para validação

---

## 1.1 Elevator Pitch (máx. 50 palavras)

> *Céu de Aço* é um jogo 2D de estratégia espacial em que equipes de três jogadores coordenam personagens, tanques, aviões e torres para destruir a base inimiga. As partidas duram até 30 minutos; na morte súbita, as defesas explodem e as torres principais ficam com 1 ponto de vida.

---

## 1.2 Conceito de alto nível

Jogo de estratégia/defesa de base com partidas PvP online 3v3; antes da partida, cada jogador escolhe um personagem de uma lista. Inclui unidades terrestres e aéreas e personagens com habilidades inspiradas em animais e máquinas. O projeto também terá modo de história e lore. O primeiro protótipo valida a batalha contra bots; a meta de lançamento inclui o 3v3 online.

> ⚠️ **[PENDENTE]** A forma exata de controlar personagens e comandar unidades ainda é uma pendência de design.

---

## 1.3 Gênero, plataforma e público-alvo

- **Gênero:** estratégia em tempo real + defesa de base + ação tática `[SUPOSIÇÃO a partir do limite de 30 minutos, unidades e torres]`.
- **Plataforma:** desktop web, paisagem, teclado e mouse `[SUPOSIÇÃO aprovada como base do brief]`.
- **Stack:** React + Phaser + TypeScript + Vite.
- **Público:** fãs de estratégia e ficção científica. Faixa sugerida: 10+ `[SUPOSIÇÃO; validar classificação]`.
- **Dificuldade:** oferecer níveis selecionáveis. **Não usar idade informada para definir pareamento no MVP.**

---

## 1.4 Pilares de design

Os pilares abaixo são uma **[PROPOSTA]** derivada do brief; confirmar na próxima revisão.

1. **Estratégia com escolhas:** mais de uma composição deve poder vencer; decisões precisam ter resposta compreensível.
2. **Trabalho em equipe:** cada integrante do 3v3 contribui; a partida não deve ser decidida apenas por uma pessoa.
3. **Combate legível:** vida, alcance, perigo e estado da base são claros, inclusive para novos jogadores.
4. **Mundo original de aço e estrelas:** personagens, veículos e lore têm identidade própria; sem copiar personagens ou marcas existentes.

---

## 1.5 USP / Diferenciais

Combina partidas de base com **três jogadores por lado**, estruturas com **pontos de vida elevados**, unidades terrestres/aéreas e **heróis com traços animais ou mecânicos**.

> O diferencial precisa ser validado por playtests; **ainda não há pesquisa de mercado**.

---

## 1.6 Jogos de referência e diferenciação

- O usuário citou **Sonic** no contexto de personagens que fazem animações quando ficam parados. Isso fica registrado como referência de **animação de espera**, **não** como autorização para copiar personagens, arte, música ou mecânicas protegidas.
- Outras referências: **[PENDENTE — usuário ainda não indicou jogos de estratégia como referência]**.
- **Diferenciação:** guerra espacial original, equipes 3v3 e regra própria de morte súbita descrita em [2.6](./02-gameplay.md#26-regras-de-vitória-derrota-continue-e-respawn).

---

## 1.7 Experiência-alvo do jogador (emoções e fantasia de poder)

Sentir **desafio, cooperação e autoria estratégica**: escolher como contribuir para a equipe, defender a própria base e pressionar a base rival. A história e a lore devem recompensar a exploração fora das partidas competitivas.

---

## 1.8 Classificação indicativa prevista e justificativa

**[SUPOSIÇÃO] ClassInd 10**, sujeita a avaliação oficial. A premissa inclui guerra e combate ficcional, mas este GDD propõe **violência estilizada, sem gore, linguagem imprópria ou compra aleatória**. A classificação final depende dos conteúdos efetivamente produzidos e da avaliação aplicável.

---

## 1.9 Escopo: Dentro / Fora (MoSCoW)

| Prioridade | Escopo |
|---|---|
| **Must** | Protótipo de batalha contra bots; duas equipes; base principal e torres de defesa; tanques e aviões; personagens e habilidades; regra de partida de 30 min e morte súbita; prova técnica de rede; versão-alvo com 3v3 online; acessibilidade básica; save local de configurações. |
| **Should** | Uma arena competitiva; lobby e reconexão; loja simples de recursos/upgrades; prólogo de história com lore; bots para vagas de teste; pings predefinidos sem chat livre. |
| **Could** | Mais mapas, personagens, tipos de unidade, campanha maior, replay e estatísticas detalhadas. |
| **Won't (primeira versão)** | Chat de texto/voz, ranking competitivo, monetização, contas de menores, matchmaking por idade, clãs, cross-play mobile e multiplayer cooperativo PvE. |

**Plano de escopo:** "3v3 online" é requisito da versão-alvo. O "ok" do usuário foi interpretado como aceitação da rota **protótipo contra bots → 3v3 online antes do lançamento**; confirmar em revisão se a interpretação estiver errada (ver [Pendência 1](./12-pendencias-e-riscos.md)).

---

[🏠 Índice](./README.md) · [Próximo: 2 · Gameplay →](./02-gameplay.md)
