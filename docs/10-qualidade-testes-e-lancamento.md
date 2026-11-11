# 10 · Qualidade, Testes e Lançamento

[← Anterior: Produção e Gestão](./09-producao-e-gestao.md) · [🏠 Índice](./README.md) · [Próximo: Requisitos Consolidados →](./11-requisitos-consolidados.md)

> **Versão do documento:** GDD v0.7.0 · **Data:** 2026-11-04

---

## 10.1 Plano de QA e matriz de dispositivos/navegadores

| Ambiente | Prioridade | Cobertura |
|---|---|---|
| Chrome desktop atual | Must | Partida, lobby, rede, áudio, resolução. |
| Firefox desktop atual | Should | UI, input, rede, performance. |
| Edge desktop atual | Should | Fluxo completo e compatibilidade. |
| Safari desktop atual | Should | Áudio, WebSocket, escala e fontes. |
| Hardware desktop modesto | Must | FPS, tempo de carga, temperatura/memória. |
| Mobile browser | Fora do MVP | Só após aprovar touch/layout responsivo. |

---

## 10.2 Casos de teste críticos e critérios de aceite por mecânica

| ID | Caso | Critério |
|---|---|---|
| TST-001 | HP de torres | Defesa inicia em 25.000 e base em 45.000; dano negativo/duplicado é rejeitado. |
| TST-002 | Vitória normal | Base a 0 antes de 30:00 encerra uma vez e escolhe vencedor correto. |
| TST-003 | Morte súbita | Aos 30:00 sem vencedor, defesas são removidas e as duas bases ficam em 1 HP. |
| TST-004 | Ataque simultâneo | Ataques no mesmo tick seguem desempate documentado; proposta atual é empate. |
| TST-005 | Integridade de rede | Cliente adulterado não escolhe dano, HP, recurso ou resultado. |
| TST-006 | 3v3 | Seis clientes recebem time, relógio e eventos consistentes. |
| TST-007 | Desconexão | Jogador reconecta dentro da janela proposta sem duplicar unidade/sessão. |
| TST-008 | Save | Save inválido migra/recupera sem bloquear o menu. |
| TST-009 | Ataque e barra das torres | Cada torre ataca no máximo um alvo por vez; defesa mostra 5 segmentos de 5.000 HP, principal não segmenta. |
| TST-010 | Chefe neutro | Aviso aos 4:30 e surgimento uma vez no centro aos 5 min de teste; aproximação dispara ataque. |
| TST-011 | Bônus do chefe | A equipe que deu o golpe final recebe +15% velocidade e +5% dano por 90 s; buff sincronizado e sem acúmulo. |
| TST-012 | Seleção 3v3 | Seis jogadores escolhem um personagem cada; servidor associa picks às vagas e aplica a regra de duplicatas definida. |

---

## 10.3 Plano de playtest (perfil, roteiro, métricas, perguntas)

**Perfil:** fãs de estratégia, com mistura de iniciantes e pessoas experientes; **não selecionar por idade real** no protótipo.

**Roteiro**
1. Explicar objetivo sem ensinar toda a estratégia.
2. Tutorial.
3. Partida.
4. Entrevista curta.

**Métricas**
- Entendimento do objetivo.
- Tempo até a primeira ação útil.
- Duração da partida e taxa de abandono.
- Uso de unidades e desconexões.
- Resultado e diversão autoavaliada.

**Perguntas**
- "O que você achou que precisava fazer?"
- "Quando sua equipe ganhou/perdeu, entendeu por quê?"
- "O que gostaria de comandar ou melhorar?"

**Volume:** mínimo **cinco testadores por milestone**; para validar online 3v3, realizar sessão com **seis** quando possível.

---

## 10.4 KPIs e métricas de sucesso

Para portfólio, priorizar **qualidade e conclusão**, não monetização.

| Meta | Alvo inicial [PROPOSTA] |
|---|---|
| Testadores que identificam o objetivo sem ajuda | ≥80% |
| Conclusão do tutorial | ≥70% |
| Sessões de teste sem crash | ≥99% |
| Partidas de staging com estado consistente | ≥90% |
| FPS médio desktop | ≥55 |

D1/D7/D30 **não aplicáveis** a protótipo fechado sem consentimento/analytics apropriados.

---

## 10.5 Checklist de lançamento

- [ ] Revisar ClassInd/conteúdo e avisos de fotossensibilidade.
- [ ] Confirmar direitos/licenças de arte, fontes, áudio e dependências.
- [ ] Publicar política de privacidade/termos se houver coleta de dados ou beta público.
- [ ] Revisar LGPD, segurança e salvaguardas para menores antes de acesso público.
- [ ] Testar HTTPS/WSS, reconexão, limites de taxa, monitoramento e capacidade do servidor.
- [ ] Conferir fluxo de erro, manutenção, suporte e botão de sair.
- [ ] Validar metadados/OG, página de apresentação e créditos.
- [ ] Executar matriz de navegadores e testes de carga 3v3.

---

[← Anterior: Produção e Gestão](./09-producao-e-gestao.md) · [🏠 Índice](./README.md) · [Próximo: Requisitos Consolidados →](./11-requisitos-consolidados.md)
