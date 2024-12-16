## Database-Oscar

# Quantas vezes Natalie Portamn ganhou?
```sql
SELECT COUNT(*) * FROM indicados_ao_oscar WHERE = "Name" like = "%Natalie Portamn%";
```

**Resposta**: 3 vezes.
# Quantos Oscars Natalie Portman ganhou?
```sql
SELECT * FROM indicados_ao_oscar WHERE nome_do_indicado like "%Natalie Portman%" AND vencedor = "true";
```

**Resposta**: 1 vez.

# Amy Adams já ganhou algum Oscar?
```sql
SELECT * FROM indicados_ao_oscar WHERE nome_do_indicado like "%Amy Adams%";
```

**Resposta**: Não

# A série de filmes Toy Story ganhou um Oscar em quais anos?
```sql
SELECT * FROM indicados_ao_oscar WHERE nome_do_filme like "%Toy Story%" AND vencedor = "true";
```

**Resposta**: Em 2011 e 2020

# A partir de que ano que a categoria "Actress" deixa de existir?
```sql
SELECT * FROM indicados_ao_oscar WHERE categoria = "ACTRESS" ORDER BY ano_cerimonia DESC;
```

**Resposta**: 1977

# Quem ganhou o primeiro Oscar para Melhor Atriz? Em que ano?
```sql
SELECT * FROM indicados_ao_oscar WHERE vencedor = "true" AND categoria = "ACTRESS";
```

**Resposta**: Janet Gaynor

# Na campo "Vencedor", altere todos os valores com "true" para 1 e todos os valores "false" para 0.
```sql
UPDATE indicados_ao_oscar SET vencedor = "1" WHERE vencedor = "true";
UPDATE indicados_ao_oscar SET vencedor = "0" WHERE vencedor = "false";
```

# Em qual edição do Oscar "Crash" concorreu ao Oscar?
```sql
SELECT nome_do_filme, cerimonia FROM indicados_ao_oscar WHERE nome_do_filme like "%Crash";
```

**Resposta**: A 78

# O filme Central do Brasil aparece no Oscar?
```sql
 SELECT * FROM indicados_ao_oscar WHERE nome_do_filme like "Central%";
```

**Resposta**: Sim, em 1999

# Inclua no banco 3 filmes que nunca foram nem nomeados ao Oscar, mas que merecem ser.
```sql
 INSERT INTO indicados_ao_oscar(ano_filmagem,ano_cerimonia,cerimonia,categoria,nome_do_indicado,nome_do_filme,vencedor) VALUES (2015,2016,5,'Melhor Filme de Terror','James DeMonaco','Uma Noite de Crime','true');
INSERT INTO indicados_ao_oscar(ano_filmagem,ano_cerimonia,cerimonia,categoria,nome_do_indicado,nome_do_filme,vencedor) VALUES (2017,2018,7,'Melhor Filme Jurassico','Michael Crichton',' Jurassic World','true');
INSERT INTO indicados_ao_oscar(ano_filmagem,ano_cerimonia,cerimonia,categoria,nome_do_indicado,nome_do_filme,vencedor) VALUES (2019,2020,3,'Melhor Filme de Animação','Walter Lantz','Pica Pau','true');
```

# Denzel Washington já ganhou algum Oscar?
```sql
SELECT * FROM indicados_ao_oscar WHERE nome_do_indicado like "%Denzel Washington%" AND vencedor = "1";
```

**Resposta**: Sim

# Quais os filmes que ganharam o Oscar de Melhor Filme?
```sql
SELECT * FROM indicados_ao_oscar WHERE categoria = "BEST PICTURE" AND vencedor = "1";
```

**Resposta**: Lawrence of Arabia Tom Jones | My Fair Lady | The Sound of Music | A Man for All Seasons | In the Heat of the Night | Oliver! | Midnight Cowboy | Patton | The French Connection | The Godfather | The Sting | The Godfather Part II | One Flew over the Cuckoo's Nest | Rocky | Annie Hall | The Deer Hunter | Kramer vs. Kramer | Ordinary People | Chariots of Fire | Gandhi | Terms of Endearment | Amadeus | Out of Africa | Platoon | The Last Emperor | Rain Man | Driving Miss Daisy | Dances With Wolves | The Silence of the Lambs | Unforgiven | Schindler's List | Forrest Gump | Braveheart | The English Patient | Titanic | Shakespeare in Love | American Beauty | Gladiator | A Beautiful Mind | Chicago | The Lord of the Rings: The Return of the King | Million Dollar Baby | Crash | The Departed | No Country for Old Men | Slumdog Millionaire | The Hurt Locker | The King's Speech | The Artist | Argo | 12 Years a Slave | Birdman or (The Unexpected Virtue of Ignorance) | Spotlight | Moonlight | The Shape of Water | Green Book | Parasite | Nomadland | CODA | Everything Everywhere All at Once | Oppenheimer

# Bonus: Quais os filmes que ganharam o Oscar de Melhor Filme e Melhor Diretor na mesma cerimonia?
```sql
SELECT * FROM indicados_ao_oscar WHERE vencedor = "1" AND categoria = "BEST PICTURE" AND categoria = "DIRECTING";
```

**Respota**: Não

# Bonus: Denzel Washington e Jamie Foxx já concorreram ao Oscar no mesmo ano?
```sql
SELECT nome_do_indicado, ano_cerimonia FROM indicados_ao_oscar WHERE nome_do_indicado like "%Denzel Washington%" AND nome_do_indicado like "%Jamie Foxx%";
```

**Resposta**: Não.

