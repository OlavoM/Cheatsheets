# SQL

</br>

## Descrição
Este arquivo contém comandos básicos que funcionam para praticamente qualquer SQL. Observação: em trechos de código, "[]" significa opcional.

</br>

## Operadores

- Operadores Relacionais: ` = ` e ` <> ` ; `<` e `<=`; `>` e `>=`; `LIKE(` `_` pra um caracter, `%` pra nenhum ou muitos`)`; `BETWEEN`;

- Operadores Lógicos: `AND`; `OR`; `NOT`

- Operadores Aritméticos: `+`; `-`; `*`; `/`

- Operadores Conjunturais: `EXISTS`; `NOT EXISTS`; `IN`; `NOT IN`

- Operador Nulo: `NULL` (`IS NULL`)

- Alias: `AS` (para tabela ou coluna)

</br>

## Select
```sql
SELECT [DISTINCT] colunas
FROM tabelas
[WHERE condições]
[GROUP BY colunas]
[HAVING critérios sobre os grupos (colunas)]
[ORDER BY critérios de ordenação {ASC/DESC}]
```

` DISTINCT ` : não permite a repetição de valores no resultado

` WHERE ` : condição para a busca dos resultados

` GROUP BY ` : agrupamento de dados com mesmo valor

` HAVING ` : condições para a definição de grupos no resultado

` ORDER BY ` : ordenação lógica do resultado

</br>

## INSERT INTO
```sql
INSERT INTO tabela [(colunas)]
VALUES (valores)
```

</br>

## UPDATE
```sql
UPDATE tabela
SET coluna1 = valor1, etc
WHERE condições
```

</br>

## DELETE
```sql
DELETE FROM tabela WHERE condições
```

</br>

## INNER JOIN
```sql
SELECT colunas
FROM tabela1 INNER JOIN tabela2
ON tabela1.coluna = tabela2.coluna
```
É uma junção por intersecção


</br>

## LEFT JOIN
mesma sintaxe do INNER JOIN

Junta todos os dados da intersecção mais os tabela da esquerda (com NULL quando não há match)

</br>

## RIGHT JOIN
mesma sintaxe do INNER JOIN

Junta todos os dados da intersecção mais os tabela da direita

</br>

## FULL JOIN
mesma sintaxe do INNER JOIN

Junta todos os dados da intersecção mais os das tabelas

</br>

## UNION
```sql
SELECT colunas from tabela1
UNION (ou UNION ALL para resultados repetidos)
SELECT colunas from tabela2
```
Pega as colunas e une os resultados delas numa mesma coluna resultante

</br>

## CREATE DATABASE
```sql
CREATE DATABASE nome
(DROP DATABASE nome) --exclui
```

</br>

## CREATE TABLE
```sql
CREATE TABLE nomeTabela (coluna1 tipo1 [características], etc)
(DROP TABLE nome) --exclui
(TRUNCATE TABLE nome) --exclui somente os dados
```

</br>

## KEYS
[dentro da especificação de colunas no CREATE TABLE]
```sql
ID int NOT NULL PRIMARY KEY,
FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
```

</br>

## DEMAIS DECLARAÇÕES DE COLUNAS
```sql
Age int CHECK (Age>=18),
City varchar(255) DEFAULT 'Sandnes'
ID int NOT NULL IDENTITY(início , incremento ) PRIMARY KEY
```

</br>

## ALTER TABLE
```sql
ALTER TABLE tabela ADD coluna tipo
ALTER TABLE tabela DROP COLUMN coluna
```

</br>

## FUNÇÕES AGREGADAS
- `AVG` : obtém o valor médio de um atributo

- `COUNT` : obtém o número de linhas analisadas, `COUNT(atributo)` retorna o número de linhas não NULL do atributo

- `MAX` : obtém o maior valor de um atributo (numérico ou não)

- `MIN` : obtém o menor valor de um atributo (numérico ou não)

- `SUM` : obtém a soma dos valores de um atributo

</br>

## PROCEDURE
- Obs: sintaxe ORACLE
- procedures são executadas a partir de um programa ou executadas manualmente por um usuário
```sql
CREATE [OR REPLACE] PROCEDURE nome_da_procedure
[( argumentoUm modo tipo_do_dado,
    argumentoDois modo tipo_do_dado,
    argumentoTres modo tipo_do_dado )]
IS
    [variaveis_locais e/ou constantes]
BEGIN
    -- Bloco PL/SQL
END nome_da_procedure;
```
- `modo` deve ser `IN`, `OUT` ou `IN OUT`
- se executa com `EXECUTE nome_da_procedure (argumentoUm, argumentoDois, argumentoTres);`
- se exclui com `DROP PROCEDURE nome_da_procedure;`

</br>

## FUNCTION
- Semelhante a uma PROCEDURE, mas retorna um valor
```sql
CREATE [OR REPLACE] FUNCTION nome_da_funcao
[( argumentoUm IN tipo_do_dado,
    argumentoDois IN tipo_do_dado,
    argumentoTres IN tipo_do_dado )]
RETURN tipo_do_dado
IS
    [variaveis_locais e/ou constantes]
BEGIN
    -- Bloco PL/SQL
    RETURN variavel;
END nome_da_funcao;
```
- Executa e exibe o resultado com `SELECT nome_da_funcao(Argumento) FROM tabela`
- É possível executar só chamando a função mesmo
- Se exclui com `DROP FUNCTION nome_da_funcao;`

</br>

## TRIGGER
- É um bloco disparado automaticamente após INSERT, DELETE ou UPDATE


</br>

## OUTROS
- `--comentário`

- `/*comentário de várias linhas*/`

- https://poorsql.com/ -> site para formatar SQL (identação e clean code)