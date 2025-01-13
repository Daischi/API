# 🌟 API de Gerenciamento de Usuários

![Badge](https://img.shields.io/badge/Node.js-v16.13.2-green)
![Badge](https://img.shields.io/badge/Express-v4.18.2-blue)
![Badge](https://img.shields.io/badge/Prisma-v4.15.0-purple)

Esta é uma API simples, criada para gerenciar usuários em um sistema. Com ela, você pode **cadastrar**, **editar**, **deletar** e **listar** usuários. Ideal para aplicações que precisam de um gerenciamento básico de contas ou perfis de usuários. 🚀

---

## 📚 **Funcionalidades**
- ✅ **Criar Usuários:** Registra novos usuários no sistema.
- ✏️ **Editar Usuários:** Atualiza informações de um usuário existente.
- 🗑️ **Deletar Usuários:** Remove usuários do banco de dados.
- 📋 **Listar Usuários:** Exibe todos os usuários cadastrados.

---

## 🛠️ **Tecnologias Utilizadas**
Esta API foi desenvolvida com as seguintes tecnologias:

- [Node.js](https://nodejs.org/) - Ambiente de execução JavaScript.
- [Express.js](https://expressjs.com/) - Framework minimalista para aplicações web.
- [Prisma](https://www.prisma.io/) - ORM para gerenciar banco de dados.
- [SQLite](https://www.sqlite.org/) - Banco de dados leve e integrado.
- [Postman](https://www.postman.com/) - Ferramenta de testes de APIs (recomendado para testar).

---

## 🚀 **Como Rodar o Projeto**

### **Pré-requisitos**
Certifique-se de ter instalado:
- **Node.js** (v16 ou superior)
- **NPM** (ou Yarn)

### **Passo a Passo**

1. Clone o repositório:
   ```bash
   git clone https://github.com/Daischi/API.git
   cd API
2. Instale as dependências:
   ```bash
   npm install
3. Configure o banco de dados:

- Certifique-se de que o arquivo prisma/schema.prisma está configurado corretamente.
- Execute as migrações
  ```bash
   npx prisma migrate dev

4. Inicie o Servidor:
   ```bash
   npm start
5. Acesse a API no endereço:
   ```bash
   npm start

# 🛤️ Rotas da API Criar 

## Criar Usuário

### Endpoint
`POST /users`

### Descrição
Cria um novo usuário na plataforma.

### Corpo da Requisição
O corpo da requisição deve ser enviado no formato JSON com os seguintes campos:

 ```json
{
  "nome": "João Silva",
  "email": "joao.silva@example.com",
  "senha": "senha123",
  "data_nascimento": "1990-01-01"
}

````

# 🛤️ Rotas da API Listar

## Listar Usuários

### Endpoint
`GET /users`

### Descrição
Retorna uma lista de todos os usuários cadastrados na plataforma.

### Resposta

#### Sucesso (200 OK)

Caso a requisição seja bem-sucedida, a resposta será no formato JSON com a lista de usuários:

```json
[
  {
    "id": 1,
    "nome": "João Silva",
    "email": "joao.silva@example.com",
    "data_nascimento": "1990-01-01"
  },
  {
    "id": 2,
    "nome": "Maria Oliveira",
    "email": "maria.oliveira@example.com",
    "data_nascimento": "1985-05-23"
  }
]
```

# 🛤️ Rotas da API Editar


## 3. Editar Usuário

**Endpoint:** `PUT /users/:id`

Este endpoint permite editar os dados de um usuário existente, identificando-o pelo seu `id`. O corpo da requisição deve conter as informações a serem atualizadas.

### Exemplo de Requisição:

```json
{
  "name": "João da Silva",
  "email": "joaodasilva@email.com",
  "age": 26
}

```
## 4. Deletar Usuário

**Endpoint:** `DELETE /users/:id`

Este endpoint permite deletar um usuário existente, identificando-o pelo seu `id`. Ao realizar a exclusão, todos os dados do usuário serão removidos do sistema.

### Parâmetros:
- `:id` (no caminho) – O identificador único do usuário que será deletado.

### Resposta de Sucesso:
- **Código 204**: Usuário deletado com sucesso.


# 📁 Estrutura do Projeto

```plaintext
📂 graphql
├── 📂 API
│   ├── 📂 prisma
│   │   └── 📄 schema.prisma   # Configuração do banco de dados
│   ├── 📄 server.js          # Arquivo principal da aplicação
│   ├── 📄 package.json       # Gerenciador de dependências
│   └── 📄 .gitignore         # Arquivos ignorados pelo Git
```

---

## ✅ Boas Práticas

- 🔍 Sempre valide os dados enviados nas requisições.
- 🛠️ Use ferramentas como Postman ou Insomnia para testar a API.
- 🔒 Considere implementar autenticação para proteger as rotas.

---

## 📬 Contato

Se você tiver alguma dúvida ou sugestão, entre em contato:

- **Autor:** Guilherme Poppi
- **GitHub:** [Daischi](https://github.com/Daischi)
