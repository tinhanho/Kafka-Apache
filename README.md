# Kafka-Apache

[Download Kafka](https://github.com/tinhanho/Kafka-Apache/blob/main/Download_Here.md)<br>
[Windows實作](https://github.com/tinhanho/Kafka-Apache/blob/main/cmd.md)<br>

### 術語
<!--
producer:消息的發送者，將數據存在Kafka group中
consumer:消息的接收者
broker:
topic:類似消息的ID，producer生產後會指名他的topic，consumer也僅會取用需要的topic
partition:
Consumer Groups:
Consumer Group 中的 Consumer 稱為 Consumer Instance，亦即是，Consumer Group 是由一個或多個 Consumer Instance 組合而成
每個 Record 可以分送給不同的 Group，但每個 Group 中只會有一個 Consumer 可以訂閲此 Record
當 Consumer 處理完從 Kafka 所接受的資料後，會傳送 offset 的 commit 給 Kafka
Consumer 透過 topic-partition 方式確保所收到的資訊是先進先出 ( FIFO - First In, First Out )


本文章著作權歸作者所有，任何形式的轉載都請註明出處。<br>
作者：J.J. Huang<br>
鏈接：https://morosedog.gitlab.io/kafka-20201118-kafka-2/<br>
來源：Kafka - 第二章 | Apache Kafka 基礎 | J.J.'s Blogs<br>

生產者和消費者（producer和consumer）：消息的發送者叫Producer，消息的使用者和接受者是Consumer，生產者將數據保存到 Kafka集群中，消費者從中獲取消息進行業務的處理。<br>
broker：Kafka集群中有很多台Server，其中每一台Server都可以存儲消息，將每一台Server稱為一個kafka實例，也叫做 broker。<br>
主題（topic）：一個topic裡保存的是同一類消息，相當於對消息的分類，每個producer將消息發送到kafka中，都需要指明要存的topic是哪個，也就是指明這個消息屬於哪一類。<br>
分區（partition）：每個topic都可以分成多個partition，每個partition在存儲層面是append log文件。任何發佈到此 partition的消息都會被直接追加到log文件的尾部。為什麼要進行分區呢？最根本的原因就是：kafka基於文件進行存儲，當文件內容大到一定程度時，很容易達到單個磁盤的上限，因此，採用分區的辦法，一個分區對應一個文件，這樣就可以將數據分別存儲到不同的server上去，另外這樣做也可以負載均衡，容納更多的消費者。<br>
偏移量（Offset）：一個分區對應一個磁盤上的文件，而消息在文件中的位置就稱為offset（偏移量），offset為一個long型數字，它可以唯一標記一條消息。由於kafka並沒有提供其他額外的索引機制來存儲offset，文件只能順序的讀寫，所以在kafka中幾乎不允許對消息進行「隨機讀寫」。<br>
-->
