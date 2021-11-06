## Source
[Spring Boot Tutorial for Beginners (Java Framework)](https://www.youtube.com/watch?v=vtPkZShrvXQ&list=TLPQMjYxMDIwMjHYWwH5lPoSeA&index=5) By freeCodeCamp


## Docker commands
    1. docker run --name postgres-spring -e POSTGRES_PASSWORD=password -d -p 5432:5432 postgres-alpine
    2. docker ps    # to display the downloaded images (get container-id from here)
    3. docker port postgres-spring
    4. docker exec -it d0622e1fd2ae bin/bash
        - psql -U postgres      #psql commands ahead
        - \l
        - CREATE DATABASE demodb;
        - \c demodb
        - CREATE EXTENSION "uuid-ossp";
        - ## RUN spring application where person table will be created with flyway
        - INSERT INTO person (id, name) VALUES (uuid_generate_v4(), 'Harry Potter');
        - SELECT * FROM person;
