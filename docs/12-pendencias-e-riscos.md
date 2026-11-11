# 12 · Premissas, Riscos Abertos e Perguntas Pendentes

[← Anterior: Requisitos Consolidados](./11-requisitos-consolidados.md) · [🏠 Índice](./README.md) · [Próximo: Apêndices →](./13-apendices.md)

> **Versão do documento:** GDD v0.7.0 · **Data:** 2026-11-04

Este documento é o **único lugar onde uma regra pode mudar de status**. Qualquer promoção de `[PROPOSTA]`/`[SUPOSIÇÃO]` para `[DECIDIDO]` deve ser registrada aqui e no [CHANGELOG](./CHANGELOG.md).

---

## ✅ [DECIDIDO] pelo usuário

- Nome: ***Céu de Aço***.
- Guerra espacial com estratégia; jogadores podem criar suas estratégias.
- Deve haver modo de história/lore, loja, recursos/upgrades, inimigos, NPCs e chefes.
- Um **chefe neutro de 300 m** surge no centro aos **5 min** [horário proposto a validar] e ataca quem se aproxima.
- **Aviso 30 s antes do chefe** (4:30, para surgimento proposto aos 5:00). A equipe do jogador que desfere o golpe final recebe **+15% velocidade e +5% dano por 90 s**.
- O jogo terá **torres, aviões, tanques** e personagens com características de animais/máquinas, visuais e mecânicas.
- **Partida 3v3**; cada jogador escolhe **um personagem de uma lista antes da partida**; as duas equipes fazem o mesmo; **limite de 30 minutos**; **morte súbita**.
- HP de cada torre de defesa: **25.000**; HP da torre principal: **45.000**.
- Torres de defesa e torre principal atacam inimigos, **um alvo por vez** [interpretação a confirmar; prioridade/tipos pendentes].
- A torre de defesa tem 25.000 HP em **5 segmentos de 5.000 HP**; a torre principal tem 45.000 HP em **barra contínua**.
- Na morte súbita, as torres de defesa explodem e cada torre principal fica com **1 HP**.
- Projeto de **portfólio/hobby**; usuário iniciante.

---

## 🔶 [SUPOSIÇÃO] usada neste documento

- 2D top-down em **desktop web**, paisagem, teclado/mouse.
- Combate em **tempo real**; partida online **sem pausa individual**.
- **Protótipo contra bots primeiro**; 3v3 online antes do lançamento. Interpretado do "ok" do usuário à rota sugerida.
- **Uma arena inicial**; dois pontos/torres defensivas por equipe; equipe **compartilha recursos**.
- **Um personagem** controlado por jogador; dano simultâneo às duas bases na morte súbita resulta em **empate**.
- **ClassInd provisória 10**; violência estilizada e sem gore.

---

## ❓ [PENDENTE] para próxima revisão

| # | Pendência | Bloqueia |
|---|---|---|
| 1 | Confirmar se a interpretação do "ok" sobre **protótipo contra bots** está correta e se **3v3 precisa estar no MVP** ou somente antes do lançamento. | Escopo / cronograma |
| 2 | Definir **prazo, tamanho da equipe e horas disponíveis por semana**; cronograma atual é apenas cenário. | Planejamento |
| 3 | Confirmar **faixa etária, classificação indicativa** e se haverá matchmaking por habilidade (não por idade). | Conteúdo / legal |
| 4 | Definir **número/posição das torres de defesa**, condição de **proteção da base**, quais inimigos as torres podem atacar e **prioridade de alvo**; definir resultado de **ataques simultâneos**. | MEC-004, MEC-005, MEC-008 |
| 5 | Definir **papéis/controles exatos** de personagem, tanques, aviões e construção; confirmar tempo real com pausa somente no modo treino/offline. | MEC-002, MEC-003, MEC-006 |
| 6 | Definir **fontes e custos de recursos**, valores de dano, respawn, habilidades e bots. | MEC-007, balanceamento |
| 7 | Definir **trama, facções, nomes, estilo visual final, áudio, origem/licença dos assets**. | Arte, áudio, narrativa |
| 8 | Validar em **playtest o horário de 5 min**; definir **HP, dano, raio de aproximação e seleção de alvo do chefe**. | MEC-012 |
| 9 | Definir **provedor/região/custo do servidor** e **política de privacidade** para beta. | Backend / beta |
| 10 | Definir o que significa **"personagens de 10 anos mais fáceis e 18 mais difíceis"**: recomendação atual é dificuldade escolhida, **sem coletar idade**. | UX / legal |
| 11 | Definir se uma equipe pode **repetir personagens**, **tamanho do elenco**, **tempo limite de seleção** e como lidar com **jogador que não escolhe**. | MEC-013 / REQ-F-016 |

---

## 🔗 Referências cruzadas

- Riscos técnicos e de produção: [seção 9.6](./09-producao-e-gestao.md#96-gestão-de-riscos-prob--impacto--mitigação--dono).
- Parâmetros marcados como pendentes na tabela de balanceamento: [seção 2.11](./02-gameplay.md#211-balanceamento-inicial-tabela-de-parâmetros-tunáveis-com-valores-padrão-min-e-max).
- Relatório de auditoria do GDD: [Apêndice D](./13-apendices.md#d-relatório-de-auditoria-do-gdd).

---

[← Anterior: Requisitos Consolidados](./11-requisitos-consolidados.md) · [🏠 Índice](./README.md) · [Próximo: Apêndices →](./13-apendices.md)
