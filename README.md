
## 1. Mostrar todos os registros da tabela de filmes

```sql
SELECT 
    title 
FROM 
    movies_db.movies;
```

---

## 2. Exibir o primeiro nome, o sobrenome e a classificação de todos os atores

```sql
SELECT 
    first_name, 
    last_name, 
    rating 
FROM 
    movies_db.actors;
```

---

## 3. Exibir o título de todas as séries e usar aliases para que o nome da tabela e o campo estejam em inglês

```sql
SELECT 
    title  AS 'título' 
FROM 
    movies_db.series AS series;
```

---

## 4. Exibir o primeiro nome e o sobrenome dos atores cuja classificação seja superior a 7,5

```sql
SELECT 
    first_name, 
    last_name, 
    rating 
FROM 
    movies_db.actors
WHERE
    rating >= 7.5;
```

---

## 5. Exibir o título do filme, a classificação e os prêmios dos filmes com classificação superior a 7,5 e com mais de dois prêmios

```sql
SELECT 
    title, 
    rating, 
    awards 
FROM
    movies_db.movies
WHERE 
    rating > 7.5
AND 
    awards > 2;
```

---

## 6. Exibir o título do filme e a classificação ordenados por classificação em ordem crescente

```sql
SELECT 
    title, 
    rating
FROM
    movies_db.movies 
ORDER BY
    rating;
```

---

## 7. Exibir os títulos dos filmes e a classificação ordenados por classificação em ordem decrescente

```sql
SELECT 
    title, 
    rating
FROM
    movies_db.movies 
ORDER BY
    rating DESC;
```

---

## 8. Exibir os títulos dos três primeiros filmes no banco de dados

```sql
SELECT 
    title
FROM
    movies_db.movies 
LIMIT
    3;
```

---

## 9. Exibir os 5 filmes mais bem classificados (ordenar em ordem alfabética)

```sql
SELECT 
    title, 
    rating
FROM
    movies_db.movies 
ORDER BY
    rating DESC
LIMIT
    5;
```

---

## 10. Listar os 10 primeiros atores

```sql
SELECT 
    * 
FROM 
    movies_db.actors
LIMIT
    10;
```

---

## 11. Exibir o título e a classificação de todos os filmes cujo título é "Toy Story"

```sql
SELECT 
    title, 
    rating
FROM 
    movies_db.movies 
WHERE 
    title LIKE 'Toy Story%';
```

---

## 12. Exibir todos os atores cujos nomes começam com "Sam"

```sql
SELECT 
    first_name, 
    last_name
FROM 
    movies_db.actors
WHERE 
    first_name LIKE 'Sam%';
```

---

## 13. Exibir o título dos filmes lançados entre 2004 e 2008

```sql
SELECT 
    title 
FROM 
    movies_db.movies 
WHERE 
    release_date BETWEEN '20040101' AND '20081231';
```

---

## 14. Exibir o título dos filmes com classificação superior a 3, com mais de 1 prêmio e com data de lançamento entre 1988 e 2009

```sql
SELECT 
    title,  
    rating, 
    awards, 
    release_date 
FROM 
    movies_db.movies 
WHERE 
    rating > 3 
AND 
    awards > 1
AND 
    release_date BETWEEN '19880101' AND '20091231';
```

---

## 15. Ordenar os resultados por classificação

```sql
SELECT 
    title,  
    rating, 
    awards, 
    release_date 
FROM 
    movies_db.movies 
WHERE 
    rating > 3 
AND 
    awards > 1
AND 
    release_date BETWEEN '19880101' AND '20091231'
ORDER BY 
    rating;
```

---
