🛠️ Projeto de Banco de Dados: JV AutoCar (Experiência Prática IV)

Este repositório contém o projeto de Modelagem Física e Manipulação de Dados para o sistema "JV AutoCar" (Auto Peças e Oficina Mecânica), criado como entregável da Experiência Prática IV.

O modelo lógico (DER) foi previamente verificado e atende plenamente à Terceira Forma Normal (3FN).

🚀 Estrutura e Instruções de Execução

O banco de dados foi desenvolvido e testado no ambiente *MySQL Workbench*.

Ordem de Execução dos Scripts:

Para recriar e testar o banco de dados, execute os arquivos **em ordem** no MySQL Workbench:

1.  **`01_schema_creation.sql`** (DDL): Cria o banco de dados `JV_AUTOCAR_DB` e todas as 5 tabelas com suas chaves primárias e estrangeiras.
2.  **`02_data_inserts.sql`** (DML): Popula todas as tabelas com dados de exemplo (clientes, veículos, peças, OS e itens da OS).
3.  **`03_data_queries.sql`** (DQL): Contém as consultas SQL que demonstram a funcionalidade e os relacionamentos do banco de dados (usando `SELECT`, `JOIN`, `WHERE`, `ORDER BY`).
4.  **`04_data_manipulation.sql`** (DML): Contém os comandos de manipulação de dados (`UPDATE` e `DELETE` com cláusulas `WHERE`) para testar a integridade referencial.

⚙️ Tabelas Implementadas

| Tabela | Chave Primária | Relacionamentos com FK |
| :--- | :--- | :--- |
| **CLIENTE** | `CPF_CLIENTE` | Não possui |
| **VEICULO** | `PLACA_VEICULO` | `FK: CPF_CLIENTE` |
| **PEÇAS** | `COD_PECA` | Não possui |
| **ORDEM_SERVICO** | `NUMERO_OS` | `FK: PLACA_VEICULO` |
| **ITENS_OS** | Composta (`NUMERO_OS`, `COD_PECA`) | `FK: NUMERO_OS`, `FK: COD_PECA` |


*Desenvolvido por: João Vitor Lopes Souza Alves*
