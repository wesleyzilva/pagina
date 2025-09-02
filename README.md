# Plano de Evolução

Este documento descreve a visão e a arquitetura planejada para a evolução do portfólio, transformando-o de uma página web estática para um ecossistema de aplicações completo e moderno, focado em práticas de desenvolvimento robustas e escaláveis.

## 🚀 Visão do Projeto

O objetivo é refatorar o portfólio atual para uma arquitetura full-stack, aplicando conceitos de desenvolvimento modular e de microserviços. Esta transição servirá como um projeto prático para demonstrar proficiência em tecnologias e metodologias de ponta, incluindo a criação de um contador de acessos flutuante para mostrar resultados em tempo real no github pessoal.

Repositorio: https://github.com/wesleyzilva/pagina

Produto: https://wesleyzilva.github.io/pagina/


---

## 🛠️ Arquitetura Proposta (Evolução)

A nova arquitetura será composta por três camadas principais que se comunicam de forma fluida para garantir a modularidade e a manutenibilidade do código.

1.  **Frontend (Angular):**
    * **Tecnologia:** A interface do usuário será desenvolvida com **Angular**, aproveitando sua estrutura de componentes e módulos para criar uma aplicação escalável e responsiva. O objetivo é transformar a experiência do usuário em uma Single-Page Application (SPA).

2.  **API Facade (Camada Intermediária):**
    * **Tecnologia:** Uma API de fachada será implementada para servir como a única porta de entrada para o frontend. Esta camada simplificará as chamadas ao backend, orquestrando as requisições e garantindo a segurança.

3.  **API Business (Backend):**
    * **Tecnologia:** Esta será a API principal, responsável por toda a lógica de negócio, como a gestão dos dados dos projetos e habilidades. Ela será a fonte da verdade para as informações do portfólio.

4.  **Banco de Dados (PostgreSQL):**
    * **Tecnologia:** O banco de dados **PostgreSQL** será o repositório de dados persistente, armazenando informações como projetos, experiências, habilidades e dados para o contador de acessos.

---

## 📈 Nova Funcionalidade: Contador de Acessos Flutuante

Uma nova funcionalidade será implementada para demonstrar a interação entre o frontend e o backend: um **contador de acessos flutuante**.

* **Como funcionará:** Toda vez que a página do portfólio for acessada, o frontend fará uma chamada à API de negócios. Esta API, por sua vez, incrementará o valor de um contador no banco de dados e retornará o número total de acessos. O frontend exibirá este valor em um componente flutuante na tela, dando uma visão em tempo real da popularidade do site.

---

## 🗺️ Próximos Passos

1.  **Configuração do Ambiente:** Criar a estrutura de pastas do projeto (por exemplo, `frontend/`, `backend/`).
2.  **Início do Frontend:** Inicializar um novo projeto Angular dentro da pasta `frontend/`.
3.  **Desenvolvimento do Backend:** Criar a API de negócios e a API de fachada.
4.  **Configuração do Banco de Dados:** Criar a base de dados PostgreSQL e as tabelas necessárias para armazenar os dados do portfólio e o contador de acessos.
5.  **Implementação da Funcionalidade:** Construir o endpoint para o contador de acessos na API e o componente no Angular para exibi-lo.

Este README servirá como um guia para a jornada de desenvolvimento, garantindo que o projeto mantenha o foco e a coesão arquitetônica.
```eof

Este documento pode ser o ponto de partida ideal para o seu projeto, servindo como uma visão clara do que precisa ser construído e por que, além de ser um excelente item para o seu portfólio. Se precisar de ajuda com os próximos passos, é só me dizer!