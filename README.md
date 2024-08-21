````md
# Mini API com Express e Prisma

## Descrição

Esta mini API foi desenvolvida utilizando Express.js e Prisma ORM para realizar operações CRUD (Create, Read, Update, Delete) com uma tabela de usuários no banco de dados.

## Funcionalidades

- **Criar Usuário:** Registra um novo usuário no banco de dados.
- **Buscar Usuários:** Retorna todos os usuários ou filtra usuários por nome, e-mail ou idade.
- **Atualizar Usuário:** Atualiza os dados de um usuário específico pelo ID.
- **Deletar Usuário:** Remove um usuário específico pelo ID.

## Tecnologias Utilizadas

- [Express.js](https://expressjs.com/)
- [Prisma ORM](https://www.prisma.io/)

## Requisitos

- **Node.js** v14 ou superior
- **Prisma Client** configurado com seu banco de dados (MySQL, PostgreSQL, SQLite, etc.)

## Instalação

1. Clone este repositório:

   ```bash
   git clone https://github.com/seu-usuario/nome-do-repositorio.git
   ```

2. Instale as dependências:

   ```bash
   npm install
   ```

3. Configure o Prisma:
   
   - Execute o comando para inicializar o Prisma:
   
     ```bash
     npx prisma init
     ```

   - Configure o arquivo `.env` com suas credenciais de banco de dados.

4. Execute as migrações para criar a tabela no banco de dados:

   ```bash
   npx prisma migrate dev --name init
   ```

5. Execute a aplicação:

   ```bash
   npm start
   ```

## Endpoints

### `POST /usuarios`

Cria um novo usuário.

- **Corpo da Requisição:**
  ```json
  {
    "name": "Nome do Usuário",
    "email": "email@exemplo.com",
    "age": 30
  }
  ```

- **Resposta:**
  - Status: `200 OK`
  - Mensagem: `criado`

---

### `GET /usuarios`

Retorna uma lista de usuários. Pode filtrar por nome, email e idade.

- **Parâmetros de Query (Opcional):**
  - `name`: Filtro pelo nome do usuário.
  - `email`: Filtro pelo email do usuário.
  - `age`: Filtro pela idade do usuário.

- **Resposta:**
  - Status: `200 OK`
  - Corpo: Lista de usuários.

---

### `PUT /usuarios/:id`

Atualiza as informações de um usuário existente.

- **Parâmetros:**
  - `id`: ID do usuário a ser atualizado.

- **Corpo da Requisição:**
  ```json
  {
    "name": "Novo Nome",
    "email": "novoemail@exemplo.com",
    "age": 25
  }
  ```

- **Resposta:**
  - Status: `200 OK`
  - Mensagem: `atualizado`

---

### `DELETE /usuarios/:id`

Remove um usuário pelo ID.

- **Parâmetros:**
  - `id`: ID do usuário a ser removido.

- **Resposta:**
  - Status: `200 OK`
  - Corpo: `{ "message": "deletado" }`

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
````
