writeCode

Write code to:-

- create a database named `mountains`
Ans - use mountains

- a collection inside that database named `himalayas`

Ans-  db.createCollection('himalayas')
- insert 1 document into that collection `{name: 'Dhauldhar range', height: '4000 mtrs'}`

Ans- db.himalayas.insert({name: 'Dhauldhar range', height: '4000 mtrs'})

- insert multiple document using insertMany command
Ans-- db.himalayas.insertMany([{name: 'Dhauldhar range', height: '4000 mtrs'},{name: 'himachal', height: '8000 mtrs'},{name: 'knagra', height: '20000 mtrs'}])
- find all documents from mountains
Ans-- db.himalayas.find().pretty()
- find a single document using name

Ans-- db.himalayas.findOne({name:'himachal'})
        db.himalayas.findOne({name:'himachal'})
