# ClientFlow — Fase 3: Arquitetura de Software

## Objetivo

Definir como o backend do ClientFlow será organizado e separar corretamente as responsabilidades do sistema.

## Arquitetura

Foi adotada inicialmente uma arquitetura em camadas:

Route → Service → Repository → Banco

## Route

Responsável pela entrada e saída HTTP da API.

Exemplos:

- receber requisições;
- chamar Services;
- retornar respostas.

## Service

Responsável pelas regras e decisões do negócio.

Exemplos:

- impedir CPF duplicado;
- decidir sobre reativação de clientes;
- coordenar operações da aplicação.

## Repository

Responsável pelo acesso e persistência dos dados.

Exemplos:

- buscar cliente;
- salvar cliente;
- atualizar cliente;
- consultar registros.

## Direção das dependências

Foi definida:

Route
↓
Service
↓
Repository
↓
PostgreSQL

As regras de negócio não devem depender da camada HTTP.

## Estrutura inicial

Foi preparada a estrutura:

backend/
└── app/
    ├── routes/
    ├── services/
    └── repositories/

## DESIGN.md

A arquitetura foi documentada em:

`DESIGN.md`

## Conceitos praticados

- Arquitetura em Camadas;
- Service Layer;
- Repository Pattern;
- Separation of Concerns;
- direção de dependências;
- separação de responsabilidades.

## Resultado

O ClientFlow passou a possuir uma arquitetura inicial definida e documentada.

Mais importante do que criar pastas foi compreender quais responsabilidades pertencem a cada parte do sistema.