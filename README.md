# API REST com FastAPI + PostgreSQL + Docker

Este projeto é uma API RESTful construída com **FastAPI** e banco de dados **PostgreSQL**, totalmente dockerizada para facilitar o setup e execução.

Requisitos: Docker e Docker Compose

## Estrutura do Projeto

** Estrutura **

dockenizado/
├── docker-compose.yml # Orquestração dos containers
├── Dockerfile # Configuração da imagem FastAPI
├── povoar_bd.py # Script para popular o banco com tabelas
├── requirement.txt # Dependências da aplicação
├── conexao_singleton.py # Conexão Singleton com o banco
└── docker_fastapi_simcc/
└── app/
├── app.py # Aplicação principal FastAPI
├── controller/ # Rotas da API
├── dao/ # Lógica de acesso ao banco de dados
└── model/ # Modelos de dados Pydantic


---

## Como Executar

### 1. Clonar o Repositório

```bash```
git clone https://github.com/tiagojesilva/fastapi/.git
cd dockenizado

** Suca o container com Docker **
docker compose up --build

** Popular o banco **
docker compose exec backend python povoar_bd.py


Acessar a API
Swagger UI: http://localhost:8000/docs
