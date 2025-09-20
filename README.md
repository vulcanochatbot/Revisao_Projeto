# 🔥 Vulcano ChatBot — Projeto Integrador (CEUB)

- Projeto acadêmico que investiga por que a contratação na construção civil emperra (informalidade, informação solta e baixo letramento digital) e organiza um plano de solução inclusivo, padronizado e mensurável. Foco em **diagnóstico e documentação**; sem implementação nesta fase.

---

## 🪙 Pitch de valor
- Reduzir atrito na ponta: **dados mínimos comparáveis**, inclusão de quem se comunica por **voz/foto**, **filtros justos** e **histórico** para recontratar bem. Resultado esperado: **menos atraso, menos retrabalho e decisões menos enviesadas**.

---

## 🧭 Sumário (atalhos rápidos)
1. [Biblioteca — evidências & diagnóstico](#sec-biblioteca)  
2. [Problema social — síntese](#sec-problema)  
3. [5W2H do problema](#sec-5w2h)  
4. [Personas & Jornada (AS-IS → TO-BE)](#sec-personas)  
5. [Diretrizes de solução](#sec-diretrizes)  
6. [KPIs & Métricas](#sec-kpis)  
7. [Riscos, mitigação & LGPD](#sec-riscos)  
8. [Escopo, MVP & Não-escopo](#sec-escopo)  
9. [Equipe & Papéis](#sec-equipe)

---

<a id="sec-biblioteca"></a>
## 1. Biblioteca — evidências & diagnóstico
- **Evidências do problema:** [evidencias_problema_sociedade.md](./evidencias_problema_sociedade.md)  
- **Diagnóstico (síntese):** [diagnostico_problema_sociedade.md](./diagnostico_problema_sociedade.md)

### Conteúdo: panorama de informalidade, canais fragmentados de contratação, barreiras de letramento digital e efeitos em prazo/custo/qualidade.

---

<a id="sec-problema"></a>
## 2. Problema social — síntese
- A contratação no setor é **dispersa e pouco rastreável**: informações chegam por indicações e mensagens avulsas; há **baixa padronização** (função, experiência, região, disponibilidade, diária) e **dificuldade de uso de formulários** por parte de quem acessa só o celular. Isso gera **demora, no-show, retrabalho** e pouca memória para recontratar quem performou bem.

---

<a id="sec-5w2h"></a>
## 3. 5W2H do problema
Documento completo: [05_5w2h_problema_social.md](./05_5w2h_problema_social.md)  

- Resumo: **o quê** (dificuldade estrutural de encontrar/triar/contratar), **por quê** (informalidade, dados soltos, letramento limitado), **onde** (obras privadas/públicas no Brasil), **quando** (mobilização, picos e trocas), **quem** (trabalhadores, RH/encarregado, empreiteiros), **como** (indicação e triagem manual) e **quanto** (indicadores de tempo, no-show, retrabalho etc.).

---

<a id="sec-personas"></a>
## 4. Personas & Jornada (AS-IS → TO-BE)
- **Arquivo:** [02_personas_jornada.md](./02_personas_jornada.md)

### Foco em três atores: **Trabalhador**, **Encarregado/RH** e **Pequeno empreiteiro**.  
Desejo comum: **cadastro simples**, **comparação justa** por proximidade/experiência e **confirmação clara** com **registro** para recontratação.

---

<a id="sec-diretrizes"></a>
## 5. Diretrizes de solução
- **Arquivo:** [04_diretrizes_solucao.md](./04_diretrizes_solucao.md)

### Eixos: **cadastro mínimo padronizado**, **fluxos que aceitam voz/foto**, **filtros e ranking transparentes**, **geolocalização/agenda**, **histórico e verificação progressiva**, **linguagem simples** e **LGPD**.

---

<a id="sec-kpis"></a>
## 6. KPIs & Métricas
Base de avaliação do impacto:
- **Tempo até preenchimento** (h/d)  
- **Taxa de no-show** (%)  
- **Retrabalho** (h refeitas / h totais)  
- **% perfis com dados mínimos completos**  
- **% recontratação**  
- **Satisfação pós-serviço** (0–10)

> Esses KPIs aparecem nos arquivos de diretrizes e 5W2H; serão a régua do futuro MVP.

---

<a id="sec-riscos"></a>
## 7. Riscos, mitigação & LGPD
###Riscos mapeados: **escopo inflado**, **prazos curtos**, **evidência fraca/viesada**, **baixa adesão a entrevistas**, **privacidade**.  
Mitigações: **MoSCoW + time-box**, **checkpoints**, **fontes diversas e premissas registradas**, **roteiro curto com consentimento**, **minimização de dados/anonimização/linguagem clara**.  
- Complementos: [PLANO_CURADORIA_LOTE1.md](./PLANO_CURADORIA_LOTE1.md) • [CONTRIBUTING.md](./CONTRIBUTING.md) • [LICENSE](./LICENSE) • [CITATION_GUIDE.md](./CITATION_GUIDE.md) • [CITATION.cff](./CITATION.cff)

---

<a id="sec-escopo"></a>
## 8. Escopo, MVP & Não-escopo
- **Visão geral:** [02_visao_geral_vulcano.md](./02_visao_geral_vulcano.md)  
- **Análise revisada:** [03_analise_revisada.md](./03_analise_revisada.md)

### **MVP (fase conceitual):** fluxo **documentado** de triagem padronizada, inclusão por voz/foto, filtros de comparação, confirmação e registro + KPIs de acompanhamento.  

### **Não-escopo:** implementação técnica, integrações reais e operação piloto nesta disciplina.

---

<a id="sec-equipe"></a>
## 9. Equipe & Papéis
| Papel | Responsável | Atribuições |
|------|-------------|-------------|
| Product Owner | **João César** | Visão e priorização; relacionamento externo; aceite do plano; agenda/stakeholders. |
| Tech Lead (conceitual) | **João Vítor** | Fluxos e arquitetura conceitual; padronização de artefatos; requisitos e critérios. |
| QA / Pesquisa | **Carlos Eduardo** | Personas/jornadas; métricas e KPIs; matriz de riscos; revisão de consistência. |

---

## 10. Requisitos

### Requisitos — Vulcano ChatBot

- Este arquivo lista requisitos derivados do **problema social** na contratação da construção civil (informalidade, assimetria de informação, exclusão digital, riscos EHS e desigualdade de acesso).

- **Requisitos Funcionais (RF)**: onboarding com consentimento LGPD; cadastro mínimo padronizado; entrada por voz/foto; publicar demanda padronizada; triagem cega; filtros por proximidade/experiência/NR; justificativa do ranking; convite/aceite com SLA; lembretes; pré-checagem de NR; avaliação mútua; histórico recontratável; verificação progressiva (selos); FAQ/busca; direitos do titular; reenvio automático; relatórios/KPIs.

- **Requisitos Não Funcionais (RNF)**: latência p95 ≤2s; busca/match p95 ≤5s; disponibilidade ≥99,0%; retomada ≤1min; fluxo em ≤5 passos e linguagem simples; acessibilidade prática (voz/foto, WCAG espírito); criptografia; minimização & logs auditáveis; exclusão ≤7 dias; auditoria de decisões; escalabilidade (MVP); compatibilidade móvel; MTTR ≤30min; portabilidade (CSV/JSON).

> Detalhamento e racional socio-técnico: **[Explicação](./EXPLICACAO.md)**


---

## Extras úteis
- Mensagem de commit sugerida:  
  `docs: README organizado (sumário, visão, 5W2H, personas, diretrizes, KPIs, riscos, escopo e equipe)`  

- Arquivos auxiliares:  
  [01_mapa_da_empatia.md](./01_mapa_da_empatia.md) • [PGP.md](./PGP.md) • [SUGGESTED_COMMIT_MESSAGE.txt](./SUGGESTED_COMMIT_MESSAGE.txt)
