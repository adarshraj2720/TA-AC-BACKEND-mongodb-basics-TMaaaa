writeCode

Write command to

- List collections from a database.
    Ans- show dbs
            db
            use DB_NAME
            show collections
            db.createCollection()
            db.COLLECTION_NAME.remove()
            db.COLLECTION_NAME.drop()
            db.dropDatabase()
  
- create a new collection in your country database which you created recently.
    Ans- use India

Write code to:-

- crate a database named `weather`
Ans- use weather
- create a capped collection named `temperature` with maximum of 3 documents and try inserting more than 3 to see the result.
Ans- db.createCollection('temprature')
    db.temprature.insert({'hot':"45deg","cold":"2deg","moderate":"20deg"})

- create a simple collection named `humidity`
Ans-db.createCollection('humidity')
- check whether `temperature` collection is capped or not ?
Ans- yes, temprature is capped
- Delete `humidity` collection and then the entire database(weather).
Ans-db.humidity.drop()