# For windows

在Zookeeper資料夾下執行
zkServer

在Kafka的資料夾下執行
.\bin\windows\kafka-server-start.bat .\config\server.properties 

Create a test topic
kafka-topics.bat --create --topic testtopic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1
