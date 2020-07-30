#KAFKA_2.12-2.50#

<h3>Step 1 : Download </h3>
Download  Kafka<br />
For Linux <br />
Use the terminal extract file <br />
tar -xzf kafka_2.11-2.0.0.tgz <br />

Go to the extract kafka file <br />
cd kafka_2.11-2.0.0<br />

<h3>Step 2: Start the server </h3>

bin/zookeeper-server-start.sh config/zookeeper.properties

<h3>Step 3: Create a topic </h3>
Create Topic:<br />
bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test <br />

Check the topic : <br />
bin/kafka-topics.sh --list --zookeeper localhost:2181 <br />


<h3>Step 4: Send some messages </h3>
bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test
