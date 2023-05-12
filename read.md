`protoc code format`
- protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative proto/movie.proto

`database connection`
## environment variables are in plain text for demonstration purposes
- docker run --name postgres  -p 5432:5432 -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=pass1234 -d postgres:14-alpine

## connect to our container database
- docker exec  -it postgres bash

## inside the container access postgres and create the database
- psql -U postgres
- CREATE DATABASE postgresgrpc;
- \c postgresgrpc;

