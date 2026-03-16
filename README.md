# Cypress Automation Project

Projeto de automação de testes E2E usando Cypress para o site [saucedemo.com](https://www.saucedemo.com/).

##  Tecnologias Utilizadas

* **Cypress**: Framework de automação de testes E2E.
* **JavaScript**: Linguagem base do projeto.
* **Node.js**: Ambiente de execução.

##  Casos de Teste Automatizados

O foco deste projeto é garantir o fluxo principal de compra no site **SauceDemo**.

### Autenticação (login.cy.js)
- [x] **Login com sucesso:** Valida o acesso com um usuário padrão e redirecionamento para a página de produtos.
- [x] **Login inválido:** Verifica a exibição da mensagem de erro ao inserir credenciais incorretas.

### Carrinho e Compra (carrinho.cy.js)
- [x] **Adicionar produto:** Valida se o badge do carrinho atualiza corretamente ao adicionar um item.
- [x] **Persistência do item:** Verifica se o produto selecionado permanece visível na página de checkout.

##  Estrutura do projeto

- `cypress.config.js`: configuração do Cypress.
- `cypress/e2e/login.cy.js`: testes de login.
- `cypress/e2e/carrinho.cy.js`: testes de carrinho.
- `cypress/fixtures/`: dados estáticos para testes (atualmente `example.json`).
- `cypress/support/commands.js`: comandos personalizados de Cypress.
- `cypress/support/e2e.js`: suporte global para testes.
- `package.json`: dependências do projeto (Cypress 15.x).

##  Requisitos

- Node.js 18+ (recomendado)
- npm (ou yarn)
- Conexão com internet (acesso a `https://www.saucedemo.com/`)

##  Instalação

```bash
cd c:/QA/Cypress
npm install
```

##  Executar testes

### 1) Abrir UI do Cypress

```bash
npx cypress open
```

- Selecionar `login.cy.js` ou `carrinho.cy.js` para rodar no navegador.

### 2) Rodar todos os testes no modo headless

```bash
npx cypress run
```

- Rodará todos os arquivos `*.cy.js` em `cypress/e2e`.

### 3) Executar teste específico

```bash
npx cypress run --spec "cypress/e2e/login.cy.js"
```

##  Cobertura atual

`cypress/e2e/login.cy.js`
- login com usuário válido (`standard_user` / `secret_sauce`)
- login inválido e verificação de mensagem de erro

`cypress/e2e/carrinho.cy.js`
- login
- adicionar produto ao carrinho
- validação do badge do carrinho e item visível na página de carrinho


