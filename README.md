# herbertaonovo-playwright1

Projeto de automação de testes E2E com **Playwright**, gerado pelo QA Portfolio Builder (Qazando).
Aplicação sob teste: [https://automationpratice.com.br](https://automationpratice.com.br)

## Tecnologias

- @playwright/test
- @faker-js/faker (massa de dados dinâmica)
- Page Objects
- GitHub Actions (CI/CD)

## Pré-requisitos

- Node.js 20+
- npm

## Instalação

```bash
npm install
```

O `postinstall` já baixa os navegadores necessários.

## Executar os testes

```bash
npm test
```

## Ver o relatório

```bash
npm run report
```

## Estrutura

```text
tests/      # cenários de teste (login, cadastro, interações)
pages/      # Page Objects
fixtures/   # massa de dados estática
utils/      # data factory com Faker
```

## Cenários cobertos

**Login:** sucesso, e-mail inválido, e-mail vazio, senha vazia.

**Cadastro:** sucesso com massa dinâmica, cadastro pela home, nome vazio, e-mail vazio, e-mail inválido, senha vazia, senha menor que o mínimo.

**Interações básicas:** navegação, localização de elementos, preenchimento, clique, select, checkbox, radio e validação de texto.

## CI/CD

O workflow `.github/workflows/playwright.yml` roda os testes a cada push e pull request e publica o relatório HTML como artefato.

_Nível do projeto: intermediate_
