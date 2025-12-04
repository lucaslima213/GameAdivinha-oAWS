# Jogo de Adivinhação Serverless AWS

## Descrição do Projeto

Este projeto consiste em um jogo de adivinhação desenvolvido com arquitetura serverless na AWS. O objetivo é integrar múltiplos serviços da AWS para criar uma aplicação interativa, onde o usuário tenta adivinhar um número entre 1 e 10. Toda a lógica do jogo é processada por uma função Lambda, exposta via API Gateway, e o frontend é hospedado de forma estática no Amazon S3.

## O que foi construído

- **Função Lambda em Python:** Implementa a lógica do jogo de adivinhação, recebendo o número do usuário e retornando se acertou ou não.
- **API RESTful:** API Gateway configurado para expor a função Lambda e permitir chamadas GET do frontend.
- **Frontend Web Estático:** Página HTML hospedada no Amazon S3, permitindo interação do usuário com o jogo.
- **Integração entre serviços:** O frontend faz requisições à API Gateway, que aciona a função Lambda e retorna o resultado ao usuário.
- **Configuração de CORS:** Permite que o site hospedado no S3 se comunique com a API sem bloqueios de navegador.
- **Permissões e Políticas:** Configuração de políticas de acesso público ao bucket S3 para garantir que o site seja acessível.

## Serviços AWS Utilizados

- **AWS Lambda:** Execução da lógica do jogo de adivinhação em Python.
- **Amazon API Gateway:** Exposição da função Lambda via endpoint HTTP.
- **Amazon S3:** Hospedagem do site estático (index.html).
- **AWS IAM:** Gerenciamento de permissões e políticas de acesso ao bucket S3.

## Passos para Conclusão do projeto

1. Criar a função Lambda em Python para a lógica do jogo.
2. Configurar o API Gateway para expor a função Lambda via método GET.
3. Publicar o arquivo index.html no Amazon S3.
4. Integrar o frontend ao endpoint da API Gateway.
5. Configurar permissões e políticas públicas no bucket S3.
6. Validar o funcionamento do site e da API.
