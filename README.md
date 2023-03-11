# mongodb atividade 01

## Passo a passo:
1. Instalar o mongo compass e mongo shell.
2. Criar o database e o collection: sudo mongoimport --db aula --collection livros --file=/#/books.json.
3. Iniciar o mongo shell: mongosh.
4. Acessar o database: use aula.
## 

## Exercícios

Exercício 4:
```
db.livros.find().count()
```
```
Output: 431
```

Exercício 5:
```
db.livros.find({pageCount:{$lte: 100}}).count()
```
```
Output: 166
```
Exercício 6:
```
db.livros.find({isbn:{$lte: "1617200000"}}).count()
```
```
Output: 22
```
```
db.livros.find({isbn:{$gt: "1933988746"}}).count()
```
```
Output: 85
```

Exercício 7:
```
db.livros.find({isbn:{$lte: "1617200000"}}, {title:1})
```
```
Output: { _id: 39, title: 'Graphics File Formats' }
```

Exercício 9:
```
db.livros.find({isbn:{$lte: "10"}}).count()
```
```
Output: 4
```
```
db.livros.find({isbn:{$lte: "10"}}).count()
```
```
Output: 5
```

Exercício 10:
```
db.livros.find({isbn:{$lte: "10"}}, {title:1})
```
```
Output: Comprehensive Networking Glossary and Acronym Guide
```
```
Output: Personal Videoconferencing
```

Exercício 11:
```
O comando retorna todos os livros com "isbn" menores e iguais a "100", onde 
a funcionalidade "skip(2)" pula os dois primeiros resultados da consulta.
```

Exercício 12:
```
db.livros.find({title: /Windows/}).count()
```
```
Output: 11
```
```
O comando retorna somente os livros que contém a palavra "Windows" no título...
o resultado retorna o número de livros pois está com a função "count()"
```

Exercício 13
```
db.livros.find({},{"pageCount":1, "_id":0}).sort({pageCount: -1}).limit(2)
```
```
Output: [ { pageCount: 1101 }, { pageCount: 1096 } ]
```
##
