# The hostname of your db server node
```
[root@masternode opt]# hostname 
masternode.com
```

# mysql verison info
```
[root@masternode opt]#  mysql --version
mysql  Ver 14.14 Distrib 5.6.36, for Linux (x86_64) using  EditLine wrapper

```

# databases created
```
mysql>  show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
9 rows in set (0.00 sec)

```


# db users
```
mysql>  select host,user from mysql.user;      
+----------------+--------+
| host           | user   |
+----------------+--------+
| %              | hive   |
| %              | hue    |
| %              | oozie  |
| %              | rman   |
| %              | scm    |
| %              | sentry |
| 127.0.0.1      | root   |
| ::1            | root   |
| localhost      | root   |
| masternode.com | root   |
+----------------+--------+
10 rows in set (0.00 sec)

```