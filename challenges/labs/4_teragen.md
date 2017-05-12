# The full teragen command and job output

```
[root@masternode opt]# time sudo -u zhou hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -D mapreduce.job.maps=6 -D dfs.blocksize=64m -D mapreduce.map.memory.mb=1024 65536000 /user/zhou/tgen
17/05/12 02:39:30 INFO client.RMProxy: Connecting to ResourceManager at masternode.com/172.31.41.25:8032
17/05/12 02:39:31 INFO terasort.TeraSort: Generating 65536000 using 6
17/05/12 02:39:31 INFO mapreduce.JobSubmitter: number of splits:6
17/05/12 02:39:32 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494555695128_0001
17/05/12 02:39:32 INFO impl.YarnClientImpl: Submitted application application_1494555695128_0001
17/05/12 02:39:32 INFO mapreduce.Job: The url to track the job: http://masternode.com:8088/proxy/application_1494555695128_0001/
17/05/12 02:39:32 INFO mapreduce.Job: Running job: job_1494555695128_0001
17/05/12 02:39:40 INFO mapreduce.Job: Job job_1494555695128_0001 running in uber mode : false
17/05/12 02:39:40 INFO mapreduce.Job:  map 0% reduce 0%
17/05/12 02:39:54 INFO mapreduce.Job:  map 5% reduce 0%
17/05/12 02:39:55 INFO mapreduce.Job:  map 14% reduce 0%
17/05/12 02:39:57 INFO mapreduce.Job:  map 17% reduce 0%
17/05/12 02:39:58 INFO mapreduce.Job:  map 21% reduce 0%
17/05/12 02:40:00 INFO mapreduce.Job:  map 23% reduce 0%
17/05/12 02:40:01 INFO mapreduce.Job:  map 25% reduce 0%
17/05/12 02:40:03 INFO mapreduce.Job:  map 27% reduce 0%
17/05/12 02:40:04 INFO mapreduce.Job:  map 30% reduce 0%
17/05/12 02:40:06 INFO mapreduce.Job:  map 31% reduce 0%
17/05/12 02:40:07 INFO mapreduce.Job:  map 33% reduce 0%
17/05/12 02:40:09 INFO mapreduce.Job:  map 34% reduce 0%
17/05/12 02:40:10 INFO mapreduce.Job:  map 36% reduce 0%
17/05/12 02:40:12 INFO mapreduce.Job:  map 37% reduce 0%
17/05/12 02:40:13 INFO mapreduce.Job:  map 40% reduce 0%
17/05/12 02:40:15 INFO mapreduce.Job:  map 41% reduce 0%
17/05/12 02:40:16 INFO mapreduce.Job:  map 43% reduce 0%
17/05/12 02:40:18 INFO mapreduce.Job:  map 44% reduce 0%
17/05/12 02:40:19 INFO mapreduce.Job:  map 46% reduce 0%
17/05/12 02:40:21 INFO mapreduce.Job:  map 47% reduce 0%
17/05/12 02:40:22 INFO mapreduce.Job:  map 49% reduce 0%
17/05/12 02:40:24 INFO mapreduce.Job:  map 50% reduce 0%
17/05/12 02:40:25 INFO mapreduce.Job:  map 52% reduce 0%
17/05/12 02:40:27 INFO mapreduce.Job:  map 53% reduce 0%
17/05/12 02:40:28 INFO mapreduce.Job:  map 55% reduce 0%
17/05/12 02:40:30 INFO mapreduce.Job:  map 57% reduce 0%
17/05/12 02:40:31 INFO mapreduce.Job:  map 59% reduce 0%
17/05/12 02:40:33 INFO mapreduce.Job:  map 60% reduce 0%
17/05/12 02:40:34 INFO mapreduce.Job:  map 62% reduce 0%
17/05/12 02:40:36 INFO mapreduce.Job:  map 63% reduce 0%
17/05/12 02:40:37 INFO mapreduce.Job:  map 65% reduce 0%
17/05/12 02:40:39 INFO mapreduce.Job:  map 66% reduce 0%
17/05/12 02:40:41 INFO mapreduce.Job:  map 68% reduce 0%
17/05/12 02:40:43 INFO mapreduce.Job:  map 70% reduce 0%
17/05/12 02:40:44 INFO mapreduce.Job:  map 72% reduce 0%
17/05/12 02:40:46 INFO mapreduce.Job:  map 73% reduce 0%
17/05/12 02:40:47 INFO mapreduce.Job:  map 75% reduce 0%
17/05/12 02:40:49 INFO mapreduce.Job:  map 76% reduce 0%
17/05/12 02:40:50 INFO mapreduce.Job:  map 78% reduce 0%
17/05/12 02:40:52 INFO mapreduce.Job:  map 79% reduce 0%
17/05/12 02:40:53 INFO mapreduce.Job:  map 82% reduce 0%
17/05/12 02:40:55 INFO mapreduce.Job:  map 83% reduce 0%
17/05/12 02:40:56 INFO mapreduce.Job:  map 84% reduce 0%
17/05/12 02:40:57 INFO mapreduce.Job:  map 86% reduce 0%
17/05/12 02:40:59 INFO mapreduce.Job:  map 87% reduce 0%
17/05/12 02:41:00 INFO mapreduce.Job:  map 89% reduce 0%
17/05/12 02:41:02 INFO mapreduce.Job:  map 90% reduce 0%
17/05/12 02:41:03 INFO mapreduce.Job:  map 93% reduce 0%
17/05/12 02:41:04 INFO mapreduce.Job:  map 95% reduce 0%
17/05/12 02:41:06 INFO mapreduce.Job:  map 96% reduce 0%
17/05/12 02:41:07 INFO mapreduce.Job:  map 99% reduce 0%
17/05/12 02:41:08 INFO mapreduce.Job:  map 100% reduce 0%
17/05/12 02:41:09 INFO mapreduce.Job: Job job_1494555695128_0001 completed successfully
17/05/12 02:41:09 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=738180
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=511
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=24
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters 
                Launched map tasks=6
                Other local map tasks=6
                Total time spent by all maps in occupied slots (ms)=508237
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=508237
                Total vcore-seconds taken by all map tasks=508237
                Total megabyte-seconds taken by all map tasks=520434688
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=511
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1259
                CPU time spent (ms)=127200
                Physical memory (bytes) snapshot=1937498112
                Virtual memory (bytes) snapshot=9382408192
                Total committed heap usage (bytes)=1922039808
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters 
                Bytes Read=0
        File Output Format Counters 
                Bytes Written=6553600000

```
# The result of the time command
```
real    1m41.819s
user    0m6.523s
sys     0m0.732s
```
# The command and output of hdfs dfs -ls /user/zhou/tgen
```
[root@masternode opt]# hdfs dfs -ls /user/zhou/tgen
Found 7 items
-rw-r--r--   3 zhou beijing          0 2017-05-12 02:41 /user/zhou/tgen/_SUCCESS
-rw-r--r--   3 zhou beijing 1092266700 2017-05-12 02:41 /user/zhou/tgen/part-m-00000
-rw-r--r--   3 zhou beijing 1092266700 2017-05-12 02:41 /user/zhou/tgen/part-m-00001
-rw-r--r--   3 zhou beijing 1092266600 2017-05-12 02:41 /user/zhou/tgen/part-m-00002
-rw-r--r--   3 zhou beijing 1092266700 2017-05-12 02:41 /user/zhou/tgen/part-m-00003
-rw-r--r--   3 zhou beijing 1092266700 2017-05-12 02:41 /user/zhou/tgen/part-m-00004
-rw-r--r--   3 zhou beijing 1092266600 2017-05-12 02:41 /user/zhou/tgen/part-m-00005

```