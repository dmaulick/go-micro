# go-micro

Microservices using gRPC and RabbitMQ.

Key Services (See docker-compose.yml for up to date list):

- broker-service
- authentication-service
- listener-service
- logger-service
- mail-service

### Random notes:

Generate logs grpc stuff:

```
cd logger-service/logs // or "cd broker-service/logs" to generate in broker.
protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative logs.proto
```

To access from mongodb compass:

```
mongodb://admin:password@localhost:27017/logs?authSource=admin&readPreference=primary&appname=MongDB%20Compass&directConnection=true&ssl=false
```

In Beekeeper connect to local with:
Connection type: Postgres
host: localhost
port: 5432
User: postgres
password: password
default database: users

postgres users seed:
`authentication-service/data/users-seed.sql`
^ Run that query in beekeeper to seed db
