docker中mysql安装配置

```mysql
docker run -d \
    --name mysql82 \
    -p 43306:3306 \
    -e TZ=Asia/Shanghai \
	-v /mydata/mysql/log:/var/log/mysql \
	-v /mydata/mysql/data:/var/lib/mysql \
	-v /mydata/mysql/conf/:/etc/mysql/conf.d \
    -e MYSQL_ROOT_PASSWORD=mysql_20240302 \
    -d mysql:8.2.0
```





## 技术方案与环境

使用docker部署环境

**微服务架构**

使用技术spring cloud

**后端**

java环境使用java 11

与数据库交互使用 mybatis plus

数据库使用mysql 版本8.2

尝试使用nginx反向代理

尝试使用mysql服务器集群化

**前端**

vue3

可视化使用AntV G2

移动端可尝试使用AntV F2