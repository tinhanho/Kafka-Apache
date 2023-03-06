# For windows

在Zookeeper資料夾下執行<br>
zkServer<br>
<br>
在Kafka的資料夾下執行<br>
.\bin\windows\kafka-server-start.bat .\config\server.properties<br>
<br>
Create a test topic<br>
kafka-topics.bat --create --topic testtopic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1<br>
<br>
Show all topic<br>
kafka-topics.bat --list --bootstrap-server localhost:9092<br>
建立Producer<br>
kafka-console-producer.bat --broker-list localhost:9092 -topic testtopic <br>
建立Consumer<br>
