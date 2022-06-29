# API Nest CRUD
API exemplo publicada no heroku utilizando NestJS persistindo dados no MongoDB.

## Pré-requistos

- Database no mongodb
  - Collection:  
    - `users`
  - Fields:
    - `name: string`
    - `email: string`
    - `password: string`

## API

- Acesso: <https://esb-api-nest-crud.herokuapp.com/>

### End-points
  **CRUD** - **C**reate / **R**ead / **U**pdate / **D**elete

ação     | verbo end-point    | descrição          | parâmetro
---------|--------------------|--------------------|-------------------------
Create   | `POST /users`      | retorna todos os usuários cadastrados|`{ "email": "sample@gmail.com", "name": "Sample Júnior", "password": "123456" }`
Find All | `GET /users`       | retorna todos os usuários cadastrados| sem parâmetro
Find One | `GET /users:id`    |retorna usuários pelo `id` informado|`62bbc9d93fa1b47d0b22136f`
Update   | `PATCH /users:id`  |Atualiza os campos enviados para o `id` informado|`62bbc9d93fa1b47d0b22136f`
Delete   | `DELETE /users:id` |remove o usuário para o `id` informado|{`"id":"62bbc9d93fa1b47d0b22136f", "email": "new_sample@gmail.com", "name": "New Sample Júnior" }`
