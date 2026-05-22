# Restaurante

Este repositório já vem com um **MySQL** pronto (via Docker) e o dump do banco (`database/bd.sql`).

## Subir o banco (Docker)

```bash
docker compose up -d
```

Isso cria:
- MySQL: porta **3306**
- Adminer (interface do banco): porta **8081**

## Acessar o Adminer

Abra no navegador:
- `http://localhost:8081`

Preencha:
- System: **MySQL**
- Server: **db**
- Username: **root**
- Password: **root**
- Database: **restaurante**

## Observações

- O dump é importado automaticamente **na primeira vez** que o container do MySQL inicializa.
- Se você já subiu o container antes e quer reimportar do zero, apague o volume:

```bash
docker compose down -v
docker compose up -d
```
