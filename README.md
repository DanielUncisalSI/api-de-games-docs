# API de Games
Esta API é utilizada
## Endpoints
### GET /games
Esse endpoint é responsável por retornar a listagem de todos os games cadstrados no banco de dados.
#### Parametros
Nenhum
#### Respostas
##### OK 200C
Caso essa resposta aconteça você vai receber a listagem de todos os games
#### Falha na autenticação! 404
Caso essa resposta aconteça. isso significa que aconteceu alguma falha durante o processo de autenticação da requisição: Motivos: Token inválido, Token expirado 
