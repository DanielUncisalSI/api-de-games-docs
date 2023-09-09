# API de Games
Esta API é utilizada
## Endpoints
### GET /games
Esse endpoint é responsável por retornar a listagem de todos os games cadstrados no banco de dados.
#### Parametros
Nenhum
#### Respostas
##### OK 200C
Caso essa resposta aconteça você vai receber a listagem de todos os games.

Exemplo de resposta:

```
[
    {
        "id": 23,
        "title": "Mario",
        "year": 1980,
        "price": 60
    },
    {
        "id": 65,
        "title": "Pepsi Man",
        "year": 2000,
        "price": 50
    },
    {
        "id": 75,
        "title": "Formula 1",
        "year": 2015,
        "price": 95
    }
]

```

#### Falha na autenticação! 404
Caso essa resposta aconteça. isso significa que aconteceu alguma falha durante o processo de autenticação da requisição: Motivos: Token inválido, Token expirado.

Exemplo de resposta:
```
{
    "err": "Token inválido"
}
```
