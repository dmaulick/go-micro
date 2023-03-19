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

