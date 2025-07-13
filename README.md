# SlothAgent

Projeto desenvolvido durante um evento da Rocketseat.

## 🚀 Tecnologias

- **Runtime**: Node.js com TypeScript
- **Framework**: Fastify
- **Database**: PostgreSQL com pgvector
- **ORM**: Drizzle ORM
- **Validação**: Zod
- **Linting/Formatting**: Biome
- **Containerização**: Docker & Docker Compose

## 📁 Estrutura do Projeto

```
src/
├── db/
│   ├── connection.ts
│   ├── migrations/
│   ├── schema/
│   └── seed.ts
├── http/
│   └── routes/
├── env.ts
└── server.ts
```

## 🛠️ Setup

### Pré-requisitos

- Node.js 18+
- Docker e Docker Compose

### Instalação

1. Clone o repositório
2. Instale as dependências:

```bash
npm install
```

3. Configure as variáveis de ambiente:

```bash
# Crie um arquivo .env na raiz do projeto
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/sloth
```

4. Inicie o banco de dados:

```bash
docker-compose up -d
```

5. Execute as migrações:

```bash
npx drizzle-kit migrate
```

6. (Opcional) Popule o banco com dados iniciais:

```bash
npm run db:seed
```

## 🚀 Executando o Projeto

### Desenvolvimento

```bash
npm run dev
```

### Produção

```bash
npm start
```

## 📋 Scripts Disponíveis

- `npm run dev` - Executa em modo desenvolvimento com hot reload
- `npm start` - Executa em modo produção
- `npm run db:seed` - Popula o banco com dados iniciais

## 🔧 Padrões de Projeto

- **Arquitetura**: API REST com Fastify
- **Validação**: Schema validation com Zod
- **Database**: Migrations com Drizzle Kit
- **Type Safety**: TypeScript em todo o projeto
- **Code Style**: Biome para linting e formatação

## 🌐 Endpoints

- `GET /health` - Health check
- `GET /rooms` - Lista todas as salas

O servidor roda na porta 3333 por padrão.
