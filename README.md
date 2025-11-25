# API REST para implementar CRUD de tabela animaiss no MySQL (Backend) e Formulário para acessá-la (Frontend)
  
## 1. Pré-requisitos:
1. Ter o **Visual Code** e o **node** instalado. Para fazer o download acesse https://nodejs.org/pt/download . Prefira o download de uma versão LTS.

2. Ter um banco **MySQL** instalado . Para fazer o download acesse https://dev.mysql.com/downloads/. Pode usar também o **MariaDB** que é instalado com o XAMPP, disponível em https://www.apachefriends.org/pt_br/index.html. 
  
Para executar este código siga os seguintes passos:  

## 2. Baixar o código e script para criar a base de dados
1. Abra um shell (cmd ou git bash ou PowerShell - este último pode ter restrições para executar o `npm`)
2. Clone o código deste repositório (pode ser dentro de qualquer pasta em seu computador na qual tenha permissão de escrita):
```
git clone https://github.com/maromarcioaray/api-crud-js.git 
```
3. Mude para dentro da pasta criada `fbd`:
```
cd fbd
```
4. Nessa pasta digite o comando abaixo (vai instalar os pacotes listados nas dependências):
```
npm install


serão instalados os seguintes módulos:


dotenv
express
knex 
mysql2
nodemon 

```
5. Crie uma cópia do arquivo `.env-modelo` com o nome `.env` (observe que o ponto `.` faz parte do nome do arquivo). 

6. Edite o conteúdo do arquivo `.env` para que fique com os valores adequados ao seu ambiente. 
```
# conexão com banco de dados
# Endereço do host (computador) onde o MySQL está rodando
DB_HOST=localhost
# porta que o MySQL está usando. Na Faculdade Senac pode ser 3307 - verifique na configuração de conexão do Workbench ou painel de controle do XAMPP
DB_PORT=3306
# usuário para acesso ao banco de dados
DB_USER=root
# senha do usuário para acesso ao banco de dados
DB_PASSWORD=sua_senha
# database ou schema (no MySQL são sinônimos)
DB_NAME=nome_do_banco # neste exemplo será lpw
# porta utilizada pelo Express para subir um servidor web simples
PORT=3000
```
  
## 3. Criar a base de dados  

 Importar o arquivo com a definição do schema lpw e tabela clientes.
1. No MySQL, execute os comandos que estão no arquivo `bancoBoizinho.sql` que está na pasta `bancoDados`. Nesse arquivo estão incluídos os comandos para criar o database `boizinho` e  a tabela `animais`.
  

## 4. Iniciando a aplicação
  
Para iniciar a aplicação digite:
```
npm run dev
```

Deve aparecer a mensagem: 
```
> api-crud@1.0.0 dev
> nodemon src/server.js

[nodemon] 3.1.10
[nodemon] to restart at any time, enter `rs`
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js,mjs,cjs,json
[nodemon] starting `node src/server.js`
Servidor rodando na porta 3000
```
> nodemon serve para que a aplicação seja recarregada automaticamente caso algum arquivo seja editado e salvo. Caso contrário seria necessário parar a aplicação (CTRL-C) e iniciá-la novamente depois de salvar as alterações.

Para acessar o frontend da aplicação, abra o navegador e digite:

http://localhost:3000/

