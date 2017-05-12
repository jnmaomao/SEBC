```
[root@masternode ~]# kdestroy 
[root@masternode ~]# kinit chen      
Password for chen@JNMAOMAO.CN: 
[root@masternode ~]# klist 
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: chen@JNMAOMAO.CN

Valid starting     Expires            Service principal
05/12/17 03:27:35  05/13/17 03:27:35  krbtgt/JNMAOMAO.CN@JNMAOMAO.CN
        renew until 05/19/17 03:27:35
[root@masternode ~]# hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 10 20
Number of Maps  = 10
Samples per Map = 20
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Wrote input for Map #8
Wrote input for Map #9
Starting Job
17/05/12 03:27:53 INFO client.RMProxy: Connecting to ResourceManager at masternode.com/172.31.41.25:8032
17/05/12 03:27:53 INFO hdfs.DFSClient: Created token for chen: HDFS_DELEGATION_TOKEN owner=chen@JNMAOMAO.CN, renewer=yarn, realUser=, issueDate=1494559673857, maxDate=1495164473857, sequenceNumber=2, masterKeyId=2 on 172.31.41.25:8020
17/05/12 03:27:53 INFO security.TokenCache: Got dt for hdfs://masternode.com:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.41.25:8020, Ident: (token for chen: HDFS_DELEGATION_TOKEN owner=chen@JNMAOMAO.CN, renewer=yarn, realUser=, issueDate=1494559673857, maxDate=1495164473857, sequenceNumber=2, masterKeyId=2)
17/05/12 03:27:54 INFO input.FileInputFormat: Total input paths to process : 10
17/05/12 03:27:54 INFO mapreduce.JobSubmitter: number of splits:10
17/05/12 03:27:54 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494558460258_0002
17/05/12 03:27:54 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.41.25:8020, Ident: (token for chen: HDFS_DELEGATION_TOKEN owner=chen@JNMAOMAO.CN, renewer=yarn, realUser=, issueDate=1494559673857, maxDate=1495164473857, sequenceNumber=2, masterKeyId=2)
17/05/12 03:27:54 INFO impl.YarnClientImpl: Submitted application application_1494558460258_0002
17/05/12 03:27:54 INFO mapreduce.Job: The url to track the job: http://masternode.com:8088/proxy/application_1494558460258_0002/
17/05/12 03:27:54 INFO mapreduce.Job: Running job: job_1494558460258_0002
17/05/12 03:28:04 INFO mapreduce.Job: Job job_1494558460258_0002 running in uber mode : false
17/05/12 03:28:04 INFO mapreduce.Job:  map 0% reduce 0%
17/05/12 03:28:12 INFO mapreduce.Job:  map 20% reduce 0%
17/05/12 03:28:17 INFO mapreduce.Job:  map 40% reduce 0%
17/05/12 03:28:18 INFO mapreduce.Job:  map 50% reduce 0%
17/05/12 03:28:19 INFO mapreduce.Job:  map 100% reduce 0%
17/05/12 03:28:25 INFO mapreduce.Job:  map 100% reduce 100%
17/05/12 03:28:25 INFO mapreduce.Job: Job job_1494558460258_0002 completed successfully
17/05/12 03:28:25 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=82
                FILE: Number of bytes written=1369240
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=2680
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=43
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters 
                Launched map tasks=10
                Launched reduce tasks=1
                Data-local map tasks=10
                Total time spent by all maps in occupied slots (ms)=95500
                Total time spent by all reduces in occupied slots (ms)=3826
                Total time spent by all map tasks (ms)=95500
                Total time spent by all reduce tasks (ms)=3826
                Total vcore-seconds taken by all map tasks=95500
                Total vcore-seconds taken by all reduce tasks=3826
                Total megabyte-seconds taken by all map tasks=97792000
                Total megabyte-seconds taken by all reduce tasks=3917824
        Map-Reduce Framework
                Map input records=10
                Map output records=20
                Map output bytes=180
                Map output materialized bytes=340
                Input split bytes=1500
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=340
                Reduce input records=20
                Reduce output records=0
                Spilled Records=40
                Shuffled Maps =10
                Failed Shuffles=0
                Merged Map outputs=10
                GC time elapsed (ms)=468
                CPU time spent (ms)=9350
                Physical memory (bytes) snapshot=4678623232
                Virtual memory (bytes) snapshot=17191460864
                Total committed heap usage (bytes)=5471993856
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters 
                Bytes Read=1180
        File Output Format Counters 
                Bytes Written=97
Job Finished in 31.973 seconds
Estimated value of Pi is 3.12000000000000000000
```