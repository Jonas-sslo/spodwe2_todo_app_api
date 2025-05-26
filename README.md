# TODO API


API para ser consumida pela aplicação de exemplo [TODO APP] da disciplina SPODWE2.



Instruções:

1. Ir até a pasta raíz do projeto

2. Executar o comando para a instalação das dependências: 
```bash
npm install
```

3. Iniciar o servidor da aplicação:

```bash
node src/app.js
```

Caso seja a intenção executar a aplicação com *hot reload* habilitado (útil durante o desenvolvimento):

```bash
npm run dev
```

Desta forma, qualquer alteração de arquivo resultará na reinicialização da aplicação.

Para ambas as formas de execução da aplicação, basta usar *crtl+c* no terminal em questão para que a aplicação seja interrompida.


## Comandos úteis (sempre a partir da raíz do projeto)

Para realizar a criação de um novo usuário.

### Autenticação

- POST  (Criação de um novo usuário):

```bash
curl -i -H "Content-Type: application/json" -X POST -d @samples/users/post/new-user.json  http://localhost:3000/users
```

### Criação de tarefas

Para testar a API:

- GET:

```bash
curl -i http://localhost:3000/todos
```

- POST: 

```bash
curl -i -H "Content-Type: application/json" -X POST -d @samples/todos/post/new-todo.json  http://localhost:3000/todos

curl -i -H "Content-Type: application/json" -X POST -d @samples/todos/post/new-todo-invalid.json  http://localhost:3000/todos
```

- PUT:

```bash
curl -i -H "Content-Type: application/json" -X PUT -d @samples/todos/put/update-todo.json  http://localhost:3000/todos/{ID_DO_TODO}

curl -i -H "Content-Type: application/json" -X PUT -d @samples/todos/put/update-todo-text.json  http://localhost:3000/todos/{ID_DO_TODO}

curl -i -H "Content-Type: application/json" -X PUT -d @samples/todos/put/update-todo-done.json  http://localhost:3000/todos/{ID_DO_TODO}

curl -i -H "Content-Type: application/json" -X PUT -d @samples/todos/put/update-todo-invalid.json  http://localhost:3000/todos/{ID_DO_TODO}