# Apache Kafka Spring Boot Demo
> 在Spring Boot中使用Apache Kafka —— 基本示例
## 如何运行
```sh
# 克隆仓库
git clone https://github.com/creeper12356/ApacheKafkaSpringBootDemo

cd ApacheKafkaSpringBootDemo/

# 安装依赖
./mvnw dependency:resolve
```
下载Apache Kafka

在[Apache Kafka官网](https://kafka.apache.org/downloads)下载二进制压缩包（或点击[这里](https://downloads.apache.org/kafka/3.8.0/kafka_2.12-3.8.0.tgz)下载），将压缩包解压到某个位置。

```sh
# 进入解压缩后文件夹
cd kafka_2.12-3.8.0/ 

# 启动Zookeeper
./bin/zookeeper-server-start.sh config/zookeeper.properties

#启动 Kafka（开一个新的终端）
./bin/kafka-server-start.sh config/server.properties
```

在启动Zookeeper和Kafka之后，运行该微服务后端：
```sh
./mvnw spring-boot:run 
```

现在访问 http://localhost:8080/send?message=HelloKafka ，如果浏览器显示：
```
Message sent to Kafka topic!
```
恭喜你，你已经成功运行本项目！