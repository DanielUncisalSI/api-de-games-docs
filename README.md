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

### POST /auth
Esse endpoint é responsável por fazer o processo de login.
#### Parametros
email: E-mail cadastrado no sistema

senha: Senha cadastrada no sistema com aquele determinado e-mail.

Exemplo:
```
{
    "email":"daniel@gmail.com",
    "senha":"123456"
}
```

#### Respostas
##### OK! 200
Caso essa resposta aconteça você vai receber o token JWT para conseguir acessar endpoints protegidos na API.

Exemplo de resposta:

```
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJkYW5pZWxAZ21haWwuY29tIiwiaWF0IjoxNjk0Mjg4OTc5LCJleHAiOjE2OTQ0NjE3Nzl9.I62UFOEYBqoMm8xgHYl7VfVioEMg-5pH0LBINusy9dg"
}

```

#### Falha na autenticação! 401
Caso essa resposta aconteça. isso significa que aconteceu alguma falha durante o processo de autenticação da requisição: Motivos: E-mail ou senha incorreto.

Exemplo de resposta:
```
{
    "err": "Credenciais inválidas"
}
```

