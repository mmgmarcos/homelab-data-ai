# Padrões do Projeto

Este documento define os padrões obrigatórios para todos os serviços do HomeLab Data & AI.

---

# 1. Estrutura de Diretórios

Todos os serviços devem seguir a estrutura abaixo.

| Tipo | Caminho |
|------|----------|
| Docker Compose | `/dados/compose/<serviço>` |
| Dados | `/dados/data/<serviço>` |
| Configuração | `/dados/configs/<serviço>` |
| Backups | `/dados/backups/<serviço>` |
| Logs | `/dados/logs/<serviço>` |

---

# 2. Docker Compose

Todo serviço deve possuir:

- `docker-compose.yml`
- `.env`
- `.env.example`
- `README.md`

---

# 3. Containers

Todos os containers devem possuir:

- `container_name`
- `hostname`
- `restart: unless-stopped`
- `env_file`
- `healthcheck` (quando suportado)
- `logging`
- `labels`

---

# 4. Rede

Todos os containers devem utilizar a rede Docker:

```text
dados-net
```

Não criar redes adicionais sem necessidade.

---

# 5. Persistência

Sempre utilizar **bind mounts**.

Exemplo:

```yaml
volumes:
  - /dados/data/postgres:/var/lib/postgresql/data
```

Volumes nomeados somente quando houver justificativa técnica.

---

# 6. Variáveis de Ambiente

Nunca publicar arquivos `.env`.

Sempre fornecer um arquivo `.env.example` com valores fictícios.

Exemplo:

```env
POSTGRES_USER=admin
POSTGRES_PASSWORD=CHANGE_ME
POSTGRES_DB=dados
```

---

# 7. Documentação

Cada serviço deverá conter um `README.md` com, no mínimo:

- Objetivo
- Função na arquitetura
- Portas
- Volumes
- Variáveis de ambiente
- Dependências
- Como iniciar
- Como parar
- Como atualizar
- Backup
- Restore
- Troubleshooting

---

# 8. Logs

Todos os serviços deverão limitar o crescimento dos logs.

Padrão:

```yaml
logging:
  driver: json-file
  options:
    max-size: "10m"
    max-file: "5"
```

---

# 9. Healthcheck

Sempre que a imagem oferecer suporte, configurar um `healthcheck`.

---

# 10. Versionamento

Antes de instalar um novo serviço:

1. Atualizar a documentação.
2. Validar o `docker-compose.yml` com:

```bash
docker compose config
```

3. Implantar:

```bash
docker compose up -d
```

4. Validar:

```bash
docker ps
```

5. Registrar a mudança no Git.

---

# 11. Convenções de Nome

## Containers

- postgres17
- minio
- jupyter
- redis
- airflow
- mlflow
- ollama
- open-webui
- grafana
- prometheus

## Rede

- dados-net

---

# 12. Timezone

Todos os serviços deverão utilizar:

```text
America/Sao_Paulo
```

---

# 13. Objetivo

Todos os padrões definidos neste documento são obrigatórios para manter a plataforma organizada, reproduzível e fácil de manter.
