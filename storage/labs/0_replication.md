¡ñ Choose a partner in class
```
my partner GitHub handle is :  hackty
```

¡ñ Name a source directory after your GitHub handle
```
[root@masternode ~]# sudo -u hdfs hdfs dfs -mkdir -p /user/jnmaomao/source
[root@masternode ~]# sudo -u hdfs hdfs dfs -mkdir -p /user/jnmaomao/target
```

¡ñ Name a target directory after your partner's GitHub handle
```
[root@masternode ~]# sudo -u hdfs hdfs dfs -mkdir -p /user/hackty/source
[root@masternode ~]# sudo -u hdfs hdfs dfs -mkdir -p /user/hackty/target
```

¡ñ Use teragen to create a 500 MB file
```
[root@masternode ~]# sudo -u hdfs hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen 5242880 /user/jnmaomao/source/test_data_for_replicate
17/05/09 03:56:35 INFO client.RMProxy: Connecting to ResourceManager at masternode.com/172.31.36.73:8032
17/05/09 03:56:35 INFO terasort.TeraSort: Generating 5242880 using 2
17/05/09 03:56:35 INFO mapreduce.JobSubmitter: number of splits:2
17/05/09 03:56:36 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494300061404_0002
17/05/09 03:56:36 INFO impl.YarnClientImpl: Submitted application application_1494300061404_0002
17/05/09 03:56:36 INFO mapreduce.Job: The url to track the job: http://masternode.com:8088/proxy/application_1494300061404_0002/
17/05/09 03:56:36 INFO mapreduce.Job: Running job: job_1494300061404_0002
17/05/09 03:56:43 INFO mapreduce.Job: Job job_1494300061404_0002 running in uber mode : false
17/05/09 03:56:43 INFO mapreduce.Job:  map 0% reduce 0%
17/05/09 03:56:53 INFO mapreduce.Job:  map 50% reduce 0%
17/05/09 03:56:54 INFO mapreduce.Job:  map 100% reduce 0%
17/05/09 03:56:54 INFO mapreduce.Job: Job job_1494300061404_0002 completed successfully
17/05/09 03:56:54 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=246112
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=167
                HDFS: Number of bytes written=524288000
                HDFS: Number of read operations=8
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters 
                Launched map tasks=2
                Other local map tasks=2
                Total time spent by all maps in occupied slots (ms)=16646
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=16646
                Total vcore-seconds taken by all map tasks=16646
                Total megabyte-seconds taken by all map tasks=17045504
        Map-Reduce Framework
                Map input records=5242880
                Map output records=5242880
                Input split bytes=167
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=211
                CPU time spent (ms)=13260
                Physical memory (bytes) snapshot=740544512
                Virtual memory (bytes) snapshot=3135188992
                Total committed heap usage (bytes)=875560960
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=11257830824958050
        File Input Format Counters 
                Bytes Read=0
        File Output Format Counters 
                Bytes Written=524288000
```

  ¡ñ Copy your partner's file to your target directory
  1.Let one partner use distCp on the command line
  ```
  [root@cmnode ~]#  sudo -u hdfs hadoop distcp hdfs://ec2-34-207-109-113.compute-1.amazonaws.com:8020/user/hackty/500m-input hdfs://ec2-54-201-183-41.us-west-2.compute.amazonaws.com:8020/user/jnmaomao/target/
17/05/09 06:06:54 INFO tools.DistCp: Input Options: DistCpOptions{atomicCommit=false, syncFolder=false, deleteMissing=false, ignoreFailures=false, overwrite=false, append=false, useDiff=false, useRdiff=false, fromSnapshot=null, toSnapshot=null, skipCRC=false, blocking=true, numListstatusThreads=0, maxMaps=20, mapBandwidth=100, sslConfigurationFile='null', copyStrategy='uniformsize', preserveStatus=[], preserveRawXattrs=false, atomicWorkPath=null, logPath=null, sourceFileListing=null, sourcePaths=[hdfs://ec2-34-207-109-113.compute-1.amazonaws.com:8020/user/hackty/500m-input], targetPath=hdfs://ec2-54-201-183-41.us-west-2.compute.amazonaws.com:8020/user/jnmaomao/target, targetPathExists=true, filtersFile='null'}
17/05/09 06:06:54 INFO Configuration.deprecation: session.id is deprecated. Instead, use dfs.metrics.session-id
17/05/09 06:06:54 INFO jvm.JvmMetrics: Initializing JVM Metrics with processName=JobTracker, sessionId=
17/05/09 06:06:55 INFO tools.SimpleCopyListing: Paths (files+dirs) cnt = 4; dirCnt = 1
17/05/09 06:06:55 INFO tools.SimpleCopyListing: Build file listing completed.
17/05/09 06:06:55 INFO Configuration.deprecation: io.sort.mb is deprecated. Instead, use mapreduce.task.io.sort.mb
17/05/09 06:06:55 INFO Configuration.deprecation: io.sort.factor is deprecated. Instead, use mapreduce.task.io.sort.factor
17/05/09 06:06:55 INFO tools.DistCp: Number of paths in the copy list: 4
17/05/09 06:06:55 INFO tools.DistCp: Number of paths in the copy list: 4
17/05/09 06:06:55 INFO jvm.JvmMetrics: Cannot initialize JVM Metrics with processName=JobTracker, sessionId= - already initialized
17/05/09 06:06:55 INFO mapreduce.JobSubmitter: number of splits:1
17/05/09 06:06:55 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_local327825651_0001
17/05/09 06:06:55 INFO mapreduce.Job: The url to track the job: http://localhost:8080/
17/05/09 06:06:55 INFO tools.DistCp: DistCp job-id: job_local327825651_0001
17/05/09 06:06:55 INFO mapreduce.Job: Running job: job_local327825651_0001
17/05/09 06:06:55 INFO mapred.LocalJobRunner: OutputCommitter set in config null
17/05/09 06:06:55 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
17/05/09 06:06:55 INFO mapred.LocalJobRunner: OutputCommitter is org.apache.hadoop.tools.mapred.CopyCommitter
17/05/09 06:06:56 INFO mapred.LocalJobRunner: Waiting for map tasks
17/05/09 06:06:56 INFO mapred.LocalJobRunner: Starting task: attempt_local327825651_0001_m_000000_0
17/05/09 06:06:56 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
17/05/09 06:06:56 INFO mapred.Task:  Using ResourceCalculatorProcessTree : [ ]
17/05/09 06:06:56 INFO mapred.MapTask: Processing split: file:/tmp/hadoop-hdfs/mapred/staging/hdfs1275911915/.staging/_distcp-2033828367/fileList.seq:0+856
17/05/09 06:06:56 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
17/05/09 06:06:56 INFO mapred.CopyMapper: Copying hdfs://ec2-34-207-109-113.compute-1.amazonaws.com:8020/user/hackty/500m-input to hdfs://ec2-54-201-183-41.us-west-2.compute.amazonaws.com:8020/user/jnmaomao/target/500m-input
17/05/09 06:06:56 INFO mapred.CopyMapper: Copying hdfs://ec2-34-207-109-113.compute-1.amazonaws.com:8020/user/hackty/500m-input/_SUCCESS to hdfs://ec2-54-201-183-41.us-west-2.compute.amazonaws.com:8020/user/jnmaomao/target/500m-input/_SUCCESS
17/05/09 06:06:56 INFO mapred.CopyMapper: Skipping copy of hdfs://ec2-34-207-109-113.compute-1.amazonaws.com:8020/user/hackty/500m-input/_SUCCESS to hdfs://ec2-54-201-183-41.us-west-2.compute.amazonaws.com:8020/user/jnmaomao/target/500m-input/_SUCCESS
17/05/09 06:06:56 INFO mapred.CopyMapper: Copying hdfs://ec2-34-207-109-113.compute-1.amazonaws.com:8020/user/hackty/500m-input/part-m-00000 to hdfs://ec2-54-201-183-41.us-west-2.compute.amazonaws.com:8020/user/jnmaomao/target/500m-input/part-m-00000
17/05/09 06:06:56 INFO mapred.RetriableFileCopyCommand: Creating temp file: hdfs://ec2-54-201-183-41.us-west-2.compute.amazonaws.com:8020/user/jnmaomao/target/.distcp.tmp.attempt_local327825651_0001_m_000000_0
17/05/09 06:06:56 INFO mapreduce.Job: Job job_local327825651_0001 running in uber mode : false
17/05/09 06:06:56 INFO mapreduce.Job:  map 0% reduce 0%
17/05/09 06:07:02 INFO mapred.LocalJobRunner: Copying hdfs://ec2-34-207-109-113.compute-1.amazonaws.com:8020/user/hackty/500m-input/part-m-00000 to hdfs://ec2-54-201-183-41.us-west-2.compute.amazonaws.com:8020/user/jnmaomao/target/500m-input/part-m-00000 > map
17/05/09 06:07:02 INFO mapreduce.Job:  map 73% reduce 0%
17/05/09 06:07:56 WARN hdfs.BlockReaderFactory: I/O error constructing remote block reader.
org.apache.hadoop.net.ConnectTimeoutException: 60000 millis timeout while waiting for channel to be ready for connect. ch : java.nio.channels.SocketChannel[connection-pending remote=/172.31.19.226:50010]
        at org.apache.hadoop.net.NetUtils.connect(NetUtils.java:533)
        at org.apache.hadoop.hdfs.DFSClient.newConnectedPeer(DFSClient.java:3527)
        at org.apache.hadoop.hdfs.BlockReaderFactory.nextTcpPeer(BlockReaderFactory.java:840)
        at org.apache.hadoop.hdfs.BlockReaderFactory.getRemoteBlockReaderFromTcp(BlockReaderFactory.java:755)
        at org.apache.hadoop.hdfs.BlockReaderFactory.build(BlockReaderFactory.java:376)
        at org.apache.hadoop.hdfs.DFSInputStream.blockSeekTo(DFSInputStream.java:652)
        at org.apache.hadoop.hdfs.DFSInputStream.readWithStrategy(DFSInputStream.java:879)
        at org.apache.hadoop.hdfs.DFSInputStream.read(DFSInputStream.java:932)
        at java.io.DataInputStream.read(DataInputStream.java:100)
        at org.apache.hadoop.tools.util.ThrottledInputStream.read(ThrottledInputStream.java:77)
        at org.apache.hadoop.tools.mapred.RetriableFileCopyCommand.readBytes(RetriableFileCopyCommand.java:286)
        at org.apache.hadoop.tools.mapred.RetriableFileCopyCommand.copyBytes(RetriableFileCopyCommand.java:251)
        at org.apache.hadoop.tools.mapred.RetriableFileCopyCommand.copyToFile(RetriableFileCopyCommand.java:184)
        at org.apache.hadoop.tools.mapred.RetriableFileCopyCommand.doCopy(RetriableFileCopyCommand.java:124)
        at org.apache.hadoop.tools.mapred.RetriableFileCopyCommand.doExecute(RetriableFileCopyCommand.java:100)
        at org.apache.hadoop.tools.util.RetriableCommand.execute(RetriableCommand.java:87)
        at org.apache.hadoop.tools.mapred.CopyMapper.copyFileWithRetry(CopyMapper.java:280)
        at org.apache.hadoop.tools.mapred.CopyMapper.map(CopyMapper.java:252)
        at org.apache.hadoop.tools.mapred.CopyMapper.map(CopyMapper.java:50)
        at org.apache.hadoop.mapreduce.Mapper.run(Mapper.java:145)
        at org.apache.hadoop.mapred.MapTask.runNewMapper(MapTask.java:787)
        at org.apache.hadoop.mapred.MapTask.run(MapTask.java:341)
        at org.apache.hadoop.mapred.LocalJobRunner$Job$MapTaskRunnable.run(LocalJobRunner.java:270)
        at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:471)
        at java.util.concurrent.FutureTask.run(FutureTask.java:262)
        at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1145)
        at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:615)
        at java.lang.Thread.run(Thread.java:745)
17/05/09 06:07:56 WARN hdfs.DFSClient: Failed to connect to /172.31.19.226:50010 for block, add to deadNodes and continue. org.apache.hadoop.net.ConnectTimeoutException: 60000 millis timeout while waiting for channel to be ready for connect. ch : java.nio.channels.SocketChannel[connection-pending remote=/172.31.19.226:50010]
org.apache.hadoop.net.ConnectTimeoutException: 60000 millis timeout while waiting for channel to be ready for connect. ch : java.nio.channels.SocketChannel[connection-pending remote=/172.31.19.226:50010]
        at org.apache.hadoop.net.NetUtils.connect(NetUtils.java:533)
        at org.apache.hadoop.hdfs.DFSClient.newConnectedPeer(DFSClient.java:3527)
        at org.apache.hadoop.hdfs.BlockReaderFactory.nextTcpPeer(BlockReaderFactory.java:840)
        at org.apache.hadoop.hdfs.BlockReaderFactory.getRemoteBlockReaderFromTcp(BlockReaderFactory.java:755)
        at org.apache.hadoop.hdfs.BlockReaderFactory.build(BlockReaderFactory.java:376)
        at org.apache.hadoop.hdfs.DFSInputStream.blockSeekTo(DFSInputStream.java:652)
        at org.apache.hadoop.hdfs.DFSInputStream.readWithStrategy(DFSInputStream.java:879)
        at org.apache.hadoop.hdfs.DFSInputStream.read(DFSInputStream.java:932)
        at java.io.DataInputStream.read(DataInputStream.java:100)
        at org.apache.hadoop.tools.util.ThrottledInputStream.read(ThrottledInputStream.java:77)
        at org.apache.hadoop.tools.mapred.RetriableFileCopyCommand.readBytes(RetriableFileCopyCommand.java:286)
        at org.apache.hadoop.tools.mapred.RetriableFileCopyCommand.copyBytes(RetriableFileCopyCommand.java:251)
        at org.apache.hadoop.tools.mapred.RetriableFileCopyCommand.copyToFile(RetriableFileCopyCommand.java:184)
        at org.apache.hadoop.tools.mapred.RetriableFileCopyCommand.doCopy(RetriableFileCopyCommand.java:124)
        at org.apache.hadoop.tools.mapred.RetriableFileCopyCommand.doExecute(RetriableFileCopyCommand.java:100)
        at org.apache.hadoop.tools.util.RetriableCommand.execute(RetriableCommand.java:87)
        at org.apache.hadoop.tools.mapred.CopyMapper.copyFileWithRetry(CopyMapper.java:280)
        at org.apache.hadoop.tools.mapred.CopyMapper.map(CopyMapper.java:252)
        at org.apache.hadoop.tools.mapred.CopyMapper.map(CopyMapper.java:50)
        at org.apache.hadoop.mapreduce.Mapper.run(Mapper.java:145)
        at org.apache.hadoop.mapred.MapTask.runNewMapper(MapTask.java:787)
        at org.apache.hadoop.mapred.MapTask.run(MapTask.java:341)
        at org.apache.hadoop.mapred.LocalJobRunner$Job$MapTaskRunnable.run(LocalJobRunner.java:270)
        at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:471)
        at java.util.concurrent.FutureTask.run(FutureTask.java:262)
        at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1145)
        at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:615)
        at java.lang.Thread.run(Thread.java:745)
  ```
  2.Let the other use BDR
  ```
  I take a snapshot by name replication_hdfs_BDR.png
  ```


