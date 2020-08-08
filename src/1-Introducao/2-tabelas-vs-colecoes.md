## 2. Tabelas VS Coleções
Tabelas em bancos relacionais são a união entre estrutura (schema/esquema/esboço) e os dados. Logo, precisamos definir o que vai ser salvo e qual sua tipagem.

Vamos ver na prática. Aqui temos uma criação de tipagem/schema da tabela _Product_ no SQL, todos os dados que forem _NOT NULL_ não poderam ser ignorados nas inserções de Produtos.

```sql
CREATE TABLE Product (
    sku INT PRIMARY KEY NOT NULL,
    name VARCHAR (50) NOT NULL,
    description VARCHAR (200) NOT NULL,
    qty INT,
    price MONEY NOT NULL
)
```

Aqui temos a criação da coleção (uma coleção de livros/documentos)

```nosql

```

Não é necessario fazer a tipagem/schema de uma coleção no Mongodb, mas quando lidamos com muitos dados, é bom ser criado uma schema padrão para ser realizado indexes e buscas que não retorem vazias (que não retornem nenhum dado), podemos fazer criar a schema usando o mongoose no NodeJS

```js

const mongoose = require("mongoose")

const ProductSchema = new mongoose.Schema({
    sku: {
        type: String,
        required: true
    },
    name: {
        type: String,
        required: true
    },
    description: {
        type: String,
        required: true
    },
    qty: {
        type: Number,
    },
    price: {
        type: Number,
        required: true
    }
}, {
    strict: false
})

module.exports = mongoose.model("Product", ProductSchema)
```
Assim está definido nosso schema, utilizando a biblioteca _mongoose_ essa tarefa fica simplificada.
Podemos definir um _required_ como _false_ também, ou apenas não descrever como necessário.
A propriedade _strict_ define se o objeto a ser inserido na coleção deve seguir as definições firmemente, sem nenhum campo a mais, quando declado como _false_ continua obedecendo a tipagem, porém, é possível inserir mais dados. 