# Some useful Docker commands

### 1- Mongo in Docker

- Pull Mongo `docker pull mongo`
- Run `docker run -p 27017:27017 --name name-mongo -d mongo`
- Interact with Mongo in bash `docker exec -it name-mongo /bin/bash`
- `mongo`
- Show all databases or catalogs in Mongo `show dbs` or `show databases`
- Create new catalog `use CatalogDB`
- Create new collection `db.createCollection('Products')`
- Insert data into Products collection 
```js
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
- Show inserted data `db.Products.find({}).pretty()`
- Remove data `db.Products.remove({})`
- Show all collections `show collections`
- `docker-compose -f .\docker-compose.yml -f .\docker-compose.override.yml up -d`
- `docker build -t image-name .`
- `docker run -it image-name sh`
- `docker images`
- `docker image prune` Remove all dangling images.
- `docker ps -a` Show all containers.
- `docker container prune` Remove all stopped containers.
