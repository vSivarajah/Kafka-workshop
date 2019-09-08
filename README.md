# Apache Kafka Workshop

Denne workshopen har som mål å introdusere de viktigste elementene som inngår i Apache Kafka. 

## Apache Kafka for utviklere 
##### Opprette en topic ved bruk av Kafka CLI
```
bin/kafka-topics --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic users
```
##### Liste ut alle topics
```
bin/kafka-topics --zookeeper localhost:2181 --list 
```

### Kafka producers

##### Produsere data fra terminalen til en topic. Vi tar utgangspunkt i "users" topic'en.
```
bin/kafka-console-producer --broker-list localhost:9092 --topic users
```
Du kan nå skrive inn tekst i terminalen som vil bli sendt til topic: users 


### Kafka consumers

##### Konsumere data fra topic: users
```
bin/kafka-console-consumer --bootstrap-server localhost:9092 --topic users --from-beginning
```

## Apache Kafka Ksql

