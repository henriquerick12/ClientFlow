# ClientFlow — Fase 4: Banco de Dados com PostgreSQL e Docker

## Objetivo

Transformar a modelagem do ClientFlow em um banco de dados PostgreSQL funcional, persistente e reproduzível.

## Docker

O PostgreSQL foi executado através de Docker.

Foi criado:

`docker-compose.yml`

O ambiente configurado possui:

- PostgreSQL;
- banco `clientflow`;
- usuário da aplicação;
- porta `5432`;
- volume persistente.

## Docker Compose

Foi aprendido na prática que:

`docker compose up -d`

inicia os serviços configurados no projeto.

Já o acesso manual ao banco pode ser realizado através do `psql` existente dentro do container.

## Modelagem

Foram implementadas duas tabelas principais:

### clientes

- id;
- nome;
- telefone;
- CPF;
- status;
- criado_em;
- atualizado_em.

### funcionarios

- id;
- usuário;
- senha_hash;
- perfil;
- criado_em;
- atualizado_em.

## Integridade

Foram utilizadas constraints como:

- PRIMARY KEY;
- NOT NULL;
- UNIQUE;
- DEFAULT;
- CHECK.

Foi testado que CPF duplicado é rejeitado.

Também foi testado que um status inválido é rejeitado pelo PostgreSQL.

## Triggers

Foi criada uma função PostgreSQL para atualizar automaticamente `atualizado_em`.

Essa função é utilizada por triggers nas tabelas:

- clientes;
- funcionarios.

## Schema versionado

Foi criado:

`backend/database/schema.sql`

Esse arquivo registra a estrutura necessária para reconstruir o banco.

## Validação

Foi criado temporariamente:

`clientflow_test`

O banco começou vazio e recebeu nosso `schema.sql`.

Foram criados corretamente:

- 2 tabelas;
- 1 função;
- 2 triggers.

Isso comprovou que o schema conseguia reconstruir a estrutura do banco sem depender dos comandos executados manualmente anteriormente.

Depois da validação, o banco temporário foi removido.

## Conceitos praticados

- PostgreSQL;
- SQL;
- Docker;
- Docker Compose;
- containers;
- volumes;
- modelagem relacional;
- constraints;
- integridade;
- funções;
- triggers;
- schema versionado;
- banco de teste;
- validação;
- Git.

## Resultado

Ao final da fase, o ClientFlow passou a possuir um PostgreSQL funcional e reproduzível.

A estrutura do banco está registrada no projeto e preparada para receber a conexão do backend Python/FastAPI.