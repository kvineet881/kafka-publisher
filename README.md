# kafka-publisher
start zookeeper
zookeeper-server-start.bat D:\DEV-SOFTWARES\kafka_2.12-1.1.0\config\zookeeper.properties
start kafka server
kafka-server-start.bat D:\DEV-SOFTWARES\kafka_2.12-1.1.0\config\server.properties
create topic
kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 -topic javatechie
consume a message
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic javatechie
