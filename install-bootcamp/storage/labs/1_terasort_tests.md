# Create an end-user Linux account named with your GitHub handle 

sudo -u hdfs hdfs dfs -mkdir /user/underttree
sudo -u hdfs hdfs dfs -chmod -R 777 /user/underttree
sudo -u hdfs hdfs dfs -chmod -R 777 /user/
 
# Create a 10 GB file using teragen
 CM HDFS > Config > HDFS Block Size 32 MiB

time hadoop jar /opt/cloudera/parcels/CDH-5.9.3-1.cdh5.9.3.p0.4/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen 100000000 /user/underttree/tengigafile

18/07/24 18:45:42 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-33-182.us-east-2.compute.internal/172.31.33.182:8032
18/07/24 18:45:42 INFO terasort.TeraSort: Generating 100000000 using 2
18/07/24 18:45:43 INFO mapreduce.JobSubmitter: number of splits:2
18/07/24 18:45:43 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1532457325179_0022
18/07/24 18:45:44 INFO impl.YarnClientImpl: Submitted application application_1532457325179_0022
18/07/24 18:45:44 INFO mapreduce.Job: The url to track the job: http://ip-172-31-33-182.us-east-2.compute.internal:8088/proxy/application_1532457325179_0022/
18/07/24 18:45:44 INFO mapreduce.Job: Running job: job_1532457325179_0022
18/07/24 18:46:03 INFO mapreduce.Job: Job job_1532457325179_0022 running in uber mode : false
18/07/24 18:46:03 INFO mapreduce.Job:  map 0% reduce 0%
18/07/24 18:46:23 INFO mapreduce.Job:  map 1% reduce 0%
18/07/24 18:46:26 INFO mapreduce.Job:  map 2% reduce 0%
18/07/24 18:46:29 INFO mapreduce.Job:  map 4% reduce 0%
18/07/24 18:46:32 INFO mapreduce.Job:  map 5% reduce 0%
18/07/24 18:46:35 INFO mapreduce.Job:  map 6% reduce 0%
18/07/24 18:46:38 INFO mapreduce.Job:  map 8% reduce 0%
18/07/24 18:46:41 INFO mapreduce.Job:  map 9% reduce 0%
18/07/24 18:46:44 INFO mapreduce.Job:  map 11% reduce 0%
18/07/24 18:46:47 INFO mapreduce.Job:  map 12% reduce 0%
18/07/24 18:46:51 INFO mapreduce.Job:  map 13% reduce 0%
18/07/24 18:46:54 INFO mapreduce.Job:  map 15% reduce 0%
18/07/24 18:46:57 INFO mapreduce.Job:  map 16% reduce 0%
18/07/24 18:47:00 INFO mapreduce.Job:  map 17% reduce 0%
18/07/24 18:47:03 INFO mapreduce.Job:  map 19% reduce 0%
18/07/24 18:47:06 INFO mapreduce.Job:  map 20% reduce 0%
18/07/24 18:47:09 INFO mapreduce.Job:  map 22% reduce 0%
18/07/24 18:47:12 INFO mapreduce.Job:  map 23% reduce 0%
18/07/24 18:47:15 INFO mapreduce.Job:  map 24% reduce 0%
18/07/24 18:47:18 INFO mapreduce.Job:  map 26% reduce 0%
18/07/24 18:47:21 INFO mapreduce.Job:  map 27% reduce 0%
18/07/24 18:47:24 INFO mapreduce.Job:  map 28% reduce 0%
18/07/24 18:47:27 INFO mapreduce.Job:  map 30% reduce 0%
18/07/24 18:47:30 INFO mapreduce.Job:  map 31% reduce 0%
18/07/24 18:47:33 INFO mapreduce.Job:  map 32% reduce 0%
18/07/24 18:47:36 INFO mapreduce.Job:  map 33% reduce 0%
18/07/24 18:47:39 INFO mapreduce.Job:  map 34% reduce 0%
18/07/24 18:47:42 INFO mapreduce.Job:  map 35% reduce 0%
18/07/24 18:47:46 INFO mapreduce.Job:  map 37% reduce 0%
18/07/24 18:47:49 INFO mapreduce.Job:  map 38% reduce 0%
18/07/24 18:47:52 INFO mapreduce.Job:  map 39% reduce 0%
18/07/24 18:47:53 INFO mapreduce.Job:  map 40% reduce 0%
18/07/24 18:47:55 INFO mapreduce.Job:  map 41% reduce 0%
18/07/24 18:47:58 INFO mapreduce.Job:  map 42% reduce 0%
18/07/24 18:47:59 INFO mapreduce.Job:  map 43% reduce 0%
18/07/24 18:48:02 INFO mapreduce.Job:  map 44% reduce 0%
18/07/24 18:48:04 INFO mapreduce.Job:  map 45% reduce 0%
18/07/24 18:48:07 INFO mapreduce.Job:  map 46% reduce 0%
18/07/24 18:48:08 INFO mapreduce.Job:  map 47% reduce 0%
18/07/24 18:48:11 INFO mapreduce.Job:  map 48% reduce 0%
18/07/24 18:48:13 INFO mapreduce.Job:  map 49% reduce 0%
18/07/24 18:48:17 INFO mapreduce.Job:  map 51% reduce 0%
18/07/24 18:48:20 INFO mapreduce.Job:  map 52% reduce 0%
18/07/24 18:48:22 INFO mapreduce.Job:  map 53% reduce 0%
18/07/24 18:48:26 INFO mapreduce.Job:  map 55% reduce 0%
18/07/24 18:48:29 INFO mapreduce.Job:  map 56% reduce 0%
18/07/24 18:48:31 INFO mapreduce.Job:  map 57% reduce 0%
18/07/24 18:48:32 INFO mapreduce.Job:  map 58% reduce 0%
18/07/24 18:48:35 INFO mapreduce.Job:  map 59% reduce 0%
18/07/24 18:48:38 INFO mapreduce.Job:  map 60% reduce 0%
18/07/24 18:48:41 INFO mapreduce.Job:  map 62% reduce 0%
18/07/24 18:48:44 INFO mapreduce.Job:  map 63% reduce 0%
18/07/24 18:48:47 INFO mapreduce.Job:  map 64% reduce 0%
18/07/24 18:48:50 INFO mapreduce.Job:  map 66% reduce 0%
18/07/24 18:48:53 INFO mapreduce.Job:  map 67% reduce 0%
18/07/24 18:48:57 INFO mapreduce.Job:  map 68% reduce 0%
18/07/24 18:49:00 INFO mapreduce.Job:  map 70% reduce 0%
18/07/24 18:49:03 INFO mapreduce.Job:  map 71% reduce 0%
18/07/24 18:49:06 INFO mapreduce.Job:  map 73% reduce 0%
18/07/24 18:49:09 INFO mapreduce.Job:  map 74% reduce 0%
18/07/24 18:49:12 INFO mapreduce.Job:  map 75% reduce 0%
18/07/24 18:49:15 INFO mapreduce.Job:  map 77% reduce 0%
18/07/24 18:49:18 INFO mapreduce.Job:  map 78% reduce 0%
18/07/24 18:49:21 INFO mapreduce.Job:  map 79% reduce 0%
18/07/24 18:49:24 INFO mapreduce.Job:  map 80% reduce 0%
18/07/24 18:49:27 INFO mapreduce.Job:  map 82% reduce 0%
18/07/24 18:49:30 INFO mapreduce.Job:  map 83% reduce 0%
18/07/24 18:49:33 INFO mapreduce.Job:  map 85% reduce 0%
18/07/24 18:49:39 INFO mapreduce.Job:  map 87% reduce 0%
18/07/24 18:49:42 INFO mapreduce.Job:  map 88% reduce 0%
18/07/24 18:49:45 INFO mapreduce.Job:  map 89% reduce 0%
18/07/24 18:49:48 INFO mapreduce.Job:  map 91% reduce 0%
18/07/24 18:49:51 INFO mapreduce.Job:  map 92% reduce 0%
18/07/24 18:49:54 INFO mapreduce.Job:  map 94% reduce 0%
18/07/24 18:50:01 INFO mapreduce.Job:  map 95% reduce 0%
18/07/24 18:50:04 INFO mapreduce.Job:  map 96% reduce 0%
18/07/24 18:50:07 INFO mapreduce.Job:  map 97% reduce 0%
18/07/24 18:50:10 INFO mapreduce.Job:  map 99% reduce 0%
18/07/24 18:50:13 INFO mapreduce.Job:  map 100% reduce 0%
18/07/24 18:50:15 INFO mapreduce.Job: Job job_1532457325179_0022 completed successfully
18/07/24 18:50:15 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=247076
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=170
		HDFS: Number of bytes written=10000000000
		HDFS: Number of read operations=8
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=4
	Job Counters 
		Launched map tasks=2
		Other local map tasks=2
		Total time spent by all maps in occupied slots (ms)=495590
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=495590
		Total vcore-seconds taken by all map tasks=495590
		Total megabyte-seconds taken by all map tasks=507484160
	Map-Reduce Framework
		Map input records=100000000
		Map output records=100000000
		Input split bytes=170
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=4590
		CPU time spent (ms)=164340
		Physical memory (bytes) snapshot=589545472
		Virtual memory (bytes) snapshot=3129434112
		Total committed heap usage (bytes)=697303040
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=214760662691937609
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=10000000000

