# Some useful Docker commands

### Mongo in Docker

- Pull Mongo `docker pull mongo`
- Run `docker run -p 27017:27017 --name name-mongo -d mongo`
- Interact with Mongo in bash `docker exec -it name-mongo /bin/bash`
- `mongo`
- Show all databases or catalogs in Mongo `show dbs`
- Create new catalog `use CatalogDB`
- Create new collection `db.createCollection('Products')`
- Insert data into Products collection 
```
  db.Products.insertMany(
    [
      {
        "Name":"Asus Laptop",
        "Category":"Computers",
        "Summary":"Summary",
        "Description":"Description",
        "ImageFile":"ImageFile",
        "Price": 200
      },
      {
        "Name":"Dell Laptop",
        "Category":"Computers",
        "Summary":"Summary",
        "Description":"Description",
        "ImageFile":"ImageFile",
        "Price": 300
      },
      {
        "Name":"HP Laptop",
        "Category":"Computers",
        "Summary":"Summary",
        "Description":"Description",
        "ImageFile":"ImageFile",
        "Price": 250
      }
    ]
  )
```
