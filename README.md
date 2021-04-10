# SQL

## Problemas Resolvidos

|[#URI](https://github.com/JefersonMelo/01-URI/tree/master/09-SQL)|[#LubySoftware](https://github.com/JefersonMelo/08-LubySoftware/blob/master/02-SQL/SQL.md)|[#MRV](https://github.com/JefersonMelo/13-SQL/tree/main/Atividades-Propostas)|
| ----- | ----- | ----- |

## Comandos de Criação

- ### Criar Banco de Dados

```"
CREATE DATABASE NAME_DB
USE NAME_DB
GO
```

- ### Criar da Tabela

```"
CREATE TABLE NAME_TABLE_DB(
    /*Atributos*/
)
GO
```

- ### Criar Constraints

```"
ALTER TABLE NAME_TABLE_DB
ADD CONSTRAINT CK_SEXO CHECK (
    SEXO IN('M','F')
)
GO
```

- ### Criar Foreign key

```"
ALTER TABLE NAME_TABLE_DB 
ADD CONSTRAINT 
FK_ENDERECO
FOREIGN KEY(ID_ALUNO) 
REFERENCES ALUNO(IDALUNO)
GO
```

- ### Criar Produceres

```"
SP_COLUMNS NAME_TABLE_DB 
GO
SP_HELP NAME_TABLE_DB 
GO
```

- ### Criar Trigger

```"
CREATE TRIGGER TRG_ATUALIZA_PRECO
ON DBO.NAME_DB
FOR UPDATE
AS
DECLARE @IDPRODUTO INT
GO
```

- ### Criar Producere

```"
CREATE PRODC CONTA @NUM1 INT, @NUM2 INT
AS
SELECT @NUM1 + @NUM2 AS RESULTADO
GO
```

- ## Comando de Execução

- ### Execução Producere

```"
EXEC CONTA 90, 78
GO
```

- ### Inserir Dados

```"
INSERT INTO NAME_TABLE_DB VALUES()
GO
```
