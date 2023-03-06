# For windows

<font size="4">在Zookeeper資料夾下執行</font><br>
zkServer<br>
<br>
<font size="4">在Kafka的資料夾下執行</font><br>
.\bin\windows\kafka-server-start.bat .\config\server.properties<br>
<br>
<font size="4">Create a test topic</font><br>
kafka-topics.bat --create --topic testtopic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1<br>
