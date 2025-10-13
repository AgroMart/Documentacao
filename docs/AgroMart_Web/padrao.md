# Padrões de Desenvolvimento — AgroMart Web

O **AgroMart Web** é a plataforma administrativa destinada aos produtores, construída em **Next.js** com **TypeScript** e integrada à **AgroMart API (Strapi)**.  
Para manter a **consistência** e **qualidade** do projeto, todo desenvolvimento deve seguir este padrão.

---

## Fluxo de Desenvolvimento

### 1. Definição da Tarefa
- Toda alteração deve partir de uma tarefa definida no **Kanban Board**.  
- A tarefa deve estar associada a um **requisito válido** ou issue aprovada.  
- Sem aprovação prévia, nenhuma implementação deve ser iniciada.  

### 2. Criação da Branch
- Crie branches a partir de `devel`.  
- Padrões de nomenclatura:  
  - `feature/nome-da-feature` → novas funcionalidades;  
  - `fix/nome-do-bug` → correções;  
  - `docs/nome-da-doc` → documentação.  

### 3. Desenvolvimento
- Seguir boas práticas de **Next.js + React** com **TypeScript**.  
- **Componentes reutilizáveis** → `src/components`;  
- **Hooks personalizados** → `src/hooks`;  
- **Integrações com API** → `src/services` (via **Axios**);  
- **Configurações globais** (tema, constantes) → `src/config`;  
- **Estilização** → CSS-in-JS (**styled-components**, **Tailwind**) ou **CSS Modules**;  
- **Internacionalização (i18n)** → utilizar para textos, evitando strings fixas em componentes.  

### 4. Commits
- Mensagens em **português no gerúndio**.  
- Sempre referenciar a issue ou tarefa:  

```bash
(#72) Criando dashboard de lojas
(#81) Ajustando fluxo de autenticação
```

### 5. Testes Locais
- Rodar `npm run dev` ou `yarn dev` e validar em `http://localhost:3000`.  
- Corrigir **warnings** antes do commit.  
- Testar fluxos principais: **login**, **cadastro de loja**, **cadastro de produto**.  

### 6. Pull Request
- Criar **PR** para `devel`, **nunca direto em `master`**.  
- O PR deve conter:
- Descrição clara da mudança;  
- Prints (ou vídeos) de telas alteradas/adicionadas;  
- Referência ao número da issue/tarefa.  
- É necessária **pelo menos 1 aprovação** antes do merge.  

---

## Regras Obrigatórias

!!! warning "Obrigatório"
    Não desenvolver sem tarefa definida no **Kanban Board**.  
    Cada **PR** deve conter apenas **uma alteração específica**.  
    Seguir as instruções do **Guia de Contribuição**.  
    Respeitar a política de **commits** e **branches**.

---

## Boas Práticas

- Prefira **componentes pequenos, desacoplados e reutilizáveis**.  
- Utilize **TypeScript** com **tipagem estrita** para evitar erros em tempo de execução.  
- Centralize **requisições HTTP** em `src/services`.  
- Documente todas as **variáveis de ambiente** em `.env.local`.  
- Evite duplicação de código — use **hooks** ou **utils** para lógica repetida.  
- Mantenha **consistência visual** com o tema global do projeto.  
- Atualize a documentação sempre que houver impacto em funcionalidades.  

---

## Exemplo de Fluxo Real

1. Tarefa criada no Kanban: *“Implementar página de relatórios”* (#88).  
2. Criação da branch:  
 ```bash
 git checkout -b feature/pagina-relatorios
 ```
3. Desenvolvimento em src/pages/reports/index.tsx e componentes auxiliares em src/components/Reports/.

4. Commit:

```bash
git commit -m "(#88) Criando página de relatórios"
```

5. PR aberto para devel, revisado e aprovado.

6. Merge realizado conforme as regras.