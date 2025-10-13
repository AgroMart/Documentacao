# Padrões de Desenvolvimento — AgroMart Mobile

O desenvolvimento do **AgroMart Mobile** segue um conjunto de práticas que asseguram qualidade, consistência e alinhamento com os objetivos do projeto.  
Toda contribuição deve respeitar estas diretrizes e estar previamente **definida no Kanban Board**.

---

##  Fluxo de Desenvolvimento

### 1. Definição da Tarefa
- Toda nova funcionalidade, correção de bug ou ajuste deve estar registrada no Kanban Board.  
- A tarefa precisa estar associada a um requisito válido ou issue aprovada.  
- Sem aprovação prévia, nenhuma alteração deve ser iniciada.

### 2. Criação da Branch
- A branch deve ser criada a partir da `devel`.  
- Use o padrão de nomenclatura:  
  - `feature/nome-da-feature` → novas funcionalidades.  
  - `fix/nome-do-bug` → correções de erro.  
  - `docs/nome-da-doc` → alterações em documentação.  

### 3. Desenvolvimento
- Seguir as boas práticas de React Native + Expo.  
- Componentes devem ser **modulares e reutilizáveis** (criar em `src/components`).  
- Evitar lógica duplicada → criar funções auxiliares em `src/utils`.  
- Centralizar chamadas de API em `src/services` usando **Axios**.  
- Utilizar **Context API** (ou Redux, quando aprovado) para estado global.  
- Para formulários, usar **Formik + Yup**.  
- Estilização preferencial com **styled-components**.

### 4. Commits
- Mensagens em **português e no gerúndio**.  
- Devem sempre referenciar a issue ou tarefa:  

 ```bash
(#45) Criando tela de listagem de lojas
(#52) Ajustando validação de endereço no cadastro
 ```

### 5. Testes Locais
- Antes do commit, rodar o app no **Expo Go** ou emulador.  
- Validar fluxos principais: login, listagem de lojas, pedidos e perfil.  
- Checar warnings no console e corrigir sempre que possível.

### 6. Pull Request
- Criar PR para a branch `devel`, **nunca diretamente em `master`**.  
- O PR deve conter:
- Descrição clara da mudança.  
- Prints ou vídeos (quando aplicável).  
- Referência à issue/tarefa do Kanban.  
- Requer pelo menos **1 revisão/aprovação** antes do merge.

---

##  Regras Obrigatórias

!!! warning "Obrigatório"
    Não desenvolver sem tarefa previamente definida no **Kanban Board**.  
    Cada **PR** deve conter apenas **uma alteração específica**.  
    Sempre seguir o **guia de contribuição** antes de abrir PR.  
    Respeitar a **política de commits** e de **branches**.

---

##  Boas Práticas

- Prefira **componentes pequenos** e de fácil manutenção.  
- Mantenha **nomes descritivos** para variáveis, funções e arquivos.  
- Documente trechos de código mais complexos com comentários.  
- Sempre valide no emulador **Android** (mínimo) e, quando possível, também no **iOS**.  
- Atualize a documentação se sua alteração impactar o uso da aplicação.  

---

## Exemplo de Fluxo Real

1. Tarefa criada no Kanban: *“Implementar histórico de pedidos”* (#60).  
2. Desenvolvedor cria a branch: 

 ```bash
 git checkout -b feature/historico-pedidos
  ``` 

3. Implementação realizada no diretório src/screens/OrdersHistory.

4. Commit:

 ```bash
git commit -m "(#60) Criando tela de histórico de pedidos"
 ```

5. Pull Request aberto para devel, revisado e aprovado.

6. Merge realizado conforme as regras de contribuição.