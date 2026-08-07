# Roadmap - HomeLab Data & AI

Este documento descreve a evolução planejada da plataforma.

---

# Sprint 1 — Fundação da Plataforma ✅

## Infraestrutura

- [x] Ubuntu Server 24.04 LTS
- [x] Disco dedicado montado em `/dados`
- [x] Docker Engine
- [x] Docker Compose
- [x] Rede Docker `dados-net`
- [x] Tailscale
- [x] Portainer

## Dados

- [x] PostgreSQL 17
- [x] MinIO

## Organização

- [x] Estrutura de diretórios
- [x] Estrutura do projeto
- [x] Documentação inicial

---

# Sprint 2 — Plataforma de Engenharia de Dados

## JupyterLab

- [ ] Instalação
- [ ] Persistência
- [ ] Integração com PostgreSQL
- [ ] Integração com MinIO

## Redis

- [ ] Instalação
- [ ] Configuração

## MLflow

- [ ] Instalação
- [ ] Integração com PostgreSQL
- [ ] Integração com MinIO

---

# Sprint 3 — Orquestração

## Apache Airflow

- [ ] Instalação
- [ ] Scheduler
- [ ] Webserver
- [ ] Integração com PostgreSQL
- [ ] DAG de exemplo

---

# Sprint 4 — Inteligência Artificial

## Ollama

- [ ] Instalação
- [ ] Download de modelos

## Open WebUI

- [ ] Instalação
- [ ] Integração com Ollama

---

# Sprint 5 — Observabilidade

## Prometheus

- [ ] Instalação
- [ ] Métricas

## Grafana

- [ ] Dashboards
- [ ] Alertas

---

# Sprint 6 — Publicação

- [ ] Nginx Proxy Manager
- [ ] HTTPS
- [ ] DNS (opcional)

---

# Sprint 7 — Operação

- [ ] Backups automáticos
- [ ] Scripts administrativos
- [ ] Atualizações
- [ ] Testes de recuperação

---

# Sprint 8 — Versionamento

- [ ] Publicação no GitHub
- [ ] Documentação completa
- [ ] Release v1.0
