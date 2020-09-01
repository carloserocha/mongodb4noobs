## Utilização

### 1. Conectando o compass ao mongoDB
Primeiro inicie o serviço do mongoDB no seu computador e abra o MongoDB Compass.

Na Tela de início crie um nova conexão e, se o mongoDB estiver rodando corretamente na sua máquina, por padrão ele vai usar o localhost e a porta 27017, apenas clique em conectar e o compass vai mostrar uma tabela contendo todos os bancos de dados nesse servidor.

### 1.2 Conectando o compass com um cluster do Atlas
Para se conectar com o Compass usando um cluster do atlas procure a opção Connect dentro do Atlas e selecione a opção *Connect with Compass* para obter a string de conexão.
Copie a string e abra o compass que automáticamente ele já reconhece e preenche todos o dados da conexão para conectar com a base de dados.

### 1.1 Criando um novo banco de dados e um documento manualmente
Crie uma nova base de dados clicando no botão **CREATE DATABASE** e escolha o nome do base de dados e da coleção (você pode criar mais coleções depois).

Entre na coleção que você criou, clique em **INSERT DOCUMENT** para criar um documento e insira alguns atributo, por exemplo:
```bash
{
  nome: "He4rt Devs"
  avaliação: "100"
}
```
Depois, clique em criar e pronto! Você tem um banco de dados mongoDB utilizando a GUI MongoDB Compass.

