## Project Setup 

Abra o terminal integrado no Vs Code e rode estes comandos;

```sh
npm install
```

### Compila e Modifica para Produção

```sh
npm run build
```

### Compila e carrega o projeto

```sh
npm run dev
```

### Run End-to-End Tests with [Playwright](https://playwright.dev)

```sh
# Install browsers for the first run
npx playwright install

# When testing on CI, must build the project first
npm run build

# Runs the end-to-end tests
npm run test:e2e
# Runs the tests only on Chromium
npm run test:e2e -- --project=chromium
# Runs the tests of a specific file
npm run test:e2e -- tests/example.spec.ts
# Runs the tests in debug mode
npm run test:e2e -- --debug
```
