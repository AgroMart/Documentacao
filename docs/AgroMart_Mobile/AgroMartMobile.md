# AgroMart Mobile

O **AgroMart Mobile** foi criado para aproximar consumidores e agricultores familiares, oferecendo um canal direto de acesso a produtos frescos, de qualidade e com origem conhecida.  
Enquanto o AgroMart Web funciona como painel administrativo para os produtores, o aplicativo mobile é a vitrine acessível ao público, permitindo que qualquer pessoa descubra, conheça e entre em contato com os agricultores de sua região.

Mais do que uma simples lista de produtos, o AgroMart Mobile busca criar uma experiência de consumo transparente e consciente, onde o usuário pode explorar lojas, filtrar categorias, localizar pontos de venda próximos e interagir diretamente com o produtor.  
Dessa forma, o aplicativo fortalece a rede de CSAs, valoriza o que é local e promove a agricultura familiar como alternativa viável e sustentável.

Em síntese, o AgroMart Mobile existe para conectar quem planta com quem consome, reduzindo distâncias e criando um ambiente de confiança mútua entre produtores e consumidores.

---

## Objetivo

O objetivo do AgroMart Mobile é disponibilizar aos consumidores uma plataforma prática e acessível para:

- Explorar produtos frescos e de qualidade, diretamente de agricultores locais;  
- Encontrar pontos de venda e lojas por meio de filtros e geolocalização;  
- Acessar informações claras sobre preço, descrição e disponibilidade dos produtos;  
- Iniciar contato direto com o agricultor, facilitando negociações e combinações de entrega ou retirada.  

!!! info "Importante"
    O AgroMart Mobile foi desenvolvido com foco no consumidor final.  
    Sua função é tornar a agricultura familiar mais visível e acessível, promovendo um consumo saudável e consciente.

---

## Funcionalidades Atuais

O AgroMart Mobile já está em funcionamento e oferece aos usuários uma experiência completa para interação com agricultores locais.  
Entre os principais recursos disponíveis estão:

- **Criação de conta e autenticação** do usuário;  
- **Listagem das lojas** na página principal;  
- **Pesquisa de lojas por nome**;  
- **Pesquisa por região administrativa**;  
- **Visualização da loja** com catálogo, descrição, **produtos e preços**;  
- **Ação de contato** com o dono da loja (link para mensageria/contato);  
- **Realização de pedidos**;  
- **Histórico de pedidos**;  
- **Planos (assinaturas)**: visualizar planos ativos e **pular a cesta da semana**;  
- **Endereços**: cadastrar e editar;  
- **Perfil**: editar dados do usuário.  

---

## Próximos Desenvolvimentos

Mesmo já funcional, o AgroMart Mobile continuará a ser evoluído para oferecer novas formas de engajamento.  
Entre os pontos planejados estão:

- **Aprimoramento da usabilidade** – ajustes na interface para tornar a experiência de navegação ainda mais simples e agradável;  
- **Notificações personalizadas** – alertas sobre novos produtos, promoções ou disponibilidade de itens favoritos;  
- **Integração com formas de pagamento digital** – facilitando a conclusão de negociações diretamente pelo aplicativo.  

---

## Stack Tecnológica

O aplicativo Mobile foi desenvolvido com foco em **multiplataforma**, garantindo acesso tanto em Android quanto em iOS:

| Categoria | Tecnologias |
|------------|--------------|
| **Framework** | React Native + Expo |
| **Integração com API** | AgroMart API (Strapi) |
| **Gerenciamento de estado** | Context API |
| **UI e Estilização** | styled-components |
| **Formulários e Validação** | Formik + Yup |
| **Navegação** | React Navigation (stack, tab e drawer navigation) |
| **Carrosséis e destaques** | React Native Snap Carousel |
| **Mapas e geolocalização** | React Native Maps |
| **Consumo de API** | Axios |
| **Datas e formatação** | date-fns |
| **Integrações futuras** | Push notifications, gateways de pagamento, relatórios avançados |

!!! tip "Observação"
    A experiência do aplicativo foi pensada para ser rápida, intuitiva e confiável, refletindo em tempo real todas as atualizações realizadas pelos produtores no AgroMart Web.

---

## Como navegar nesta documentação

Esta seção da documentação do **AgroMart Mobile** está organizada para orientar o leitor quanto ao funcionamento e às diretrizes do projeto.  
Recomenda-se seguir a leitura na seguinte ordem:

1. **Planejamento** → apresenta os objetivos, funcionalidades atuais e próximos desenvolvimentos;  
2. **Arquitetura** → descreve a estrutura técnica, tecnologias utilizadas e integrações;  
3. **Guia de Instalação** → explica os requisitos e o passo a passo para executar o aplicativo localmente;  
4. **Padrões de Desenvolvimento** → define convenções adotadas no código, versionamento e boas práticas;  
5. **Contribuição** → orienta como participar do projeto, abrir issues ou enviar pull requests.  
