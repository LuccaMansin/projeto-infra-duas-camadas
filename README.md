# projeto-infra-duas-camadas

# Infraestrutura Web Segura de Duas Camadas na AWS

Este projeto demonstra a criação e configuração de uma infraestrutura em nuvem resiliente e segura utilizando a AWS, separando a camada de aplicação da camada de dados.

## Arquitetura do Projeto
- VPC Personalizada: Criada do zero com sub-redes públicas e privadas distribuídas em múltiplas zonas de disponibilidade.
- Camada Computacional (Amazon EC2): Um servidor Linux hospedado em sub-rede pública executando uma aplicação backend em Python (Flask).
- Camada de Dados (Amazon RDS): Um banco de dados relacional MySQL totalmente isolado em sub-rede privada, sem acesso direto à internet.
- Segurança (Security Groups): Configuração de firewalls onde o banco de dados aceita tráfego exclusivamente vindo do grupo de segurança do servidor web (Porta 3306).

## Tecnologias Utilizadas
- Cloud: AWS (VPC, EC2, RDS, Security Groups)
- Linguagem: Python 3 (Framework Flask)
- Banco de Dados: SQL (MySQL)
- Sistema Operacional: Linux (Amazon Linux)

## Como testar a infraestrutura
1. O servidor Flask foi inicializado na porta 80 da instância EC2.
2. A comunicação foi validada acessando o IP público da EC2 via navegador, retornando a mensagem de sucesso na conexão com o banco de dados privado.
