## POST /register

### Padrão de requisição

```json
{
  "email": "User2@gmail.com",
  "password": "12345",
  "name": "User",
  "userType": "user"
}
```

### Padrão de resposta

```json
{
  "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6IlVzZXIyQGdtYWlsLmNvbSIsImlhdCI6MTY3MzM3NDIwMiwiZXhwIjoxNjczMzc3ODAyLCJzdWIiOiIzIn0.0W0SnhK2jLGLX8dAHPiPf2KR6m1p8tb5kZ3GGT8umTU",
  "user": {
    "email": "User2@gmail.com",
    "name": "User",
    "userType": "user",
    "id": 3
  }
}
```

## POST /login

### Padrão de requisição

```json
{
  "email": "User2@gmail.com",
  "password": "12345"
}
```

### Padrão de resposta

```json
{
  "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6IlVzZXIyQGdtYWlsLmNvbSIsImlhdCI6MTY3MzM3NDMyOSwiZXhwIjoxNjczMzc3OTI5LCJzdWIiOiIzIn0.UPwfJ3dmqJ0OVlJ85083ZZvjzTj8TH9kjgVtir2yLMc",
  "user": {
    "email": "User2@gmail.com",
    "name": "User",
    "userType": "user",
    "id": 3
  }
}
```

## Rotas com autorização

```js
{
  headers: {
    Authorization: `Bearer ${token}`
  }
}
```

## GET /posts

### Padrão de resposta

```json
[
  {
    "id": 1,
    "userId": 1,
    "title": "Casa",
    "description": "Teste da api",
    "img": "https://www.plantapronta.com.br/projetos/161/01.jpg",
    "value": 100,
    "adress": {
      "city": "Jaú",
      "street": "Teste",
      "number": 2
    },
    "checker": {
      "checked": false,
      "observation": ""
    }
  }
]
```

## POST /posts

### Padrão de requeisição

```json
{
  "userId": 3,
  "title": "Casa2",
  "description": "Teste da api",
  "img": "https://www.plantapronta.com.br/projetos/161/01.jpg",
  "value": 100,
  "adress": {
    "city": "Jaú",
    "street": "Teste2",
    "number": 3
  }
}
```

### Padrão de resposta

```json
{
  "userId": 3,
  "title": "Casa2",
  "description": "Teste da api",
  "img": "https://www.plantapronta.com.br/projetos/161/01.jpg",
  "value": 100,
  "adress": {
    "city": "Jaú",
    "street": "Teste2",
    "number": 3
  },
  "id": 2
}
```

## PUT /posts/:id

### Padrão de requeisição

```json
{
  "userId": 3,
  "title": "Casa4",
  "description": "Teste da api",
  "img": "https://www.plantapronta.com.br/projetos/161/01.jpg",
  "value": 100,
  "adress": {
    "city": "Jaú",
    "street": "Teste2",
    "number": 3
  }
}
```

### Padrão de resposta

```json
{
  "userId": 3,
  "title": "Casa4",
  "description": "Teste da api",
  "img": "https://www.plantapronta.com.br/projetos/161/01.jpg",
  "value": 100,
  "adress": {
    "city": "Jaú",
    "street": "Teste2",
    "number": 3
  },
  "id": 2
}
```

## DELETE /posts/:id

### Padrão de resposta

não precisa de corpo e não precisa de resposta
