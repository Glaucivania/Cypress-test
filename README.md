# Cypress Automation Project

Projeto de automação de testes E2E usando Cypress para o site [saucedemo.com](https://www.saucedemo.com/).

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

## ▶ Executar testes

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


