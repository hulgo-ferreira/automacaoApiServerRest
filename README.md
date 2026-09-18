# Automação API - ServerRest
 
Projeto de automação de testes de API utilizando:
 
- Postman
- Newman
- JavaScript
- GitHub Actions
 
## Como executar
 
```bash
newman run collections/serverRest.postman_collection.json \
-e environments/base_serverRest.postman_environment.json
