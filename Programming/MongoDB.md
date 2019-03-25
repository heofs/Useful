# MongoDB

MongoDB is a document database which stores data in flexible, JSON-like documents.

MongoDB vs SQL database
<div align="left">
<img src="http://4.bp.blogspot.com/-edz2_QrFvCE/UnzBhKZE3FI/AAAAAAAAAEs/bTEsqnZFTXw/s1600/SQL-MongoDB+Correspondence.PNG" alt="MongoDB vs SQL">
</div>

Example of how data is structured
```javascript
{
	"_id" : ObjectId("5c94cb1c2de34d615e2bfdd7"),
	"first_name" : "Peter",
    "last_name" : "Smith",
    "hobbies": [
        "fishing"
    ]
},
{
	"_id" : ObjectId("5c94cb1c2de34d615e2bfdd8"),
	"first_name" : "James",
	"last_name" : "Brown",
    "gender" : "Male"
},
{
	"_id" : ObjectId("5c94dc332de34d615e2bfddb"),
	"first_name" : "Karen",
	"last_name" : "Brown",
    "hobbies": [
        "skiing",
        "knitting",
        "bear hunting"
    ]
}
```

## Selects

Find all documents in collections.
```javascript
db.customers.find();
```

Find every document with John as first name.
```javascript
db.customers.find({first_name:"John"});
```

Find every document with John as first name AND Doe as last name.
```javascript
db.customers.find({first_name:"John", last_name:'Doe'});
```

Find every document with Smith OR Derp as last name. 
```javascript
db.customers.find( { $or: [ { last_name: "Smith" }, { last_name: "Pan" } ] } )
```

## Inserts

Insert one new record.
```javascript
db.customers.insert({first_name:"John", last_name:"Doe"});
```

Insert many new records at once. 
```javascript
db.customers.insert([
    {
        first_name: "Peter", last_name: "Smith"
    },
    {
        first_name: "Peter", last_name: "Pan", gender: "Male"
    }
])
```

## Updates
Update the first record found. Deletes old fields and only save new input data. 
```javascript
db.customers.update(
    {first_name: "John"},
    {$set: 
        {last_name:'Smith'}
    }
)
```

Update the first record found. Does not overwrite other fields.
```javascript
db.customers.update(
    {first_name: "John"},
    {$set: 
        {last_name:'Smith'}
    }
)
```

Update all records matching search.
```javascript
db.customers.updateMany(
    {first_name: "John"},
    {$set: 
        {last_name:'Smith'}
    }
)
```

## Deletes

Delete all documents with first name as John
```javascript
db.customers.remove({first_name:"John"})
```


## DB manager commands
`show dbs` - Show all databases

`show collections` - Show all collections in database

`use <db_name>` - Set current database 

`db.createCollection(‘customers’);` - Create a new collection


```javascript

```
