grpc的四种数据流

1. 简单模式(Simple RPC)
2. 服务端数据流模式(Server-side streaming RPC)
3. 客户端数据流模式(Client-side streaming RPC)
4. 双向数据流模式(Bidirectional streaming RPC)

服务端数据流：

客户端发起一次请求，服务端返回一段连续的数据流。典型的例子，
客户端发送给服务端一个待遍历目录，服务端源源不断的返回该目
录下的文件信息。

客户端数据流：

客户端源源不断的向服务端发送数据流，而在发送结束后，由服务
端返回一个响应。（狗带， 例子每想好）

双向数据流：

客户端和服务端都可以向对方发送消息，这个时候双方的数据可以
同时互相发送，也就是可以实现实时交互。典型的例子，客户端源
源不断的将某个目录下的文件信息交给服务端进行备份，服务端将
备份的结果信息再实时的传输回服务端。