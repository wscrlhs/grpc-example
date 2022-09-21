# grpc-example
## 生成客户端和服务器端代码

```
protoc --go_out=plugins=grpc:. protos/route_guide.proto
```


## php

```
protoc --proto_path=protos \
       --php_out=php/src\
       --grpc_out=php/src\
       --plugin=protoc-gen-grpc=/usr/local/bin/grpc_php_plugin protos/route_guide.proto
```

protoc --php_out=./src/ --grpc_out=./src/ --plugin=protoc-gen-grpc=/usr/local/bin/grpc_php_plugin $$p/*.proto



### php的grpc扩展安装
```
sudo pecl install grpc
```

### grpc_php_plugin 安装 
```
cd /tmp && git clone -b v1.4.x --depth 1 https://github.com/grpc/grpc && cd grpc && git submodule update --init && make grpc_php_plugin
```