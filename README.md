# Projeto Banco de Dados — Jogo RPG

## Sobre o projeto

Este projeto foi desenvolvido como atividade acadêmica do SENAI, com o objetivo de aplicar conceitos de Banco de Dados por meio da criação e manipulação de estruturas relacionais.

O banco de dados representa a estrutura de um jogo RPG, permitindo organizar usuários, personagens, classes e habilidades.

O desenvolvimento foi realizado utilizando **MySQL**, por meio do MySQL Workbench, adaptando os comandos e procedimentos apresentados no material didático originalmente direcionado ao SQL Server.

## Tecnologias utilizadas

- MySQL
- MySQL Workbench
- Linguagem SQL (DDL)
- GitHub

## Estrutura do banco de dados

O banco de dados utilizado no projeto é denominado `JogoRPG` e possui cinco tabelas:

| Tabela | Descrição |
|---|---|
| USUARIOS | Armazena os dados dos usuários. |
| PERSONAGENS | Armazena os personagens e seus respectivos usuários e classes. |
| CLASSES | Armazena as classes disponíveis no jogo. |
| HABILIDADES | Armazena as habilidades disponíveis. |
| CLASSES_HABILIDADES | Relaciona as classes às suas respectivas habilidades. |

## Relacionamentos

O projeto apresenta os seguintes relacionamentos:

- **USUARIOS 1:N PERSONAGENS:** um usuário pode possuir vários personagens.
- **CLASSES 1:N PERSONAGENS:** uma classe pode estar associada a vários personagens.
- **CLASSES N:N HABILIDADES:** uma classe pode possuir várias habilidades, e uma habilidade pode pertencer a várias classes.

O relacionamento N:N é resolvido pela tabela intermediária `CLASSES_HABILIDADES`, que utiliza uma chave primária composta por `ClasseId` e `HabilidadeId`.

## Conceitos aplicados

Durante o desenvolvimento foram utilizados os seguintes comandos e conceitos:

- `CREATE DATABASE`: criação do banco de dados.
- `USE`: seleção do banco de dados.
- `CREATE TABLE`: criação das tabelas.
- `PRIMARY KEY`: definição de chaves primárias.
- `FOREIGN KEY`: definição de chaves estrangeiras.
- `AUTO_INCREMENT`: geração automática de identificadores.
- `ALTER TABLE`: alteração da estrutura das tabelas.
- `ADD COLUMN`: adição de colunas.
- `DROP COLUMN`: exclusão de colunas.
- `DROP TABLE`: exclusão de tabelas.
- `SHOW TABLES` e `DESCRIBE`: consultas para conferência da estrutura.

## Como executar o projeto

1. Instale o MySQL Server e o MySQL Workbench.
2. Abra o MySQL Workbench e estabeleça uma conexão com o servidor.
3. Baixe o arquivo `jogo_rpg_senai.sql` disponível neste repositório.
4. Abra o arquivo no editor SQL do MySQL Workbench.
5. Execute o script em uma instância limpa do banco de dados.

**Observação:** o script foi desenvolvido para MySQL e deve ser executado em uma base sem as tabelas do projeto previamente criadas.

## Arquivo do projeto

- `jogo_rpg_senai.sql` — contém os comandos SQL desenvolvidos durante a atividade.

## Finalidade acadêmica

Projeto desenvolvido para fins de aprendizagem e aplicação prática dos conceitos de modelagem, criação, alteração e exclusão de estruturas de banco de dados relacionais.

**Instituição:** SENAI  
**Projeto:** Banco de Dados — Jogo RPG  
**SGBD utilizado:** MySQL
