╔══════════════════════════════════════════════════════╗
║          CI/CD DE TESTES COM JENKINS E DOCKER         ║
╚══════════════════════════════════════════════════════╝

Projeto de estudo de integração contínua de testes Cypress usando Jenkins, Docker e arquivos de configuração versionados.

══════════════════════════════════════════════════════

## Sobre o projeto

O repositório explora a estrutura de um pipeline como código, a instalação de dependências e a execução automatizada de testes, além de arquivos de apoio às atividades com Docker.

══════════════════════════════════════════════════════

## Objetivos

- Conhecer a estrutura de um pipeline como código.
- Automatizar a instalação de dependências e a execução dos testes.
- Praticar execução reproduzível e análise de resultados.
- Explorar arquivos de apoio à containerização.

══════════════════════════════════════════════════════

## Tecnologias e ferramentas

- Jenkins
- Docker
- Cypress
- Node.js e npm
- Allure

══════════════════════════════════════════════════════

## Pré-requisitos

- Jenkins configurado com acesso ao repositório.
- Agente Windows para executar o `Jenkinsfile` atual, pois utiliza comandos `bat`.
- Node.js e npm disponíveis no agente e ferramenta Jenkins NodeJS configurada como `nodejs`.
- Docker instalado para as atividades de containerização descritas nos arquivos do projeto.

══════════════════════════════════════════════════════

## Como executar pelo Jenkins

1. Configure um job do tipo **Pipeline** apontando para este repositório.
2. Confirme que o agente é Windows ou adapte os comandos do Jenkinsfile ao sistema operacional utilizado.
3. Execute o job e verifique o console output para acompanhar `npm install` e `npm test`.
4. O comando `npm test` executa `npx cypress run --browser chrome`; confirme que o Chrome e as dependências necessárias estão disponíveis no agente.

══════════════════════════════════════════════════════

## Execução local

Na raiz do projeto, com Node.js e npm instalados:

```bash
npm install
npm test
```

Para gerar ou abrir relatórios Allure, consulte os scripts em `package.json` e confirme que existem resultados em `allure-results`.

══════════════════════════════════════════════════════

## Arquivos principais

- `Jenkinsfile`: pipeline para agente Windows.
- `Dockerfile` e `docker-comandos.txt`: arquivos de apoio às atividades com Docker.
- `cypress.config.js` e `cypress/`: configuração e testes Cypress.
- `logs-cypress/` e `allure-results/`: diretórios de logs e resultados presentes no repositório.

══════════════════════════════════════════════════════

## Desafios práticos

- Integrar dependências e execução automatizada.
- Configurar o agente de acordo com o sistema operacional.
- Analisar logs quando uma etapa do pipeline falha.

══════════════════════════════════════════════════════

## Boas práticas

- Versionar o pipeline junto ao código.
- Manter a configuração de ambiente documentada.
- Armazenar logs e resultados para apoiar a análise.
- Verificar se os artefatos correspondem à execução mais recente antes de utilizá-los como evidência.

══════════════════════════════════════════════════════

## Aprendizados

A atividade permite praticar conceitos de CI/CD, execução automatizada de testes e configuração de pipeline, além de compreender como logs e artefatos ajudam a diagnosticar falhas.

══════════════════════════════════════════════════════

## Considerações finais

A configuração do Jenkinsfile deve corresponder ao sistema operacional do agente. Antes de executar o fluxo com Docker, confira os comandos e os requisitos definidos nos arquivos do projeto.

══════════════════════════════════════════════════════

## Formação e natureza da atividade

Este projeto foi desenvolvido como uma **atividade facultativa** no contexto dos estudos de Quality Assurance (QA), durante a formação da EBAC — Escola Britânica de Artes Criativas e Tecnologia. Seu objetivo é praticar e consolidar conhecimentos de CI/CD, testes automatizados e Docker.

══════════════════════════════════════════════════════