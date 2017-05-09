# Test HDFS Snapshots
1.Create a precious directory in HDFS; copy the ZIP course file into it.
```
[jnmaomao@datanode2 ~]$ su - jnmaomao
Password: 
[jnmaomao@datanode2 ~]$ hdfs dfs -mkdir precious
[jnmaomao@datanode2 ~]$ hdfs dfs -put /opt/SEBC-Shanghai.zip precious/
[jnmaomao@datanode2 ~]$ hdfs dfs -ls precious/
Found 1 items
-rw-r--r--   3 jnmaomao supergroup     474957 2017-05-09 07:50 precious/SEBC-Shanghai.zip
```

2.Enable snapshots for precious
```
[jnmaomao@datanode2 ~]$ su - root
Password: 
[root@datanode2 ~]# sudo -u hdfs hdfs dfsadmin -allowSnapshot /user/jnmaomao/precious
Allowing snaphot on /user/jnmaomao/precious succeeded
```

3.Create a snapshot called sebc-hdfs-test
```
[root@datanode2 ~]# sudo -u jnmaomao hdfs dfs -createSnapshot /user/jnmaomao/precious sebc-hdfs-test
Created snapshot /user/jnmaomao/precious/.snapshot/sebc-hdfs-test
```

4.Delete the directory
```
[root@datanode2 ~]# sudo -u jnmaomao hdfs dfs -rm -f -R /user/jnmaomao/precious
rm: Failed to move to trash: hdfs://masternode.com:8020/user/jnmaomao/precious: The directory /user/jnmaomao/precious cannot be deleted since /user/jnmaomao/precious is snapshottable and already has snapshots
```

5.Delete the ZIP file
```
[root@datanode2 ~]# sudo -u jnmaomao hdfs dfs -rm -f precious/SEBC-Shanghai.zip 
17/05/09 07:58:24 INFO fs.TrashPolicyDefault: Moved: 'hdfs://masternode.com:8020/user/jnmaomao/precious/SEBC-Shanghai.zip' to trash at: hdfs://masternode.com:8020/user/jnmaomao/.Trash/Current/user/jnmaomao/precious/SEBC-Shanghai.zip
```

6.Restore the deleted file

```
[root@datanode2 ~]# sudo -u jnmaomao hdfs dfs -cp precious/.snapshot/sebc-hdfs-test/SEBC-Shanghai.zip precious
[root@datanode2 ~]# sudo -u jnmaomao hdfs dfs -ls precious
Found 1 items
-rw-r--r--   3 jnmaomao supergroup     474957 2017-05-09 08:00 precious/SEBC-Shanghai.zip
```


