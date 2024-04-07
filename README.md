# API de Gerenciamento de Produtos

Esta é uma API simples desenvolvida em Node.js e Express para gerenciamento de produtos. A API permite criar, listar, atualizar e excluir produtos de um banco de dados simulado em memória.

## Configuração da Porta

A API está configurada para ser executada na porta 3003 por padrão.

```javascript
const porta = 3003;
```

## Rotas Disponíveis

### GET /produtos

Retorna todos os produtos cadastrados.

### GET /produtos/:id

Retorna o produto correspondente ao ID fornecido na rota.

### POST /produtos

Adiciona um novo produto ao banco de dados. Deve-se fornecer o nome e o preço do produto no corpo da requisição.

### PUT /produtos/:id

Atualiza as informações de um produto existente. Deve-se fornecer o ID do produto na rota e o nome e preço atualizados no corpo da requisição.

### DELETE /produtos/:id

Exclui um produto existente com base no ID fornecido na rota.



## Imagens:
![Screenshot_20240323_224008](https://github.com/RobsonMendes37/Projeto_API-Com-Express/assets/111722533/54a9f7c5-e3ac-487e-8b99-0642bf882deb)

![Screenshot_20240323_224347_2](https://github.com/RobsonMendes37/Projeto_API-Com-Express/assets/111722533/4812d73d-c85e-4a30-a7d4-6fa6b5292af5)



## Banco de Dados Simulado

O banco de dados utilizado é simulado em memória, com a utilização de um objeto JavaScript para armazenar os produtos. A cada novo produto adicionado, é gerado um ID único automaticamente.

```javascript
const sequence = {
    _id: 1,
    get id() { return this._id++ }
}

const produtos = {}
```

## Funcionalidades do Banco de Dados

- `salvarProduto(produto)`: Adiciona um novo produto ao banco de dados.
- `getProduto(id)`: Retorna um produto específico com base no ID fornecido.
- `getProdutos()`: Retorna todos os produtos cadastrados.
- `excluirProduto(id)`: Exclui um produto com base no ID fornecido.

## Execução do Servidor

Para executar o servidor e iniciar a API, utilize o seguinte comando:

```bash
node server.js
```

O servidor será executado na porta especificada, e você poderá acessar as rotas da API conforme descrito acima.

---
