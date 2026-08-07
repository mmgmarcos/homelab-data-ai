# Nome do Serviço

## Objetivo

Descreva o objetivo do serviço.

---

## Imagem Docker

```
imagem:tag
```

---

## Portas

| Porta | Descrição |
|--------|-----------|
| | |

---

## Persistência

```
/dados/data/<serviço>
```

---

## Rede

```
dados-net
```

---

## Variáveis

Arquivo:

```
.env
```

---

## Dependências

- Docker
- Docker Compose

---

## Comandos

### Iniciar

```bash
docker compose up -d
```

### Parar

```bash
docker compose down
```

### Logs

```bash
docker logs <container>
```

### Atualizar

```bash
docker compose pull
docker compose up -d
```

---

## Backup

Descrever.

---

## Restore

Descrever.

---

## Troubleshooting

Descrever.
