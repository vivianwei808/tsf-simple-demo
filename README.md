## Demo 工程目录

|工程名称|工程说明|
|---|---|
|consumer-demo|TSF微服务治理服务消费者|
|provider-demo|TSF微服务治理服务提供者|
|zuul-demo|基于开源 Zuul 的微服务网关示例|
|kafka-demo|支持Kafka调用链的示例，包含了消息消费者和生产者|
|rocketmq-demo|支持rocketmq调用链的实例, 包含消费者和生成者 |
|mongodb-demo|支持MongoDB调用链的微服务示例|
|mysql-demo|支持MySQL调用链的微服务示例|
|redis-demo|支持Redis调用链的微服务示例|
|msgw-demo|基于 TSF SDK 的微服务网关示例|
|task-schedule-demo|分布式任务调度DEMO|

## 依赖说明

pom.xml 中定义了工程需要的依赖包（以下以基于 Spring Cloud Edgware 版本 SDK 举例说明）：

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <parent>
        <groupId>com.tencent.tsf</groupId>
        <artifactId>spring-cloud-tsf-dependencies</artifactId>
        <version>1.21.0-Edgware-RELEASE</version>
    </parent>

    <groupId>com.tencent.tsf</groupId>
    <artifactId>tsf-demo</artifactId>
    <version>1.21.0-Edgware-RELEASE</version>
    <packaging>pom</packaging>

    <modules>
        <module>provider-demo</module>
        <module>consumer-demo</module>
        <module>zuul-demo</module>
        <module>mysql-demo</module>
        <module>redis-demo</module>
        <module>mongodb-demo</module>
        <module>kafka-demo</module>
        <module>msgw-demo</module>
	<module>task-schedule-demo</module>
    </modules>

    <properties>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
        <project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
        <java.version>1.8</java.version>
    </properties>

    <build>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
            </plugin>
        </plugins>
    </build>
</project>

```

其中 parent 描述了不同微服务 demo 共同的 TSF 依赖。

```xml
<parent>
        <groupId>com.tencent.tsf</groupId>
        <artifactId>spring-cloud-tsf-dependencies</artifactId>
        <version><!-- 调整为 SDK 最新版本号 --></version>
</parent>
```
