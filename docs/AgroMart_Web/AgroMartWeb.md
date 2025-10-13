# AgroMart Web

O **AgroMart Web** foi concebido como a **plataforma administrativa do agricultor** dentro do ecossistema AgroMart.Diferentemente do aplicativo mobile, que concentra a interação com os consumidores, o sistema Web tem como finalidade organizar e centralizar a gestão das informações do produtor, oferecendo um ambiente simples e eficiente para o controle das CSAs e dos produtos.

Mais do que apenas um painel de cadastro, o AgroMart Web busca proporcionar ao agricultor um espaço unificado de gestão, no qual ele possa atualizar dados de sua loja, cadastrar novos produtos, ajustar preços, inserir descrições e manter fotos atualizadas.  
Essa centralização facilita o dia a dia do produtor, reduz a duplicidade de informações e garante que os consumidores, ao acessarem o aplicativo mobile, encontrem sempre dados corretos e confiáveis.

O objetivo também envolve atender às especificidades da agricultura familiar, oferecendo uma ferramenta acessível, leve e prática, que possa ser utilizada por produtores com diferentes níveis de familiaridade com a tecnologia.Nesse sentido, o AgroMart Web foi planejado para reduzir barreiras digitais, permitindo que a gestão de uma CSA seja feita de forma mais organizada e eficiente.

Em síntese, o AgroMart Web existe para concentrar a administração das informações do produtor em um só lugar, garantindo consistência entre os diferentes canais do ecossistema AgroMart e fortalecendo a atuação do agricultor no ambiente digital.

---

## Objetivo

O objetivo principal do **AgroMart Web** é disponibilizar ao agricultor um painel de gestão digital capaz de:

- Registrar e atualizar dados da loja ou ponto de venda;  
- Cadastrar produtos com informações completas (nome, descrição, preço, imagens e categorias);  
- Gerenciar alterações de forma autônoma;  
- Assegurar que todas as informações fiquem sincronizadas com o aplicativo mobile, garantindo consistência entre as plataformas.  

!!! info "Importante"
    O AgroMart Web é voltado exclusivamente aos produtores e não ao consumidor final.  
    Sua função é oferecer um ambiente administrativo confiável para o gerenciamento de dados.

---

## Funcionalidades

O **AgroMart Web** já se encontra em funcionamento e oferece aos produtores um conjunto de funcionalidades administrativas que permitem gerenciar suas operações de forma prática e centralizada.  
Entre os principais recursos disponíveis estão:

- **Cadastro e autenticação de produtores:** sistema de login e registro seguro, garantindo que cada produtor tenha seu próprio acesso administrativo;  
- **Gestão de lojas:** possibilidade de criar e atualizar informações da loja ou ponto de venda, incluindo dados gerais, localização e formas de contato;  
- **Gerenciamento de produtos:** inclusão de novos itens no catálogo, com suporte a descrição detalhada, preço, imagens e categorias, além da edição de informações já cadastradas;  
- **Integração direta com o AgroMart Mobile:** todas as atualizações feitas no Web refletem imediatamente no aplicativo mobile, assegurando que os consumidores encontrem dados corretos e atualizados.  

---

##  Próximos Desenvolvimentos

Mesmo já funcional, o **AgroMart Web** continuará sendo aprimorado para oferecer uma experiência cada vez mais completa ao produtor.  
Entre os pontos planejados estão:

- **Aprimoramento da usabilidade:** criação de uma interface mais clara e objetiva, que facilite a compreensão do agricultor no uso diário da plataforma;  
- **Camada visual sobre o Strapi:** desenvolvimento de uma capa mais intuitiva sobre o painel administrativo do Strapi, simplificando a navegação e reduzindo a complexidade técnica para o usuário final.  

---

## Stack Tecnológica

A plataforma Web adota tecnologias modernas que permitem **escalabilidade e robustez**, alinhadas ao crescimento do projeto:

| Camada | Tecnologias |
|---------|--------------|
| **Frontend** | Next.js, React e TypeScript |
| **Backend** | API AgroMart (Strapi) |
| **Banco de Dados** | Relacional, gerenciado pela API |
| **Integrações Previstas** | Geolocalização, upload otimizado de imagens e meios de pagamento |

!!! tip "Observação"
    Embora o **Strapi** não seja naturalmente intuitivo para usuários sem familiaridade técnica, o AgroMart Web foi planejado para oferecer uma camada de interface mais clara e organizada, tornando a experiência de gestão mais simples, acessível e adequada à realidade do agricultor.

---

## Como Navegar Nesta Documentação

Esta seção da documentação do **AgroMart Web** está organizada para facilitar a compreensão do projeto e do sistema.  
Recomenda-se seguir a leitura na seguinte ordem:

1. **Planejamento** → apresenta como foram definidos os requisitos, funcionalidades atuais e próximos desenvolvimentos;  
2. **Arquitetura** → descreve a estrutura técnica, tecnologias utilizadas e comunicação com a API;  
3. **Guia de Instalação** → explica os requisitos e o passo a passo para executar o sistema localmente;  
4. **Padrões de Desenvolvimento** → define convenções adotadas no código, versionamento e boas práticas;  
5. **Contribuição** → orienta como participar do projeto, abrir issues ou enviar pull requests.  
