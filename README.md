# ✂️ shorten-me.com — Encurtador de URLs com plano premium

Um encurtador de URLs moderno e escalável, com autenticação, rate limiting para usuários comuns e recursos avançados para usuários premium, como URLs ilimitadas e personalizadas.

> 🔗 Hospedado em: [https://shorten-me.com](https://shorten-me.com)

## 🚀 Funcionalidades

- 🔗 Encurtamento de URLs com redirecionamento instantâneo
- 🔒 Autenticação via OAuth (Google/GitHub)
- 🧾 Histórico de URLs por usuário
- ⚠️ Rate limit para usuários gratuitos (ex: 5 URLs por dia)
- 💳 Plano premium via Stripe:
  - URLs ilimitadas
  - Slugs personalizados (`shorten-me.com/meu-link`)
  - Expiração configurável
  - Analytics de acessos
- 📱 Totalmente responsivo

## 🧱 Arquitetura

**Framework:** Next.js 15 (App Router)  
**Banco de dados:** PostgreSQL (via Prisma ORM)  
**Estilização:** Tailwind CSS  
**Validação:** Zod  
**Pagamentos:** Stripe Checkout  
**Autenticação:** NextAuth.js  
**Rate Limiting:** por IP/usuário (com suporte a Redis)

## 🧪 Tecnologias

- Next.js
- TypeScript
- Tailwind
- Prisma
- Stripe SDK
- PostgreSQL

## ⚙️ Como rodar localmente

### 1. Clone o projeto

```bash
git clone https://github.com/seu-user/shorten-me.com.git
cd shorten-me.com
```

### 2. Crie o arquivo `.env`

```env
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
POSTGRES_DB=shortenme
DATABASE_URL=postgresql://postgres:postgres@db:5432/shortenme
NEXT_PUBLIC_APP_URL=http://localhost:3000
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...
```

### 3. Suba o ambiente com Docker

```bash
docker-compose up --build
```

### 4. Execute a migração do banco

```bash
docker-compose exec web npx prisma migrate dev --name init
```

## 📦 Scripts úteis

```bash
npm run dev             # Executa a aplicação local
npm run db:generate     # Gera o client Prisma
npm run db:migrate      # Aplica migrações
npm run db:studio       # Abre o Prisma Studio
npm run db:seed         # Executa seed (se implementado)
```

## 🛡 Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo [LICENSE](./LICENSE) para mais informações.

## ✉️ Autor

Jefferson Sarti  
[LinkedIn](https://www.linkedin.com/in/jeffersonsarti)
