# Documentação de Deploy do Projeto

## Objetivo

O objetivo desta atividade é desenvolver um projeto em Java, documentar o processo de deploy no Azure e apoiar o colega designado no processo de deploy. Isso promove a colaboração e o aprendizado técnico por meio da troca de conhecimentos.

## Introdução

Esta documentação fornece um guia detalhado para o deploy do projeto no Azure. O projeto foi desenvolvido em Java (usando o Spring Framework) e está configurado para utilizar um banco de dados Oracle hospedado na Oracle FIAP.

## Requisitos de Desenvolvimento

* **Linguagem de Programação** : Java
* **Banco de Dados** : Banco de Dados Oracle no Azure ou Oracle FIAP
* **Hospedagem** : Azure Web App

## Configuração de Deploy

### Passo 1: Configurar o Banco de Dados

1. **Configuração da Conexão com o Banco de Dados** :

* Edite o arquivo `application.yml` para corresponder às credenciais específicas do banco de dados.
* Substitua os espaços reservados por sua credencial:
  ```yaml
  1
  2
  3
  4
  5
  6
  7
  8
  9
  10
  spring:
    datasource:
      url: jdbc:oracle:thin:@oracle.fiap.com.br:1521:ORCL
      username: RM_USERNAME
      password: ORACLE_SENHA
    jpa:
      hibernate:
        ddl-auto: create  # ou 'none', conforme as necessidades de configuração
  open-in-view: false
  show-sql: true
  ```
* Oriente seu colega a substituir `SEU_COLEGA_USERNAME` e `SEU_COLEGA_SENHA` pelo nome de usuário e senha do banco de dados dele.

### Passo 2: Configurar o Azure Web App

1. **Criar um Web App** :

* Acesse sua conta do Azure.
* Navegue até "App Services" e selecione "Create".
* Siga as instruções para configurar o novo Web App, garantindo a compatibilidade com aplicações Java.

1. **Realizar o Deploy da Aplicação** :

* Utilize ferramentas do Azure como Azure DevOps ou o deploy direto do App Service para implantar seu projeto Java.
* Verifique se todas as dependências estão configuradas e se a configuração do servidor está correta.

1. **Configurar Permissões e Autenticação** :

* Configure as permissões necessárias de Identity and Access Management (IAM) para seu Web App.
* Certifique-se de que o banco de dados permite conexões de entrada do seu Web App.

![index.png](documentacao/index.png)
