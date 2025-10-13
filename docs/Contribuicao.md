# Guia de Contribuição para o AgroMart

Agradecemos por dedicar seu tempo e interesse em contribuir para o nosso projeto!  
Sua colaboração é essencial para que possamos evoluir continuamente e entregar soluções cada vez melhores.  

Antes de começar, pedimos que leia atentamente este documento — ele orienta sobre as **práticas recomendadas** e o **fluxo de contribuição**, garantindo que sua participação seja clara, produtiva e integrada ao trabalho da comunidade.

---

##  Como Contribuir

1. Crie um **fork** do projeto.  
2. Clone o fork criado em sua máquina local:  
   ```bash
   git clone https://github.com/seu-usuario/agromart.git
   ```
3. Crie uma branch para sua contribuição:
```bash
git checkout -b minha-contribuicao
```

4. Realize as alterações necessárias na sua branch.

5. Teste suas alterações localmente.

6. Faça um commit com uma mensagem clara e descritiva:

```bash
git commit -m "Adiciona funcionalidade X"
```

7. Envie as alterações para o seu fork:

```bash
git push origin minha-contribuicao
```

8. Abra um Pull Request para a branch master do repositório original e aguarde a revisão.

!!! info "Política de Pull Request"
    Cada Pull Request deve conter apenas uma funcionalidade ou correção de bug.
    A mensagem de commit deve ser descritiva e objetiva.
    Todo PR deve ter pelo menos um revisor antes de ser mesclado.

---

## Regras de Contribuição

- Para manter a qualidade e a consistência do projeto, siga as diretrizes abaixo:

- Escreva código claro e bem documentado;

- Siga as boas práticas da linguagem e do framework;

- Teste o código antes de enviar a contribuição;

- Cada Pull Request deve ser focado em uma alteração específica;

- Mensagens de commit devem ser curtas, diretas e em português.

---

## Política de Commits

- Commits devem ser redigidos em português e no gerúndio;

- Devem ser simples, concisos e descritivos;

- Sempre associe ao número da issue quando aplicável.

Padrão:

```bash
(#NUMERO_DA_ISSUE) Mensagem
```

Exemplo:

```bash
(#26) Criando componente menu
```

---

## Política de Branches
#### Padrões de nomenclatura:

- Novas funcionalidades → feature/nome-da-feature

- Correções de bugs → fix/nome-do-bug

- Documentação → docs/nome-da-doc

- Outros → siga a convenção apropriada ao tipo de alteração

---

## Bugs e Problemas
#### Se você encontrar um bug ou tiver algum problema com o projeto:

- Abra uma issue detalhando o problema;

- Sempre que possível, adicione prints de tela ou logs para facilitar a reprodução.

- Nós ficaremos felizes em ajudar a solucionar o problema!

##  Licença

Ao contribuir com este projeto, você concorda que sua contribuição será licenciada sob a mesma licença do projeto original.

##  Explore o AgroMart

Conheça os **repositórios oficiais** do ecossistema AgroMart:  

| **Projeto** | 💡 **Descrição** | 🔗 **Repositório** |
|----------------|------------------|--------------------|
| **AgroMart Mobile** | Aplicativo voltado ao **consumidor final**, conectando compradores a **agricultores familiares**. | [GitHub - AgroMart Mobile](https://github.com/AgroMart/mobile-client) |
| **AgroMart Web** | Plataforma administrativa para **agricultores** gerenciarem suas **lojas e produtos**. | [GitHub - AgroMart Web](https://github.com/AgroMart/agromart-web) |

!!! tip "Dica"
    Você pode explorar cada repositório para conhecer a arquitetura, as boas práticas e os padrões de desenvolvimento adotados no projeto.