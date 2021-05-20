# Projeto Todo-Auth

**Ideia:** Criar uma Todo List com integração de Usuários
**Fullstack ou Rest:** A decidir.


**Rotas**: 

* POST - /auth/register - Registra um usuário
* POST - /auth/login - Autentica um usuário
* GET - /todos - Retorna uma lista/view de todos os afazeres do usuário
* GET - /todos/{todoId} - Retorna um array/view com o todo selecionado do usuário (precisa pertencer ao mesmo)
* POST - /todos - Cria um TODO para o usuário autenticado
* PUT - /todos/{todoId} - Atualiza um TODO de um usuário autenticado
* DELETE - /todos/{todoId} - Deleta um TODO de um usuário autenticado

**Migrations**: 

table: users

- id: int (usar id padrão)
- name: string
- email: string unique
- password: string


table: todos

- id: int (usar id padrão)
- user_id: int references id on users
- name: string
- description: string
- deadline: date
- ended_at: date nullable
