
# Mini API com Express e Prisma

Uma mini API construída com Node.js, Express e Prisma ORM, oferecendo operações CRUD para gerenciar usuários no banco de dados.

## 🚀 Começando

Essas instruções ajudarão você a obter uma cópia da API em execução localmente para fins de desenvolvimento e testes.

### 📋 Pré-requisitos

Você precisará das seguintes ferramentas instaladas:

- Node.js v14 ou superior
- Prisma Client configurado com seu banco de dados (MySQL, PostgreSQL, SQLite, etc.)

### 🔧 Instalação

Siga os passos abaixo para rodar a API localmente:

1. Clone o repositório:

   ```bash
   git clone https://github.com/gesley/api-node.git
   ```

2. Instale as dependências:

   ```
   npm install
   ```

3. Configure o Prisma:

   - Inicialize o Prisma:
     ```bash
     npx prisma init
     ```

   - Configure o arquivo `.env` com as credenciais do banco de dados.

4. Execute as migrações para criar as tabelas no banco de dados:

   ```bash
   npx prisma migrate dev --name init
   ```

5. Inicie a aplicação:

   ```bash
   npm start
   ```


## 📦 Implantação

Para implantar a API em produção, você precisará configurar variáveis de ambiente no servidor e rodar as migrações do Prisma, conforme mostrado na seção de instalação.

## 🛠️ Construído com

Ferramentas utilizadas no desenvolvimento:

* [Express.js](https://expressjs.com/) - O framework web usado
* [Prisma ORM](https://www.prisma.io/) - ORM para banco de dados
* [Node.js](https://nodejs.org/) - Ambiente de execução JavaScript
