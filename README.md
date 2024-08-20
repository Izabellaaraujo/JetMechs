# JetMechs

# Sistema de Agendamento Online para Mecânica e Lava Rápido

## 1. Visão Geral
O projeto consiste em um desenvolvimento de um sistema de agendamento online para a empresa Jet Mechs, que oferece serviços de mecânica e lava rápido. 

### 1.1 Aplicativo/site e suas funcionalidades:
O aplicativo desenvolvido é um sistema de agendamento online para a empresa Jet Mechs, que oferece serviços de mecânica e lava rápido. Cliente realiza o cadastro e 
consegue agendar o serviço desejado, a empresa Jet Mechs, com login, consegue visualizar todos os agendamentos e histórico dos clientes atendidos.

### 1.2 Funcionalidades para Clientes: 
- **Cadastro de Clientes:** Os clientes podem se cadastrar no sistema fornecendo 
informações como nome, CPF, telefone e e-mail. 
- **Agendamento de Serviço Online:** Os clientes podem agendar serviços através 
do site, inserindo detalhes como nome, tipo de serviço, informações do veículo 
(modelo e placa), data e horário desejados para o agendamento.

### 1.3 Funcionalidades para a Empresa: 
- **Controle de Agendamentos de Serviço:** A empresa pode visualizar todos os 
agendamentos feitos pelos clientes, contendo informações como nome do 
cliente, serviço a ser prestado, detalhes do veículo, data e hora do agendamento. 
- **Histórico de Clientes Atendidos:** A empresa pode acessar um histórico dos 
clientes atendidos, com informações como nome do cliente, data e hora do 
serviço realizado, detalhes do veículo, data e hora do serviço finalizado. 

### 1.4 Funcionalidades de Autenticação: 
- **Login da Empresa:** A empresa precisa de um login para acessar as informações 
dos clientes atendidos, agendamentos e serviços fornecidos. Esse login deve ser 
feito utilizando o e-mail da empresa e uma senha. 
Nossa aplicação foi desenvolvida para proporcionar uma experiência intuitiva e eficiente 
no agendamento de serviços de mecânica e lava rápido. Com uma interface amigável, 
os clientes podem facilmente agendar serviços e a empresa acompanhar seu histórico 
de serviços agendados e realizados.

## 2. Requisitos 
Os requisitos do sistema incluem cadastro de clientes, agendamento de serviços online, 
controle de agendamentos e histórico de clientes atendidos. Além disso, há a 
necessidade de autenticação para a empresa. 

### 2.1 Requisito 1
- **Empresa: Jet Mechs.**: Uma empresa que fornece serviço de mecânica e lava rápido. O cliente possui acesso ao 
site para realizar o agendamento online. O mesmo efetua um cadastro com seus dados e acessa o portal para agendar o serviço escolhido.
A empresa possui a opção para visualizar todos os agendamentos e histórico do mês.  

### 2.2 Requisito  2
- **Cadastramento**: O cliente tem a necessidade de efetuar os seguintes cadastros: 
Cadastramento de clientes deve conter os seguintes campos: Nome, CPF, telefone e e
mail.  
Agendamento de serviço online deve conter os seguintes campos: Nome do cliente, tipo 
de serviço, dados do veículo como: modelo e placa, data e horário do agendamento. 

### 2.3 Requisito  3
- **Controle**: A empresa necessita dos seguintes controles: 
Agendamento de serviço deve conter os seguintes campos: Nome do cliente, serviço a 
ser prestado, dados do veículo, data e hora do agendamento e previsão de entrega do 
veículo.  
Histórico de clientes atendidos com os seguintes campos: Nome do cliente, data e hora, 
serviço realizado, dados de veículo, data e hora do serviço finalizado, data da entrega do 
veículo e avaliação do cliente. 

### 2.4 Requisito 4
- **Login**: A empresa possui a necessidade de criar um login no site para visualizar os clientes 
atendidos e agendados e serviços fornecidos. Para isso deve conter: E-mail e senha.  

## 3. Visão Geral do Sistema de Agendamento Online: Funcionalidades e Autenticação 
O código foi desenvolvido em Python usando a framework Flask para criar a aplicação 
web. A aplicação consiste em um sistema de agendamento online, incluindo rotas para 
cadastro de clientes, visualização de agendamentos, editar, excluir e autenticar o 
usuário empresa.  
O Flask gerencia rotas e requisições HTTP e o SQLAlchemy facilita a interação com o 
banco de dados MySQL. Utilizamos Flask para definir rotas correspondentes a 
diferentes funcionalidades, como cadastro de clientes, listagem de agendamentos e 
autenticação de usuários. A autenticação ocorre comparando credenciais com um 
conjunto pré-definido de administradores. E as mensagens flash são usadas para 
fornecer feedback ao usuário.

## 4. Banco de dados:

A tabela criada no projeto, armazena as informações sobre os clientes, com 
detalhes sobre os veículos e serviços agendados. Os campos importantes precisam 
sempre ser preenchidos, como: nome do cliente e CPF.  
A chave primária é o "id_cliente", que é incrementado automaticamente para garantir a 
unicidade de cada registro:

CREATE table clientes ( 
id_cliente INT PRIMARY KEY AUTO_INCREMENT, 
nome_cliente VARCHAR(100) NOT NULL, 
cpf_cliente VARCHAR(11) NOT NULL UNIQUE, 
telefone_cliente VARCHAR(15), 
email_cliente VARCHAR(100), 
veiculo_cliente VARCHAR(50), 
modelo_veiculo VARCHAR(50), 
placa_veiculo VARCHAR(50), 
t
 ipo_servico VARCHAR(50), 
data_agendamento VARCHAR(50), 
hora_agendamento VARCHAR(50) 
); 

