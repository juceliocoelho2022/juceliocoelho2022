# Portfolio Engineering Roadmap

Este roadmap organiza a evolução do portfólio com foco em **autonomia, decisão técnica, qualidade, operação e diagnóstico** — competências esperadas de um Java Backend Pleno.

## Prioridade P0 — Evidência forte de Backend Pleno

### 1. NexaPay — Production Hardening
Issue: https://github.com/juceliocoelho2022/nexapay-event-driven-payments/issues/14

Objetivos:
- definir SLIs/SLOs;
- executar failure drills;
- validar replay seguro;
- documentar runbook de incidentes;
- registrar evidências em métricas, logs e traces.

**Por que primeiro:** já é o projeto mais completo e pode virar a principal demonstração de backend distribuído, resiliência e operação.

---

### 2. SentinelFraud — Operational Readiness
Issue: https://github.com/juceliocoelho2022/sentinelfraud-platform/issues/1

Objetivos:
- testar Redis indisponível;
- testar backlog da Outbox;
- testar crescimento de DLT;
- validar timeout/retry/circuit breaker;
- documentar rollback do challenger.

**Evidência esperada:** capacidade de diagnosticar e recuperar um sistema crítico.

---

### 3. InnovationHub — Quality Hardening
Issue: https://github.com/juceliocoelho2022/innovationhub/issues/2

Objetivos:
- testes de integração com SQL Server;
- teste de optimistic locking;
- migrations Flyway no pipeline;
- métricas via Micrometer;
- dashboard básico de latência, erros e throughput.

**Evidência esperada:** backend corporativo consistente sem complexidade arquitetural prematura.

---

## Prioridade P1 — Sistemas Distribuídos

### 4. OrderFlow — Reliability Hardening
Issue: https://github.com/juceliocoelho2022/orderflow-saga-orchestration/issues/1

Objetivos:
- consumidores idempotentes;
- retry/DLT;
- avaliar Transactional Outbox;
- correlation id;
- métricas de Saga;
- testes de compensação.

**Evidência esperada:** entendimento de consistência eventual e falhas distribuídas.

---

### 5. ObserveFlow — Observability Lab
Issue: https://github.com/juceliocoelho2022/observeflow/issues/1

Objetivos:
- fluxo real entre serviços;
- trace distribuído;
- dashboard RED;
- logs correlacionados;
- SLI/SLO;
- incidente simulado.

**Evidência esperada:** troubleshooting baseado em sinais operacionais.

---

## Prioridade P2 — Cloud

### 6. SisAWS — Cloud Readiness
Issue: https://github.com/juceliocoelho2022/SisAWS/issues/1

Objetivos:
- validar Terraform;
- revisar IAM e Security Groups;
- PostgreSQL em cenário real;
- budget/alerta de custo;
- documentar recursos efetivamente implantados.

**Evidência esperada:** cloud com segurança, custo e validação, não apenas infraestrutura declarada.

---

## Regra para novas tecnologias

Antes de adicionar qualquer tecnologia ao portfólio, responder:

1. Qual problema ela resolve?
2. Qual alternativa mais simples foi considerada?
3. Qual trade-off estou aceitando?
4. Como vou testar?
5. Como vou observar em produção?
6. Como vou diagnosticar uma falha?
7. Qual evidência objetiva mostrará que a solução funciona?

Se essas perguntas não tiverem resposta clara, a tecnologia provavelmente ainda não é necessária.

---

## Definition of Done para projetos de portfólio

Um projeto deixa de ser apenas "funcional" e passa a ser uma evidência forte de engenharia quando possui:

- problema de negócio claramente definido;
- arquitetura explicada;
- decisões e trade-offs documentados;
- testes automatizados;
- CI;
- banco versionado;
- tratamento de erros;
- segurança adequada ao contexto;
- observabilidade;
- cenário de falha documentado;
- procedimento de diagnóstico;
- README executável;
- distinção entre implementado, em andamento e planejado.

---

## Ordem recomendada para entrevistas

1. **NexaPay** — sistemas distribuídos e pagamentos.
2. **SentinelFraud** — resiliência, fraude e operação.
3. **InnovationHub** — arquitetura corporativa e decisão de simplicidade.
4. **OrderFlow** — Saga e consistência eventual.
5. **ObserveFlow** — observabilidade.
6. **SisAWS** — cloud e IaC.

O objetivo não é apresentar todos em uma entrevista. Escolha o projeto cuja decisão técnica melhor responde ao problema ou requisito da vaga.