real	4m35.534s
user	0m5.804s
sys	0m0.397s


# Run the terasort command on this file 

time hadoop jar /opt/cloudera/parcels/CDH-5.9.3-1.cdh5.9.3.p0.4/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort /user/underttree/tengigafile /user/underttree/tengigasort
18/07/24 18:58:22 INFO terasort.TeraSort: starting
18/07/24 18:58:24 INFO input.FileInputFormat: Total input paths to process : 2
Spent 253ms computing base-splits.
Spent 6ms computing TeraScheduler splits.
Computing input splits took 260ms
Sampling 10 splits of 298
Making 6 from 100000 sampled records
Computing parititions took 898ms
Spent 1160ms computing partitions.
18/07/24 18:58:25 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-33-182.us-east-2.compute.internal/172.31.33.182:8032
18/07/24 18:58:26 INFO mapreduce.JobSubmitter: number of splits:298
18/07/24 18:58:26 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1532457325179_0086
18/07/24 18:58:26 INFO impl.YarnClientImpl: Submitted application application_1532457325179_0086
18/07/24 18:58:26 INFO mapreduce.Job: The url to track the job: http://ip-172-31-33-182.us-east-2.compute.internal:8088/proxy/application_1532457325179_0086/
18/07/24 18:58:26 INFO mapreduce.Job: Running job: job_1532457325179_0086
18/07/24 18:58:42 INFO mapreduce.Job: Job job_1532457325179_0086 running in uber mode : false
18/07/24 18:58:42 INFO mapreduce.Job:  map 0% reduce 0%
18/07/24 18:59:00 INFO mapreduce.Job:  map 1% reduce 0%
18/07/24 18:59:08 INFO mapreduce.Job:  map 2% reduce 0%
18/07/24 18:59:09 INFO mapreduce.Job:  map 3% reduce 0%
18/07/24 18:59:17 INFO mapreduce.Job:  map 4% reduce 0%
18/07/24 18:59:29 INFO mapreduce.Job:  map 5% reduce 0%
18/07/24 18:59:33 INFO mapreduce.Job:  map 6% reduce 0%
18/07/24 18:59:35 INFO mapreduce.Job:  map 7% reduce 0%
18/07/24 18:59:40 INFO mapreduce.Job:  map 8% reduce 0%
18/07/24 18:59:52 INFO mapreduce.Job:  map 9% reduce 0%
18/07/24 18:59:57 INFO mapreduce.Job:  map 10% reduce 0%
18/07/24 19:00:04 INFO mapreduce.Job:  map 11% reduce 0%
18/07/24 19:00:07 INFO mapreduce.Job:  map 12% reduce 0%
18/07/24 19:00:18 INFO mapreduce.Job:  map 13% reduce 0%
18/07/24 19:00:22 INFO mapreduce.Job:  map 14% reduce 0%
18/07/24 19:00:30 INFO mapreduce.Job:  map 15% reduce 0%
18/07/24 19:00:35 INFO mapreduce.Job:  map 16% reduce 0%
18/07/24 19:00:41 INFO mapreduce.Job:  map 17% reduce 0%
18/07/24 19:00:53 INFO mapreduce.Job:  map 18% reduce 0%
18/07/24 19:00:55 INFO mapreduce.Job:  map 19% reduce 0%
18/07/24 19:01:04 INFO mapreduce.Job:  map 20% reduce 0%
18/07/24 19:01:11 INFO mapreduce.Job:  map 21% reduce 0%
18/07/24 19:01:26 INFO mapreduce.Job:  map 22% reduce 0%
18/07/24 19:01:29 INFO mapreduce.Job:  map 23% reduce 0%
18/07/24 19:01:30 INFO mapreduce.Job:  map 24% reduce 0%
18/07/24 19:01:45 INFO mapreduce.Job:  map 25% reduce 0%
18/07/24 19:01:51 INFO mapreduce.Job:  map 26% reduce 0%
18/07/24 19:01:57 INFO mapreduce.Job:  map 27% reduce 0%
18/07/24 19:02:00 INFO mapreduce.Job:  map 28% reduce 0%
18/07/24 19:02:03 INFO mapreduce.Job:  map 29% reduce 0%
18/07/24 19:02:16 INFO mapreduce.Job:  map 30% reduce 0%
18/07/24 19:02:22 INFO mapreduce.Job:  map 31% reduce 0%
18/07/24 19:02:30 INFO mapreduce.Job:  map 32% reduce 0%
18/07/24 19:02:34 INFO mapreduce.Job:  map 33% reduce 0%
18/07/24 19:02:44 INFO mapreduce.Job:  map 34% reduce 0%
18/07/24 19:02:50 INFO mapreduce.Job:  map 35% reduce 0%
18/07/24 19:02:56 INFO mapreduce.Job:  map 36% reduce 0%
18/07/24 19:03:03 INFO mapreduce.Job:  map 37% reduce 0%
18/07/24 19:03:07 INFO mapreduce.Job:  map 38% reduce 0%
18/07/24 19:03:19 INFO mapreduce.Job:  map 39% reduce 0%
18/07/24 19:03:23 INFO mapreduce.Job:  map 40% reduce 0%
18/07/24 19:03:26 INFO mapreduce.Job:  map 41% reduce 0%
18/07/24 19:03:34 INFO mapreduce.Job:  map 42% reduce 0%
18/07/24 19:03:47 INFO mapreduce.Job:  map 43% reduce 0%
18/07/24 19:03:53 INFO mapreduce.Job:  map 44% reduce 0%
18/07/24 19:03:56 INFO mapreduce.Job:  map 45% reduce 0%
18/07/24 19:04:14 INFO mapreduce.Job:  map 46% reduce 0%
18/07/24 19:04:17 INFO mapreduce.Job:  map 47% reduce 0%
18/07/24 19:04:18 INFO mapreduce.Job:  map 48% reduce 0%
18/07/24 19:04:34 INFO mapreduce.Job:  map 49% reduce 0%
18/07/24 19:04:35 INFO mapreduce.Job:  map 50% reduce 0%
18/07/24 19:04:44 INFO mapreduce.Job:  map 51% reduce 0%
18/07/24 19:04:51 INFO mapreduce.Job:  map 52% reduce 0%
18/07/24 19:04:57 INFO mapreduce.Job:  map 53% reduce 0%
18/07/24 19:05:05 INFO mapreduce.Job:  map 54% reduce 0%
18/07/24 19:05:08 INFO mapreduce.Job:  map 55% reduce 0%
18/07/24 19:05:19 INFO mapreduce.Job:  map 56% reduce 0%
18/07/24 19:05:25 INFO mapreduce.Job:  map 57% reduce 0%
18/07/24 19:05:29 INFO mapreduce.Job:  map 58% reduce 0%
18/07/24 19:05:40 INFO mapreduce.Job:  map 59% reduce 0%
18/07/24 19:05:44 INFO mapreduce.Job:  map 60% reduce 0%
18/07/24 19:05:51 INFO mapreduce.Job:  map 61% reduce 0%
18/07/24 19:05:58 INFO mapreduce.Job:  map 62% reduce 0%
18/07/24 19:06:05 INFO mapreduce.Job:  map 63% reduce 0%
18/07/24 19:06:11 INFO mapreduce.Job:  map 64% reduce 0%
18/07/24 19:06:16 INFO mapreduce.Job:  map 65% reduce 0%
18/07/24 19:06:26 INFO mapreduce.Job:  map 66% reduce 0%
18/07/24 19:06:31 INFO mapreduce.Job:  map 67% reduce 0%
18/07/24 19:06:34 INFO mapreduce.Job:  map 68% reduce 0%
18/07/24 19:06:45 INFO mapreduce.Job:  map 69% reduce 0%
18/07/24 19:06:50 INFO mapreduce.Job:  map 70% reduce 0%
18/07/24 19:06:57 INFO mapreduce.Job:  map 71% reduce 0%
18/07/24 19:07:02 INFO mapreduce.Job:  map 72% reduce 0%
18/07/24 19:07:06 INFO mapreduce.Job:  map 73% reduce 0%
18/07/24 19:07:20 INFO mapreduce.Job:  map 74% reduce 0%
18/07/24 19:07:23 INFO mapreduce.Job:  map 75% reduce 0%
18/07/24 19:07:25 INFO mapreduce.Job:  map 76% reduce 0%
18/07/24 19:07:38 INFO mapreduce.Job:  map 77% reduce 0%
18/07/24 19:07:40 INFO mapreduce.Job:  map 78% reduce 0%
18/07/24 19:07:48 INFO mapreduce.Job:  map 79% reduce 0%
18/07/24 19:07:56 INFO mapreduce.Job:  map 80% reduce 0%
18/07/24 19:07:59 INFO mapreduce.Job:  map 81% reduce 0%
18/07/24 19:08:12 INFO mapreduce.Job:  map 82% reduce 0%
18/07/24 19:08:16 INFO mapreduce.Job:  map 83% reduce 0%
18/07/24 19:08:16 INFO mapreduce.Job: Task Id : attempt_1532457325179_0086_r_000000_0, Status : FAILED
Error: org.apache.hadoop.mapreduce.task.reduce.Shuffle$ShuffleError: error in shuffle in fetcher#1
	at org.apache.hadoop.mapreduce.task.reduce.Shuffle.run(Shuffle.java:134)
	at org.apache.hadoop.mapred.ReduceTask.run(ReduceTask.java:376)
	at org.apache.hadoop.mapred.YarnChild$2.run(YarnChild.java:164)
	at java.security.AccessController.doPrivileged(Native Method)
	at javax.security.auth.Subject.doAs(Subject.java:415)
	at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1912)
	at org.apache.hadoop.mapred.YarnChild.main(YarnChild.java:158)
