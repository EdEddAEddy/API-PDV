### PDV API

**Recursos**

* Gerenciamento de usuários (cadastro, login, atualização)
* Gerenciamento de categorias de produtos
* Gerenciamento de produtos (cadastro, atualização, listagem, exclusão)
* Gerenciamento de clientes (cadastro, listagem, exclusão)
* Gerenciamento de pedidos (cadastro, listagem)

**Tecnologias utilizadas**
Node.js
Prisma
Express.js
PostgreSQL
Bcrypt para criptografia de senhas
JSON Web Tokens (JWT) para autenticação

**Pré-requisitos**

Antes de começar, você precisa ter o Node.js instalado em sua máquina.


**Instalação**

1. Clone o repositório para a sua máquina local:

```
git clone git@github.com:EdEddAEddy/PdvAPI.git
```

2. Navegue até o diretório do projeto:

```
cd PdvAPI
```

3. Instale as dependências do projeto:

```
npm install
```

4. Crie um arquivo `.env` na raiz do projeto e adicione as seguintes variáveis de ambiente:

```
DATABASE_URL=
JWT_SECRET=
```

**Iniciando o servidor**

1. Rode o seguinte comando para iniciar o servidor:

```
npm run dev
```

O servidor estará em execução na porta 3000. Você pode acessar o sistema em http://localhost:3000/

**Rotas da API**

A API do sistema pode ser acessada através de requisições HTTP. As rotas da API estão listadas abaixo:

**Rota** | **Método** | **Descrição**
------- | -------- | --------
/usuario | POST | Cadastra um novo usuário
/usuario | GET | Obtém o usuário atual
/usuario | PUT | Atualiza o usuário atual
/login | POST | Autentica um usuário
/categoria | GET | Lista todas as categorias de produtos
/produto | POST | Cadastra um novo produto
/produto/:id | PUT | Atualiza um produto existente
/produto | GET | Lista todos os produtos
/produto/:id | GET | Obtém um produto específico
/produto/:id | DELETE | Exclui um produto
/cliente | POST | Cadastra um novo cliente
/cliente | GET | Lista todos os clientes
/cliente/:id | GET | Obtém um cliente específico
/cliente/:id | PUT | Atualiza um cliente existente
/pedido | POST | Cadastra um novo pedido
/pedido | GET | Lista todos os pedidos

Como utilizar

Você pode usar uma ferramenta como o Postman ou realizar chamadas HTTP diretas para interagir com a API e realizar operações no sistema.

**Autenticação**

Para acessar as rotas que requerem autenticação, é necessário enviar um token JWT no cabeçalho da requisição. O token JWT pode ser obtido através da rota `/login`.
