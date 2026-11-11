# 11 · Requisitos Consolidados

[← Anterior: Qualidade e Testes](./10-qualidade-testes-e-lancamento.md) · [🏠 Índice](./README.md) · [Próximo: Pendências e Riscos →](./12-pendencias-e-riscos.md)

> **Versão do documento:** GDD v0.7.0 · **Data:** 2026-11-04

---

## 11.1 Requisitos funcionais (REQ-F-###)

| ID | Requisito |
|---|---|
| **REQ-F-001** | O cliente deve apresentar arena 2D jogável e movimento dentro dos limites. |
| **REQ-F-002** | Cada torre de defesa deve iniciar com **25.000 HP**. |
| **REQ-F-003** | Cada torre principal deve iniciar com **45.000 HP**, atacar inimigos automaticamente **um de cada vez** [alvo/prioridade pendentes] e encerrar a partida ao ser destruída. |
| **REQ-F-004** | Ao atingir **30:00** sem vencedor, o servidor deve remover torres de defesa e ajustar cada torre principal para **1 HP**. |
| **REQ-F-005** | O jogo deve representar tanques e aviões com papéis e comandos distinguíveis. |
| **REQ-F-006** | A loja deve bloquear compras sem saldo e registrar alterações de recursos no servidor em partida online. |
| **REQ-F-007** | O personagem deve ter habilidade com recarga e efeito validado. |
| **REQ-F-008** | O modo história deve oferecer prólogo/lore no escopo inicial; campanha completa fica fora do primeiro recorte. |
| **REQ-F-009** | O servidor autoritativo deve validar dano, timer, HP, recursos e resultado. |
| **REQ-F-010** | A versão-alvo deve permitir partida **3v3 online** (seis jogadores) em uma sala. |
| **REQ-F-011** | O usuário deve poder ajustar áudio, controles básicos e acessibilidade suportada. |
| **REQ-F-012** | O cliente deve mostrar conexão, reconexão, erro e resultado de partida. |
| **REQ-F-013** | Torres de defesa devem iniciar com **25.000 HP** apresentados em **5 segmentos de 5.000 HP**; torres de defesa e principais devem atacar **no máximo um inimigo por vez** [tipos e prioridade de alvo pendentes]. |
| **REQ-F-014** | Anunciar o chefe aos **4:30** e criar o chefe neutro no centro aos **5:00** [horário proposto a testar]; atacar entidades que se aproximem segundo raio/alvo definidos após playtest. |
| **REQ-F-015** | O servidor deve identificar a equipe do jogador que desfere o **golpe final** no chefe e conceder a essa equipe **+15% velocidade** e **+5% dano** por **90 s**, **sem acúmulo**. |
| **REQ-F-016** | Antes da partida 3v3, cada um dos **seis jogadores** deve selecionar um personagem da lista; o servidor valida e sincroniza as escolhas das duas equipes. |

---

## 11.2 Requisitos não funcionais (REQ-NF-###)

| ID | Requisito |
|---|---|
| **REQ-NF-001** | Renderizar a **60 FPS** alvo em desktop de referência; teste de hardware definirá mínimo. |
| **REQ-NF-002** | Protocolo de partida deve ser **autoritativo**, validado e protegido por HTTPS/WSS e limites de taxa. |
| **REQ-NF-003** | A UI deve suportar contraste, remapeamento, redução de movimento e indicadores que **não dependam só de cor**. |
| **REQ-NF-004** | Coletar apenas dados estritamente necessários; **sem idade/data de nascimento ou chat livre** no MVP. |
| **REQ-NF-005** | Bundle inicial gzip **<500 KB** excluindo Phaser; assets da primeira arena **<10 MB** (metas a verificar). |
| **REQ-NF-006** | Suporte inicial a versões atuais de **Chrome, Firefox, Edge e Safari** desktop. |
| **REQ-NF-007** | O servidor mantém consistência de estado com **seis clientes** de teste e registra desconexões **sem PII**. |
| **REQ-NF-008** | Regras puras devem ter testes unitários; build passa `lint`, `tsc`, testes e **bundle-size check**. |

---

## 11.3 Matriz de rastreabilidade

| Mecânica | Requisito | Tarefa | Teste |
|---|---|---|---|
| MEC-001 equipes 3v3 | REQ-F-009, REQ-F-010, REQ-NF-007 | BKL-009 | TST-006 |
| MEC-002 movimento | REQ-F-001, REQ-NF-001 | BKL-001 | TST-006 |
| MEC-003 ataque | REQ-F-009 | BKL-002, BKL-008 | TST-001, TST-005 |
| MEC-004 torres de defesa | REQ-F-002, REQ-F-004, REQ-F-013 | BKL-002, BKL-003 | TST-001, TST-003, TST-009 |
| MEC-005 torre principal | REQ-F-003, REQ-F-009, REQ-F-013 | BKL-002, BKL-008 | TST-002, TST-005, TST-009 |
| MEC-006 tanque/avião | REQ-F-005 | BKL-004 | TST-006 |
| MEC-007 economia | REQ-F-006 | BKL-005 | TST-005 |
| MEC-008 morte súbita | REQ-F-004 | BKL-003 | TST-003, TST-004 |
| MEC-009 traços/habilidade | REQ-F-007 | BKL-006 | TST-005 |
| MEC-010 idle | REQ-F-001 | BKL-001 | TST-006 |
| MEC-011 história/lore | REQ-F-008 | BKL-007 | TST-008 |
| MEC-012 chefe neutro | REQ-F-014, REQ-F-009, REQ-F-015 | BKL-012, BKL-013 | TST-010, TST-011 |
| MEC-013 seleção de personagem | REQ-F-016, REQ-F-010 | BKL-014, BKL-009 | TST-012 |

---

[← Anterior: Qualidade e Testes](./10-qualidade-testes-e-lancamento.md) · [🏠 Índice](./README.md) · [Próximo: Pendências e Riscos →](./12-pendencias-e-riscos.md)
