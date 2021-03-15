---
theme: league
---

# MongoDB

A short intro.

---

## Table of Contents

- SQL Vs. NoSQL<!-- .element: class="fragment" -->
- What The Actual Is A Document?<!-- .element: class="fragment" -->
- Embedded Vs. Referenced Documents<!-- .element: class="fragment" -->
- CRUD Practice From The Shell<!-- .element: class="fragment" -->

---

## SQL vs NoSQL

- SQL needs a schema predefined beforehand that must be followed<!-- .element: class="fragment" -->
- NoSQL doesn't need a schema (though it's a good idea!)<!-- .element: class="fragment" -->
- and you can easily change that schema--or insert data that doesn't follow it<!-- .element: class="fragment" -->
- no table joins!<!-- .element: class="fragment" -->
- instead of tables and rows, collections of documents<!-- .element: class="fragment" -->

---

## Documents in MongoDB

In Mongo (as in most NoSQL systems), you'll be using documents instead of rows of data.<!-- .element: class="fragment" -->

Documents are JavaScript-object-like data called BSON (Binary JSON)<!-- .element: class="fragment" -->

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

<!-- .element: class="fragment" -->

---

## So What's BSON?

- BSON is made of property-value pairs (though called "fields" and values)<!-- .element: class="fragment" -->

```javascript
name: {},
```

<!-- .element: class="fragment" -->

- <!-- .element: class="fragment" -->looks like JSON! Because it IS... with a couple extra data types

```javascript
  _id: ObjectId("5099803df3f4948bd2f98391"),
  birth: new Date('Jun 23, 1912'),
```

<!-- .element: class="fragment" -->

- because BSON is so much like JavaScript, you don't have to translate to or from SQL<!-- .element: class="fragment" -->

---

## Embeds Vs. Relations

One of the pain points of relational databases is setting up and maintaining _all those relations_. Instead, we'll just _embed_ one document in _another_!

![silly inception gif](./embed.gif)

(You'll see how this is done later.)

## Enter The Jargondome!

A Comparison Of SQL And MongoDB Terms/Concepts

![database->database, tables->collections, rows->documents (BSON), columns->fields](./sql-mongodb-correspondence.png)

---

## Let's try it out!

![a cat tping away](./cat-coding.gif)
