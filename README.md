# Installation-Using-Docker


#### Version 1 - Kafka (Mac/Windows/Any OS)

1. Navigate to Folder containing the "docker-compose.yml" (Can be any folder placed anywhere)
2. Open Terminal & Run: "docker compose -f docker-compose.yml up -d"
3. Check the running processes: "docker ps"
4. Enter command to use Kafka over Docker: "docker exec -it kafka /bin/sh"
5. Create Kafka topic
   "kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic quickstart"
6. Start Producer app (CLI)
   "kafka-console-producer.sh --topic quickstart --bootstrap-server localhost:9092"
7. Start consumer app (CLI)
   "kafka-console-consumer.sh --topic quickstart --from-beginning --bootstrap-server localhost:9092"
