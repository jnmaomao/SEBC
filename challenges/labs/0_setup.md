# List the cloud provider you are using (AWS, GCE, Azure, other)
```
AWS in us-west-2b
```

# List the nodes you are using by IP address and name
```
public ip      private ip    hostname
34.210.81.151  172.31.41.25 masternode.com masternode
54.202.26.201 172.31.47.238 cmnode.com cmnode
34.210.79.118 172.31.44.186 datanode1.com datanode1
54.191.174.78 172.31.32.176 datanode2.com datanode2
54.202.54.174 172.31.38.243 datanode3.com datanode3
```

# List the Linux release you are using
```
CentOS6.5
```

# Demonstrate the disk capacity available on each node is >= 30 GB
```
[root@masternode ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  682M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
```

# List the command and output for yum repolist enabled
```
[root@masternode ~]# yum repolist enabled
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: mirrors.xmission.com
 * extras: centos.sonn.com
 * updates: mirror.san.fastserv.com
base                                                                                                                                             | 3.7 kB     00:00     
extras                                                                                                                                           | 3.4 kB     00:00     
updates                                                                                                                                          | 3.4 kB     00:00     
repo id                                                                    repo name                                                                              status
base                                                                       CentOS-6 - Base                                                                        6,706
extras                                                                     CentOS-6 - Extras                                                                         64
updates                                                                    CentOS-6 - Updates                                                                       270
repolist: 7,040
```

# Add the following Linux accounts to all nodes
```
[root@masternode ~]# groupadd shanghai
[root@masternode ~]# groupadd beijing
[root@masternode ~]# useradd -u 2900 -g shanghai chen
[root@masternode ~]# useradd -u 2800 -g beijing zhou
[root@masternode ~]# usermod -a -G shanghai chen
[root@masternode ~]# usermod -a -G beijing zhou
```

# List the /etc/passwd entries for zhou and chen
```
[root@masternode ~]# cat /etc/passwd | grep -E 'chen|zhou'
chen:x:2900:500::/home/chen:/bin/bash
zhou:x:2800:501::/home/zhou:/bin/bash

```

# List the /etc/group entries for shanghai and beijing
```
[root@masternode ~]# cat /etc/group | grep -E 'shanghai|beijing'
shanghai:x:500:chen
beijing:x:501:zhou

```