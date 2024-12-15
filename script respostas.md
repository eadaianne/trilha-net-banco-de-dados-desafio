### Buscar o nome e ano dos filmes
----
SELECT NOME, ANO FROM Filmes; <br> <br>
![image](https://github.com/user-attachments/assets/bfc3b9ab-174f-4337-88cf-e40faf83cfb7)
<br>
### Buscar o nome e ano dos filmes, ordenados por ordem crescente pelo ano
----
SELECT NOME, ANO FROM Filmes ORDER BY ANO ASC; <br> <br>
![image](https://github.com/user-attachments/assets/a333c256-0cfb-4346-be9c-ce2fa9d71e66)
<br>
### Buscar pelo filme de volta para o futuro, trazendo o nome, ano e a duração
----
SELECT * FROM Filmes WHERE NOME = 'De volta para o futuro'; <br> <br>  
![image](https://github.com/user-attachments/assets/252f6a17-8bb6-4af8-9b3a-a67297d5913a)
<br>
### Buscar os filmes lançados em 1997
----
SELECT * FROM Filmes WHERE ANO = 1997; <br> <br>
![image](https://github.com/user-attachments/assets/86c50890-0023-430a-a777-19e14900e587)
<br>
### Buscar os filmes lançados APÓS o ano 2000
----
SELECT * FROM Filmes WHERE ANO > 2000; <br> <br>
![image](https://github.com/user-attachments/assets/aa46cfd4-ead4-4a2c-94aa-3ff8d7097e02)
<br>
### Buscar os filmes com a duracao maior que 100 e menor que 150, ordenando pela duracao em ordem crescente
----
SELECT * FROM Filmes WHERE DURACAO BETWEEN 101 AND 150 ORDER BY DURACAO ASC; <br> <br>
![image](https://github.com/user-attachments/assets/c8d5de82-446c-454b-bf73-7483e1cc768b)
<br>
### Buscar a quantidade de filmes lançadas no ano, agrupando por ano, ordenando pela duracao em ordem decrescente
----
SELECT ANO, COUNT(1) QUANTIDADE FROM FILMES GROUP BY ANO ORDER BY QUANTIDADE DESC <br> <br>
![image](https://github.com/user-attachments/assets/e0eeed5b-ec8d-4ed9-8a6f-fdd474569ca7)
<br>
### Buscar os Atores do gênero masculino, retornando o PrimeiroNome, UltimoNome
----
SELECT * FROM ATORES WHERE GENERO = 'M'; <br> <br>
![image](https://github.com/user-attachments/assets/9bf529bc-c258-44e1-936e-fde816705548)
<br>
### Buscar os Atores do gênero feminino, retornando o PrimeiroNome, UltimoNome, e ordenando pelo PrimeiroNome
----
SELECT * FROM ATORES WHERE GENERO = 'F' ORDER BY PRIMEIRONOME; <br> <br>
![image](https://github.com/user-attachments/assets/d6543471-dd9b-441d-ab17-b372e2cae3eb)
<br>
### Buscar o nome do filme e o gênero
----
SELECT f.Nome, g.Genero FROM Filmes f
INNER JOIN FilmesGenero fg ON f.Id = fg.IdFilme
INNER JOIN Generos g ON fg.IdGenero = g.Id; <br> <br>
![image](https://github.com/user-attachments/assets/d89b0623-4e08-4502-a66b-c96bf26894aa)
<br>
### Buscar o nome do filme e o gênero do tipo "Mistério"
----
SELECT f.Nome, g.Genero FROM Filmes f
INNER JOIN FilmesGenero fg ON f.Id = fg.IdFilme
INNER JOIN Generos g ON fg.IdGenero = g.Id
WHERE g.Genero = 'Mistério'; <br> <br>
![image](https://github.com/user-attachments/assets/0d807820-e478-409e-b0d0-d047dc43d537)
<br>
### Buscar o nome do filme e os atores, trazendo o PrimeiroNome, UltimoNome e seu Papel
----
SELECT f.Nome, a.PrimeiroNome, a.UltimoNome, ef.Papel
FROM Filmes f
INNER JOIN ElencoFilme ef ON f.Id = ef.IdFilme
INNER JOIN Atores a ON ef.IdAtor = a.Id; <br> <br>
![image](https://github.com/user-attachments/assets/adf074ed-d3be-42cf-a7c2-f32cf61f7499)
<br>
