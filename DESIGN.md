# ClientFlow — Arquitetura

## Arquitetura do Backend

O backend do ClientFlow será organizado em camadas para separar responsabilidades.

Fluxo principal:

Route → Service → Repository → Banco de Dados

## Route

Responsável pela entrada e saída da API.

- recebe requisições HTTP
- chama a camada de Service
- retorna respostas HTTP

## Service

Responsável pelas regras e decisões do negócio.

Exemplos:

- impedir cadastro de CPF duplicado
- decidir quando um cliente pode ser reativado
- aplicar regras do sistema

## Repository

Responsável pelo acesso e persistência dos dados.

Exemplos:

- buscar cliente por CPF
- salvar cliente
- atualizar cliente

## Banco de Dados

O banco planejado para o projeto é PostgreSQL.

## Direção das dependências

Route → Service → Repository → PostgreSQL

As camadas de negócio não devem depender das camadas de entrada HTTP.

## Estrutura inicial

backend/
└── app/
    ├── routes/
    ├── services/
    └── repositories/