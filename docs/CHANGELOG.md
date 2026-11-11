# Changelog — GDD *Céu de Aço*

Todas as mudanças relevantes neste documento são registradas aqui.
Formato inspirado em [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/); versionamento semântico `MAJOR.MINOR.PATCH`.

- **MAJOR** — mudança que altera regra confirmada ou reestrutura o documento.
- **MINOR** — nova regra, mecânica, requisito ou seção.
- **PATCH** — correção, esclarecimento ou formatação.

[🏠 Índice](./README.md)

---

## [0.7.0] — 2026-11-04

### Adicionado
- **MEC-013 / REQ-F-016 / BKL-014 / TST-012:** seleção pré-partida — cada um dos seis jogadores escolhe um personagem da lista; servidor valida e sincroniza as escolhas das duas equipes.
- **EVT-009 / EVT-010:** eventos de ponte para seleção de personagem (`lobby:select-character`, `lobby:pick-state`).
- **UI-03:** wireframe da tela de seleção de personagem.

### Pendente
- Regra de repetição de personagem na mesma equipe, tamanho do elenco, tempo limite de seleção e tratamento de jogador que não escolhe.

---

## [0.6.0] — 2026-11-04

### Alterado
- **Regra de recompensa do chefe fechada:** a equipe do jogador que dá o golpe final recebe **+15% velocidade e +5% dano por 90 s** (antes: percentuais propostos para teste).
- **REQ-F-015 / TST-011 / BKL-013** atualizados para refletir a decisão; sem acúmulo.

---

## [0.5.0] — 2026-11-04

### Adicionado
- Aviso do chefe aos **4:30**.
- Bônus temporário por derrotar o chefe: aumento de velocidade e pequeno bônus de dano por **90 s** (percentuais propostos para teste).
- **RSK-09:** risco de o chefe favorecer demais uma equipe / snowball.

---

## [0.4.0] — 2026-11-04

### Alterado
- **Horário de surgimento do chefe revisado de 15 para 5 min** conforme correção do usuário; timing marcado para playtest.

---

## [0.3.0] — 2026-11-04

### Adicionado
- **MEC-012 / ENT-007:** chefe neutro gigante (300 m) surge no centro aos 15 min (valor posteriormente revisado para 5 min) e ataca quem se aproxima.
- Recompensa do chefe registrada como pendente naquele momento.

---

## [0.2.0] — 2026-11-04

### Adicionado
- Torres de defesa e torre principal atacam inimigos automaticamente.
- **HP da torre de defesa dividido em 5 segmentos de 5.000** (25.000 HP totais).

### Pendente
- Prioridade e tipos de alvo das torres.

---

## [0.1.0] — 2026-11-04

### Adicionado
- Primeiro GDD a partir do **Game Brief aprovado**.
- Estrutura completa de 13 seções.
- Separação explícita entre **regras confirmadas**, **propostas** e **pendências**.

---

## Próxima versão planejada — 0.8.0

Candidatos (dependem de decisão do usuário):

- [ ] Confirmar escopo do MVP online (Pendência 1).
- [ ] Definir número e posição das torres de defesa (Pendência 4).
- [ ] Definir regra de repetição de personagens e tempo de seleção (Pendência 11).
- [ ] Definir prazo, equipe e horas semanais (Pendência 2).
- [ ] Substituir o cronograma ilustrativo por um calendário aprovado.
