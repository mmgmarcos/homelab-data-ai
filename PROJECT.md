# HomeLab Data & AI
> Especificação oficial do projeto

---

# 1. Visão Geral

O **HomeLab Data & AI** é uma plataforma self-hosted desenvolvida para estudos, experimentação e desenvolvimento nas áreas de:

- Engenharia de Dados
- Ciência de Dados
- Inteligência Artificial
- Machine Learning
- MLOps
- Engenharia de Software
- DevOps
- Automação

O projeto tem como objetivo criar um ambiente completo, reproduzível e documentado utilizando tecnologias Open Source executadas em containers Docker.

---

# 2. Objetivos

## Objetivo Principal

Construir uma plataforma moderna para desenvolvimento e aprendizado em Engenharia de Dados e Inteligência Artificial.

## Objetivos Específicos

- Centralizar todos os serviços em Docker.
- Utilizar Docker Compose para gerenciamento.
- Padronizar toda a infraestrutura.
- Documentar todos os componentes.
- Automatizar backups.
- Facilitar futuras atualizações.
- Utilizar Git para versionamento.
- Criar uma plataforma facilmente reproduzível.

---

# 3. Escopo da Plataforma

A plataforma será composta pelos seguintes módulos.

## Infraestrutura

- Ubuntu Server 24.04 LTS
- Docker Engine
- Docker Compose
- Portainer
- Tailscale

## Banco de Dados

- PostgreSQL 17

## Data Lake

- MinIO

## Engenharia de Dados

- JupyterLab
- Redis
- Apache Airflow
- MLflow

## Inteligência Artificial

- Ollama
- Open WebUI

## Observabilidade

- Prometheus
- Grafana

## Publicação

- Nginx Proxy Manager

---

# 4. Arquitetura

```text
Internet
      │
Tailscale VPN
      │
Ubuntu Server 24.04
      │
Docker Engine
      │
Docker Compose
      │
dados-net
      │
├── PostgreSQL
├── MinIO
├── JupyterLab
├── Redis
├── Airflow
├── MLflow
├── Ollama
├── Open WebUI
├── Prometheus
└── Grafana
```

---

# 5. Estrutura de Diretórios

```text
/dados
├── compose
├── data
├── backups
├── configs
├── datasets
├── logs
├── projetos
├── scripts
└── docs
```

---

# 6. Princípios do Projeto

- Infraestrutura como código (IaC)
- Containers desacoplados
- Persistência de dados
- Documentação obrigatória
- Versionamento em Git
- Segurança por padrão
- Simplicidade na administração
- Fácil manutenção
- Reprodutibilidade

---

# 7. Convenções

Todos os serviços devem possuir:

- docker-compose.yml
- .env
- .env.example
- README.md

Todos os containers devem possuir:

- container_name
- hostname
- restart: unless-stopped
- healthcheck (quando suportado)
- logging
- labels

---

# 8. Estrutura dos Serviços

| Item | Local |
|------|-------|
| Compose | `/dados/compose/<serviço>` |
| Dados | `/dados/data/<serviço>` |
| Backup | `/dados/backups/<serviço>` |
| Configuração | `/dados/configs/<serviço>` |
| Logs | `/dados/logs/<serviço>` |

---

# 9. Rede

Rede Docker padrão:

```
dados-net
```

Todos os serviços deverão utilizar essa rede.

---

# 10. Tecnologias Utilizadas

- Ubuntu Server 24.04 LTS
- Docker Engine
- Docker Compose
- Portainer
- PostgreSQL
- MinIO
- JupyterLab
- Redis
- Apache Airflow
- MLflow
- Ollama
- Open WebUI
- Prometheus
- Grafana
- Nginx Proxy Manager
- Git

---

# 11. Roadmap

## Sprint 1 — Fundação

- [x] Ubuntu
- [x] Docker
- [x] Portainer
- [x] PostgreSQL
- [x] MinIO
- [x] Estrutura do projeto

## Sprint 2 — Plataforma de Dados

- [ ] JupyterLab
- [ ] Redis
- [ ] MLflow

## Sprint 3 — Orquestração

- [ ] Apache Airflow

## Sprint 4 — Inteligência Artificial

- [ ] Ollama
- [ ] Open WebUI

## Sprint 5 — Observabilidade

- [ ] Prometheus
- [ ] Grafana

## Sprint 6 — Publicação

- [ ] Nginx Proxy Manager
- [ ] Backup Automatizado
- [ ] CI/CD

---

# 12. Documentação

Este documento apresenta a visão geral do projeto.

Os detalhes encontram-se em:

- `README.md`
- `ROADMAP.md`
- `docs/arquitetura.md`
- `docs/padroes.md`
- `docs/rede.md`
- `docs/backup.md`
- `docs/monitoramento.md`

---

# 13. Status Atual

**Versão:** 0.1.0

**Estado:** Em desenvolvimento

**Última atualização:** Agosto/2026

# 14. Arquitetura Física

Hardware

- Ubuntu Server 24.04 LTS
- Disco do sistema
- Disco dedicado para dados (/dados)

Rede

- Rede Docker: dados-net
- Acesso remoto: Tailscale

Persistência

- Bind mounts em /dados/data
- Backups em /dados/backups
