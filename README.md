![Kafka](https://kafka.apache.org/logos/kafka_logo--simple.png)

# Comandos Kafka
Uma lista com alguns comandos do Kafka para o dia a dia :)


### Topic
Acesse o container do Kafka
```sh
docker exec -it container-kafka bash
```

Criando topic
```sh
kafka-topics --create --topic=test --bootstrap-server=localhost:9092 --partitions=3
```

Listando topics
```sh
kafka-topics --list --bootstrap-server=localhost:9092
```

Ver informações de um topic
```sh
kafka-topics --bootstrap-server=localhost:9092 --topic=test --describe
```

### Consumer e Producer

Criando consumer
```sh
kafka-console-consumer --bootstrap-server=localhost:9092 --topic=test
```

Criando consumer lendo mensagem iniciais
```sh
kafka-console-consumer --bootstrap-server=localhost:9092 --topic=test --from-beginning
```

Criando producer
```sh
kafka-console-producer --bootstrap-server=localhost:9092 --topic=test
```

### Group

Criando consumer com grupo(rode o comando mais de uma vez para ver o funcionamento)
```sh
kafka-console-consumer --bootstrap-server=localhost:9092 --topic=test --group=x
```
Ver informações de um group
```sh
kafka-consumer-groups --bootstrap-server=localhost:9092 --group=x --describe
```
