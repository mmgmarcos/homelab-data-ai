# 🚀 HomeLab Data & AI

> Plataforma Self-Hosted para Engenharia de Dados, Ciência de Dados, Inteligência Artificial e MLOps.

---

## 📖 Sobre o Projeto

O **HomeLab Data & AI** é um laboratório pessoal desenvolvido para estudo, experimentação e desenvolvimento utilizando tecnologias Open Source.

O objetivo é construir uma plataforma completa para:

- Engenharia de Dados
- Ciência de Dados
- Inteligência Artificial
- Machine Learning
- MLOps
- DevOps

Toda a infraestrutura é executada em containers Docker e documentada desde a instalação até a operação.

---

# 🏗 Arquitetura

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
├── MLflow
├── Apache Airflow
├── Ollama
├── Open WebUI
├── Prometheus
└── Grafana
```

---

# 📦 Tecnologias

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
- Apache Airflow
- Redis
- MLflow

## Inteligência Artificial

- Ollama
- Open WebUI

## Observabilidade

- Prometheus
- Grafana

---

# 📂 Estrutura

```text
/dados

compose/
data/
backups/
configs/
datasets/
logs/
scripts/
projetos/
```

---

# 📚 Documentação

| Documento | Descrição |
|-----------|-----------|
| PROJECT.md | Especificação técnica da plataforma |
| ROADMAP.md | Planejamento do projeto |
| docs/arquitetura.md | Arquitetura |
| docs/padroes.md | Padrões utilizados |
| docs/rede.md | Rede |
| docs/backup.md | Estratégia de backup |
| docs/monitoramento.md | Observabilidade |
| docs/hardware.md | Hardware e limitações conhecidas |

---

# 🚧 Roadmap

- ✅ Infraestrutura
- ✅ Docker
- ✅ Portainer
- ✅ PostgreSQL
- ✅ MinIO
- 🔄 JupyterLab
- ⏳ MLflow
- ⏳ Airflow
- ⏳ Ollama
- ⏳ Open WebUI
- ⏳ Prometheus
- ⏳ Grafana

---

# 🎯 Objetivos

- Plataforma reproduzível
- Infraestrutura documentada
- Ambientes desacoplados
- Persistência de dados
- Versionamento em Git
- Automação
- Boas práticas de DevOps

---

# 📄 Licença

Projeto desenvolvido para fins educacionais.
