Colinha SQL

---

## 📌 **SELECT – Consulta de Dados**

### Estrutura básica

```sql
SELECT coluna1, coluna2
FROM tabela
WHERE condicao;
```

### ORDER BY – Ordenação

```sql
SELECT coluna1, coluna2
FROM tabela
ORDER BY coluna1 ASC; -- ASC | DESC
```

### DISTINCT – Valores únicos

```sql
SELECT DISTINCT coluna1
FROM tabela;
```

---

## 📊 **Funções de Agregação**

```sql
-- Máximo
SELECT MAX(coluna2) AS max_value FROM tabela;

-- Mínimo
SELECT MIN(coluna2) AS min_value FROM tabela;

-- Média
SELECT AVG(coluna2) AS average_value FROM tabela;

-- Soma
SELECT SUM(coluna2) AS sum_value FROM tabela;

-- Contagem
SELECT COUNT(*) AS record_count FROM tabela;
```

---

## 📦 **GROUP BY & HAVING**

### GROUP BY – Agrupamento

```sql
SELECT coluna1, COUNT(*)
FROM tabela
GROUP BY coluna1;
```

### HAVING – Filtro pós-agrupamento

```sql
SELECT coluna1, COUNT(*)
FROM tabela
GROUP BY coluna1
HAVING COUNT(*) > 1;
```

---

## 🔗 **JOINs – Relacionamento entre Tabelas**

### INNER JOIN

```sql
SELECT t1.coluna1, t2.coluna2
FROM tabela1 t1
INNER JOIN tabela2 t2 ON t1.id = t2.id;
```

### LEFT JOIN

```sql
SELECT t1.coluna1, t2.coluna2
FROM tabela1 t1
LEFT JOIN tabela2 t2 ON t1.id = t2.id;
```

### RIGHT JOIN

```sql
SELECT t1.coluna1, t2.coluna2
FROM tabela1 t1
RIGHT JOIN tabela2 t2 ON t1.id = t2.id;
```

### FULL JOIN

```sql
SELECT t1.coluna1, t2.coluna2
FROM tabela1 t1
FULL JOIN tabela2 t2 ON t1.id = t2.id;
```

### CROSS JOIN

```sql
SELECT t1.coluna1, t2.coluna2
FROM tabela1 t1
CROSS JOIN tabela2 t2;
```

---

## 🧱 **CRUD – Manipulação de Dados**

### INSERT

```sql
INSERT INTO tabela (coluna1, coluna2)
VALUES (valor1, valor2);
```

### UPDATE

```sql
UPDATE tabela
SET coluna1 = valor1
WHERE condicao;
```

### DELETE

```sql
DELETE FROM tabela
WHERE condicao;
```

---

## 🔍 **Condições (WHERE)**

### Comparações

```sql
-- Igual
WHERE coluna1 = 'valor'

-- Diferente
WHERE coluna1 <> 'valor'

-- Maior / Menor
WHERE coluna1 > 5
WHERE coluna1 < 10

-- Maior ou igual / Menor ou igual
WHERE coluna1 >= 10
WHERE coluna1 <= 20
```

### IN / NOT IN

```sql
WHERE coluna1 IN ('valor1', 'valor2', 'valor3');
WHERE coluna1 NOT IN ('valor1', 'valor2', 'valor3');
```

### LIKE – Padrões

```sql
WHERE coluna1 LIKE 'prefixo%';
WHERE coluna1 LIKE '%texto%';
```

### BETWEEN

```sql
WHERE coluna1 BETWEEN 10 AND 20;
```

### NULL

```sql
WHERE coluna1 IS NULL;
WHERE coluna1 IS NOT NULL;
```
