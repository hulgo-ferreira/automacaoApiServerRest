# Automação API - ServerRest
 
Projeto de automação de testes de API utilizando:
 
- Postman
- Newman
- JavaScript
- GitHub Actions
 
## Como executar
 
```bash
newman run collections/ServerRest.postman_collection.json \
-e environments/base_serveRest.postman_environment.json


# 🧪 Integração Postman + Newman

Este projeto utiliza o **Postman** para definir collections de testes de API e o **Newman** para executar esses testes em linha de comando e em pipelines de CI/CD.

---

## 📦 Pré-requisitos
- Node.js instalado (versão 18.x recomendada)
- NPM instalado
- Collections e environments exportados do Postman

---

## 📂 Estrutura de arquivos
- `serverRest.postman_collection.json` → Collection de testes
- `base_serverRest.postman_environment.json` → Environment com variáveis de execução

---

## 🚀 Instalação do Newman
```bash
npm install -g newman


## ▶️ Executando testes localmente
newman run serverRest.postman_collection.json \
  -e base_serverRest.postman_environment.json


## 🔒 Problemas de certificado
Caso ocorra erro de certificado, utilize a flag --insecure:

newman run serverRest.postman_collection.json \
  -e base_serverRest.postman_environment.json \
  --folder "BFF API - Protocolo" \
  --insecure


## 📊 Gerando relatório HTML
npm install -g newman-reporter-htmlextra


## Execute com reporter configurado
newman run collections/serverRest.postman_collection.json \
  -e base_serverRest.postman_environment.json \
  -r htmlextra \
  --reporter-htmlextra-export ./reports/report.html


