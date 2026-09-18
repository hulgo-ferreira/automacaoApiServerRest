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