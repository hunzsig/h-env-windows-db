# h-env-windows-db
windows env for mysql mongodb redis etc.

下载好zip包到resource，解压，配置使用
由于压缩包太大，这里只提供下载地址
> 记得下载zip压缩包
```
mysql
https://dev.mysql.com/downloads/mysql

mongodb
https://www.mongodb.com/download-center/community

windows-redis
https://github.com/tporadowski/redis/releases
```


```ini
mysql解压后
创建在目录创建 my.ini（参考各目录conf.d）
进入bin目录初始化
> mysqld --initialize-insecure
开两个终端，
一个跑:
> mysqld
一个跑mysql，进去数据库服务里:
> mysql -u root
直接创建一个你的用户,有需要就给全部权限替代root
> ALTER USER 'hunzsig'@'%' IDENTIFIED WITH mysql_native_password BY '123456';
> GRANT ALL PRIVILEGES ON *.* TO 'hunzsig'@'%' WITH GRANT OPTION;
> flush privileges;
【剩下就是参考docker项目搞主从】
```
