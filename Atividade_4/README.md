# Atividade 4 - Implementação e Manipulação de Dados com SQL

## 🚀 Como Executar

### Pré-requisitos
- PostgreSQL instalado
- PGAdmin ou outra ferramenta SQL

### 📥 Passos para Execução

1. **Crie as tabelas:**

```sql
CREATE TABLE cliente (
    cpf BIGINT PRIMARY KEY,
    primeiro_nome VARCHAR(80) NOT NULL,
    data_nascimento DATE,
    sexo VARCHAR(1) NOT NULL,
    rua VARCHAR(40),
    estado VARCHAR(20),
    cidade VARCHAR(40),
    cep INTEGER,
    ultimo_nome VARCHAR(40)
);

CREATE TABLE client_telefone_email (
    cliente_cpf BIGINT REFERENCES cliente(cpf),
    telefoneum BIGINT NOT NULL,
    telefonedois BIGINT,
    emailum VARCHAR(50) NOT NULL,
    emaildois VARCHAR(50)
);
```
  Observação: O ideal seria as tabelas conterem id_cliente ao invés do CPF e é desaconselhável guardar informações como número (telefone, por exemplo, deve ser adicionado como string). No entanto, como o objetivo é de aprendizado, utilizei números inteiros para ter contato com mais tipos de dados.

  Observação 2: Algumas queries utilizadas são um pouco mais avançadas, pois já havia estudado a linguagem SQL antes até a parte de subquery.

  Execute os scripts na ordem:

  insert_dados.sql - Popula as tabelas

  consultas_select.sql - Consultas de seleção

  updates_deletes.sql - Comandos de atualização e exclusão

  Verifique os resultados com SELECT * FROM nome_tabela após cada execução

📊 Estrutura dos Scripts
🔹 INSERTs

   10 clientes na tabela cliente;

   Telefones e e-mails (multivalorados) na tabela client_telefone_email, que referencia a tabela cliente, utilizando o CPF como chave-estrangeira

🔹 SELECTs

   Consultas com WHERE, ORDER BY (futuramente), LIMIT (futuramente) e JOIN

🔹 UPDATEs

   3 comandos de atualização com condições

🔹 DELETEs

   3 comandos de exclusão com condições

⚠️ Observações

   Verifique constraints de chaves estrangeiras

Aluno: Gabriel Augusto Lyra Porto

Disciplina: Banco de Dados – Turma 004
