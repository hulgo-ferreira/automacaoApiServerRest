<p align="center">
  <a href="https://serverest.dev/">
    <img src="./assets/logo.jpg" alt="ServeRest" width="300">
  </a>
</p>

<h1 align="center">🧪 Automação de API - ServerRest</h1>

Projeto de automação de testes de API utilizando **Postman**, **Newman**, **JavaScript** e **GitHub Actions**, testando a API pública do [ServeRest](https://serverest.dev/).

---

## 📋 Sobre o projeto

Este projeto utiliza o **Postman** para definir collections de testes de API e o **Newman** para executar esses testes via linha de comando e em pipelines de CI/CD.

---

## 🛠️ Tecnologias utilizadas

- [Postman](https://www.postman.com/)
- [Newman](https://github.com/postmanlabs/newman)
- JavaScript
- GitHub Actions

---

## 📦 Pré-requisitos

- Node.js instalado (versão 18.x recomendada)
- NPM instalado
- Collections e environments exportados do Postman

---

## 📂 Estrutura de arquivos

```
├── collections/
│   └── serverRest.postman_collection.json     # Collection de testes
├── environments/
│   └── base_serverRest.postman_environment.json # Environment com variáveis de execução
└── reports/
    └── report.html                             # Relatório gerado (HTML)
```

---

## 🚀 Instalação

Instale o Newman globalmente:

```bash
npm install -g newman
```

Para gerar relatórios em HTML, instale também o reporter `htmlextra`:

```bash
npm install -g newman-reporter-htmlextra
```

---

## ▶️ Executando os testes

### Execução padrão

```bash
newman run collections/serverRest.postman_collection.json \
  -e environments/base_serverRest.postman_environment.json
```

### Execução de uma pasta (folder) específica

```bash
newman run collections/serverRest.postman_collection.json \
  -e environments/base_serverRest.postman_environment.json \
  --folder "nome_da_pasta"
```

---

## 🔒 Problemas de certificado

Caso ocorra erro relacionado a certificado SSL durante a execução, utilize a flag `--insecure`:

```bash
newman run collections/serverRest.postman_collection.json \
  -e environments/base_serverRest.postman_environment.json \
  --folder "BFF API - Protocolo" \
  --insecure
```

---

## 📊 Gerando relatório HTML

Com o reporter `htmlextra` instalado, execute:

```bash
newman run collections/serverRest.postman_collection.json \
  -e environments/base_serverRest.postman_environment.json \
  -r htmlextra \
  --reporter-htmlextra-export ./reports/report.html
```

O relatório será gerado em `./reports/report.html`.

---

## 🔄 Integração contínua (CI/CD)

Este projeto está preparado para execução via **GitHub Actions**, permitindo rodar a suíte de testes automaticamente a cada push ou pull request.

---

## 📄 Licença

Este projeto está sob a licença MIT. Consulte o arquivo `LICENSE` para mais detalhes.
