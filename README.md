# 🐳 Testes E2E com Cypress, Docker Compose & GitHub Actions

Este repositório faz parte dos meus estudos práticos em **Engenharia de Qualidade de Software**, com foco em automação de testes end-to-end (E2E), conteinerização de ambientes e integração contínua (CI/CD).

## 🚀 Sobre o Projeto
O objetivo principal deste projeto é subir uma aplicação completa (backend e frontend) utilizando **Docker Compose**, executar uma suíte automatizada de testes com **Cypress** de forma isolada dentro de um container, e garantir que todo o processo rode automaticamente a cada alteração no código através do **GitHub Actions**.

## 🛠️ Tecnologias e Ferramentas Utilizadas
* **Testes & Automação:** Cypress, BDD (Cucumber/Gherkin), Interceptação de Requisições (`cy.intercept`)
* **Infraestrutura & Containers:** Docker, Docker Compose
* **CI/CD:** GitHub Actions (Pipelines automatizados)
* **Controle de Versão:** Git & GitHub

## 📂 Estrutura do Projeto
```text
📦 docker-gms-compose-Ale
 ┣ 📂 .github
 ┃ ┗ 📂 workflows
 ┃   ┗ 📜 docker-tests.yml   # Pipeline de CI/CD do GitHub Actions
 ┣ 📂 golden-movie-studio-backend   # Serviço de Backend
 ┣ 📂 golden-movie-studio-frontend  # Serviço de Frontend
 ┣ 📂 tests                         # Suíte de testes Cypress
 ┣ 📜 docker-compose.yml            # Orquestração dos containers
 ┗ 📜 README.md

 ⚙️ Como Executar o Projeto Localmente
Certifique-se de ter o Docker e o Docker Compose instalados na sua máquina.

Clone este repositório:

Bash

git clone [https://github.com/AlexandreLuan/docker-gms-compose-Ale.git](https://github.com/AlexandreLuan/docker-gms-compose-Ale.git)

Entre na pasta do projeto:

Bash

cd docker-gms-compose-Ale

Suba os containers e execute os testes:

Bash

docker compose up --build

🤖 Pipeline de CI/CD (GitHub Actions)

O pipeline configurado no GitHub Actions executa automaticamente os seguintes passos a cada push na branch main:

Faz o checkout do código.

Sobe os serviços de backend e frontend via Docker Compose.

Aguarda a estabilização dos serviços.

Executa a suíte de testes do Cypress isoladamente em container.

Salva automaticamente as evidências (vídeos e capturas de tela) em caso de falhas.

✍️ Desenvolvido por Alexandre Luan — Em transição de carreira para a Engenharia de Qualidade de Software (QA).


Basta colar no arquivo, salvar e rodar o `git add`, `git commit` e `git push` no terminal!