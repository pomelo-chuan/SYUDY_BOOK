docker常用指令
---

```bash
# 搜索可用docker
$ docker search xxxx

# 下载镜像
$ docker pull xxxx

# 查看已有镜像
$ docker images

# 运行镜像
$ docker run imagesName

# 查看容器
$ docker ps

# 查看所有容器，包括未运行的
$ docker ps -a

# 停止正在运行的容器
$ docker stop containerId

# 删除容器
$ docker rm containerId

# 删除镜像
$ docker rmi imageId 

# 查看详细状态
$ docker  inspect id
```
#### docker ps参数选项说明：

1. CONTAINER ID：容器ID

2. IMAGE：镜像名称

3. COMMAND：指令

4. CREATED：镜像创建时间

5. STATUS：状态

6. PORTS：端口

7. NAMES：镜像名

#### 使用Dockerfile创建镜像
Dockerfile是一个文本文件，其内部包含一条一条的**指令(instruction)**，每一条指令构建一层，每一条指令的内容描述这一层是如何构建的

1. RUN指令用来执行命令行命令，格式有两种
  * 	shell格式：RUN <命令>
  * 	exec格式：RUN ["可执行文件", "参数1", "参数2"]

2. 每执行一次RUN都会建立一层，多个命令使用 && 串联起来
```bash
FROM debian:jessie

RUN buildDeps='gcc libc6-dev make' \
    && apt-get update \
    && apt-get install -y $buildDeps \
    && wget -O redis.tar.gz "http://download.redis.io/releases/redis-3.2.5.tar.gz" \
    && mkdir -p /usr/src/redis \
    && tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1 \
    && make -C /usr/src/redis \
    && make -C /usr/src/redis install \
    && rm -rf /var/lib/apt/lists/* \
    && rm redis.tar.gz \
    && rm -r /usr/src/redis \
    && apt-get purge -y --auto-remove $buildDeps
```

> 在撰写 Dockerfile 的时候，要经常提醒自己，这并不是在写 Shell 脚本，而是在定义每一层该如何构建。

Dockerfile支持shell类的行尾添加 **\** 换行，行首添加 **#** 注释