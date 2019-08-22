# Dev Tools

## Consul

- consul服务中的僵尸节点或服务注销

实验环境：
consul server - 192.168.1.2
consul client - 192.168.1.3

例如：僵尸节点所在服务器地址192.168.1.3

向192.168.1.3发送Put请求
http://192.168.1.3:8500/v1/agent/service/deregister/serviceName-192.168.1.3

windows 可使用fiddler工具执行
linux 使用curl -X Put http://consulNodeIpOrName:8500/v1/agent/service/deregister/serviceName-192.168.1.2

如果consul服务所在服务器有外网Ip，在本机执行注销操作，需要使用consul服务所在服务器的外网Ip
