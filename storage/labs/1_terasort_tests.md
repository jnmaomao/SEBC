1.First I Create linux account on all node use by my gitname£¬jnmaomao
```
[root@masternode ~]# useradd jnmaomao
[jnmaomao@masternode ~]$ hdfs dfs -ls 
Found 2 items
drwxr-xr-x   - hdfs supergroup          0 2017-05-09 03:56 source
drwxr-xr-x   - hdfs supergroup          0 2017-05-09 06:06 target
```
2.Create a 10 GB file using teragen
```
[jnmaomao@datanode3 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -D dfs.blocksize=32m -Dmapred.map.tasks.speculative.execution=false 100000000 terasort_test_data
17/05/09 07:30:32 INFO client.RMProxy: Connecting to ResourceManager at masternode.com/172.31.36.73:8032
17/05/09 07:30:32 INFO terasort.TeraSort: Generating 100000000 using 4
17/05/09 07:30:33 INFO mapreduce.JobSubmitter: number of splits:4
17/05/09 07:30:33 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/05/09 07:30:33 INFO Configuration.deprecation: mapred.map.tasks.speculative.execution is deprecated. Instead, use mapreduce.map.speculative
17/05/09 07:30:33 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494300061404_0005
17/05/09 07:30:33 INFO impl.YarnClientImpl: Submitted application application_1494300061404_0005
17/05/09 07:30:33 INFO mapreduce.Job: The url to track the job: http://masternode.com:8088/proxy/application_1494300061404_0005/
17/05/09 07:30:33 INFO mapreduce.Job: Running job: job_1494300061404_0005
17/05/09 07:30:39 INFO mapreduce.Job: Job job_1494300061404_0005 running in uber mode : false
17/05/09 07:30:39 INFO mapreduce.Job:  map 0% reduce 0%
17/05/09 07:30:53 INFO mapreduce.Job:  map 8% reduce 0%
17/05/09 07:30:56 INFO mapreduce.Job:  map 11% reduce 0%
17/05/09 07:30:59 INFO mapreduce.Job:  map 15% reduce 0%
17/05/09 07:31:02 INFO mapreduce.Job:  map 17% reduce 0%
17/05/09 07:31:05 INFO mapreduce.Job:  map 20% reduce 0%
17/05/09 07:31:08 INFO mapreduce.Job:  map 22% reduce 0%
17/05/09 07:31:11 INFO mapreduce.Job:  map 23% reduce 0%
17/05/09 07:31:13 INFO mapreduce.Job:  map 24% reduce 0%
17/05/09 07:31:14 INFO mapreduce.Job:  map 25% reduce 0%
17/05/09 07:31:16 INFO mapreduce.Job:  map 26% reduce 0%
17/05/09 07:31:17 INFO mapreduce.Job:  map 28% reduce 0%
17/05/09 07:31:20 INFO mapreduce.Job:  map 30% reduce 0%
17/05/09 07:31:23 INFO mapreduce.Job:  map 32% reduce 0%
17/05/09 07:31:25 INFO mapreduce.Job:  map 33% reduce 0%
17/05/09 07:31:26 INFO mapreduce.Job:  map 34% reduce 0%
17/05/09 07:31:28 INFO mapreduce.Job:  map 35% reduce 0%
17/05/09 07:31:29 INFO mapreduce.Job:  map 36% reduce 0%
17/05/09 07:31:31 INFO mapreduce.Job:  map 38% reduce 0%
17/05/09 07:31:35 INFO mapreduce.Job:  map 40% reduce 0%
17/05/09 07:31:38 INFO mapreduce.Job:  map 42% reduce 0%
17/05/09 07:31:41 INFO mapreduce.Job:  map 45% reduce 0%
17/05/09 07:31:44 INFO mapreduce.Job:  map 47% reduce 0%
17/05/09 07:31:47 INFO mapreduce.Job:  map 49% reduce 0%
17/05/09 07:31:50 INFO mapreduce.Job:  map 51% reduce 0%
17/05/09 07:31:53 INFO mapreduce.Job:  map 53% reduce 0%
17/05/09 07:31:56 INFO mapreduce.Job:  map 55% reduce 0%
17/05/09 07:31:59 INFO mapreduce.Job:  map 57% reduce 0%
17/05/09 07:32:02 INFO mapreduce.Job:  map 60% reduce 0%
17/05/09 07:32:05 INFO mapreduce.Job:  map 62% reduce 0%
17/05/09 07:32:08 INFO mapreduce.Job:  map 64% reduce 0%
17/05/09 07:32:11 INFO mapreduce.Job:  map 66% reduce 0%
17/05/09 07:32:14 INFO mapreduce.Job:  map 68% reduce 0%
17/05/09 07:32:18 INFO mapreduce.Job:  map 70% reduce 0%
17/05/09 07:32:20 INFO mapreduce.Job:  map 71% reduce 0%
17/05/09 07:32:21 INFO mapreduce.Job:  map 72% reduce 0%
17/05/09 07:32:23 INFO mapreduce.Job:  map 73% reduce 0%
17/05/09 07:32:24 INFO mapreduce.Job:  map 74% reduce 0%
17/05/09 07:32:26 INFO mapreduce.Job:  map 75% reduce 0%
17/05/09 07:32:27 INFO mapreduce.Job:  map 76% reduce 0%
17/05/09 07:32:29 INFO mapreduce.Job:  map 77% reduce 0%
17/05/09 07:32:30 INFO mapreduce.Job:  map 78% reduce 0%
17/05/09 07:32:32 INFO mapreduce.Job:  map 79% reduce 0%
17/05/09 07:32:33 INFO mapreduce.Job:  map 80% reduce 0%
17/05/09 07:32:35 INFO mapreduce.Job:  map 81% reduce 0%
17/05/09 07:32:36 INFO mapreduce.Job:  map 83% reduce 0%
17/05/09 07:32:38 INFO mapreduce.Job:  map 84% reduce 0%
17/05/09 07:32:39 INFO mapreduce.Job:  map 85% reduce 0%
17/05/09 07:32:41 INFO mapreduce.Job:  map 87% reduce 0%
17/05/09 07:32:44 INFO mapreduce.Job:  map 90% reduce 0%
17/05/09 07:32:47 INFO mapreduce.Job:  map 92% reduce 0%
17/05/09 07:32:50 INFO mapreduce.Job:  map 94% reduce 0%
17/05/09 07:32:53 INFO mapreduce.Job:  map 96% reduce 0%
17/05/09 07:32:56 INFO mapreduce.Job:  map 98% reduce 0%
17/05/09 07:33:00 INFO mapreduce.Job:  map 100% reduce 0%
17/05/09 07:33:01 INFO mapreduce.Job: Job job_1494300061404_0005 completed successfully
17/05/09 07:33:01 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=492280
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters 
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=549870
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=549870
                Total vcore-seconds taken by all map tasks=549870
                Total megabyte-seconds taken by all map tasks=563066880
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1515
                CPU time spent (ms)=154970
                Physical memory (bytes) snapshot=1059479552
                Virtual memory (bytes) snapshot=6249435136
                Total committed heap usage (bytes)=854065152
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters 
                Bytes Read=0
        File Output Format Counters 
                Bytes Written=10000000000

real    2m31.663s
user    0m5.885s
sys     0m0.762s

--Land the output in your user's home directory

[jnmaomao@datanode3 ~]$ hdfs dfs -ls ./
Found 4 items
drwx------   - jnmaomao supergroup          0 2017-05-09 07:33 .staging
drwxr-xr-x   - hdfs     supergroup          0 2017-05-09 03:56 source
drwxr-xr-x   - hdfs     supergroup          0 2017-05-09 06:06 target
drwxr-xr-x   - jnmaomao supergroup          0 2017-05-09 07:32 terasort_test_data
[jnmaomao@datanode3 ~]$ hdfs dfs -ls ./terasort_test_data
Found 5 items
-rw-r--r--   3 jnmaomao supergroup          0 2017-05-09 07:32 terasort_test_data/_SUCCESS
-rw-r--r--   3 jnmaomao supergroup 2500000000 2017-05-09 07:32 terasort_test_data/part-m-00000
-rw-r--r--   3 jnmaomao supergroup 2500000000 2017-05-09 07:32 terasort_test_data/part-m-00001
-rw-r--r--   3 jnmaomao supergroup 2500000000 2017-05-09 07:32 terasort_test_data/part-m-00002
-rw-r--r--   3 jnmaomao supergroup 2500000000 2017-05-09 07:32 terasort_test_data/part-m-00003
```
--Run the terasort command on this file
time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort ./terasort_test_data ./terasort_output


