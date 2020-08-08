## 1. Instalando o Mongodb
Para você conseguir aprender o que será introduzido, é de suma importância que tenha o serviço do banco rodando localmente (ou na cloud, vamos falar isso mais para frente).

## 1.2 Instalando no Ubuntu e derivados
Vamos seguir os seguintes passos para a instalação

```bash
# Primeiramente, vamos atualizar tudo
sudo apt update && sudo apt upgrade -y;
# Segundamente, vamos instalar o mongodb
sudo apt install mongodb;
# Terceiramente, vamos checar se o mongo está rodando
sudo systemctl status mongodb;
# Quartamente, podemos entrar no mongodb diretamente pela bash
mongo
```

## 1.3 Instalando no Windows
Para baixar no win, é necessário fazer o download do instalador do [mongo](https://www.mongodb.com/try/download/community?tck=docs_server) e realizar o famoso click-next (aceitar e avançar) e podemos executar o mongodb diretamente pelo cmd.
```cmd
"C:\Program Files\MongoDB\Server\4.4\bin\mongo.exe"
```
Dessa forma, podemos já estamos conectados ao banco.

## 1.4 Instalando em outros sistemas
Para instalar em outros sistemas operacionais, siga os passos de [instalação na documentação oficial](https://docs.mongodb.com/manual/installation/) do mongodb ou se tiveram problemas na instalação demonstrada.

## 2. Utilizando na Cloud
Podemos utilizar o serviço de hospedagem do [Mongo Atlas](https://docs.mongodb.com/manual/installation), segundo eles mesmos, um serviço de nuvem de banco de dados global para aplicações modernas. Para criar o seu primeiro banco de dados na nuvem, siga o [tutorial oficial](https://docs.atlas.mongodb.com/getting-started/).