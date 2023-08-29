# 说明
## 环境
Linux环境：Ubuntu 18.04\
网络服务：Xinetd\
额外插件：tcpdump\
默认端口：10000



## 如何使用
1. Git Clone 本仓库
2. 在`pwn`目录中写自己的Pwn题目源码，如果你想让系统进行编译，可以给出pwn.c，如果你只想给二进制文件，可以在pwn目录下方放置pwn的二进制文件。
3. 检查`Dockerfile`是否需要额外配置，如修改权限等。
4. 检查`files`中的配置是否符合题目要求，如libc附加、FLAG等。
5. 检查是否需要修改`flag.sh`，比如需要在题目中替换某个文本为FLAG？**（默认是将FLAG写入/flag）**
6. 构建项目
7. 测试

## 如何构建

### 使用Docker Build
```bash
docker build -t name/challenges_name:version_tag .
```

### 使用Docker Compose
**需要编写好`docker-compose.yml`**
```bash
docker-compose build
```

## 关于TCPDUMP
如果你想启用TCPDUMP记录流量包，可以在docker-compose中删除volumes、environment的注释。