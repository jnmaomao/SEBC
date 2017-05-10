# Verify user privileges
```
[root@masternode ~]# kinit 
Password for jnmaomao@JNMAOMAO.CN: 
[root@masternode ~]# beeline 
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://masternode.com:10000/default;principal=hive/masternode.com@JNMAOMAO.COM
scan complete in 2ms
Connecting to jdbc:hive2://masternode.com:10000/default;principal=hive/masternode.com@JNMAOMAO.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://masternode.com:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170510094646_303c04c3-e51a-4d2b-b591-d73f43fa74e1): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170510094646_303c04c3-e51a-4d2b-b591-d73f43fa74e1); Time taken: 0.71 seconds
INFO  : Executing command(queryId=hive_20170510094646_303c04c3-e51a-4d2b-b591-d73f43fa74e1): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170510094646_303c04c3-e51a-4d2b-b591-d73f43fa74e1); Time taken: 0.292 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.381 seconds)
```

# Create a Sentry role with full authorization
```
0: jdbc:hive2://masternode.com:10000/default> CREATE ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20170510094747_394e428d-ad95-4b34-b019-3e00601e5b84): CREATE ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170510094747_394e428d-ad95-4b34-b019-3e00601e5b84); Time taken: 0.067 seconds
INFO  : Executing command(queryId=hive_20170510094747_394e428d-ad95-4b34-b019-3e00601e5b84): CREATE ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170510094747_394e428d-ad95-4b34-b019-3e00601e5b84); Time taken: 0.852 seconds
INFO  : OK
No rows affected (0.933 seconds)
0: jdbc:hive2://masternode.com:10000/default> GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20170510094747_fe4988bb-d62e-46a7-b7e5-c933ce16f59e): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170510094747_fe4988bb-d62e-46a7-b7e5-c933ce16f59e); Time taken: 0.106 seconds
INFO  : Executing command(queryId=hive_20170510094747_fe4988bb-d62e-46a7-b7e5-c933ce16f59e): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170510094747_fe4988bb-d62e-46a7-b7e5-c933ce16f59e); Time taken: 0.1 seconds
INFO  : OK
No rows affected (0.218 seconds)
0: jdbc:hive2://masternode.com:10000/default> GRANT ROLE sentry_admin TO GROUP root;
INFO  : Compiling command(queryId=hive_20170510094848_69b13eca-e417-4f45-b6f8-923515c2d6f8): GRANT ROLE sentry_admin TO GROUP root
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170510094848_69b13eca-e417-4f45-b6f8-923515c2d6f8); Time taken: 0.061 seconds
INFO  : Executing command(queryId=hive_20170510094848_69b13eca-e417-4f45-b6f8-923515c2d6f8): GRANT ROLE sentry_admin TO GROUP root
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170510094848_69b13eca-e417-4f45-b6f8-923515c2d6f8); Time taken: 0.084 seconds
INFO  : OK
No rows affected (0.161 seconds)
0: jdbc:hive2://masternode.com:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20170510094848_ade9fa41-ac59-4b84-9428-893300467372): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170510094848_ade9fa41-ac59-4b84-9428-893300467372); Time taken: 0.062 seconds
INFO  : Executing command(queryId=hive_20170510094848_ade9fa41-ac59-4b84-9428-893300467372): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170510094848_ade9fa41-ac59-4b84-9428-893300467372); Time taken: 0.139 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.26 seconds)
```

# kinit as george, login to beeline, and use SHOW TABLES;
```
[root@masternode ~]# kinit george
Password for george@JNMAOMAO.CN: 
[root@masternode ~]# beeline 
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://masternode.com:10000/default;principal=hive/masternode.com@JNMAOMAO.COM
scan complete in 3ms
Connecting to jdbc:hive2://masternode.com:10000/default;principal=hive/masternode.com@JNMAOMAO.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://masternode.com:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170510095555_acc4276f-f203-43c1-94b8-8748e25b0f61): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170510095555_acc4276f-f203-43c1-94b8-8748e25b0f61); Time taken: 0.071 seconds
INFO  : Executing command(queryId=hive_20170510095555_acc4276f-f203-43c1-94b8-8748e25b0f61): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170510095555_acc4276f-f203-43c1-94b8-8748e25b0f61); Time taken: 0.146 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.324 seconds)
```

# kinit as ferdinand, login to beeline, and use SHOW TABLES;
```
[root@masternode ~]# kinit ferdinand
Password for ferdinand@JNMAOMAO.CN: 
[root@masternode ~]# beeline 
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://masternode.com:10000/default;principal=hive/masternode.com@JNMAOMAO.COM
scan complete in 3ms
Connecting to jdbc:hive2://masternode.com:10000/default;principal=hive/masternode.com@JNMAOMAO.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://masternode.com:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170510095757_146e5bd4-2677-4dcc-b71f-37568c807024): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170510095757_146e5bd4-2677-4dcc-b71f-37568c807024); Time taken: 0.07 seconds
INFO  : Executing command(queryId=hive_20170510095757_146e5bd4-2677-4dcc-b71f-37568c807024): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170510095757_146e5bd4-2677-4dcc-b71f-37568c807024); Time taken: 0.152 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.336 seconds)
```