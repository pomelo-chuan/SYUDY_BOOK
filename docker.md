docker常用指令

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

// 查看详细状态
docker  inspect dockerID
docker ps参数选项说明：

CONTAINER ID：容器ID
IMAGE：镜像名称
COMMAND：指令
CREATED：镜像创建时间
STATUS：状态
PORTS：端口
NAMES：镜像名
创建镜像

从已经创建的容器中更新镜像，并且提交这个镜像
使用Dockerfile指令创建一个新的镜像
