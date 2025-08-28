# Plataforma-de-Analise-de-Dados-de-Saude-Fitness
Possivel TCC Parte 1


# 
## Passo 1: Instalação das Ferramentas
Você vai precisar de 5 ferramentas. Para cada uma, basta ir no site oficial e seguir as instruções.

## Editor de código:

Onde: Visual Studio Code, Sublime Text ou Atom.

O que fazer: Baixe e instale. O VS Code é o mais recomendado, por ter muitas extensões úteis.

## Python:

Onde: Site oficial do Python.

O que fazer: Baixe e instale a versão mais recente (3.9 ou superior). Não se esqueça de marcar a opção "Add Python to PATH" durante a instalação.

## AWS CLI:

Onde: Página de instalação da AWS CLI.

O que fazer: Siga o passo a passo para o seu sistema operacional (Windows, macOS ou Linux). Depois de instalar, abra o terminal e digite aws --version para confirmar.

## AWS SAM CLI:

Onde: Página de instalação da AWS SAM CLI.

O que fazer: Siga as instruções. É uma instalação bem simples, geralmente via pip (o gerenciador de pacotes do Python). Digite sam --version no terminal para verificar.

## Node.js:

Onde: Site oficial do Node.js.

## O que fazer: Baixe e instale a versão LTS. Isso já inclui o npm (gerenciador de pacotes), que é útil para o frontend.

Passo 2: Criando e Configurando o Backend (no seu PC)
Abra o terminal ou prompt de comando.

Crie a pasta do projeto: Digite sam init e siga as opções:

Escolha AWS Quick Start Templates.

Escolha zip.

Escolha python3.9.

Nomeie o projeto como tcc-fitness.

## Inicie o banco de dados DynamoDB no seu PC:

Onde: Página de download do DynamoDB Local.

O que fazer: Baixe o arquivo ZIP, extraia a pasta e abra o terminal dentro dela. Digite o comando:

Bash:

<code>java -jar DynamoDBLocal.jar -sharedDb
Deixe este terminal aberto. Ele vai rodar o banco de dados.</code>

## Escreva o código da sua API:

Onde: Na pasta tcc-fitness/hello_world/app.py que o sam init criou.

O que fazer: Você vai apagar o código de exemplo e escrever sua lógica em Python para:

## Conectar com o DynamoDB Local.

Receber dados (como peso, treinos, etc.) em JSON.

Salvar esses dados na tabela do banco.

Ter uma lógica de análise que processa os dados (a "mineração") e devolve uma resposta.

Passo 3: Criando e Testando o Frontend (no seu PC)
Crie a pasta do Frontend: Crie uma nova pasta chamada frontend ao lado da pasta tcc-fitness.

Crie os arquivos: Dentro da pasta frontend, crie três arquivos de texto: index.html, style.css e script.js.

## Escreva o código:

index.html: Onde você vai colocar os botões e formulários.

style.css: Onde você vai fazer o design.

script.js: O código mais importante. Ele vai se comunicar com sua API local. Para fazer isso, use fetch() para enviar e receber dados, direcionando as requisições para a URL do seu backend local:

## JavaScript

const urlBackend = 'http://127.0.0.1:3000/sua-rota-aqui';
// Código para enviar ou receber dados da API
Passo 4: Testando tudo junto no seu PC
Inicie o Backend: Abra um novo terminal (diferente do que está rodando o DynamoDB) e entre na pasta tcc-fitness. Digite o comando:

Bash:

<code>sam local start-api</code>

Deixe este terminal aberto. Ele vai simular o API Gateway e o Lambda.

## Abra o Frontend:

Onde: Onde você salvou o arquivo index.html.

O que fazer: Clique duas vezes no index.html para abri-lo no seu navegador.

### Pronto! Agora, quando você interagir com a página, o JavaScript vai enviar os dados para sua API local, que vai processar tudo e salvar no DynamoDB que também está no seu PC. Você pode ver o resultado da "mineração" na própria página.

Você tem um ambiente de desenvolvimento completo e gratuito no seu próprio computador para desenvolver e testar o seu TCC. Quando estiver pronto, basta usar um comando do AWS SAM para enviar tudo para a nuvem.
