# Plano de Evolução do Portfólio

Este documento descreve a visão, a arquitetura e o plano de execução para evoluir este portfólio de uma página web estática para um ecossistema de aplicações moderno, demonstrando práticas de desenvolvimento full-stack.

## 🚀 Visão do Projeto

O objetivo é refatorar o portfólio atual para uma arquitetura completa, aplicando conceitos de desenvolvimento modular e comunicação via APIs. Esta transição servirá como um projeto prático para demonstrar proficiência em tecnologias e metodologias de ponta.

- **Repositório:** https://github.com/wesleyzilva/pagina
- **Produto Final:** https://wesleyzilva.github.io/pagina/

---

## 🛠️ Arquitetura Proposta

A nova arquitetura será composta por camadas distintas que se comunicam para garantir modularidade, escalabilidade e manutenibilidade.

1.  **Frontend (Angular):**
    *   A interface do usuário será uma **Single-Page Application (SPA)** desenvolvida com Angular, aproveitando sua estrutura de componentes para criar uma experiência de usuário rica e interativa.

2.  **API Facade (Camada Intermediária):**
    *   Uma API de fachada servirá como a única porta de entrada para o frontend. Ela irá orquestrar requisições, simplificar a comunicação com o backend e centralizar a segurança.

3.  **API Business (Backend):**
    *   Esta API será responsável por toda a lógica de negócio, como a gestão dos dados de projetos, habilidades e o processamento do contador de acessos.

4.  **Banco de Dados (PostgreSQL):**
    *   O **PostgreSQL** será o repositório de dados, armazenando de forma persistente as informações do portfólio.

---

## 📈 Funcionalidade Chave: Contador de Acessos

Para demonstrar a interação ponta a ponta, a primeira funcionalidade a ser implementada será um **contador de acessos em tempo real**.

*   **Como funcionará:** Ao carregar a página, o frontend fará uma chamada à API, que incrementará o valor do contador no banco de dados e retornará o total de acessos. O frontend exibirá este valor em um componente na tela.

---

## 🗺️ Plano de Sprints (Execução em 5 dias)

O desenvolvimento inicial será dividido em 5 dias de trabalho focado.

### **Sprint 1 (Dia 1): Planejamento e Configuração do Ambiente**
- **Objetivo:** Estruturar o projeto e preparar o ambiente de desenvolvimento.
- **Tarefas:**
    - [x] Detalhar o plano de sprints.
    - [ ] Criar a estrutura de pastas do projeto (`frontend/`, `backend/`).
    - [ ] Configurar os repositórios no Git.
    - [ ] Inicializar um novo projeto Angular.
    - [ ] Definir a estrutura base do projeto backend (API Facade e Business).

### **Sprint 2 (Dia 2): Backend - API e Banco de Dados**
- **Objetivo:** Construir a base da API e a persistência de dados.
- **Tarefas:**
    - [ ] Modelar e criar as tabelas no PostgreSQL (ex: `access_counter`).
    - [ ] Configurar a conexão do backend com o banco de dados.
    - [ ] Desenvolver o endpoint para o contador de acessos (`POST /visits`).
    - [ ] Implementar a lógica para incrementar e retornar o número de visitas.

### **Sprint 3 (Dia 3): Frontend - Integração do Contador**
- **Objetivo:** Conectar o frontend com a API para exibir o contador.
- **Tarefas:**
    - [ ] Criar um serviço em Angular (`CounterService`) para se comunicar com a API.
    - [ ] Implementar a chamada à API no carregamento da página.
    - [ ] Criar um componente visual para exibir o número de acessos.
    - [ ] Estilizar o componente do contador.

### **Sprint 4 (Dia 4): Refatoração e Integração Contínua**
- **Objetivo:** Melhorar a estrutura do código e automatizar o deploy.
- **Tarefas:**
    - [ ] Refatorar o HTML estático para componentes Angular reutilizáveis (ex: `ProjectCardComponent`).
    - [ ] Garantir que a integração Frontend <-> Backend está robusta (tratamento de erros, CORS).
    - [ ] Configurar um pipeline de CI/CD básico (GitHub Actions) para o build do frontend.

### **Sprint 5 (Dia 5): Deploy e Finalização**
- **Objetivo:** Publicar a primeira versão funcional e documentar o processo.
- **Tarefas:**
    - [ ] Realizar o deploy da nova versão do frontend no GitHub Pages.
    - [ ] (Opcional) Realizar o deploy do backend em uma plataforma (ex: Heroku, Vercel).
    - [ ] Testar a funcionalidade em produção.
    - [ ] Atualizar o `README.md` com o status final da sprint e lições aprendidas.