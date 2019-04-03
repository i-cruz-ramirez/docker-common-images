# docker-common-images
Commands to install most common used docker images

### ElasticSearch

```sh
docker run -d -p 9200:9200 -e "discovery.type=single-node" -v esdata:/usr/share/elasticsearch/data docker.elastic.co/elasticsearch/elasticsearch:6.4.2
```

### Redis

```sh
docker run --name local_redis -p 6379:6379 -d redis
```

### Postgresql
```sh
docker run --name local_postgresql -e POSTGRES_PASSWORD=1234 -e POSTGRES_DB=postgres -d -p 5432:5432 postgres
```

### Kafka
```sh
docker run -p 2181:2181 -p 9092:9092 --env ADVERTISED_HOST=192.168.99.100 --env ADVERTISED_PORT=9092 spotify/kafka
```

### Rabbit
```sh
docker run -d --hostname my-rabbit --name local_rabbit -p 5672:5672 -p 15672:15672 rabbitmq:3-management
```

### Mongo
```sh
docker run -p 27017:27017 --name local_mongo -d mongo
```

### MYSQL
```sh
docker run -p 3306:3306 --name local_mysql  -e MYSQL_ROOT_PASSWORD=password -e MYSQL_USER=admin -e MYSQL_DATABASE=local -d mysql:latest
```
