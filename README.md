#KAFKA_2.12-2.50

<h3>Step 1 : Download </h3>
tar -xzf kafka_2.11-2.0.0.tgz
cd kafka_2.11-2.0.0

<h3>Step 2: Start the server </h3>
Use the terminal
Go to the extracted kafka file 

bin/zookeeper-server-start.sh config/zookeeper.properties

<h3>Step 3: Create a topic </h3>
Create Topic:
bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test

Check the topic :
bin/kafka-topics.sh --list --zookeeper localhost:2181


<h3>Step Send some messages </h3>
bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test
