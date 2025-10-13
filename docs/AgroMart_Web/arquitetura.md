# Arquitetura do Sistema

O **AgroMart Web** e a **AgroMart API** formam o núcleo administrativo do ecossistema AgroMart.  
Enquanto o **Web** atua como painel de gestão para o agricultor, a **API** (implementada em **Strapi**) centraliza e provê todos os dados necessários, garantindo consistência com o **Mobile**.  

Essa integração permite que os produtores administrem suas lojas, cadastrem produtos e mantenham seus catálogos sempre atualizados, enquanto consumidores acessam as mesmas informações em tempo real pelo aplicativo.

---

## Objetivo e Escopo

- **AgroMart Web** → plataforma administrativa para agricultores, com painel simples e acessível para gerenciar lojas e produtos;  
- **AgroMart API** → única fonte de verdade, responsável por armazenar e disponibilizar dados (produtores, lojas, produtos, pedidos e planos).  

!!! info "Integração"
    O Web atua como **interface visual do agricultor**, enquanto a API é a **camada de dados** que garante sincronização contínua com o Mobile.

---

## Estrutura do Repositório Web

O repositório do **AgroMart Web** foi planejado com **Next.js + React + TypeScript**, seguindo uma estrutura modular e escalável:

- **`/public/`** → arquivos estáticos (imagens, ícones, logotipos);  
- **`/pages/`** → definição de rotas e páginas principais (Login, Dashboard, Cadastro de Produtos);  
- **`/components/`** → componentes reutilizáveis (formulários, tabelas, botões, cards);  
- **`/styles/`** → estilização (CSS Modules, Tailwind ou styled-components);  
- **`/services/`** → integração com a API via **Axios**;  
- **`/contexts/`** → gerenciamento de estado global (**Context API**);  
- **`/utils/`** → funções auxiliares (datas, máscaras, validações);  
- **`/hooks/`** → hooks customizados para abstrair lógicas recorrentes.  

---

## Estrutura do Repositório API (Strapi)

A API do AgroMart segue a arquitetura padrão do **Strapi v4**, garantindo modularidade e segurança:

- **`/src/api/*`** → content-types (produtos, lojas, pedidos, assinaturas), com rotas, controllers e services;  
- **`/config/*`** → configuração de ambiente, middlewares, CORS e segurança;  
- **`/database/*`** → definição do cliente do banco (**PostgreSQL**);  
- **`/public/uploads/`** → armazenamento local de mídia (em produção usa provider externo: S3, GCS, Cloudinary);  
- **`/src/extensions/*`** → extensões de plugins (users-permissions, upload, etc).  

**Domínios Principais:**

- **Produtor (`user`)** com role `producer`;  
- **Loja (`store`)** com dados básicos e localização;  
- **Produto (`product`)** com preço, descrição e imagens;  
- **Pedido (`order`)** com itens e status;  
- **Assinatura (`plan/subscription`)** para CSAs;  
- **Endereço (`address`)** vinculado ao consumidor.  

---

## Fluxo de Dados

1. **Login e Autenticação**  
   - Agricultor acessa o Web → login via API (JWT).  
   - O JWT garante segurança e papéis de acesso (`producer`, `consumer`, `admin`).  

2. **Gestão de Lojas e Produtos (Web)**  
   - O produtor cadastra/edita informações → Web envia via Axios → API persiste no banco.  

3. **Consumo pelo Mobile**  
   - O Mobile consome a API diretamente → dados refletidos em tempo real.  

4. **Pedidos e Assinaturas**  
   - Mobile cria pedidos/assinaturas → API armazena → Web exibe relatórios simplificados para o agricultor.  

---

## Camadas Principais

### AgroMart Web
- **Interface:** Next.js + React, responsiva e acessível;  
- **Estado:** Context API (ou Redux/Zustand em futuras versões);  
- **Serviços:** integração centralizada com API (Axios);  
- **Estilização:** CSS Modules ou styled-components.  

### AgroMart API
- **Core:** Node.js + Strapi;  
- **Autenticação:** JWT + roles (`producer`, `consumer`, `admin`);  
- **Banco de Dados:** PostgreSQL;  
- **Mídia:** plugin de upload (local ou providers externos);  
- **Endpoints REST:** content-types com filtros, paginação e populate.  

---

## Configuração e Ambiente

Exemplo de `.env` para a **API AgroMart**:

```bash
HOST=0.0.0.0
PORT=1337
APP_KEYS=...
JWT_SECRET=...
DATABASE_CLIENT=postgres
DATABASE_HOST=localhost
DATABASE_PORT=5432
DATABASE_NAME=agromart
DATABASE_USERNAME=agromart_user
DATABASE_PASSWORD=******
```

---

## Ciclo de Requisições (Alto Nível)

- Web (produtor) cria/edita loja e produtos → API persiste;

- Mobile (consumidor) consulta lojas/produtos → API responde;

- Mobile cria pedidos/assinaturas → API registra e vincula ao consumidor;

Atualizações fluem entre todos os canais, mantendo consistência.

---

##  Qualidade, Logs e Observabilidade

- Validação: schemas do Strapi garantem integridade;

- Policies/Middlewares: aplicados para auditoria, sanitização e autorização;

- Logs: padronizados em JSON, integráveis a ELK, Loki ou CloudWatch;

- CORS e Rate Limiting: configurados para segurança de acesso.

---

##  Evolução Arquitetural

- Camada visual aprimorada no Web, reduzindo complexidade do Strapi;

- Normalização de responses na API para reduzir acoplamento;

- Cache de leitura para catálogos de alta demanda;

-  Filas e jobs assíncronos (notificações, uploads, processamento);

- Versionamento da API (/api/v1) e feature flags para novas funcionalidades.

!!! tip "Integração"
    O AgroMart Web é a camada visual e administrativa do sistema,
    enquanto a AgroMart API é a camada de dados e regras de negócio,
    assegurando uma comunicação contínua e confiável entre Web e Mobile.

## Localização no Repositório

> Repositório oficial: [AgroMart Web no GitHub](https://github.com/AgroMart/agromart-web)