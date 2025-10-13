# Arquitetura do Sistema

O **AgroMart Mobile** foi desenvolvido com **React Native** (em conjunto com **Expo** e **TypeScript**) para garantir a execução em múltiplas plataformas (**Android** e **iOS**) a partir de uma única base de código.  
O aplicativo é totalmente integrado à **AgroMart API (Strapi)**, que centraliza os dados de lojas, produtos, pedidos e assinaturas.

A arquitetura foi planejada para ser modular, organizada e escalável, permitindo que novos recursos sejam adicionados sem comprometer a estabilidade do sistema.

---

## Estrutura do Repositório

O repositório do **AgroMart Mobile** segue uma divisão lógica entre camadas de apresentação, lógica de negócio e comunicação com a API.  
A estrutura principal pode ser descrita da seguinte forma:

- **`src/assets/`** → contém imagens, ícones e recursos estáticos utilizados nas telas.  
- **`src/components/`** → componentes reutilizáveis (botões, inputs, cabeçalhos, cards).  
- **`src/screens/`** → telas principais da aplicação (Login, Cadastro, Lojas, Produtos, Pedidos, Perfil).  
- **`src/navigation/`** → configuração do **React Navigation**, responsável por rotas em stack, tab e drawer.  
- **`src/services/`** → integração com a **API AgroMart**, utilizando **Axios** para requisições HTTP.  
- **`src/store/`** → gerenciamento de estado global, utilizando **Context API** (com possibilidade futura de Redux).  
- **`src/utils/`** → funções auxiliares (tratamento de datas com **date-fns**, máscaras e validações).  
- **`src/config/`** → configurações gerais do projeto, como temas, constantes e chaves de API.  

---

## Fluxo de Dados

O fluxo de dados do **AgroMart Mobile** segue um ciclo bem definido:

1. **Autenticação:** o usuário cria sua conta ou realiza login. O token retornado pela API é armazenado de forma segura.  
2. **Consumo de dados:** telas de lojas, produtos e planos consultam a API através dos serviços centralizados em `src/services/`.  
3. **Gerenciamento de estado:** informações relevantes (usuário logado, pedidos, endereço) são armazenadas no **Context API**, garantindo acesso em qualquer parte do app.  
4. **Atualizações:** ações como editar perfil, cadastrar endereço ou realizar pedido disparam requisições **POST/PUT** para a API.  
5. **Reflexo no Web:** alterações feitas no Web pelos produtores (novos produtos, preços ou descrições) são refletidas automaticamente no Mobile, assegurando consistência de informações para o consumidor.  

!!! info "Integração em tempo real"
    O aplicativo foi estruturado para reagir rapidamente às atualizações da API, mantendo a sincronização entre o AgroMart Web e o Mobile.

---

## Camadas Principais

- **Interface e Navegação:** construída com **React Native**, **Expo** e **React Navigation**;  
- **Gerenciamento de Formulários:** **Formik + Yup**, garantindo validação robusta;  
- **Estilização:** **styled-components**, permitindo temas e reaproveitamento de estilos;  
- **Integração com API:** serviços em **Axios** centralizados, conectando-se ao **Strapi**;  
- **Geolocalização:** **react-native-maps** para exibir lojas e pontos de venda próximos;  
- **Experiência do Usuário:** carrosséis de destaque com **Snap Carousel** e formatações com **date-fns**.

---

## Resumo da Arquitetura

O **AgroMart Mobile** adota uma arquitetura modular e escalável, com separação clara de responsabilidades. Esse modelo favorece a manutenção, a adição de novas funcionalidades e o trabalho colaborativo entre desenvolvedores, assegurando que a evolução do sistema ocorra de forma organizada e sustentável.

---

## Localização no Repositório

> Repositório oficial: [AgroMart Mobile no GitHub](https://github.com/AgroMart/mobile-client)