Caused by: java.io.IOException: Exceeded MAX_FAILED_UNIQUE_FETCHES; bailing-out.
	at org.apache.hadoop.mapreduce.task.reduce.ShuffleSchedulerImpl.checkReducerHealth(ShuffleSchedulerImpl.java:391)
	at org.apache.hadoop.mapreduce.task.reduce.ShuffleSchedulerImpl.copyFailed(ShuffleSchedulerImpl.java:306)
	at org.apache.hadoop.mapreduce.task.reduce.Fetcher.openShuffleUrl(Fetcher.java:294)
	at org.apache.hadoop.mapreduce.task.reduce.Fetcher.copyFromHost(Fetcher.java:335)
	at org.apache.hadoop.mapreduce.task.reduce.Fetcher.run(Fetcher.java:198)

18/07/24 19:08:28 INFO mapreduce.Job:  map 83% reduce 3%
18/07/24 19:08:31 INFO mapreduce.Job:  map 83% reduce 4%
18/07/24 19:08:37 INFO mapreduce.Job:  map 84% reduce 4%
18/07/24 19:08:44 INFO mapreduce.Job:  map 84% reduce 6%
18/07/24 19:08:47 INFO mapreduce.Job:  map 85% reduce 6%
18/07/24 19:08:59 INFO mapreduce.Job:  map 85% reduce 7%
18/07/24 19:09:04 INFO mapreduce.Job:  map 86% reduce 7%
18/07/24 19:09:07 INFO mapreduce.Job:  map 86% reduce 9%
18/07/24 19:09:15 INFO mapreduce.Job:  map 87% reduce 10%
18/07/24 19:09:19 INFO mapreduce.Job:  map 87% reduce 11%
18/07/24 19:09:24 INFO mapreduce.Job:  map 87% reduce 12%
18/07/24 19:09:27 INFO mapreduce.Job:  map 87% reduce 14%
18/07/24 19:09:30 INFO mapreduce.Job:  map 88% reduce 15%
18/07/24 19:09:31 INFO mapreduce.Job:  map 88% reduce 16%
18/07/24 19:09:35 INFO mapreduce.Job:  map 88% reduce 17%
18/07/24 19:09:36 INFO mapreduce.Job:  map 88% reduce 19%
18/07/24 19:09:39 INFO mapreduce.Job:  map 88% reduce 20%
18/07/24 19:09:45 INFO mapreduce.Job:  map 88% reduce 21%
18/07/24 19:09:46 INFO mapreduce.Job:  map 89% reduce 21%
18/07/24 19:09:48 INFO mapreduce.Job:  map 89% reduce 23%
18/07/24 19:09:53 INFO mapreduce.Job:  map 89% reduce 24%
18/07/24 19:09:57 INFO mapreduce.Job:  map 90% reduce 24%
18/07/24 19:10:01 INFO mapreduce.Job:  map 90% reduce 25%
18/07/24 19:10:14 INFO mapreduce.Job:  map 91% reduce 25%
18/07/24 19:10:20 INFO mapreduce.Job:  map 92% reduce 25%
18/07/24 19:10:25 INFO mapreduce.Job:  map 92% reduce 26%
18/07/24 19:10:35 INFO mapreduce.Job:  map 93% reduce 26%
18/07/24 19:10:44 INFO mapreduce.Job:  map 94% reduce 26%
18/07/24 19:10:59 INFO mapreduce.Job:  map 95% reduce 26%
18/07/24 19:11:12 INFO mapreduce.Job:  map 96% reduce 26%
18/07/24 19:11:15 INFO mapreduce.Job:  map 96% reduce 27%
18/07/24 19:11:27 INFO mapreduce.Job:  map 97% reduce 27%
18/07/24 19:11:38 INFO mapreduce.Job:  map 98% reduce 27%
18/07/24 19:11:54 INFO mapreduce.Job:  map 99% reduce 27%
18/07/24 19:11:58 INFO mapreduce.Job:  map 100% reduce 27%
18/07/24 19:12:10 INFO mapreduce.Job:  map 100% reduce 28%
18/07/24 19:12:16 INFO mapreduce.Job:  map 100% reduce 29%
18/07/24 19:12:26 INFO mapreduce.Job:  map 100% reduce 30%
18/07/24 19:12:38 INFO mapreduce.Job:  map 100% reduce 32%
18/07/24 19:12:50 INFO mapreduce.Job:  map 100% reduce 33%
18/07/24 19:12:58 INFO mapreduce.Job:  map 100% reduce 34%
18/07/24 19:13:00 INFO mapreduce.Job:  map 100% reduce 39%
18/07/24 19:13:01 INFO mapreduce.Job:  map 100% reduce 41%
18/07/24 19:13:02 INFO mapreduce.Job:  map 100% reduce 42%
18/07/24 19:13:03 INFO mapreduce.Job:  map 100% reduce 50%
18/07/24 19:13:04 INFO mapreduce.Job:  map 100% reduce 51%
18/07/24 19:13:05 INFO mapreduce.Job:  map 100% reduce 53%
18/07/24 19:13:06 INFO mapreduce.Job:  map 100% reduce 58%
18/07/24 19:13:07 INFO mapreduce.Job:  map 100% reduce 60%
18/07/24 19:13:08 INFO mapreduce.Job:  map 100% reduce 61%
18/07/24 19:13:09 INFO mapreduce.Job:  map 100% reduce 65%
18/07/24 19:13:10 INFO mapreduce.Job:  map 100% reduce 66%
18/07/24 19:13:12 INFO mapreduce.Job:  map 100% reduce 68%
18/07/24 19:13:15 INFO mapreduce.Job:  map 100% reduce 69%
18/07/24 19:13:18 INFO mapreduce.Job:  map 100% reduce 70%
18/07/24 19:13:20 INFO mapreduce.Job:  map 100% reduce 71%
18/07/24 19:13:21 INFO mapreduce.Job:  map 100% reduce 72%
18/07/24 19:13:24 INFO mapreduce.Job:  map 100% reduce 73%
18/07/24 19:13:26 INFO mapreduce.Job:  map 100% reduce 74%
18/07/24 19:13:29 INFO mapreduce.Job:  map 100% reduce 75%
18/07/24 19:13:30 INFO mapreduce.Job:  map 100% reduce 76%
18/07/24 19:13:33 INFO mapreduce.Job:  map 100% reduce 77%
18/07/24 19:13:35 INFO mapreduce.Job:  map 100% reduce 78%
18/07/24 19:13:36 INFO mapreduce.Job:  map 100% reduce 79%
18/07/24 19:13:39 INFO mapreduce.Job:  map 100% reduce 80%
18/07/24 19:13:40 INFO mapreduce.Job:  map 100% reduce 81%
18/07/24 19:13:42 INFO mapreduce.Job:  map 100% reduce 82%
18/07/24 19:13:45 INFO mapreduce.Job:  map 100% reduce 83%
18/07/24 19:13:47 INFO mapreduce.Job:  map 100% reduce 84%
18/07/24 19:13:48 INFO mapreduce.Job:  map 100% reduce 85%
18/07/24 19:13:50 INFO mapreduce.Job:  map 100% reduce 86%
18/07/24 19:13:54 INFO mapreduce.Job:  map 100% reduce 87%
18/07/24 19:13:58 INFO mapreduce.Job:  map 100% reduce 88%
18/07/24 19:14:06 INFO mapreduce.Job:  map 100% reduce 89%
18/07/24 19:14:10 INFO mapreduce.Job:  map 100% reduce 90%
18/07/24 19:14:15 INFO mapreduce.Job:  map 100% reduce 91%
18/07/24 19:14:18 INFO mapreduce.Job:  map 100% reduce 92%
18/07/24 19:14:23 INFO mapreduce.Job:  map 100% reduce 93%
18/07/24 19:14:27 INFO mapreduce.Job:  map 100% reduce 94%
18/07/24 19:14:30 INFO mapreduce.Job:  map 100% reduce 95%
18/07/24 19:14:35 INFO mapreduce.Job:  map 100% reduce 96%
18/07/24 19:14:39 INFO mapreduce.Job:  map 100% reduce 97%
18/07/24 19:14:44 INFO mapreduce.Job:  map 100% reduce 98%
18/07/24 19:14:48 INFO mapreduce.Job:  map 100% reduce 99%
18/07/24 19:14:52 INFO mapreduce.Job:  map 100% reduce 100%
18/07/24 19:14:58 INFO mapreduce.Job: Job job_1532457325179_0086 completed successfully
18/07/24 19:14:58 INFO mapreduce.Job: Counters: 50
	File System Counters
		FILE: Number of bytes read=4450291268
		FILE: Number of bytes written=8830864645
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=10000047978
		HDFS: Number of bytes written=10000000000
		HDFS: Number of read operations=912
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=12
	Job Counters 
		Failed reduce tasks=1
		Launched map tasks=298
		Launched reduce tasks=7
		Data-local map tasks=298
		Total time spent by all maps in occupied slots (ms)=5878512
		Total time spent by all reduces in occupied slots (ms)=2022044
		Total time spent by all map tasks (ms)=5878512
		Total time spent by all reduce tasks (ms)=2022044
		Total vcore-seconds taken by all map tasks=5878512
		Total vcore-seconds taken by all reduce tasks=2022044
		Total megabyte-seconds taken by all map tasks=6019596288
		Total megabyte-seconds taken by all reduce tasks=2070573056
	Map-Reduce Framework
		Map input records=100000000
		Map output records=100000000
		Map output bytes=10200000000
		Map output materialized bytes=4342562971
		Input split bytes=47978
		Combine input records=0
		Combine output records=0
		Reduce input groups=100000000
		Reduce shuffle bytes=4342562971
		Reduce input records=100000000
		Reduce output records=100000000
		Spilled Records=200000000
		Shuffled Maps =1788
		Failed Shuffles=1
		Merged Map outputs=1788
		GC time elapsed (ms)=87485
		CPU time spent (ms)=1329640
		Physical memory (bytes) snapshot=141096960000
		Virtual memory (bytes) snapshot=455249027072
		Total committed heap usage (bytes)=178710904832
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=1
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters 
		Bytes Read=10000000000
	File Output Format Counters 
		Bytes Written=10000000000
18/07/24 19:14:58 INFO terasort.TeraSort: done

real	16m36.662s
user	0m9.830s
sys	0m0.549s

