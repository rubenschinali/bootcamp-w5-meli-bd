-- Mostrar todos os registros da tabela de filmes. 

SELECT 
	title 
FROM 
	movies_db.movies; 

-- Exibir o primeiro nome, o sobrenome e a classificação de todos os atores. 

SELECT 
	first_name, 
	last_name, 
	rating 
FROM 
	movies_db.actors;

-- Exibir o título de todas as séries e usar aliases para que o nome da tabela e o campo estejam em inglês. 

SELECT 
	title  AS 'título' 
FROM 
	movies_db.series AS series;

-- Exibir o primeiro nome e o sobrenome dos atores cuja classificação seja superior a 7,5. 

SELECT 
	first_name, last_name, rating 
FROM 
	movies_db.actors
WHERE
	rating >= 7.5; 

-- Exibir o título do filme, a classificação e os prêmios dos filmes com classificação superior a 7,5 e com mais de dois prêmios. 

SELECT 
	title, rating, awards 
FROM
	movies_db.movies
WHERE 
	rating > 7.5
AND 
	awards > 2; 

-- Exibir o título do filme e a classificação ordenados por classificação em ordem crescente.

SELECT 
	title, rating
FROM
	movies_db.movies 
ORDER BY
	rating ;

-- Exibir os títulos dos filmes e a classificação ordenados por classificação.

SELECT 
	title, rating
FROM
	movies_db.movies 
ORDER BY
	rating DESC ;


-- Exibir os títulos dos três primeiros filmes no banco de dados. 

SELECT 
	title
FROM
	movies_db.movies 
LIMIT
	3;

-- Exibir os 5 filmes mais bem classificados.  /// Ordenar em ordem alfabética

SELECT 
	title, rating
FROM
	movies_db.movies 
ORDER BY
	rating DESC
LIMIT
	5;

-- Listar os 10 primeiros atores. 

SELECT 
	* 
FROM 
	movies_db.actors
LIMIT
	10;

-- Exibir o título e a classificação de todos os filmes cujo título é Toy Story. 

SELECT 
	title, rating
FROM 
	movies_db.movies 
WHERE 
	title 
LIKE 
	'Toy Story%';

-- Exibir todos os atores cujos nomes começam com Sam. 

SELECT 
	first_name, last_name
FROM 
	movies_db.actors
WHERE 
	first_name
LIKE 
	'Sam%';

-- Exibir o título dos filmes lançados entre 2004 e 2008. 

SELECT 
	title 
FROM 
	movies_db.movies 
WHERE 
	release_date 
BETWEEN
	'20040101' 
AND 
	'20081231';

-- Exibir o título dos filmes com classificação superior a 3, com mais de 1 prêmio e com data de lançamento entre 1988 e 2009. 

SELECT 
	title,  rating, awards, release_date 
FROM 
	movies_db.movies 
WHERE 
	rating > 3 
AND 
	awards > 1
AND (
	release_date 
BETWEEN 
	'19880101' 
AND 
	'20091231');


-- Ordenar os resultados por classificação.

SELECT 
	title,  rating, awards, release_date 
FROM 
	movies_db.movies 
WHERE 
	rating > 3 
AND 
	awards > 1
AND (
	release_date 
BETWEEN 
	'19880101' 
AND 
	'20091231')
ORDER BY 
	rating ;





