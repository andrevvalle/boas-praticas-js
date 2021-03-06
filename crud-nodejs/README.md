# Contruir uma API Rest em NodeJS utilizando ExpressJS e MongoDB

API
Exemplos: Twitter, Facebook, Google Maps..

Rest - http
* POST -> Create
* GET -> Retrieve
* PUT -> Update
* DELETE -> Delete

Status Code
200 - Ok
404 - Not Found
201 - Created


# Módulos utilizados
* bluebird (para Promises)
* expressjs (como framework de rotas)
* mongojs (conector para o mongodb)

* supertest
* mocha (testes unitários)

# Teach a dog to Rest
https://blog.apigee.com/detail/restful_api_design



# Desenvolvimento

Instale o nodemon global e as dependências locais do projeto:

```
$ npm install -g nodemon
$ npm install
$ npm start
```

Para rodar os testes
```
$ npm test
```

## Testando a API pelo terminal

### POST (create)
```
$ curl -H "Content-Type: application/json" \
  -d '{"name":"Jane Doe"}' http://localhost:3000/products
```

### GET (retrieve)
```
$ curl -H "Content-Type: application/json" \
  http://localhost:3000/products
$ curl -H "Content-Type: application/json" \
  http://localhost:3000/products/55060ceba8cf25db09f3b216
```

### PUT (update)
```
$ curl -H "Content-Type: application/json" \
   -H "X-HTTP-Method-Override: PUT" -d '{"name":"Foo Bar"}' \
  http://localhost:3000/products/55061dc648ccdc491c6b2b61
```

### DELETE (delete)
```
$ curl -X POST -H "Content-Type: application/json" \
  -H "X-HTTP-Method-Override: DELETE" \
  http://localhost:3000/products/55061dc648ccdc491c6b2b61
```

