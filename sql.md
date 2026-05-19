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
## Чесноков Данил
Найди айди, имя, принадлежность к стороне, глаза (как цвет глаз),  волосы (как цвет волос), пол, появления, год (как год создания) и вселенную из супергероев начиная с 1960 года. Там не должно быть черноволосых, они должны иметь от 100 и более появлений, но не больше 1000 появлений, должны быть женщинами, из DC и не злодеями, отсортируй по году, принадлежности и волосам и ограничься только 25 первыми из них
```
SELECT name, year, align, universe, gender, hair, eye, appearances
FROM superheroes
WHERE year >= 1960
AND NOT hair = 'Black Hair'
AND appearances BETWEEN 100 and 1000
AND gender = 'Female Characters'
AND universe = 'dc'
AND align = 'Good Characters'
ORDER BY year,align,hair
LIMIT 25
```
## Гусейнов Ядигар
Я хочу увидеть 10 супергероев которые чаще всего попадались в списке супергероев по году возрастанию, год появлений чтобы был самый поздний, у всех супергероев должны быть карий цвет глаз и цвет волос блонд, персонажи могут быть как хорошие так и плохие.
```
SELECT name, year, align, universe, gender, hair, eye, appearances
FROM superheroes
WHERE hair = 'Blond Hair'
AND eye = 'Brown Eyes'
AND align IN ('Good Characters','Bad Characters')
ORDER BY year DESC
LIMIT 10
```
## Исмаилов Арсен
Мне нужна таблица про 7 плохих женских супергероев с наибольшим количеством появлений начиная от самого популярного и заканчивая не популярными, при уcловии что все женские супергерои будут иметь белый цвет волос и будут  браться в диапозоне с 1950 по  2010 года.
```
SELECT name, year, align, universe, gender, hair, eye, appearances
FROM superheroes
WHERE align = 'Bad Characters'
AND gender = 'Female Characters'
AND hair = 'White Hair'
AND year BETWEEN 1950 and 2010
ORDER BY appearances DESC
LIMIT 7
```
## Бубнив Сергей
Запрос должен вывести 5 супергероев женского пола злой стороны, чиcло появлений которых находится в диапазоне от 100 до 670. Вселенная Марвел. Цвет волос не должен быть чёрным и красным, в то время как глаза должны быть синие, белые, жёлтые и зелёные. Год появления появления не раньше 1970. Сортировка проводится по убыванию появлений.
```
SELECT name, year, align, universe, gender, hair, eye, appearances
FROM superheroes
WHERE gender = 'Female Characters'
AND align = 'Bad Characters'
AND universe = 'marvel'
AND NOT hair IN ('Black Hair','Red Hair')
AND eye IN ('Blue Eyes','White Eyes','Yellow Eyes','Green Eyes')
AND appearances BETWEEN 100 and 670
AND year >= 1970
ORDER BY appearances DESC
```
## Магомедбегов Тимур
Выведи имена персонажей, их пол, количество появлений и год первого появления, мужских и женских персонажей, которые появились после 1980 года. Отсортируй результат по убыванию количества появлений и покажи первые 10 записей.
```
SELECT name, year, align, universe, gender, hair, eye, appearances
FROM superheroes
WHERE gender IN ('Male Characters','Female Characters')
AND year > 1980
ORDER BY appearances DESC
LIMIT 10
```
## Вагин Александр
Найди 10 самых редко появляющихся мужских персонажей в промежутке с 1936 по 2004 годов. Найди их вселенные marvel и dc, а также типы хороший, плохой. Чтобы были видны их имена, года, тип персонажа(хороший или плохой), количество появлений, пол, цвет глаз, а также чтобы указывалась вселенная(marvel, dc). И отсортируй их по возрастанию появлений.
```
SELECT name, year, align, universe, gender, hair, eye, appearances
FROM superheroes
WHERE universe IN ('marvel','dc')
AND align IN ('Bad Characters','Good Characters')
ORDER BY appearances ASC
LIMIT 10
```
