# Requisitos — Vulcano Chatbot (fase acadêmica)

> Derivados diretamente do **problema social**: informalidade, assimetria de informação, exclusão digital/baixo letramento, viés/discriminação, riscos EHS (NRs) e conectividade instável.

## Sumário
- [Requisitos Funcionais (RF)](#requisitos-funcionais-rf)
- [Requisitos Não Funcionais (RNF)](#requisitos-não-funcionais-rnf)
- [Outros artefatos](#outros-artefatos)

## Requisitos Funcionais (RF)

### **RF-001 — Onboarding com consentimento LGPD (Must)**  

- Problema social: informalidade/desconfiança no uso de dados.  

-Gherkin: Given novo usuário, When iniciar cadastro, Then exibir termo e gravar aceite (data/hora/canal).  

- Meta: 100% perfis com consentimento.

### **RF-002 — Cadastro mínimo padronizado (Must)**  

- Problema social: assimetria/invisibilidade de bons profissionais.  

- Gherkin: Given cadastro, When concluir ≤5 passos, Then status “mínimo completo”.  

- Campos: função, experiência, região, disponibilidade, diária, contato.  

- Meta: ≥70% perfis completos (90 dias).

### **RF-003 — Entrada por voz/foto (Should)**  

- Problema social: exclusão digital/baixo letramento.  

- Gherkin: Given etapa experiência, When anexar voz/foto, Then anexos vinculados ao perfil.  

- Meta: ≥60% perfis com anexos.

### **RF-004 — Publicar demanda padronizada (Must)**  

- Problema social: prazo estourado por pedidos vagos.  

- Gherkin: Given RH cria demanda, When salvar, Then status “aberta” com campos mínimos.  

- Campos: local, data/horário, duração, remuneração, pré-requisitos (NRs).  

- Meta: 100% demandas válidas.

### **RF-005 — Rascunho e retomada de sessão (Should)**  

- Problema social: conectividade intermitente.  

- Gherkin: Given queda, When reconectar, Then retomar do último passo.  

- Meta: retomada ≤1 min.

### **RF-006 — Triagem cega (Must)**  

- Problema social: viés/discriminação por indicação.  

- Gherkin: Given lista, When visualizar, Then ocultar nome/foto/idade na fase inicial.  

- Meta: gap de convites ≤5 p.p. entre grupos comparáveis.

### **RF-007 — Filtro por proximidade/experiência/NR (Must)**  

- Problema social: desencontro de perfis e logística cara.  

- Gherkin: Given raio X km + NR, When filtrar, Then lista aderente (p95 ≤5s).  

- Meta: p95 da busca ≤5s.

### **RF-008 — Justificativa do ranking (Should)**  

- Problema social: opacidade/vieses não percebidos.  

- Gherkin: Given ranking, When abrir detalhes, Then exibir critérios usados.  

- Meta: 100% resultados com explicação.

### **RF-009 — Convite/aceite com SLA (Must)**  

- Problema social: vagas travadas/tempo perdido.  

- Gherkin: Given convite enviado, When expirar, Then reabrir vaga automaticamente.  

- Meta: ≤24h do convite ao aceite.

### **RF-010 — Lembretes automáticos (Should)**  

- Problema social: no-show por falhas de comunicação.  

- Gherkin: Given serviço confirmado, When T–24h/T–2h, Then enviar lembrete.  

- Meta: ≥90% lembretes enviados.

### **RF-011 — Pré-checagem de NRs (Must)**  

- Problema social: risco EHS (acidentes).  

- Gherkin: Given NR exigida, When candidato sem NR válida, Then impedir convite.  

- Meta: ≥90% matches com NR válida.

### **RF-012 — Avaliação mútua (Must)**  

- Problema social: reputação informal/memória fraca.  

- Gherkin: Given serviço finalizado, When 24h, Then solicitar avaliação a ambos.  

- Meta: ≥70% serviços avaliados.

### **RF-013 — Histórico recontratável (Must)**  

- Problema social: perda de aprendizado.  

- Gherkin: Given serviço avaliado, When fechar ciclo, Then registrar histórico recontratável.  

- Meta: recontratação ≥25% (90 dias).

### **RF-014 — Verificação progressiva (selos) (Should)**  

- Problema social: fraude documental/barreiras de entrada.  

- Gherkin: Given perfil novo, When concluir etapa (telefone→referências→certificações), Then atribuir selo.  

- Meta: ≥60% perfis com 2+ etapas.

### **RF-015 — FAQ/Busca de políticas (Could)**  

- Problema social: informação normativa dispersa (NRs/regras).

- Gherkin: Given busca “NR-35”, When consultar, Then retornar resumo confiável.  

- Meta: 95% acerto no top-3.

### **RF-016 — Direitos do titular (Must)**  

- Problema social: assimetria de poder no uso de dados.  

- Gherkin: Given solicitação, When abrir ticket, Then concluir ≤7 dias.  

- Meta: SLA ≤7 dias.

### **RF-017 — Reenvio automático (Should)**  

- Problema social: perdas por rede instável.  

- Gherkin: Given falha de envio, When reconectar, Then reenviar automaticamente.  

- Meta: sucesso ≥99%.

### **RF-018 — Relatórios e KPIs (Must)**  

- Problema social: falta de evidência para corrigir práticas.  

- Gherkin: Given período, When consolidar, Then exibir KPIs agregados/anonimizados.  

- Meta: atualização diária (tempo/no-show/recontratação/paridade/EHS).

## Requisitos Não Funcionais (RNF)

- **RNF-001 — Latência conversacional (Must):** p95 ≤2s em 300 conversas; protege RF-002/004/007/009.  
- **RNF-002 — Busca/Match (Must):** p95 ≤5s até ~5k perfis; protege RF-007/008.  
- **RNF-003 — Disponibilidade (Should):** uptime mensal ≥99,0%; previsibilidade para rotina de obra.  
- **RNF-004 — Retomada (Should):** retomada de sessão ≤1 min; protege RF-005/017.  
- **RNF-005 — Fluxos curtos (Must):** cadastro mínimo em ≤5 passos; linguagem A2–B1; protege RF-002.  
- **RNF-006 — Acessibilidade (Should):** aceitar voz/foto; leitura fácil; espírito WCAG 2.2 AA; protege RF-003.  
- **RNF-007 — Criptografia (Must):** tráfego + dados sensíveis cifrados; protege RF-001/016.  
- **RNF-008 — Minimização & logs (Must):** só o necessário; logs auditáveis; protege RF-001/016/018.  
- **RNF-009 — Exclusão de dados (Must):** pedidos concluídos ≤7 dias; protege RF-016.  
- **RNF-010 — Auditoria do matching (Must):** 100% decisões com trilhas de critérios; protege RF-007/008/018.  
- **RNF-011 — Escalabilidade (Should):** ≥500 conversas simultâneas (MVP).  
- **RNF-012 — Compatibilidade móvel (Should):** sucesso ≥95% em smartphones populares.  
- **RNF-013 — MTTR (Should):** restaurar serviço ≤30 min.  
- **RNF-014 — Portabilidade (Could):** exportar CSV/JSON anonimizado de entidades-chave.

## Outros artefatos
- Diretrizes, KPIs e salvaguardas: [../04_diretrizes_solucao.md](../04_diretrizes_solucao.md)  
- 5W2H: [../05_5w2h_problema_social.md](../05_5w2h_problema_social.md)
