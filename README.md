# Voting System 🗳️

Sistema de votação digital para cooperativas, com autenticação, sessões de votação, painel de pautas e visualização de resultados.

## 📦 Repositórios

Este projeto é um monorepo que agrupa:

- **Backend (Django + DRF + JWT):** [`voting-system-api`](https://github.com/anakarlasantana/voting-system-api)
- **Frontend (React + MUI + Redux):** [`voting-system-web`](https://github.com/anakarlasantana/voting-system-web)

## 🚀 Rodando a aplicação com Docker

> Requisitos: [Docker](https://www.docker.com/) e [Docker Compose](https://docs.docker.com/compose/)

### 1. Clone o monorepo

```bash
git clone https://github.com/anakarlasantana/voting-system.git
cd voting-system
```

### 2. Inicialize os submódulos

```bash
git submodule update --init --recursive
```

### 3. Suba a aplicação com Docker Compose

```bash
docker-compose up --build
```

🌐 Acessos
Serviço URL
Frontend http://localhost:5173
Backend API http://localhost:8000

### 4. Acessos

    Frontend: http://localhost:5173

    Backend (API): http://localhost:8000

🧪 Funcionalidades
👤 Autenticação

    Registro (/register)

    Login (/login)

    Proteção de rotas com JWT

📋 Pautas e Votação

    Listagem de pautas (pública)

    Votação protegida com token

    Sessões de votação com tempo

    Restrição: 1 voto por usuário por pauta

📊 Resultados

    Visualização dos resultados após encerramento da sessão

🛠️ Tecnologias

Backend

    Django + DRF

    SQLite (persistência de dados)

    JWT com SimpleJWT

    Djoser (autenticação)

Frontend

    React 19 + Vite

    Redux Toolkit

    React Query

    React Hook Form

    Material UI

🐳 Docker

    Frontend e Backend rodam em containers separados

    Banco de dados é persistido em arquivo db.sqlite3 no container do Django

    A aplicação sobe com apenas 1 comando

## ❗ Dívidas Técnicas

- **Ausência de Testes Automatizados no Frontend**  
  Até o momento, não foram implementados testes automatizados para os componentes e funcionalidades do frontend. A solução ideal seria incluir testes unitários e de integração utilizando ferramentas como Jest e React Testing Library.

- **Uso de SQLite no Backend**  
  O projeto utiliza o banco de dados SQLite por questões de simplicidade e agilidade no desenvolvimento e containerização. Em ambientes de produção, o ideal seria utilizar um banco mais robusto como PostgreSQL, que oferece melhor performance, segurança e suporte a múltiplos usuários.

- **Validação de Formulários**  
  Os formulários do frontend ainda possuem validações básicas. Idealmente, deveriam ter validações mais robustas, com feedback detalhado para o usuário em caso de erros, além de máscaras nos campos de entrada (como CPF, senha, etc).

- **Controle de Sessões de Votação**  
  A verificação de sessões ativas e o controle do tempo da votação ainda são simplificados. Em um cenário real, seria importante ter uma interface que indique o tempo restante para votar e bloqueie automaticamente após o fim da sessão.

🙋‍♀️ Autora

Ana Karla Santana
LinkedIn: linkedin.com/in/anakarlasantana
GitHub: @anakarlasantana
