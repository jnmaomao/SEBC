1.Check vm.swappiness on all your nodes
```
[root@cmnode .ssh]# cat /proc/sys/vm/swappiness
60
[root@cmnode .ssh]# vi /etc/sysctl.conf
[root@cmnode .ssh]# sysctl vm.swappiness=1
vm.swappiness = 1
[root@cmnode .ssh]# cat /proc/sys/vm/swappiness
1
```

2.Show the mount attributes of your volume(s)
```
[root@cmnode .ssh]# mount -l
/dev/xvde on / type ext4 (rw) [centos_root]
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
```

3.list the reserve space setting
```
[root@cmnode .ssh]# df -h -T
Filesystem     Type   Size  Used Avail Use% Mounted on
/dev/xvde      ext4    30G  655M   28G   3% /
tmpfs          tmpfs  7.4G     0  7.4G   0% /dev/shm
```

4.Disable transparent hugepage support
```
[root@cmnode .ssh]# grep -i HugePages_Total /proc/meminfo
HugePages_Total:       0
```

5.List your network interface configuration
```
[root@cmnode .ssh]# ifconfig 
eth0      Link encap:Ethernet  HWaddr 06:3B:E5:E1:5C:0C  
          inet addr:172.31.36.96  Bcast:172.31.47.255  Mask:255.255.240.0
          inet6 addr: fe80::43b:e5ff:fee1:5c0c/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:2785 errors:0 dropped:0 overruns:0 frame:0
          TX packets:2425 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000 
          RX bytes:279089 (272.5 KiB)  TX bytes:339275 (331.3 KiB)
          Interrupt:24 

lo        Link encap:Local Loopback  
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:16436  Metric:1
          RX packets:18 errors:0 dropped:0 overruns:0 frame:0
          TX packets:18 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0 
          RX bytes:3834 (3.7 KiB)  TX bytes:3834 (3.7 KiB)
```

6.Show that forward and reverse host lookups are correctly resolved
```
[root@cmnode .ssh]# getent hosts
127.0.0.1       localhost.localdomain localhost
127.0.0.1       localhost6.localdomain6 localhost6
172.31.36.96    cmnode.com cmnode
172.31.36.73    masternode.com masternode
172.31.37.33    datanode1.com datanode1
172.31.46.141   datanode2.com datanode2
172.31.33.237   datanode3.com datanode3
```

7.Show the nscd service is running
```
[root@cmnode .ssh]# service nscd start
Starting nscd:                                             [  OK  ]
[root@cmnode .ssh]# chkconfig nscd on
[root@cmnode .ssh]# service nscd status
nscd (pid 4574) is running...
```

8.Show the ntpd service is running
```
[root@cmnode .ssh]# service ntpd start
Starting ntpd:                                             [  OK  ]
[root@cmnode .ssh]# chkconfig ntpd on
[root@cmnode .ssh]# service ntpd status
ntpd (pid  4662) is running...
```