# Análise Revisada do Projeto (What/Why/Where/When/Who/How)

**Etapa:** Descoberta e Enquadramento

## 1) What (o que será feito)
Vulcano Chatbot para **auxílio à contratação** de mão de obra na construção civil, com:
- Centralização via **WhatsApp** (canal único e familiar).
- Cadastro/triagem, propostas, confirmação de disponibilidade e repasse de informações.
- Redução de falhas de comunicação e **agilidade** no fechamento.

## 2) Why (por que)
- Simplificar a comunicação entre empresas e público com **letramento digital variado**.
- **Inclusão digital**: WhatsApp é ubiquidade no público-alvo.
- **Aderência multimodal**: texto e áudio.
- *Dados citados pelo time*: adoção massiva de WhatsApp (IBGE/PNAD), e contratação informal iniciada via WhatsApp (FGV). **→ TODO:** consolidar/checar fontes e inserir referências formais.

## 3) Where (onde)
- Dev local + **deploy em nuvem** (AWS/DigitalOcean).
- **Python**, **FastAPI**, **PostgreSQL**, **WhatsApp Business API**.
- Gestão no **Notion** + **Scrum**.

## 4) When (quando)
- Sprints semanais e entregas incrementais.
- **Prazo inicial:** 2025‑07‑30
- **Prazo final:** 2025‑11‑26
- **Meta:** MVP funcional para apresentação no prazo do Projeto Integrador.

## 5) Who (quem)
| Membro      | Foco principal                              | Tecnologias/Funções                    |
|-------------|----------------------------------------------|----------------------------------------|
| João César  | Núcleo do bot (respostas + lógica)           | Python; Banco (migrations)             |
| Cadu        | Backend/APIs                                 | FastAPI                                |
| João Vitor  | DevOps/Integração/Testes/Docs                | Pipelines; testes; documentação        |

## 6) How (como)
- **Stack:** Python + FastAPI + PostgreSQL + WhatsApp Business API.
- **Processo:** Scrum + Notion.
- **Infra:** Deploy em nuvem com **backups automáticos**.
