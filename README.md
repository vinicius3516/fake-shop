# Fake Shop

Este projeto trata-se de um ecommerce de produtos eletrônicos, desenvolvido com o objetivo de aplicar os conhecimentos adquiridos durante a Imersão DevOps e Cloud com Fabrício Veronez.

Instruções de Uso

O projeto está finalizado e pronto para execução, sendo necessário seguir os seguintes passos:

## 1. Fork do Projeto

Faça um fork deste repositório para sua conta do GitHub, e no arquivo .yaml dentro de .github/workflows, atualize o nome de usuario da imagem docker.

"seu-user-dockerhub"/fake-shop:v${{ github.run_number }}

## 2. Criar Cluster Kubernetes

Acesse a DigitalOcean e crie um novo cluster Kubernetes.

## 3. Obter Configuração do Kubernetes

Na DigitalOcean, faça o download do arquivo config relacionado ao cluster Kubernetes recém-criado.

Copie o conteúdo deste arquivo.

## 4. Configurar Kubectl

Certifique-se de que o kubectl já esteja instalado.

Abra o terminal e execute o seguinte comando para abrir o arquivo de configuração do Kubernetes:

code ~/.kube/config

Substitua o conteúdo deste arquivo com o conteúdo copiado da DigitalOcean e salve o arquivo.

## 5. Criar Secrets no GitHub

No GitHub, acesse Settings > Secrets and variables > Actions e crie os seguintes secrets:

DOCKERHUB_USERNAME (nome de usuário DockerHub)

DOCKERHUB_TOKEN (senha ou token de acesso ao DockerHub)

K8S_KUBECONFIG (conteúdo do arquivo config obtido anteriormente)

## 6. Executar Pipeline

Realize qualquer alteração (por exemplo, atualização do README) e gere um novo commit no repositório.

Após o commit, a pipeline será acionada automaticamente.

## 7. Acessar Aplicação

Após a execução da pipeline, verifique o IP externo do serviço da aplicação usando:

kubectl get svc

Copie o endereço em EXTERNAL-IP e acesse a aplicação pelo navegador usando:

http://<EXTERNAL-IP>

A aplicação estará funcionando normalmente.

## Variável de Ambiente
DB_HOST	=> Host do banco de dados PostgreSQL.

DB_USER => Nome do usuário do banco de dados PostgreSQL.

DB_PASSWORD	=> Senha do usuário do banco de dados PostgreSQL.

DB_NAME	=>	Nome do banco de dados PostgreSQL.

DB_PORT	=>	Porta de conexão com o banco de dados PostgreSQL.
