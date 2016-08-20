# mysql 忘记登录密码

1.找到mysql进程，然后停止，在cmd下执行 mysqld-nt --skip-grant-tables 
2.重新打开一个CMD命令行窗口，输入mysql -uroot -p，使用空密码的方式登录MySQL（不用输入密码，直接按回车）

3.update mysql.user set password=PASSWORD('新密码') where User='root'; 

4.刷新权限表 
mysql> flush privileges; 

5.退出 
mysql> quit ;
