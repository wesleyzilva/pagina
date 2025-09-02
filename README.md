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
    *   Esta API será responsável por toda a lógica de negócio, como a gestão dos dados de projetos e habilidades.

4.  **Banco de Dados (PostgreSQL):**
    *   O **PostgreSQL** será o repositório de dados, armazenando de forma persistente as informações do portfólio.

---

## 🗺️ Plano de Sprints (Ciclo Ágil)

O desenvolvimento será guiado por um ciclo de sprints, focando em entregas incrementais de valor, qualidade de código e automação.

### **Sprint 1: Fundação e Estrutura do Projeto**
- **Objetivo:** Definir a arquitetura base e configurar o ambiente de desenvolvimento com foco em boas práticas e automação inicial.
- **Tarefas:**
    - [ ] Definir a estrutura do monorepo (`frontend`, `backend/facade`, `backend/business`).
    - [ ] Inicializar o projeto **Angular** com linter (ESLint) e formatação (Prettier).
    - [ ] Inicializar os projetos **backend** (ex: Spring Boot) com dependências para web, dados e segurança.
    - [ ] Configurar o pipeline de **CI (Continuous Integration)** inicial com um job de build para validar a estrutura.
    - [ ] Criar o primeiro componente Angular com seu **teste unitário** (Jasmine/Karma).

### **Sprint 2: Backend, Persistência e TDD**
- **Objetivo:** Desenvolver a camada de API e a conexão com o banco de dados, aplicando TDD (Test-Driven Development).
- **Tarefas:**
    - [ ] Modelar o domínio inicial no **PostgreSQL** (ex: tabela `projects`).
    - [ ] Implementar a camada de persistência (Repository) com **testes de integração** (usando H2 ou Testcontainers).
    - [ ] Criar a primeira API na camada `Business` (ex: `GET /api/projects`) com **testes unitários** para Service e Controller.
    - [ ] Adicionar a execução de testes do backend no pipeline de CI.

### **Sprint 3: Integração Frontend-Backend e Componentização**
- **Objetivo:** Conectar o frontend à API e refatorar a UI estática em componentes dinâmicos e testáveis.
- **Tarefas:**
    - [ ] Criar um serviço em Angular (`ProjectService`) para consumir a API.
    - [ ] Refatorar a seção de projetos para usar componentes dinâmicos (ex: `ProjectCardComponent`).
    - [ ] Escrever **testes unitários** para o `ProjectService` (com `HttpClientTestingModule`) e para os componentes.
    - [ ] Configurar o proxy de desenvolvimento do Angular para evitar problemas de CORS localmente.

### **Sprint 4: Automação de Testes E2E e Qualidade de Código**
- **Objetivo:** Aumentar a confiança no código através de automação de testes de ponta a ponta e análise estática.
- **Tarefas:**
    - [ ] Configurar um framework de **testes E2E (End-to-End)**, como Cypress ou Playwright.
    - [ ] Escrever o primeiro teste E2E: "visitar a página e verificar se a lista de projetos é carregada".
    - [ ] Integrar a execução dos testes E2E no pipeline de CI.
    - [ ] Documentar a API usando **Swagger/OpenAPI** no backend.

### **Sprint 5: Deploy Contínuo e Monitoramento**
- **Objetivo:** Automatizar o processo de deploy e preparar a aplicação para o ambiente de produção.
- **Tarefas:**
    - [ ] Criar um workflow de **CD (Continuous Deployment)** para publicar o frontend no GitHub Pages.
    - [ ] "Dockerizar" as aplicações backend.
    - [ ] (Opcional) Configurar o deploy do backend em uma plataforma de nuvem via pipeline de CD.
    - [ ] Adicionar **health checks** (`/actuator/health`) nas APIs de backend.