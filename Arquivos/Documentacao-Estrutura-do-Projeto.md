# 🧱 Documentação da Estrutura do Projeto – UniBlog

## 📌 1. Visão Geral
O **UniBlog** é um sistema voltado para o ambiente universitário, permitindo publicações, interações e gestão de perfis acadêmicos.  
A aplicação é composta por um **frontend mobile/web**, um **backend robusto com Node.js**, e um **banco de dados relacional PostgreSQL**, todos integrados em um ambiente **containerizado via Docker**.

---

## ⚙️ 2. Tecnologias Utilizadas

| Camada | Tecnologia | Descrição |
|--------|-------------|------------|
| **Frontend** | **React + Expo** | Interface do usuário responsiva e multiplataforma (Web e Mobile). |
| **Backend** | **Node.js (Express/Fastify)** | API REST para autenticação, publicações e interações. |
| **Banco de Dados** | **PostgreSQL** | Banco relacional utilizado para armazenar dados estruturados. |
| **Armazenamento de Arquivos** | **MinIO** | Sistema de armazenamento de mídia (imagens, anexos) compatível com S3. |
| **Containerização** | **Docker** | Facilita a execução padronizada em qualquer ambiente. |
| **Controle de Versão** | **Git + GitHub** | Versionamento e documentação do código-fonte. |

---

## 🗂️ 3. Estrutura de Pastas

```
UniBlog
├─ blog-backend
│  ├─ .dockerignore
│  ├─ .env.exemple
│  ├─ compose.yaml
│  ├─ Dockerfile
│  ├─ eslint.config.mts
│  ├─ ngrok
│  ├─ package.json
│  ├─ prisma
│  ├─ src
│  │  ├─ app.ts
│  │  ├─ lib
│  │  │  ├─ minio.ts
│  │  │  └─ prisma.ts
│  │  ├─ middlewares
│  │  │  └─ auth.middleware.ts
│  │  ├─ controllers
│  │  │  ├─ account.controller.ts
│  │  │  ├─ interacoes.controller.ts
│  │  │  ├─ post.controller.ts
│  │  │  └─ profile.controller.ts
│  │  ├─ services
│  │  │  ├─ account.service.ts
│  │  │  ├─ feed.service.ts
│  │  │  ├─ interacoes.service.ts
│  │  │  ├─ post.service.ts
│  │  │  └─ profile.service.ts
│  │  ├─ routes
│  │  │  ├─ account.routes.ts
│  │  │  ├─ interacoes.routes.ts
│  │  │  ├─ post.routes.ts
│  │  │  └─ profile.routes.ts
│  │  ├─ schemas
│  │  │  ├─ account.schema.ts
│  │  │  ├─ interacoes.schema.ts
│  │  │  ├─ post.schema.ts
│  │  │  └─ profile.schema.ts
│  │  ├─ server.ts
│  │  └─ utils
│  │     ├─ jwt.ts
│  │     ├─ parseMultipart.ts
│  │     └─ uploadToMinio.ts
│  ├─ tsconfig.json
│  └─ types
│     └─ fastify-jwt.d.ts
├─ blog-mobile
│  ├─ .expo
│  │  ├─ cache
│  │  │  └─ eslint
│  │  ├─ devices.json
│  │  ├─ README.md
│  │  ├─ settings.json
│  │  ├─ types
│  │  │  └─ router.d.ts
│  │  └─ web
│  │     └─ cache
│  │        └─ production
│  │           └─ images
│  ├─ app
│  │  ├─ (app)
│  │  │  ├─ create-post.tsx
│  │  │  ├─ feed.tsx
│  │  │  ├─ index.tsx
│  │  │  ├─ notification.tsx
│  │  │  ├─ profile.tsx
│  │  │  ├─ search.tsx
│  │  │  └─ _layout.tsx
│  │  ├─ (auth)
│  │  │  ├─ login.tsx
│  │  │  ├─ register.tsx
│  │  │  ├─ registerProfile.tsx
│  │  │  ├─ selectProfile.tsx
│  │  │  └─ _layout.tsx
│  │  └─ _layout.tsx
│  ├─ app.json
│  ├─ assets
│  │  ├─ declarations.d.ts
│  │  └─ images
│  │     ├─ logo-Uniblog.png
│  │     ├─ partial-react-logo.png
│  │     ├─ react-logo.png
│  ├─ eas.json
│  ├─ eslint.config.js
│  ├─ eslint.config.mts
│  ├─ expo-env.d.ts
│  ├─ package-lock.json
│  ├─ package.json
│  ├─ README.md
│  ├─ src
│  │  ├─ components
│  │  │  ├─ CourseSelectorComponent.tsx
│  │  │  ├─ ImageImportComponent.tsx
│  │  │  ├─ ImageProfileComponent.tsx
│  │  │  └─ navBarComponent.tsx
│  │  ├─ constants
│  │  │  ├─ calculateTimeAgo.ts
│  │  │  └─ Colors.ts
│  │  ├─ hooks
│  │  ├─ scripts
│  │  ├─ services
│  │  │  └─ api.ts
│  │  └─ utils
│  │     └─ fonts.ts
│  ├─ tailwind.config.js
│  └─ tsconfig.json

```
## 🧩 4. Integração Entre os Componentes

[React + Expo]  ➡️  consome API REST  ➡️  [Node.js Backend]  ➡️  [PostgreSQL + MinIO]

- O frontend envia requisições HTTP para o backend (login, posts, comentários, etc.).

- O backend consulta e grava dados no PostgreSQL.

- Arquivos e imagens são enviados e armazenados no MinIO.

- O Docker Compose orquestra os serviços para que funcionem juntos localmente.

## 🧠 5. Boas Práticas de Estrutura

- Utilizar nomes consistentes para pastas e arquivos.

- Separar lógica de negócio, interface e dados.

- Versionar apenas arquivos necessários (ignorar /node_modules, /dist, etc.).

- Documentar novas rotas ou componentes no README.



