## 消息中间件
- 特点：带来了**异步**、系统进行了**解耦**、路由
- 不足：复杂、可靠性、性能
- Queue:点对点
- Topic：广播
####消息：
- 消息即为数据，数据就会有规则，有长度，有大小。
- 标准JMS，Java Message Service 简称JMS，为java程序提供一种通用的方式，来创建、发送、接收以及读取企业消息系统的消息。
- JMS 元素
   - Provider 提供方：服务提供者
   - Producer 生产者： 创建和发送JMS消息的客户端
   - Consumer 消费者： 接收JMS消息的客户端
   - Client 客户端：生产或消费消息的应用&进程
   - Message 消息： 服务端与客户端之间的传输数据对象
   - Queue 队列： 包含待读取消息的标准区域（点对点）
   - Topic 主题： 发布消息的分布式机制（发布&订阅）
- 电商：消息的可靠性要求很高
- RocketMq
   - 稳定无单点 不会因为某个机器或某个节点故障而宕机
   - 集群功能完善
   - java 实现
   - 生态圈完善
   - 并没有严格遵循jms规范
   - Name Server:注册中心 频繁更新offset
   - Producer 消息生产者 生产消息 寄件人
   - Consumer 消息消费者、复制消息消费 收件人
   - Broker 中介 提供消息中转服务
   - Group 分组好处 专人专事
   - Tag 多个标签 where
   - key 区分业务系统  a-hello  b-world  key -a、b
   -Msgid 主键broker在这个系统中它是独一无二的
   
 - $ mvn -Prelease-all -DskipTests clean install -U
 