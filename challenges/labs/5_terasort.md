```
[root@masternode ~]# time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar terasort /user/zhou/tgen /user/zhou/tsort
17/05/12 03:18:43 INFO terasort.TeraSort: starting
17/05/12 03:18:45 INFO hdfs.DFSClient: Created token for zhou: HDFS_DELEGATION_TOKEN owner=zhou@JNMAOMAO.CN, renewer=yarn, realUser=, issueDate=1494559125712, maxDate=1495163925712, sequenceNumber=1, masterKeyId=2 on 172.31.41.25:8020
17/05/12 03:18:45 INFO security.TokenCache: Got dt for hdfs://masternode.com:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.41.25:8020, Ident: (token for zhou: HDFS_DELEGATION_TOKEN owner=zhou@JNMAOMAO.CN, renewer=yarn, realUser=, issueDate=1494559125712, maxDate=1495163925712, sequenceNumber=1, masterKeyId=2)
17/05/12 03:18:45 INFO input.FileInputFormat: Total input paths to process : 6
Spent 376ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 381ms
Sampling 10 splits of 102
Making 6 from 100000 sampled records
Computing parititions took 990ms
Spent 1373ms computing partitions.
17/05/12 03:18:46 INFO client.RMProxy: Connecting to ResourceManager at masternode.com/172.31.41.25:8032
17/05/12 03:18:47 INFO mapreduce.JobSubmitter: number of splits:102
17/05/12 03:18:47 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494558460258_0001
17/05/12 03:18:47 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.41.25:8020, Ident: (token for zhou: HDFS_DELEGATION_TOKEN owner=zhou@JNMAOMAO.CN, renewer=yarn, realUser=, issueDate=1494559125712, maxDate=1495163925712, sequenceNumber=1, masterKeyId=2)
17/05/12 03:18:48 INFO impl.YarnClientImpl: Submitted application application_1494558460258_0001
17/05/12 03:18:48 INFO mapreduce.Job: The url to track the job: http://masternode.com:8088/proxy/application_1494558460258_0001/
17/05/12 03:18:48 INFO mapreduce.Job: Running job: job_1494558460258_0001
17/05/12 03:19:00 INFO mapreduce.Job: Job job_1494558460258_0001 running in uber mode : false
17/05/12 03:19:00 INFO mapreduce.Job:  map 0% reduce 0%
17/05/12 03:19:11 INFO mapreduce.Job:  map 2% reduce 0%
17/05/12 03:19:19 INFO mapreduce.Job:  map 3% reduce 0%
17/05/12 03:19:20 INFO mapreduce.Job:  map 8% reduce 0%
17/05/12 03:19:21 INFO mapreduce.Job:  map 10% reduce 0%
17/05/12 03:19:31 INFO mapreduce.Job:  map 13% reduce 0%
17/05/12 03:19:32 INFO mapreduce.Job:  map 16% reduce 0%
17/05/12 03:19:33 INFO mapreduce.Job:  map 18% reduce 0%
17/05/12 03:19:40 INFO mapreduce.Job:  map 20% reduce 0%
17/05/12 03:19:43 INFO mapreduce.Job:  map 23% reduce 0%
17/05/12 03:19:44 INFO mapreduce.Job:  map 24% reduce 0%
17/05/12 03:19:45 INFO mapreduce.Job:  map 25% reduce 0%
17/05/12 03:19:51 INFO mapreduce.Job:  map 27% reduce 0%
17/05/12 03:19:55 INFO mapreduce.Job:  map 29% reduce 0%
17/05/12 03:19:56 INFO mapreduce.Job:  map 31% reduce 0%
17/05/12 03:19:57 INFO mapreduce.Job:  map 33% reduce 0%
17/05/12 03:20:00 INFO mapreduce.Job:  map 35% reduce 0%
17/05/12 03:20:07 INFO mapreduce.Job:  map 37% reduce 0%
17/05/12 03:20:08 INFO mapreduce.Job:  map 38% reduce 0%
17/05/12 03:20:09 INFO mapreduce.Job:  map 41% reduce 0%
17/05/12 03:20:11 INFO mapreduce.Job:  map 43% reduce 0%
17/05/12 03:20:19 INFO mapreduce.Job:  map 44% reduce 0%
17/05/12 03:20:20 INFO mapreduce.Job:  map 45% reduce 0%
17/05/12 03:20:21 INFO mapreduce.Job:  map 51% reduce 0%
17/05/12 03:20:31 INFO mapreduce.Job:  map 55% reduce 0%
17/05/12 03:20:32 INFO mapreduce.Job:  map 57% reduce 0%
17/05/12 03:20:33 INFO mapreduce.Job:  map 58% reduce 0%
17/05/12 03:20:34 INFO mapreduce.Job:  map 59% reduce 0%
17/05/12 03:20:40 INFO mapreduce.Job:  map 61% reduce 0%
17/05/12 03:20:42 INFO mapreduce.Job:  map 62% reduce 0%
17/05/12 03:20:43 INFO mapreduce.Job:  map 64% reduce 0%
17/05/12 03:20:44 INFO mapreduce.Job:  map 65% reduce 0%
17/05/12 03:20:45 INFO mapreduce.Job:  map 66% reduce 0%
17/05/12 03:20:46 INFO mapreduce.Job:  map 67% reduce 0%
17/05/12 03:20:50 INFO mapreduce.Job:  map 69% reduce 0%
17/05/12 03:20:53 INFO mapreduce.Job:  map 70% reduce 0%
17/05/12 03:20:55 INFO mapreduce.Job:  map 72% reduce 0%
17/05/12 03:20:56 INFO mapreduce.Job:  map 73% reduce 0%
17/05/12 03:20:57 INFO mapreduce.Job:  map 74% reduce 0%
17/05/12 03:20:58 INFO mapreduce.Job:  map 75% reduce 0%
17/05/12 03:21:00 INFO mapreduce.Job:  map 76% reduce 0%
17/05/12 03:21:03 INFO mapreduce.Job:  map 77% reduce 0%
17/05/12 03:21:07 INFO mapreduce.Job:  map 79% reduce 0%
17/05/12 03:21:08 INFO mapreduce.Job:  map 81% reduce 0%
17/05/12 03:21:09 INFO mapreduce.Job:  map 83% reduce 0%
17/05/12 03:21:10 INFO mapreduce.Job:  map 84% reduce 0%
17/05/12 03:21:15 INFO mapreduce.Job:  map 85% reduce 0%
17/05/12 03:21:18 INFO mapreduce.Job:  map 87% reduce 0%
17/05/12 03:21:19 INFO mapreduce.Job:  map 88% reduce 0%
17/05/12 03:21:21 INFO mapreduce.Job:  map 89% reduce 3%
17/05/12 03:21:23 INFO mapreduce.Job:  map 89% reduce 6%
17/05/12 03:21:24 INFO mapreduce.Job:  map 89% reduce 9%
17/05/12 03:21:26 INFO mapreduce.Job:  map 90% reduce 11%
17/05/12 03:21:27 INFO mapreduce.Job:  map 90% reduce 13%
17/05/12 03:21:29 INFO mapreduce.Job:  map 90% reduce 18%
17/05/12 03:21:31 INFO mapreduce.Job:  map 91% reduce 21%
17/05/12 03:21:32 INFO mapreduce.Job:  map 92% reduce 22%
17/05/12 03:21:33 INFO mapreduce.Job:  map 92% reduce 23%
17/05/12 03:21:34 INFO mapreduce.Job:  map 92% reduce 25%
17/05/12 03:21:38 INFO mapreduce.Job:  map 92% reduce 26%
17/05/12 03:21:39 INFO mapreduce.Job:  map 93% reduce 26%
17/05/12 03:21:40 INFO mapreduce.Job:  map 94% reduce 26%
17/05/12 03:21:43 INFO mapreduce.Job:  map 95% reduce 26%
17/05/12 03:21:46 INFO mapreduce.Job:  map 96% reduce 26%
17/05/12 03:21:47 INFO mapreduce.Job:  map 97% reduce 26%
17/05/12 03:21:48 INFO mapreduce.Job:  map 97% reduce 27%
17/05/12 03:21:50 INFO mapreduce.Job:  map 98% reduce 27%
17/05/12 03:21:52 INFO mapreduce.Job:  map 99% reduce 27%
17/05/12 03:21:54 INFO mapreduce.Job:  map 100% reduce 27%
17/05/12 03:21:55 INFO mapreduce.Job:  map 100% reduce 35%
17/05/12 03:21:57 INFO mapreduce.Job:  map 100% reduce 47%
17/05/12 03:21:58 INFO mapreduce.Job:  map 100% reduce 57%
17/05/12 03:22:00 INFO mapreduce.Job:  map 100% reduce 62%
17/05/12 03:22:01 INFO mapreduce.Job:  map 100% reduce 65%
17/05/12 03:22:03 INFO mapreduce.Job:  map 100% reduce 67%
17/05/12 03:22:04 INFO mapreduce.Job:  map 100% reduce 70%
17/05/12 03:22:06 INFO mapreduce.Job:  map 100% reduce 72%
17/05/12 03:22:07 INFO mapreduce.Job:  map 100% reduce 76%
17/05/12 03:22:09 INFO mapreduce.Job:  map 100% reduce 78%
17/05/12 03:22:10 INFO mapreduce.Job:  map 100% reduce 86%
17/05/12 03:22:12 INFO mapreduce.Job:  map 100% reduce 88%
17/05/12 03:22:13 INFO mapreduce.Job:  map 100% reduce 93%
17/05/12 03:22:15 INFO mapreduce.Job:  map 100% reduce 95%
17/05/12 03:22:16 INFO mapreduce.Job:  map 100% reduce 96%
17/05/12 03:22:19 INFO mapreduce.Job:  map 100% reduce 98%
17/05/12 03:22:22 INFO mapreduce.Job:  map 100% reduce 99%
17/05/12 03:22:23 INFO mapreduce.Job:  map 100% reduce 100%
17/05/12 03:22:24 INFO mapreduce.Job: Job job_1494558460258_0001 completed successfully
17/05/12 03:22:24 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2931602187
                FILE: Number of bytes written=5818183152
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553612138
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=324
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters 
                Launched map tasks=102
                Launched reduce tasks=6
                Data-local map tasks=102
                Total time spent by all maps in occupied slots (ms)=1059332
                Total time spent by all reduces in occupied slots (ms)=333379
                Total time spent by all map tasks (ms)=1059332
                Total time spent by all reduce tasks (ms)=333379
                Total vcore-seconds taken by all map tasks=1059332
                Total vcore-seconds taken by all reduce tasks=333379
                Total megabyte-seconds taken by all map tasks=1084755968
                Total megabyte-seconds taken by all reduce tasks=341380096
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2873057831
                Input split bytes=12138
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2873057831
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =612
                Failed Shuffles=0
                Merged Map outputs=612
                GC time elapsed (ms)=16049
                CPU time spent (ms)=755360
                Physical memory (bytes) snapshot=56777822208
                Virtual memory (bytes) snapshot=168897175552
                Total committed heap usage (bytes)=67177021440
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters 
                Bytes Read=6553600000
        File Output Format Counters 
                Bytes Written=6553600000
17/05/12 03:22:24 INFO terasort.TeraSort: done

real    3m41.697s
user    0m8.723s
sys     0m0.914s
```