# Requisitos Funcionais (RF)

---

- ### RF-001 — Onboarding com consentimento LGPD (MUST)
Problema social: informalidade e desconfiança no uso de dados.
No Vulcano: começo claro e respeitoso, registrando base legal antes de coletar qualquer dado.
Gherkin: Given novo usuário When iniciar cadastro Then exibir termo e gravar aceite (data/hora/canal).
Meta: 100% perfis com consentimento registrado.

- ### RF-002 — Cadastro mínimo padronizado (MUST)
Problema social: assimetria de informação e invisibilidade de bons profissionais.
No Vulcano: coleta curta de função, experiência, região, disponibilidade e diária para tornar perfis comparáveis.
Gherkin: Given fluxo de cadastro When concluir até 5 passos Then status “mínimo completo”.
Meta: ≥70% perfis completos em 90 dias.

- ### RF-003 — Entrada por voz/foto (SHOULD)
Problema social: exclusão digital e baixa letratividade.
No Vulcano: aceitar áudio e imagem como “prova de trabalho” (antes/depois).
Gherkin: Given etapa de experiência When anexar voz/foto Then anexos vinculados ao perfil.
Meta: ≥60% perfis com anexos.

- ### RF-004 — Publicar demanda padronizada (MUST)
Problema social: prazos estourados por pedidos vagos e dispersos.
No Vulcano: demanda com local, data/horário, duração, remuneração e pré-requisitos (NRs).
Gherkin: Given RH cria demanda When salvar Then status “aberta” com campos mínimos.
Meta: 100% demandas válidas com dados mínimos.

- ### RF-005 — Rascunho e retomada de sessão (SHOULD)
Problema social: conectividade intermitente em obra.
No Vulcano: continuar de onde parou sem perder dados.
Gherkin: Given queda de conexão When reconectar Then retomar passo anterior.
Meta: retomada ≤1 min.

- ### RF-006 — Triagem cega (MUST)
Problema social: viés/indicação que exclui gênero, raça e periferias.
No Vulcano: esconder atributos sensíveis na fase inicial de seleção.
Gherkin: Given lista de candidatos When visualizar Then ocultar nome/foto/idade.
Meta: gap de convites ≤5 p.p. entre grupos comparáveis.

- ### RF-007 — Filtro por proximidade/experiência/NR (MUST)
Problema social: desencontro de perfis e custos de deslocamento.
No Vulcano: filtrar por raio (km), anos de experiência e certificações exigidas.
Gherkin: Given raio 10 km + NR When filtrar Then retornar lista aderente (p95 ≤5s).
Meta: p95 da busca ≤5s (ver RNF-002).

- ### RF-008 — Justificativa do ranking (SHOULD)
Problema social: opacidade que alimenta desconfiança e vieses.
No Vulcano: explicar, em linguagem simples, por que cada perfil apareceu.
Gherkin: Given ranking When abrir detalhes Then exibir critérios usados.
Meta: 100% resultados com explicação.

- ### RF-009 — Convite/aceite com SLA (MUST)
Problema social: tempo perdido e vagas travadas.
No Vulcano: convites com prazo para resposta e reabertura automática.
Gherkin: Given convite enviado When expirar Then reabrir vaga automaticamente.
Meta: ≤24h do convite ao aceite.

- ### RF-010 — Lembretes automáticos (SHOULD)
Problema social: no-show por comunicação precária.
No Vulcano: lembretes T–24h e T–2h.
Gherkin: Given serviço confirmado When atingir T–24h/T–2h Then enviar lembrete.
Meta: ≥90% lembretes enviados.

- ### RF-011 — Pré-checagem de certificações (MUST)
Problema social: acidentes por falta de NR válida.
No Vulcano: bloquear match quando a NR exigida estiver ausente/vencida.
Gherkin: Given NR-35 exigida When candidato sem NR válida Then impedir convite.
Meta: ≥90% matches com NR válida.

- ### RF-012 — Avaliação mútua (MUST)
Problema social: memória fraca e reputação informal.
No Vulcano: nota 1–5 + comentário/áudio para ambos os lados.
Gherkin: Given serviço finalizado When 24h Then solicitar avaliação a contratante e contratado.
Meta: ≥70% serviços avaliados.

- ### RF-013 — Histórico recontratável (MUST)
Problema social: perda de aprendizado coletivo.
No Vulcano: preservar vínculos bem-sucedidos para repetir combinações.
Gherkin: Given serviço avaliado When fechar ciclo Then registrar no histórico.
Meta: recontratação ≥25% em 90 dias.

