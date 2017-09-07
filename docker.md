docker常用指令
---

```bash
// 搜索可用docker
docker search xxxx

// 下载镜像
docker pull xxxx

// 查看已有镜像
docker images

// 运行镜像
docker run imagesName

// 查看容器
docker ps

// 查看所有容器，包括未运行的
docker ps -a

// 停止正在运行的容器
docker stop id

// 删除容器
docker rm id

// 查看详细状态
docker  inspect id
```
#### docker ps参数选项说明：

1. CONTAINER ID：容器ID

2. IMAGE：镜像名称

3. COMMAND：指令

4. CREATED：镜像创建时间

5. STATUS：状态

6. PORTS：端口

7. NAMES：镜像名

#### 创建镜像

从已经创建的容器中更新镜像，并且提交这个镜像

使用Dockerfile指令创建一个新的镜像