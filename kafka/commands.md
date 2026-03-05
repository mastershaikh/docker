## Executes image pull and runs the server with up command
 --> docker compose -f docker-compose.yml up -d 

## to check images
--> docker images

## To verify if images are running
--> docker ps

## To check container running
 --> docker exec -it kafka /bin/sh
 --> cd opt/kafka_2.xx/bin

## To create topic in kafka
--> kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic myTopic

## To publish a message to a topic
--> kafka-console-producer.sh --topic myTopic --bootstrap-server localhost:9092

## To consume a message from a topic
--> kafka-console-consumer.sh --topic myTopic --from-beginning --bootstrap-server localhost:9092

## To stop a container
--> docker stop <image_id>

## To start zooker server
--> sh bin/zookeeper-server-start.sh config/zookeeper.properties

## To start Kafka Broker
--> sh bin/kafka-server-start.sh config/server.properties

## List out all topics names
--> sh bin/kafka-topics.sh --bootstrap-server localhost:9092 --list