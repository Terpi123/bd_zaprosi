## Буйволенко Иван
Выведи первых 10 добрых героев появившихся между 1980 и 2000 годами из Marvel мужского пола, имеющих светлые волосы и голубые глаза, а также отсортируй их по количеству появлений от большего к меньшему.
```
SELECT id, name, gender, hair, eye, align, appearances, year, universe 
FROM superheroes
WHERE universe = 'marvel'
AND gender = 'Male Characters'
AND align = 'Good Characters'
AND eye = 'Blue Eyes'
AND hair IN ('Blond Hair','White Hair','Silver Hair')
AND year BETWEEN 1980 and 2000
ORDER BY appearances DESC
LIMIT 10
```
