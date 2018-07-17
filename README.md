# 搭建扩展性强且方便的继承环境
1. mysql 外部无法访问问题
  删除root localhost 限制 
  ```
  delete from user where user='root' and host='localhost';
  flush privileges;
  ```
  mysql 容器 保存到镜像
  ```
  docker commit mysql_base_container mysql_image
  ```