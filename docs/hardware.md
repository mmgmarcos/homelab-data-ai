# Hardware do HomeLab

Este documento descreve a configuração física do servidor e as limitações conhecidas que impactam alguns componentes da plataforma.

---

# Servidor

## Processador

Intel Pentium G2030

- Arquitetura: x86_64
- Núcleos: 2
- Threads: 2
- Frequência: 3.00 GHz

---

## Sistema Operacional

Ubuntu Server 24.04 LTS

---

## Virtualização

- Docker Engine
- Docker Compose

---

# Limitações de Hardware

O processador Intel Pentium G2030 não possui suporte às seguintes instruções:

- AVX
- AVX2
- FMA

Essas instruções são exigidas por diversas bibliotecas modernas de Machine Learning e IA.

---

# Impacto

## Funciona normalmente

- Docker
- Portainer
- PostgreSQL
- MinIO
- JupyterLab
- Redis
- Apache Airflow
- MLflow
- Grafana
- Prometheus
- DuckDB
- Pandas
- NumPy
- SQLAlchemy
- PyArrow
- boto3
- pyspark (uso leve)

---

## Requer versão compatível

- Polars (`polars[rtcompat]`)

---

## Não compatível nesta CPU

As versões atuais das bibliotecas abaixo exigem AVX e encerram a execução com:

```
Illegal instruction (core dumped)
```

Bibliotecas afetadas:

- TensorFlow
- Algumas versões do PyTorch
- Outras bibliotecas compiladas com suporte obrigatório a AVX

---

# Estratégia adotada

Este HomeLab será utilizado principalmente para:

- Engenharia de Dados
- ETL
- Data Lake
- MLOps
- Orquestração
- Banco de Dados
- Observabilidade

Treinamentos intensivos de Deep Learning poderão ser executados futuramente em hardware com suporte a AVX/AVX2 ou em serviços de nuvem.

---

# Próximo Upgrade

Quando houver atualização de hardware, recomenda-se um processador com:

- AVX
- AVX2
- FMA
- 4 ou mais núcleos
- 16 GB ou mais de memória RAM

Isso permitirá executar integralmente frameworks modernos de Inteligência Artificial e Machine Learning.

---

# Última atualização

Agosto de 2026
