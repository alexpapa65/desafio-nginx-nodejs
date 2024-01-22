# Full Cycle - Módulo Docker - Desafio Nginx com Node.js

## Descrição:

Criar docker-compose para gerar aplicação na porta 8080 que use nginx como proxy reverso para chamar aplicação Node.js. A aplicação deverá, a cada chamada, inserir um registro em banco MySql e retornar a mensagem "Full Cycle Rocks!!!" com a lista de registros cadastrados. O projeto deve ser publicado em repositório Git remoto.

## Observações

1. As imagens nginx e nodejs usam o Alpine Linux para diminuir seu tamanho.
2. Não foi possível utilizar o dockerize para garantir que a aplicação seja iniciada somente após inicialização completa do MySql. Quando utilizado o dockerize, o "node index.js" não fica no ar. Essa situação será tratada oportunamente.

## Roteiro de uso

```bash
git clone alexpapa65/desafio-nginx-nodejs
cd desafio-nginx-nodejs
docker compose up -d
```
