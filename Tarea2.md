# Tarea2
-Anairam Mar Cuevas 181375
<br>
<br>
## 1) Cómo podemos saber si los tuiteros hispanohablantes interactúan más en las noches?
<br>
```javascript
db.tweets.aggregate([ 
    { $group: { _id: { "lang": "$user.lang", "hour": { $substr: ["$created_at", 11, 2] } }, "counter": { $count: {} } } }, 
    { $match: { "_id.hour": "20" } }, 
    { $sort: {"counter":-1}}
]);
```
## 2) Cómo podemos saber de dónde son los tuiteros que más tiempo tienen en la plataforma?

## 3) En intervalos de 7:00:00pm a 6:59:59am y de 7:00:00am a 6:59:59pm, de qué paises la mayoría de los tuits?

## 4) De qué país son los tuiteros más famosos de nuestra colección?
<br>
```javascript
db.tweets.aggregate([         
    {$project: {"user.followers_count":1, "user.lang":1}}, 
    {$sort: {"user.followers_count":-1}},   
    {$limit: 10},
    {$lookup: {from:"primarydialects","localField":"user.lang","foreignField":"lang","as":"language"}},
    {$lookup: {from:"languagenames","localField":"language.locale","foreignField":"locale","as":"fulllocale"}},
    {$project: {_id:1,"user.followers_count":1, "fulllocale.languages":1}}
]);

```
