# ClientFlow — Fase 1: Engenharia de Software e Definição do MVP

## Objetivo

Transformar a ideia inicial do ClientFlow em uma definição clara do produto antes de começar sua implementação.

## Problema

As informações dos clientes são mantidas em planilhas, tornando a consulta e visualização pouco eficientes e aumentando o tempo necessário para os funcionários realizarem suas tarefas.

## Solução

Criar uma aplicação web para centralizar as informações dos clientes e facilitar o trabalho dos funcionários.

## Principais funcionalidades do MVP

Foram definidas:

- autenticação individual;
- cadastro de clientes;
- consulta;
- busca por nome ou CPF;
- edição;
- inativação;
- reativação;
- perfil Atendente;
- perfil Administrador;
- administração básica de funcionários.

## Regras de negócio

Entre as regras identificadas:

- CPF não pode ser duplicado;
- clientes podem ter seus dados alterados;
- clientes não são excluídos permanentemente;
- clientes podem ser inativados e reativados;
- clientes reativados não devem ser duplicados;
- nome, telefone e CPF são obrigatórios;
- funcionários possuem diferentes perfis;
- usuários utilizados para login são únicos.

## Decisões técnicas

Foi definida inicialmente a seguinte stack:

- Aplicação Web;
- Python;
- FastAPI;
- PostgreSQL;
- React;
- TypeScript;
- monorepo.

## PRD

Foi criado o:

`PRD.md`

Esse documento passou a registrar os requisitos, regras de negócio, MVP e decisões iniciais do produto.

## Conhecimentos praticados

- levantamento de requisitos;
- requisitos funcionais;
- regras de negócio;
- definição de problema;
- definição de MVP;
- decisões técnicas;
- documentação de produto;
- versionamento.

## Resultado

O ClientFlow deixou de ser apenas uma ideia e passou a possuir uma definição formal de produto e um MVP delimitado.