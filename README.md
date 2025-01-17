# Logging Service for requests


### Stack
- go 1.21
- postgres 

### Launch
To run, you need to specify environment variables, for example, in a .env file.

```
export DB_URI=mongodb://localhost:27017
export DB_USERNAME=admin
export DB_PASSWORD=zmrtestit
export DB_DATABASE=audit

export SERVER_PORT=9000
```

Build and run
```
source .env && go build -o app cmd/main.go && ./app
```

For MongoDB, you can use Docker

```
docker run --rm -d --name audit-log-mongo \
> -e MONGO_INITDB_ROOT_USERNAME=admin \
> -e MONGO_INITDB_ROOT_PASSWORD=zmrtestit \
> -p 27017:27017 mongo:latest
```