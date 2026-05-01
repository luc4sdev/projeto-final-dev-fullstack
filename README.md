# 💻 Projeto Final Dev Fullstack — Scheduling App

Aplicação fullstack para gerenciamento de agendamentos, com áreas separadas para clientes e administradores.

O projeto é dividido em:
- **Frontend (Next.js):** interface web responsiva para autenticação, criação e gestão de agendamentos.
- **Backend (Node.js + Express):** API REST com autenticação JWT, RBAC, persistência em MySQL e documentação Swagger.

---

## ✨ Funcionalidades

### Frontend
- Login seguro para clientes e administradores.
- Área do cliente para visualizar e criar agendamentos.
- Área administrativa para gerenciar usuários, salas, horários e logs.
- Feedback visual com notificações de sucesso/erro.
- Download das tabelas em PDF.
- Layout responsivo (desktop e mobile).

### Backend
- Autenticação via JWT.
- Controle de acesso por perfil (RBAC).
- CRUD de usuários, salas e agendamentos.
- Rate-limit para segurança (ex.: bloqueio temporário após tentativas de login).
- Testes automatizados (unitários e E2E).
- Documentação de API com Swagger.

---

## 🚀 Links de Deploy

> OBS: O servidor pode demorar na primeira requisição, pois entra em modo inativo quando não está em uso.

- **App (Frontend):** https://scheduling-app-sigma.vercel.app
- **Login Admin:** https://scheduling-app-sigma.vercel.app/signin/admin
- **Login Cliente:** https://scheduling-app-sigma.vercel.app/signin
- **Documentação da API (Swagger):** https://scheduling-api-ws9u.onrender.com/api/docs

### Credenciais de Administrador (demo)
- **Email:** admin@email.com
- **Senha:** admin123

---

## 📦 Estrutura do Projeto

```bash
projeto-final-dev-fullstack/
├── backend/
└── frontend/
```

---

## 💻 Pré-requisitos

- Node.js (versão LTS mais recente)
- Docker + Docker Compose (para o banco MySQL do backend)
- Git
- Sistema operacional: Windows, Linux ou macOS

---

## ⚙️ Instalação

Instale as dependências em **cada pasta** do projeto.

### 1) Backend

```bash
cd backend
npm install
```

### 2) Frontend

```bash
cd frontend
npm install
```

Se preferir, você também pode usar `yarn` ou `pnpm`.

---

## 🔐 Variáveis de Ambiente

### Backend (`backend/.env`)

Crie o arquivo `backend/.env` com:

```env
NODE_ENV=dev
PORT="3333"
DATABASE_URL="mysql://scheduling:scheduling@localhost:3306/scheduling"
JWT_SECRET="secret"
```

### Frontend (`frontend/.env.local`)

Crie o arquivo `frontend/.env.local` com:

```env
NEXT_PUBLIC_API_BASE_URL="http://localhost:3333/api"
AUTH_SECRET="secret"
```

---

## 🐳 Banco de Dados (Backend)

Com o Docker ativo, suba o banco de dados na pasta `backend`:

```bash
cd backend
docker compose up -d
```

---

## ▶️ Rodando o Projeto Localmente

Use dois terminais, um para o backend e outro para o frontend.

### Terminal 1 — Backend

```bash
cd backend
npm run dev
```

API local: `http://localhost:3333`

### Terminal 2 — Frontend

```bash
cd frontend
npm run dev
```

App local: `http://localhost:3000`

---

## 🧪 Testes

Na pasta `backend`:

```bash
npm run test       # Testes unitários
npm run test:e2e   # Testes E2E
```

---

## 🛠️ Tecnologias Utilizadas

### Frontend
- TypeScript
- React
- Next.js
- TailwindCSS
- Radix UI
- React Hook Form + Zod
- TanStack Query
- NextAuth
- React Toastify
- Lucide React

### Backend
- TypeScript
- Node.js
- Express
- Sequelize
- MySQL
- Docker
- Vitest
- Supertest
- Swagger

---

## 📄 Observações

- O projeto segue boas práticas de Clean Code.
- A interface é responsiva e focada em usabilidade.
- O backend está preparado para escalabilidade com estratégias de segurança e testes.

---

## 📄 Licença

Este projeto está sob licença MIT.

---