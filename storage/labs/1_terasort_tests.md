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
```
[jnmaomao@datanode3 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort ./terasort_test_data ./terasort_output
17/05/09 07:38:59 INFO terasort.TeraSort: starting
17/05/09 07:39:01 INFO input.FileInputFormat: Total input paths to process : 4
Spent 298ms computing base-splits.
Spent 8ms computing TeraScheduler splits.
Computing input splits took 307ms
Sampling 10 splits of 300
Making 6 from 100000 sampled records
Computing parititions took 956ms
Spent 1266ms computing partitions.
17/05/09 07:39:02 INFO client.RMProxy: Connecting to ResourceManager at masternode.com/172.31.36.73:8032
17/05/09 07:39:03 INFO mapreduce.JobSubmitter: number of splits:300
17/05/09 07:39:03 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494300061404_0006
17/05/09 07:39:03 INFO impl.YarnClientImpl: Submitted application application_1494300061404_0006
17/05/09 07:39:03 INFO mapreduce.Job: The url to track the job: http://masternode.com:8088/proxy/application_1494300061404_0006/
17/05/09 07:39:03 INFO mapreduce.Job: Running job: job_1494300061404_0006
17/05/09 07:39:09 INFO mapreduce.Job: Job job_1494300061404_0006 running in uber mode : false
17/05/09 07:39:09 INFO mapreduce.Job:  map 0% reduce 0%
17/05/09 07:39:19 INFO mapreduce.Job:  map 1% reduce 0%
17/05/09 07:39:21 INFO mapreduce.Job:  map 2% reduce 0%
17/05/09 07:39:27 INFO mapreduce.Job:  map 3% reduce 0%
17/05/09 07:39:28 INFO mapreduce.Job:  map 4% reduce 0%
17/05/09 07:39:32 INFO mapreduce.Job:  map 5% reduce 0%
17/05/09 07:39:36 INFO mapreduce.Job:  map 6% reduce 0%
17/05/09 07:39:42 INFO mapreduce.Job:  map 7% reduce 0%
17/05/09 07:39:44 INFO mapreduce.Job:  map 8% reduce 0%
17/05/09 07:39:50 INFO mapreduce.Job:  map 9% reduce 0%
17/05/09 07:39:53 INFO mapreduce.Job:  map 11% reduce 0%
17/05/09 07:40:01 INFO mapreduce.Job:  map 12% reduce 0%
17/05/09 07:40:02 INFO mapreduce.Job:  map 13% reduce 0%
17/05/09 07:40:09 INFO mapreduce.Job:  map 14% reduce 0%
17/05/09 07:40:10 INFO mapreduce.Job:  map 15% reduce 0%
17/05/09 07:40:16 INFO mapreduce.Job:  map 16% reduce 0%
17/05/09 07:40:18 INFO mapreduce.Job:  map 17% reduce 0%
17/05/09 07:40:23 INFO mapreduce.Job:  map 18% reduce 0%
17/05/09 07:40:26 INFO mapreduce.Job:  map 19% reduce 0%
17/05/09 07:40:32 INFO mapreduce.Job:  map 20% reduce 0%
17/05/09 07:40:33 INFO mapreduce.Job:  map 21% reduce 0%
17/05/09 07:40:38 INFO mapreduce.Job:  map 22% reduce 0%
17/05/09 07:40:41 INFO mapreduce.Job:  map 23% reduce 0%
17/05/09 07:40:43 INFO mapreduce.Job:  map 24% reduce 0%
17/05/09 07:40:49 INFO mapreduce.Job:  map 25% reduce 0%
17/05/09 07:40:51 INFO mapreduce.Job:  map 26% reduce 0%
17/05/09 07:40:56 INFO mapreduce.Job:  map 27% reduce 0%
17/05/09 07:40:59 INFO mapreduce.Job:  map 28% reduce 0%
17/05/09 07:41:03 INFO mapreduce.Job:  map 29% reduce 0%
17/05/09 07:41:08 INFO mapreduce.Job:  map 30% reduce 0%
17/05/09 07:41:11 INFO mapreduce.Job:  map 31% reduce 0%
17/05/09 07:41:16 INFO mapreduce.Job:  map 32% reduce 0%
17/05/09 07:41:19 INFO mapreduce.Job:  map 33% reduce 0%
17/05/09 07:41:21 INFO mapreduce.Job:  map 34% reduce 0%
17/05/09 07:41:26 INFO mapreduce.Job:  map 35% reduce 0%
17/05/09 07:41:30 INFO mapreduce.Job:  map 36% reduce 0%
17/05/09 07:41:33 INFO mapreduce.Job:  map 37% reduce 0%
17/05/09 07:41:37 INFO mapreduce.Job:  map 38% reduce 0%
17/05/09 07:41:40 INFO mapreduce.Job:  map 39% reduce 0%
17/05/09 07:41:44 INFO mapreduce.Job:  map 40% reduce 0%
17/05/09 07:41:49 INFO mapreduce.Job:  map 41% reduce 0%
17/05/09 07:41:51 INFO mapreduce.Job:  map 42% reduce 0%
17/05/09 07:41:56 INFO mapreduce.Job:  map 43% reduce 0%
17/05/09 07:42:01 INFO mapreduce.Job:  map 44% reduce 0%
17/05/09 07:42:03 INFO mapreduce.Job:  map 45% reduce 0%
17/05/09 07:42:07 INFO mapreduce.Job:  map 46% reduce 0%
17/05/09 07:42:11 INFO mapreduce.Job:  map 47% reduce 0%
17/05/09 07:42:13 INFO mapreduce.Job:  map 48% reduce 0%
17/05/09 07:42:18 INFO mapreduce.Job:  map 49% reduce 0%
17/05/09 07:42:21 INFO mapreduce.Job:  map 50% reduce 0%
17/05/09 07:42:25 INFO mapreduce.Job:  map 51% reduce 0%
17/05/09 07:42:29 INFO mapreduce.Job:  map 52% reduce 0%
17/05/09 07:42:32 INFO mapreduce.Job:  map 53% reduce 0%
17/05/09 07:42:36 INFO mapreduce.Job:  map 54% reduce 0%
17/05/09 07:42:41 INFO mapreduce.Job:  map 55% reduce 0%
17/05/09 07:42:43 INFO mapreduce.Job:  map 56% reduce 0%
17/05/09 07:42:48 INFO mapreduce.Job:  map 57% reduce 0%
17/05/09 07:42:51 INFO mapreduce.Job:  map 58% reduce 0%
17/05/09 07:42:52 INFO mapreduce.Job:  map 59% reduce 0%
17/05/09 07:43:00 INFO mapreduce.Job:  map 60% reduce 0%
17/05/09 07:43:03 INFO mapreduce.Job:  map 61% reduce 0%
17/05/09 07:43:08 INFO mapreduce.Job:  map 62% reduce 0%
17/05/09 07:43:11 INFO mapreduce.Job:  map 63% reduce 0%
17/05/09 07:43:13 INFO mapreduce.Job:  map 64% reduce 0%
17/05/09 07:43:18 INFO mapreduce.Job:  map 65% reduce 0%
17/05/09 07:43:22 INFO mapreduce.Job:  map 66% reduce 0%
17/05/09 07:43:25 INFO mapreduce.Job:  map 67% reduce 0%
17/05/09 07:43:30 INFO mapreduce.Job:  map 68% reduce 0%
17/05/09 07:43:33 INFO mapreduce.Job:  map 69% reduce 0%
17/05/09 07:43:37 INFO mapreduce.Job:  map 70% reduce 0%
17/05/09 07:43:42 INFO mapreduce.Job:  map 71% reduce 0%
17/05/09 07:43:44 INFO mapreduce.Job:  map 72% reduce 0%
17/05/09 07:43:48 INFO mapreduce.Job:  map 73% reduce 0%
17/05/09 07:43:53 INFO mapreduce.Job:  map 74% reduce 0%
17/05/09 07:43:55 INFO mapreduce.Job:  map 75% reduce 0%
17/05/09 07:44:00 INFO mapreduce.Job:  map 76% reduce 0%
17/05/09 07:44:04 INFO mapreduce.Job:  map 77% reduce 0%
17/05/09 07:44:06 INFO mapreduce.Job:  map 78% reduce 0%
17/05/09 07:44:11 INFO mapreduce.Job:  map 79% reduce 0%
17/05/09 07:44:14 INFO mapreduce.Job:  map 80% reduce 0%
17/05/09 07:44:16 INFO mapreduce.Job:  map 81% reduce 0%
17/05/09 07:44:24 INFO mapreduce.Job:  map 82% reduce 0%
17/05/09 07:44:25 INFO mapreduce.Job:  map 83% reduce 0%
17/05/09 07:44:28 INFO mapreduce.Job:  map 83% reduce 2%
17/05/09 07:44:31 INFO mapreduce.Job:  map 83% reduce 3%
17/05/09 07:44:32 INFO mapreduce.Job:  map 83% reduce 6%
17/05/09 07:44:34 INFO mapreduce.Job:  map 83% reduce 7%
17/05/09 07:44:35 INFO mapreduce.Job:  map 84% reduce 10%
17/05/09 07:44:38 INFO mapreduce.Job:  map 84% reduce 13%
17/05/09 07:44:41 INFO mapreduce.Job:  map 84% reduce 16%
17/05/09 07:44:44 INFO mapreduce.Job:  map 85% reduce 17%
17/05/09 07:44:47 INFO mapreduce.Job:  map 85% reduce 18%
17/05/09 07:44:50 INFO mapreduce.Job:  map 85% reduce 19%
17/05/09 07:44:53 INFO mapreduce.Job:  map 86% reduce 19%
17/05/09 07:45:01 INFO mapreduce.Job:  map 87% reduce 19%
17/05/09 07:45:09 INFO mapreduce.Job:  map 88% reduce 19%
17/05/09 07:45:12 INFO mapreduce.Job:  map 88% reduce 20%
17/05/09 07:45:16 INFO mapreduce.Job:  map 89% reduce 20%
17/05/09 07:45:24 INFO mapreduce.Job:  map 90% reduce 20%
17/05/09 07:45:31 INFO mapreduce.Job:  map 91% reduce 20%
17/05/09 07:45:38 INFO mapreduce.Job:  map 92% reduce 20%
17/05/09 07:45:45 INFO mapreduce.Job:  map 93% reduce 21%
17/05/09 07:45:51 INFO mapreduce.Job:  map 94% reduce 21%
17/05/09 07:45:58 INFO mapreduce.Job:  map 95% reduce 21%
17/05/09 07:46:05 INFO mapreduce.Job:  map 96% reduce 21%
17/05/09 07:46:13 INFO mapreduce.Job:  map 97% reduce 21%
17/05/09 07:46:19 INFO mapreduce.Job:  map 97% reduce 22%
17/05/09 07:46:21 INFO mapreduce.Job:  map 98% reduce 22%
17/05/09 07:46:28 INFO mapreduce.Job:  map 99% reduce 22%
17/05/09 07:46:35 INFO mapreduce.Job:  map 100% reduce 22%
17/05/09 07:46:39 INFO mapreduce.Job:  map 100% reduce 26%
17/05/09 07:46:40 INFO mapreduce.Job:  map 100% reduce 31%
17/05/09 07:46:42 INFO mapreduce.Job:  map 100% reduce 36%
17/05/09 07:46:43 INFO mapreduce.Job:  map 100% reduce 44%
17/05/09 07:46:45 INFO mapreduce.Job:  map 100% reduce 47%
17/05/09 07:46:46 INFO mapreduce.Job:  map 100% reduce 48%
17/05/09 07:46:47 INFO mapreduce.Job:  map 100% reduce 49%
17/05/09 07:46:48 INFO mapreduce.Job:  map 100% reduce 52%
17/05/09 07:46:49 INFO mapreduce.Job:  map 100% reduce 54%
17/05/09 07:46:51 INFO mapreduce.Job:  map 100% reduce 56%
17/05/09 07:46:52 INFO mapreduce.Job:  map 100% reduce 58%
17/05/09 07:46:54 INFO mapreduce.Job:  map 100% reduce 60%
17/05/09 07:46:55 INFO mapreduce.Job:  map 100% reduce 61%
17/05/09 07:46:56 INFO mapreduce.Job:  map 100% reduce 62%
17/05/09 07:46:58 INFO mapreduce.Job:  map 100% reduce 65%
17/05/09 07:46:59 INFO mapreduce.Job:  map 100% reduce 66%
17/05/09 07:47:01 INFO mapreduce.Job:  map 100% reduce 70%
17/05/09 07:47:04 INFO mapreduce.Job:  map 100% reduce 72%
17/05/09 07:47:06 INFO mapreduce.Job:  map 100% reduce 73%
17/05/09 07:47:07 INFO mapreduce.Job:  map 100% reduce 81%
17/05/09 07:47:10 INFO mapreduce.Job:  map 100% reduce 88%
17/05/09 07:47:13 INFO mapreduce.Job:  map 100% reduce 89%
17/05/09 07:47:16 INFO mapreduce.Job:  map 100% reduce 90%
17/05/09 07:47:18 INFO mapreduce.Job:  map 100% reduce 91%
17/05/09 07:47:19 INFO mapreduce.Job:  map 100% reduce 92%
17/05/09 07:47:22 INFO mapreduce.Job:  map 100% reduce 93%
17/05/09 07:47:25 INFO mapreduce.Job:  map 100% reduce 94%
17/05/09 07:47:28 INFO mapreduce.Job:  map 100% reduce 96%
17/05/09 07:47:31 INFO mapreduce.Job:  map 100% reduce 97%
17/05/09 07:47:34 INFO mapreduce.Job:  map 100% reduce 98%
17/05/09 07:47:37 INFO mapreduce.Job:  map 100% reduce 100%
17/05/09 07:47:39 INFO mapreduce.Job: Job job_1494300061404_0006 completed successfully
17/05/09 07:47:39 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=4476978634
                FILE: Number of bytes written=8890255085
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000041100
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=918
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters 
                Launched map tasks=300
                Launched reduce tasks=6
                Data-local map tasks=300
                Total time spent by all maps in occupied slots (ms)=2239984
                Total time spent by all reduces in occupied slots (ms)=792653
                Total time spent by all map tasks (ms)=2239984
                Total time spent by all reduce tasks (ms)=792653
                Total vcore-seconds taken by all map tasks=2239984
                Total vcore-seconds taken by all reduce tasks=792653
                Total megabyte-seconds taken by all map tasks=2293743616
                Total megabyte-seconds taken by all reduce tasks=811676672
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4375170195
                Input split bytes=41100
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4375170195
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =1800
                Failed Shuffles=0
                Merged Map outputs=1800
                GC time elapsed (ms)=29099
                CPU time spent (ms)=1422820
                Physical memory (bytes) snapshot=144236105728
                Virtual memory (bytes) snapshot=478710456320
                Total committed heap usage (bytes)=174272806912
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters 
                Bytes Read=10000000000
        File Output Format Counters 
                Bytes Written=10000000000
17/05/09 07:47:39 INFO terasort.TeraSort: done

real    8m40.725s
user    0m10.271s
sys     0m1.012s
```