- ### RF-014 — Verificação progressiva com selos (SHOULD)
Problema social: fraude documental e barreiras de entrada.
No Vulcano: etapas leves (telefone→referências→certificações) com selos visíveis.
Gherkin: Given perfil novo When concluir etapa Then atribuir selo correspondente.
Meta: ≥60% perfis com 2+ etapas concluídas.

- ### RF-015 — FAQ/Busca de políticas (COULD)
Problema social: informação normativa dispersa (NRs, combinações, regras).
No Vulcano: respostas curtas e validadas sobre exigências e boas práticas.
Gherkin: Given busca “NR-35” When consultar Then retornar resumo confiável.
Meta: 95% acerto no top-3.

- ### RF-016 — Direitos do titular (MUST)
Problema social: assimetria de poder no tratamento de dados.
No Vulcano: acesso, retificação, portabilidade e exclusão simples.
Gherkin: Given solicitação When abrir ticket Then concluir em ≤7 dias.
Meta: SLA ≤7 dias para 100% dos pedidos.

- ### RF-017 — Reenvio automático (SHOULD)
Problema social: perdas por rede instável.
No Vulcano: reenfileirar e reenviar ao reconectar.
Gherkin: Given falha de envio When reconectar Then reenviar automaticamente.
Meta: sucesso ≥99%.

- ### RF-018 — Relatórios e KPIs (MUST)
Problema social: falta de evidência para corrigir práticas.
No Vulcano: dashboard de tempo, no-show, recontratação e paridade.
Gherkin: Given período When consolidar Then exibir KPIs agregados/anonimizados.
Meta: atualização diária com séries por obra/região.

---

# Requisitos Não Funcionais (RNF) — explicitando a solução protegida

- ### RNF-001 — Latência conversacional (MUST)
Solução: agilidade reduz transtornos de quem depende do celular no dia a dia.
Critério: p95 de resposta ≤2s em 300 conversas simultâneas.

- ### RNF-002 — Busca/Match rápido (MUST)
Solução: menos espera para quem precisa trabalhar e para quem precisa contratar.
Critério: p95 ≤5s até ~5k perfis.

- ### RNF-003 — Disponibilidade de serviço (SHOULD)
Solução: previsibilidade em rotina de obra.
Critério: uptime mensal ≥99,0%.

- ### RNF-004 — Retomada de sessão (SHOULD)
Solução: não punir quem tem conexão fraca.
Critério: retomar em ≤1 min após reconexão.

- ### RNF-005 — Fluxos curtos e linguagem simples (MUST)
Solução: inclusão de baixa letratividade.
Critério: cadastro mínimo em ≤5 passos; texto nível A2–B1.

- ### RNF-006 — Acessibilidade prática (SHOULD)
Solução: não excluir por barreiras de leitura; permitir voz/foto.
Critério: alternativas por voz/foto; aderência ao espírito WCAG 2.2 AA.

- ### RNF-007 — Criptografia em trânsito/repouso (MUST)
Solução: confiança no manuseio de dados sensíveis.
Critério: 100% do tráfego cifrado; dados sensíveis cifrados.

- ### RNF-008 — Minimização & logs (MUST)
Solução: reduzir coleta excessiva e viabilizar auditoria.
Critério: só campos necessários; logs auditáveis de consentimento e matching.

- ### RNF-009 — Exclusão de dados (MUST)
Solução: controle do titular sobre seus dados.
Critério: pedidos concluídos em ≤7 dias.

- ### RNF-010 — Observabilidade & auditoria de decisões (MUST)
Solução: explicabilidade e justiça no acesso a oportunidades.
Critério: 100% das decisões de ranking com trilha de critérios (SLI/SLO definidos).

- ### RNF-011 — Escalabilidade inicial (SHOULD)
Solução: não colapsar quando a demanda cresce.
Critério: ≥500 conversas simultâneas no MVP.

- ### RNF-012 — Compatibilidade móvel (SHOULD)
Solução: funcionar nos aparelhos populares da base.
Critério: sucesso ≥95% na base-alvo.

- ### RNF-013 — MTTR (SHOULD)
Solução: serviço volta rápido, evitando prejuízo para quem vive de diária.
Critério: restaurar em ≤30 min.

- ### RNF-014 — Portabilidade de dados (COULD)
Solução: evitar lock-in e permitir transparência.
Critério: exportar CSV/JSON anonimizado de entidades-chave.
