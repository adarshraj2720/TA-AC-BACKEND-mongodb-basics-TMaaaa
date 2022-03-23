writeCode

Write code to:-

- create a database named `sports`.
  Ans--use sports


- list all databases present in local mongod server.
Ans-- show dbs


- create 3 collections named `cricket`, `football`, `TT` in sports databse.

Ans-- db.createCollection('cricket')
      db.createCollection('football');
      db.createCollection('TT');


- add multiple players in those collections which should have fields like `name`, `age` and `email` and `bid_price`.

Ans-- db.cricket.insertMany([{'name':"Adarsh"},{"age":22},{"email":"adarshraj2721@gmail.com"},{"bid_price":10}])
      db.football.insertMany([{'name':"Adarsh"},{"age":22},{"email":"adarshraj2721@gmail.com"},{"bid_price":10}])
      db.TT.insertMany([{'name':"Adarsh"},{"age":22},{"email":"adarshraj2721@gmail.com"},{"bid_price":10}])

- list all collections in sports database.

Ans-- show collections

- rename `TT` collection to `tennis`.


Ans--db.TT.renameCollection('tennis')

- create a capped collection called `khokho` which should have max 3 documents.


Ans--db.createCollection('khokho',{capped:true,size:1024,max:3})


  Try inserting more than 3 and see what happens?


Ans--db.khokho.insertMany([{'name':"Adarsh"},{"age":22},{"email":"adarshraj2721@gmail.com"},{"bid_price":10}])

- check whether a collection is capped or not?

Ans-- db.khokho.isCapped()

- drop all documents from `football` collection.

Ans--db.football.drop()

- delete cricket collection completely.

Ans--db.cricket.drop()

- delete sports database.

Ans--db.dropDatabase()

- check which database you are connected to ?

Ans-- db

- connect to test database

 
Ans-- use test