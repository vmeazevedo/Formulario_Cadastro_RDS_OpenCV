# Formulário de Cadastro com database RDS AWS e reconhecimento facial via OpenCV
O algoritmo realiza um cadastro de usuário simples (Nome, CPF, E-mail e Telefone) em uma database RDS da Amazon e também realiza o armazenamento, treinamento e o reconhecimento facial do rosto do usuário para identificar os usuários já cadastrados no sistema em uma próxima vez que o usuário for visto.

# Requirements
Será necessário instalar as bibliotecas abaixo:

- numpy
- OpenCV
- mysql-connector

## Criando instancia RDS-MySQL na AWS
- Acessar o "Console de gerenciamento da AWS"
- Abra o menu de serviços e selecione a opção RDS
- Selecione a opção de "Create database"
- Selecione MySQL
- Version: MySQL 8.0.11
-> Free tier
- Entre com os dados de base, username e password:

db instance: "nome da base de dados"

username: "seu usuário"

password: "sua senha"

- DB instance size e Storage é default não mexer
- VPC: Default
- Subnet group: default
- Public acess: Yes
- VPC security group: Create new

New VPC security group name: <entrar_com_o_nome>

- Availability Zone: escolher onde você ta conectado

# Funcionamento
Ao rodar o código será apresentado no terminal o menu abaixo com as opções de cadastro e identificação:
![image](https://user-images.githubusercontent.com/40063504/103282211-d6674d80-49b3-11eb-8b8c-84fc54b6c73f.png)

Se a opção 1 for selecionada, será apresentado alguns campos para preenchimento do novo cadastro conforme mostrado abaixo:
![image](https://user-images.githubusercontent.com/40063504/103282344-3bbb3e80-49b4-11eb-8720-9faa71b78780.png)

Após realizarmos o preenchimento do novo cadastro em nossa base de dados a tela do reconhecimento fácial será apresentada.
![image](https://user-images.githubusercontent.com/40063504/103282395-673e2900-49b4-11eb-8db4-0c012b900b25.png)

Nessa tela temos a opção de cadastrar uma nova foto de usuário (tecla espaço), realizar o treinamento (letra t), ou sair (letra q). 
Pressionando a tecla 'espaço' do teclado iremos realizar a captura das fotos para realização do treinamento posteriormente.
