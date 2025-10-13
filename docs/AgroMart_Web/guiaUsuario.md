# Guia de Instalação do AgroMart Web

O **AgroMart Web** é a plataforma administrativa desenvolvida em **Next.js** com **TypeScript**, responsável por oferecer aos produtores um painel centralizado de gestão de lojas e produtos. Integrado diretamente à **AgroMart API (Strapi)**, o sistema garante que todas as informações cadastradas pelos agricultores estejam sempre sincronizadas com o aplicativo mobile.  

Este guia apresenta os **requisitos**, as **etapas de configuração** e o **processo de execução** para rodar o projeto em ambiente local.

---

## Pré-requisitos

Antes de iniciar, certifique-se de ter os seguintes itens configurados:

- **Node.js** (versão recomendada: LTS 18+)  
- **npm** ou **Yarn** (gerenciadores de pacotes)  
- **Git** para clonar o repositório  
- **AgroMart API** rodando localmente ou em ambiente remoto *(necessária para o fornecimento dos dados)*  
- (Opcional) **PostgreSQL** configurado, caso deseje rodar a API AgroMart junto ao ambiente Web  

---

## Clonar o Repositório

```bash
git clone https://github.com/AgroMart/agromart-web.git
cd agromart-web
```

---

## Instalar Dependências
```bash

# com npm
npm install

# ou com yarn
yarn install
```

---

## Configurar Variáveis de Ambiente
Crie um arquivo .env.local na raiz do projeto e copie o conteúdo do modelo abaixo (.env.sample):

```bash

# ===================================================================
# ARQUIVO DE CONFIGURAÇÃO DO PROJETO (MODELO)
# ===================================================================
# Instruções:
# 1. Copie este arquivo com o nome ".env.local" (para Web).
# 2. Preencha os campos conforme indicado.
# 3. NUNCA compartilhe este arquivo com credenciais reais.
# ===================================================================

# === Configurações Web (Next.js) ===
NEXT_PUBLIC_API_URL=http://localhost:1337
NEXT_PUBLIC_BASE_URL=http://localhost:3000
NEXT_PUBLIC_UPLOAD_URL=http://localhost:1337/uploads
NEXT_PUBLIC_GOOGLE_MAPS_API_KEY=

NODE_ENV=development
PORT=3000

# === Configurações da API (Strapi) ===
HOST=0.0.0.0
PORT=1337

APP_KEYS=chave1,chave2,chave3
API_TOKEN_SALT=sua_api_token_salt
JWT_SECRET=sua_jwt_secret
ADMIN_JWT_SECRET=sua_admin_jwt_secret

# Database (Postgres recomendado)
DATABASE_CLIENT=postgres
DATABASE_HOST=localhost
DATABASE_PORT=5432
DATABASE_NAME=agromart
DATABASE_USERNAME=agromart_user
DATABASE_PASSWORD=sua_senha_segura
DATABASE_SSL=false

# Upload Provider (Exemplo AWS S3)
# STRAPI_UPLOAD_PROVIDER=aws-s3
# AWS_ACCESS_KEY_ID=sua_chave
# AWS_SECRET_ACCESS_KEY=sua_chave_secreta
# AWS_REGION=sa-east-1
# AWS_S3_BUCKET=nome_bucket

# Outro provedor (ex.: Cloudinary)
# STRAPI_UPLOAD_PROVIDER=cloudinary
# CLOUDINARY_NAME=...
# CLOUDINARY_API_KEY=...
# CLOUDINARY_API_SECRET=...
```

---

## Rodar em Ambiente de Desenvolvimento
```bash
npm run dev
# ou
yarn dev
```

A aplicação estará disponível em:
http://localhost:3000

---

## Executar a API AgroMart
Para rodar a API (Strapi), siga as etapas abaixo:

```bash
git clone https://github.com/AgroMart/api.git
cd api
yarn install
yarn develop
```

A API estará disponível em:
 http://localhost:1337

!!! tip "Dica"
  Certifique-se de que a API AgroMart esteja rodando antes de iniciar o Web, pois o frontend consome dados diretamente dela.

---

## Repositório Oficial

> Repositório oficial: [AgroMart Web no GitHub](https://github.com/AgroMart/agromart-web)