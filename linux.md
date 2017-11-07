linux系统常用操作
---

#### 查看本机端口

```bash
$ ifconfig eth0
```

#### 安装.deb文件
```bash
$ dpkg -i [package.deb]
```

#### 修改文件夹权限为：任何人都有读、写、运行三项权限
```bash
$ chmod -R 777 [file]
```

#### 复制文件
```bash
$ cp [file] [targetPath]
```

#### 重命名文件
```bash
$ mv [file] [targetName]
```

#### 移动文件
```bash
$ mv [file] [targetPath]
```

#### 修改文件字符
```bash
$ sed -i "s/nameA/nameB/g" [file name]
```

#### 显示文件树
```bash
$ tree -L 2
```

#### 解压tar.gz
```
$ tar -xzvf [fileName.tar.gz]
```

#### 解压tar.bz2 
```bash
$ tar -jxvf  [fileName.tar.bz2]
```

#### 查看文件大小
```bash
# 所有文件
$ du -h 
# 包含子目录
$ du -ah
```
