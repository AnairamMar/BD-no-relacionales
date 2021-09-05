#Tarea queries
Anairam Mar Cuevas
12. Escribe una función find() para encontrar los restaurantes que no preparan ninguna cocina del continente americano y lograron una puntuación superior a 70 y se ubicaron en la longitud inferior a -65.754168.
```javascript
db.restaurants.find({"cuisine":{$not:/^American/},"grades.score":{$gt:70},"address.coord":{$lt:-65.754168}})
```
13. Escribe una función find() para encontrar los restaurantes que no preparan ninguna cocina del continente americano y obtuvieron una calificación de 'A' que no pertenece al distrito de Brooklyn. El documento debe mostrarse según la cocina en orden descendente.
```javascript
db.restaurants.find({"cuisine":{$not:/^American/},"grades.grade":"A","borough":{$not:/^Brooklyn/}},{"cuisine":1,"grades.grade":1,"borough":1}).sort({"cuisine":-1})
```
14. Escribe una función find() para encontrar el ID del restaurante, el nombre, el municipio y la cocina de aquellos restaurantes que contienen 'Wil' como las primeras tres letras de su nombre.
```javascript
db.restaurants.find({"name":/^Wil/},{"restaurant_id": 1,"name":1,"borough":1,"cuisine":1})
```
15. Escribe una función find() para encontrar el ID del restaurante, el nombre, el municipio y la cocina de aquellos restaurantes que contienen "ces" como las últimas tres letras de su nombre.
```javascript
db.restaurants.find({"name":/ces$/},{"restaurant_id": 1,"name":1,"borough":1,"cuisine":1})
```
16. Escribe una función find() para encontrar el ID del restaurante, el nombre, el municipio y la cocina de aquellos restaurantes que contienen 'Reg' como tres letras en algún lugar de su nombre.
```javascript
db.restaurants.find({"name":/Reg/},{"restaurant_id": 1,"name":1,"borough":1,"cuisine":1})
```
17. Escribe una función find() para encontrar los restaurantes que pertenecen al municipio del Bronx y que prepararon platos estadounidenses o chinos.
```javascript
db.restaurants.find({"borough":"Bronx","cuisine":{$in:["Chinese","American "]}})
```
18. Escribe una función find() para encontrar la identificación del restaurante, el nombre, el municipio y la cocina de los restaurantes que pertenecen al municipio de Staten Island o Queens o Bronxor Brooklyn.
```javascript
db.restaurants.find({"borough":{$in:["Brooklyn","Bronx","Queens","Staten Island"]}},{"restaurant_id": 1,"name":1,"borough":1,"cuisine":1})
```
19. Escribe una función find() para encontrar el ID del restaurante, el nombre, el municipio y la cocina de aquellos restaurantes que no pertenecen al municipio de Staten Island o Queens o Bronxor Brooklyn.
```javascript
db.restaurants.find({"borough":{$nin:["Brooklyn","Bronx","Queens","Staten Island"]}},{"restaurant_id": 1,"name":1,"borough":1,"cuisine":1})
```
20. Escribe una función find() para encontrar el ID del restaurante, el nombre, el municipio y la cocina de aquellos restaurantes que obtuvieron una puntuación que no sea superior a 10.
```javascript
db.restaurants.find({"grades.score":{$lt:10}},{"restaurant_id": 1,"name":1,"borough":1,"cuisine":1})
```
21. Escribe una función find() para encontrar el ID del restaurante, el nombre, el municipio y la cocina de aquellos restaurantes que prepararon platos excepto 'Americano' y 'Chinese' o el nombre del restaurante comienza con la letra 'Wil'.
```javascript
db.restaurants.find({"name":/^Wil/,"cuisine":{$nin:["Chinese","American "]}},{"restaurant_id": 1,"name":1,"borough":1,"cuisine":1})
```
22. Escribe una función find() para encontrar el ID del restaurante, el nombre y las calificaciones de los restaurantes que obtuvieron una calificación de "A" y obtuvieron una puntuación de 11 en un ISODate "2014-08-11T00: 00: 00Z" entre muchas de las fechas de la encuesta. .
```javascript
db.restaurants.find({ "grades" : { $elemMatch : {"score" : 11,"date": ISODate("2014-08-11T00:00:00Z")} } , "grades.grade" : "A"},{ "restaurant_id": 1, name:1, "grades.grade":1})
```
23. Escribe una función find() para encontrar el ID del restaurante, el nombre y las calificaciones de aquellos restaurantes donde el segundo elemento de la matriz de calificaciones contiene una calificación de "A" y una puntuación de 9 en un ISODate "2014-08-11T00: 00: 00Z".
```javascript
db.restaurants.find({ "grades" : { $elemMatch : {"score" : 9,"date": ISODate("2014-08-11T00:00:00Z")} } , "grades.1.grade" : "A"},{ "restaurant_id": 1, name:1, "grades.grade":1})
```

24. Escribe una función find() para encontrar el ID del restaurante, el nombre, la dirección y la ubicación geográfica para aquellos restaurantes donde el segundo elemento de la matriz de coordenadas contiene un valor que sea más de 42 y hasta 52 ..
```javascript
db.restaurants.fin({"address.1.coord":{$gt: 42,$lte:52}},{"restaurant_id":1,"name":1,"address":1})
```

25. Escribe una función find() para organizar el nombre de los restaurantes en orden ascendente junto con todas las columnas.
```javascript
db.restaurants.find().sort({"name":1})
```

26. Escribe una función find() para organizar el nombre de los restaurantes en orden descendente junto con todas las columnas.
```javascript
db.restaurants.find().sort({"name":-1})

```

27. Escribe una función find() para organizar el nombre de la cocina en orden ascendente y para ese mismo distrito de cocina debe estar en orden descendente.
```javascript
db.restaurants.find().sort({"borought":-1,"cuisine":1})
```

28. Escribe una función find() para saber si todas las direcciones contienen la calle o no.
```javascript
db.restaurants.find({"address.street":{$exists : true}}).count() == db.restaurants.find({}).count()
```

29. Escribe una función find() que seleccionará todos los documentos de la colección de restaurantes donde el valor del campo coord es Double.
```javascript
db.restaurants.find({"address.coord":{$type:"double"}})
```

30. Escribe una función find() que seleccionará el ID del restaurante, el nombre y las calificaciones para esos restaurantes que devuelve 0 como resto después de dividir la puntuación por 7.
```javascript

```

31. Escribe una función find() para encontrar el nombre del restaurante, el municipio, la longitud y la actitud y la cocina de aquellos restaurantes que contienen "mon" como tres letras en algún lugar de su nombre.
```javascript
db.restaurants.find({"name":/mon/},{"name":1,"borough":1,"cuisine":1,"address.coord":1})
```

32. Escribe una función find() para encontrar el nombre del restaurante, el distrito, la longitud y la latitud y la cocina de aquellos restaurantes que contienen 'Mad' como las primeras tres letras de su nombre.
```javascript
db.restaurants.find({"name":/^Mad/},{"name":1,"borough":1,"cuisine":1,"address.coord":1})
```
