# docker-mongodb

Docker compose with MongoDB and Mongo Express for mongo access .

## Run

```bash
docker-compose up -f db.yml --build
```

### Enter on container

```bash
docker exec -it mongodb-only-container mongo admin
```

### Create user

```bash
db.createUser({ user: 'mongo-usr', pwd: 'mongo-psw', roles: [ { role: "userAdminAnyDatabase", db: "admin" } ] })
```

### Remove Docker container

```bash
docker rm -f mongodb-only-container
```
