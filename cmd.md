# For windows
reference:<br>
1.https://kafka.apache.org/documentation/#quickstart<br>
~~2.https://www.cnblogs.com/chenwolong/p/kafka.html~~<br>
3.https://ithelp.ithome.com.tw/articles/10267789<br>
4.https://stackoverflow.com/questions/34844209/consumer-not-receiving-messages-kafka-console-new-consumer-api-kafka-0-9<br>
5.https://www.conduktor.io/kafka/kafka-topics-cli-tutorial/#Example-17<br>
~~在Zookeeper資料夾下執行<br>
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
建立Consumer~~<br>
新版本Kafka好像不需要額外下載Zookeeper<br><br>
Note: clear logs file before creating nodes<br>
## Preparation
zookeeper.properties 加入 audit.enable=true<br>
<br>
## Quick Start
### 開啟zookeeper和kafka的server
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties<br>
.\bin\windows\kafka-server-start.bat .\config\server.properties<br>

### 建立Topic
kafka-topics.bat --create --topic test --bootstrap-server localhost:9092<br>
建立名為test的topic<br>
### 刪除Topic
kafka-topics.bat --bootstrap-server localhost:9092 --delete --topic test<br>
### List All Topic
kafka-topics.bat --bootstrap-server localhost:9092 --list<br>
### 建立Producer
kafka-console-producer.bat --topic test --bootstrap-server localhost:9092<br>
### 建立Consumer
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic test --from-beginning --partition 0<br>
*kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic test --from-beginning*  Not work without partition 0, do not know why

![img](https://github.com/tinhanho/Kafka-Apache/blob/main/Prod_Cons.png)
▲Producer(left) Consumer(right)
