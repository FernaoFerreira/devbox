# 🐳 docker-fullstack-template

Template de ambiente de desenvolvimento full-stack containerizado com Docker Compose.

## Stack

| Serviço | Tecnologia | Porta |
|---------|-----------|-------|
| Frontend | React + Vite | via Nginx |
| Backend | NestJS | via Nginx |
| Banco de dados | PostgreSQL | interno |
| Admin BD | pgAdmin | 5050 |
| Proxy reverso | Nginx | 80 |

## Como usar

**1. Clone e configure**
```bash
git clone https://github.com/seu-usuario/docker-fullstack-template
cd docker-fullstack-template
cp .env.example .env
```

**2. Adicione seu código**
- Frontend React/Vite → `frontend/`
- Backend NestJS → `backend/`

**3. Suba o ambiente**
```bash
docker-compose up --build
```

Acesse em `http://localhost`.

## Roteamento

| URL | Destino |
|-----|---------|
| `localhost/` | Frontend |
| `localhost/api/` | Backend (prefixo `/api` removido) |
| `localhost:5050` | pgAdmin |

## Comandos úteis

```bash
docker-compose up -d          # subir em background
docker-compose down           # parar (dados preservados)
docker-compose logs -f        # acompanhar logs
docker-compose exec backend sh  # acessar shell do container
```

> **Hot-reload** ativo por padrão — alterações no código refletem sem rebuild.