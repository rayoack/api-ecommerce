# API Ecommerce 🏪

## Rodando o projeto

> Baixe ou clone este repositório.
>
> Vocé pode escolher qualquer banco de dados, devendo somente fazer as devidas alterações nos arquivos dentro da pasta config, assim como valores referente ao ambiente (usuário, host, etc).

> Acesse a raiz do projeto por um console e execute:

- `yarn ou npm i` para instalar as dependências do projeto
- `yarn start ou npm start` para rodar a aplicação no localhost

## Sobre o projeto: 📃

O objetivo era desenvolver uma API para um sistema de ecommerce similar ao mercado livre, com criação e autenticação de usuário, um CRUD para anúncios dos produtos e solicitações de compra. O projeto foi criado utilizando o Node.js.

> As respostas de todas requisições são em `json`.

## Requisitos do projeto: ✅

- ##### Criação e autenticação de usuário
Rota de criação: POST `/users`
Rota de sessão: POST `/sessions`

> A criação dos usuários foi feita utilizando o `mongoose` que é um ORM para o `mongoDB` um banco de dados NoSQL e a autenticação dos usuários utilizando o Json Web Token(JWT).

> Para a criação do usuário você deve passar o nome, e-mail e senha, a resposta será um `json` com todos esses dados com a senha criptografada, o `id` do usuário, e a data de criação.

> Para autenticação você deve passar o email cadastrado e a senha, a resposta será um `json` com as informações do usuário e o `token` de autenticação.

- ##### Criação, atualização, listagem e remoção de anuncios
Rota de listagem: GET `/ads`
Rota para exibir anuncio: GET `/ads/:id`
Rota de criação: POST `/ads`
Rota de atualização: PUT `/ads/:id`
Rota de remoção: DELETE `/ads/:id`

> Cadastrar produtos passando seu título, a descrição e o preço do produto, o retorno será um `json` contendo todas essas informações, o `id` do anuncios, a data de criação e as informações do usuário que o criou.

- ##### Solicitação de compra
Rota de solicitação: POST `/purchases`

> Realizar uma solicitação de compra informando o `id` do anúncio e o conteúdo do corpo do e-mail que será enviado ao criador do anúncio.

## Frameworks e Tecnologias Utilizadas: 🌌

### Front-End: 🎨

- <strong>Handlebars</strong> (Criação de templates para o envio dos emails)

### Backend: 💾

- <strong>Node.Js</strong> & o Framework <strong>Express.Js</strong>
- <strong>MongoDB</strong> (Banco de dados NoSQL)
- <strong>Mongoose</strong> (ORM para o MongoDB)
- <strong>Redis</strong> (Banco de dados NoSQL)
- <strong>Nodemailer</strong> (Envio de e-mails)
- <strong>Docker</strong> (Criação de containers)