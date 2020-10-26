# AKS Bootcamp - Aplicação de exemplo

> Esta é a aplicação de exemplo para o [AKS Bootcamp](https://channel9.msdn.com/Series/AKS-Bootcamp-From-zero-to-container-hero?WT.mc_id=containers-9948-ludossan)

## Funcionalidades

Este projeto é uma aplicação simples de controle de portos e navios. Consiste em uma parte front-end e outra back-end

## Começar

### Pré Requisitos

- Node.js versão 8 para o front-end
- Node.js versão 12 ou superior para o back-end
- Docker e Docker Compose
- MongoDB

### Instalação e Início rápido

#### Rodando com Docker

Só digite `docker-compose up` na raiz do projeto e a aplicação deverá ser executada.

#### Executando em modo stand alone

A aplicação é dividida em dois diretórios principais: `frontend` e` backend` cada um com seus respectivos códigos e arquivos de infraestrutura.

__Front End__: Criado usando Vue. Basta ir ao diretório, digitar `npm install` para instalar todas as dependências e então` npm run serve`. Você também pode construir a imagem do Dockerfile no mesmo diretório

__Front End__: Criado com TypeScript. Apenas vá para o diretório, digite `npm install` para instalar todas as dependências e então `npm run build: start` para executar o aplicativo ou `npm run start:debug` para iniciar no modo de depuração. Você também pode construir a imagem do Dockerfile no mesmo diretório

#### Kubernetes

Você pode executar todos os arquivos Kubernetes no diretório [kubernetes](./kubernetes) usando kubectl para criar os workloads em um cluster Kubernetes. Você também pode usar o [Helm](https://helm.sh) para executar os charts no diretório [charts](./charts).

### MongoDB

Este aplicativo precisa de um banco de dados MongoDB para funcionar. Você pode criar ou hospedar qualquer banco de dados e conectar com a string de conexão.

Use os arquivos `values.yml` presentes em ambos os charts no diretório de `charts` para descobrir as variáveis que precisam ser substituídas. Se você estiver usando os arquivos de manifesto do Kubernetes, substitua a string de conexão apenas no __backend__.

### Variáveis de ambiente

O backend precisa de variáveis de ambiente para ser executado

- DATABASE_MONGODB_URI: URI do banco de dados
- DATABASE_MONGODB_DBNAME: Nome do banco de dados
