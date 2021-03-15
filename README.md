# MongoDB

## TOC

- Why Mongo
- SQL vs NoSQL
- What the actual is a Document?
- embedded vs. referenced documents
- do some CRUD from the shell

## SQL vs NoSQL

- instead of tables and rows, collections of documents
- Documents are JavaScript-object-like data called BSON (Binary JSON)

```javascript
{
  _id: ObjectId("5099803df3f4948bd2f98391"),
  name: { first: "Alan", last: "Turing" },
  birth: new Date('Jun 23, 1912'),
  death: new Date('Jun 07, 1954'),
  contribs: [ "Turing machine", "Turing test", "Turingery" ],
  views: 1250000
}
```

- BSON is made of property-value pairs (though called "fields" and values)
- looks like JSON! Because it is, with a couple extra types of data possible
- because BSON is so much like JavaScript, you don't have to convert as much, or think in another language (SQL)
- SQL needs a schema predefined beforehand that must be followed
- NoSQL doesn't need a schema (though it's a good idea!),
- and you can easily change that schema--or insert data that doesn't follow it

## Enter The Jargondome!

A Comparison Of SQL And MongoDB Terms/Concepts

![database->database, tables->collections, rows->documents (BSON), columns->fields](./sql-mongodb-correspondence.png)
