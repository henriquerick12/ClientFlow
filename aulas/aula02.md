# ClientFlow — Fase 2: Domínio e Contexto

## Objetivo

Entender os principais conceitos do negócio antes de representá-los através de banco de dados e código.

## Entidades

Foram identificadas inicialmente duas entidades principais.

### Cliente

Cliente
├── ID
├── Nome
├── Telefone
├── CPF
└── Status
    ├── ATIVO
    └── INATIVO

### Funcionário

Funcionário
├── ID
├── Usuário
├── Senha
└── Perfil
    ├── ATENDENTE
    └── ADMINISTRADOR

## Entidade x atributo

Foi trabalhada a diferença entre uma entidade do domínio e suas características.

Cliente e Funcionário são entidades.

Status é um atributo de Cliente.

Perfil é um atributo de Funcionário.

## Identidade

Foi decidido utilizar um identificador interno para Cliente.

O CPF continua sendo um dado único de negócio, mas não representa a identidade técnica principal do registro.

Funcionários também possuem um ID interno e o usuário utilizado no login deve ser único.

## Ciclo de vida

Clientes não serão excluídos permanentemente.

Eles podem ser:

- ativos;
- inativos;
- reativados.

Funcionários poderão ser excluídos permanentemente por um Administrador.

## Conhecimentos praticados

- domínio;
- entidades;
- atributos;
- identidade;
- unicidade;
- regras de domínio;
- identidade técnica x dado de negócio;
- modelagem conceitual.

## Resultado

Os principais conceitos do domínio do ClientFlow foram identificados antes da implementação técnica.

A fase foi propositalmente mantida mais simples, deixando aprofundamentos para quando fossem necessários durante a construção.