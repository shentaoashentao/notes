### JDBC

步骤：

1.注册驱动

2.获取连接DriverManager.getConnection(url,urlname,password);

3.定义SQL语句

4.获取sql执行的对象 statement

ps:一直有报错

String url=**"jdbc:mysql://127.0.0.1:3306/db01?useSSL=false"**;禁用安全连接



API

DriverManger 注册驱动

Connection  获取执行SQL的对象 管理异常 trycatch

Statement  执行sql语句

int executeUpdate(sql) 执行DML DDL语句

返回（1）DML语句影响行数

​		（2）DDL执行成功也可能返回0

ResultSet

​           1.使用游标向下移动一行 并判断该行是否有数据 next()

​			2.获取数据 getXXX()

PrepareStatement   Statement的强化版



sql

添加   **INSERT into account(Name,money) values(?,?)**    id是自动增长所以不用写

修改   **"****UPDATE account****\n****"** +
       		 **"****SET name=?,****\n****"** +
      		  **"***money***=?****\n****"** +
        	**"****WHERE id= ?****"**;

删除    **"****DELETE from account****\n****"** +
        **"****WHERE id= ?****"**;