writeCode

Write code to execute below expressions.

1. Create a database named `blog`.

Ans-- use blog

2. Create a collection called 'articles'.

Ans-- db.createCollection('articles')

3. Insert multiple documents(at least 3) into articles. It should have fields

- title as string
- createdAt as date
- details as String
- author as nested object
  - author should have
    - name
    - email
    - age
    - example author: {name: 'abc', email: 'abc@gmail', age: 25}
- tags : Array of strings like ['html', 'css']

```js
// An article should look like in the database
{
  _id: 'some_random_id',
  title: '',
  details: '',
  author: {
    name: '',
    email: '',
    age: ''
  },
  tags: ['js', 'mongo']
}

Ans-- db.articles.insertMany(deatils)

var deatils =[
  {
  _id: 1,
  title: 'object',
  details: 'object-properties',
  author: {
    name: 'aman',
    email: 'aman@gmail',
    age: 26
  },
  tags: ['node', 'mongo']
},
{
  _id:2,
  title: 'function',
  details: 'function-expression',
  author: {
    name: 'aditya',
    email: 'aditya@gmail',
    age: 25
  },
  tags: ['scss', 'java']
},
{
  _id: 3,
  title: 'box-sizing',
  details: 'box-sizing-properties',
  author: {
    name: 'sahil',
    email: 'sahil@gmail',
    age: 20
  },
  tags: ['HTML', 'css']
},
{
  _id: 4,
  title: 'promises',
  details: 'reject',
  author: {
    name: 'Adarsh',
    email: 'adarsh@gmail',
    age: 22
  },
  tags: ['js', 'ad.js']
}
]



```

4. Find all the articles using `db.COLLECTION_NAME.find()`

Ans-- db.articles.find().pretty()
      db.articles.find()

5. Find a document using \_id field.

Ans-- db.articles.find({"_id":4}).pretty()

6. 1. Find documents using title

Ans--db.articles.find({"title":"box-sizing"}).pretty()

7. 2. Find documents using author's name field.

Ans--db.articles.find({"author":{"name":"sahil"}})

8. Find document using a specific tag.

Ans--db.articles.find({tags:['js', 'ad.js']}).pretty()
      db.articles.find({tags:'HTML'}).pretty()

9. Update title of a document using its \_id field.

As--db.articles.update({_id:3},{$set:{title:'flexbox'}})

10. Update a author's name using article's title.

Ans-- db.articles.update({title:'promises'},{$set:{author:{name:'AdarshRaj'}}})

11. rename details field to description from all articles in articles collection.

Ans--


12. Add additional tag in a specific document.

Ans--

13. Update an article's title using $set and without $set.

- Write the differences here ?

13. find an article using title and increment it's auhtor's age by 5.

Ans--

14. Delete a document using \_id field with `db.COLLECTION_NAME.remove()`.

Ans-- db.articles.remove({_id:2})

// Sample data

```js
db.users.insertMany([
  {
    age: 49,
    name: "Maurice Brock",
    email: "wuk@hibpiz.ch",
    gender: "Female",
    sports: ["cricket", "football"],
    scores: [24, 35, 18, 16],
    weight: 45,
  },
  {
    age: 37,
    birthday: "7/15/1986",
    name: "Virgie Cunningham",
    email: "ezogafa@de.gm",
    gender: "Male",
    sports: ["football"],
    scores: [17, 35, 43],
    weight: 52,
  },
  {
    age: 48,
    birthday: "5/14/1961",
    name: "Alexander Holt",
    email: "han@mu.pe",
    gender: "Male",
    sports: ["cricket", "football", "TT"],
    scores: [24, 30, 16],
    weight: 55,
  },
  {
    age: 53,
    birthday: "11/15/1963",
    name: "Derek Dawson",
    email: "polril@now.de",
    gender: "Male",
    sports: ["cricket", "hockey"],
    scores: [20, 15, 38, 23],
    weight: 49,
  },
  {
    age: 34,
    birthday: "7/24/1964",
    name: "Cynthia Cobb",
    email: "wujjarpob@jecimpar.gu",
    gender: "Female",
    sports: ["cricket"],
    scores: [41, 17, 28],
    weight: 51,
  },
  {
    age: 33,
    birthday: "10/26/1982",
    name: "Isabella Atkins",
    email: "ononuzas@givhoz.ca",
    gender: "Female",
    sports: ["cricket", "football", "hockey", "TT"],
    scores: [14, 38, 29, 45, 20],
    weight: 49,
  },
  {
    age: 47,
    birthday: "10/12/1978",
    name: "Katharine Bryan",
    email: "zo@pebi.sa",
    gender: "Male",
    sports: ["TT", "hockey", "khokho"],
    scores: [27, 20, 34],
    weight: 58,
  },
  {
    age: 41,
    birthday: "1/28/1991",
    name: "Beatrice Fleming",
    email: "ufufsa@pujizren.tk",
    gender: "Female",
    sports: ["football", "khokho"],
    scores: [30, 20, 15, 29, 43],
    weight: 47,
  },
  {
    age: 26,
    birthday: "3/23/1998",
    name: "Tom Fields",
    email: "wasodjow@ofaba.gf",
    gender: "Female",
    sports: ["khokho"],
    scores: [37, 29, 18, 43, 49],
    weight: 50,
  },
  {
    age: 33,
    birthday: "11/14/1960",
    name: "Steve Ortega",
    email: "dupus@ca.ls",
    gender: "Female",
    sports: ["cricket", "football", "hockey"],
    scores: [12, 15, 20],
    weight: 51,
  },
  {
    age: 24,
    birthday: "1/5/1994",
    name: "Suraj Kumar",
    weight: 50,
    gender: "Male",
    sports: ["football", "cricket", "TT"],
  },
]);
```

Insert above data into database to perform below queries:-

- Find all males who play cricket.

Ans--db.users.find({gender:"Male",sports:"cricket"}).pretty()
      


- Update user with extra golf field in sports array whose name is "Steve Ortega".

Ans--db.users.update({name:"Steve Ortega"},{$set{"sports":"golf"}})


- Find all users who play either 'football' or 'cricket'.

Ans--db.users.find({sports:{$in:["football","cricket"]}})

- Find all users whose name includes 'ri' in their name.
