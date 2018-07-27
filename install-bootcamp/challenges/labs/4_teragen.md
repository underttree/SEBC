# Challenge 4 - HDFS Testing

### The full teragen command and output
> time sudo -u goldengate hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Ddfs.blocksize=67108864 -Dmapreduce.map.memory.mb=768 -Dmapred.reduce.tasks=8 65536000 /user/goldengate/tgen 
```
18/07/27 18:35:19 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-9-19.us-east-2.compute.internal/172.31.9.19:8032
18/07/27 18:35:20 INFO terasort.TeraSort: Generating 65536000 using 2
18/07/27 18:35:20 INFO mapreduce.JobSubmitter: number of splits:2
18/07/27 18:35:20 INFO Configuration.deprecation: mapred.reduce.tasks is deprecated. Instead, use mapreduce.job.reduces
18/07/27 18:35:20 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1532714394430_0024
18/07/27 18:35:21 INFO impl.YarnClientImpl: Submitted application application_1532714394430_0024
18/07/27 18:35:21 INFO mapreduce.Job: The url to track the job: http://ip-172-31-9-19.us-east-2.compute.internal:8088/proxy/application_1532714394430_0024/
18/07/27 18:35:21 INFO mapreduce.Job: Running job: job_1532714394430_0024
18/07/27 18:35:34 INFO mapreduce.Job: Job job_1532714394430_0024 running in uber mode : false
18/07/27 18:35:34 INFO mapreduce.Job:  map 0% reduce 0%
18/07/27 18:35:50 INFO mapreduce.Job:  map 4% reduce 0%
18/07/27 18:35:53 INFO mapreduce.Job:  map 7% reduce 0%
18/07/27 18:35:56 INFO mapreduce.Job:  map 11% reduce 0%
18/07/27 18:35:59 INFO mapreduce.Job:  map 14% reduce 0%
18/07/27 18:36:02 INFO mapreduce.Job:  map 17% reduce 0%
18/07/27 18:36:05 INFO mapreduce.Job:  map 21% reduce 0%
18/07/27 18:36:08 INFO mapreduce.Job:  map 23% reduce 0%
18/07/27 18:36:09 INFO mapreduce.Job:  map 25% reduce 0%
18/07/27 18:36:12 INFO mapreduce.Job:  map 26% reduce 0%
18/07/27 18:36:17 INFO mapreduce.Job:  map 28% reduce 0%
18/07/27 18:36:18 INFO mapreduce.Job:  map 30% reduce 0%
18/07/27 18:36:20 INFO mapreduce.Job:  map 32% reduce 0%
18/07/27 18:36:21 INFO mapreduce.Job:  map 34% reduce 0%
18/07/27 18:36:23 INFO mapreduce.Job:  map 35% reduce 0%
18/07/27 18:36:24 INFO mapreduce.Job:  map 38% reduce 0%
18/07/27 18:36:26 INFO mapreduce.Job:  map 40% reduce 0%
18/07/27 18:36:27 INFO mapreduce.Job:  map 42% reduce 0%
18/07/27 18:36:29 INFO mapreduce.Job:  map 44% reduce 0%
18/07/27 18:36:30 INFO mapreduce.Job:  map 46% reduce 0%
18/07/27 18:36:32 INFO mapreduce.Job:  map 48% reduce 0%
18/07/27 18:36:33 INFO mapreduce.Job:  map 49% reduce 0%
18/07/27 18:36:41 INFO mapreduce.Job:  map 51% reduce 0%
18/07/27 18:36:42 INFO mapreduce.Job:  map 53% reduce 0%
18/07/27 18:36:44 INFO mapreduce.Job:  map 55% reduce 0%
18/07/27 18:36:45 INFO mapreduce.Job:  map 57% reduce 0%
18/07/27 18:36:48 INFO mapreduce.Job:  map 59% reduce 0%
18/07/27 18:36:49 INFO mapreduce.Job:  map 60% reduce 0%
18/07/27 18:36:52 INFO mapreduce.Job:  map 64% reduce 0%
18/07/27 18:36:55 INFO mapreduce.Job:  map 68% reduce 0%
18/07/27 18:36:58 INFO mapreduce.Job:  map 70% reduce 0%
18/07/27 18:37:01 INFO mapreduce.Job:  map 72% reduce 0%
18/07/27 18:37:04 INFO mapreduce.Job:  map 75% reduce 0%
18/07/27 18:37:07 INFO mapreduce.Job:  map 77% reduce 0%
18/07/27 18:37:10 INFO mapreduce.Job:  map 80% reduce 0%
18/07/27 18:37:13 INFO mapreduce.Job:  map 82% reduce 0%
18/07/27 18:37:16 INFO mapreduce.Job:  map 86% reduce 0%
18/07/27 18:37:19 INFO mapreduce.Job:  map 89% reduce 0%
18/07/27 18:37:22 INFO mapreduce.Job:  map 93% reduce 0%
18/07/27 18:37:25 INFO mapreduce.Job:  map 94% reduce 0%
18/07/27 18:37:28 INFO mapreduce.Job:  map 96% reduce 0%
18/07/27 18:37:31 INFO mapreduce.Job:  map 99% reduce 0%
18/07/27 18:37:33 INFO mapreduce.Job:  map 100% reduce 0%
18/07/27 18:37:33 INFO mapreduce.Job: Job job_1532714394430_0024 completed successfully
18/07/27 18:37:33 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=247058
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=170
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=8
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=4
	Job Counters 
		Launched map tasks=2
		Other local map tasks=2
		Total time spent by all maps in occupied slots (ms)=231323
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=231323
		Total vcore-seconds taken by all map tasks=231323
		Total megabyte-seconds taken by all map tasks=236874752
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Input split bytes=170
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=1212
		CPU time spent (ms)=114300
		Physical memory (bytes) snapshot=363466752
		Virtual memory (bytes) snapshot=2700959744
		Total committed heap usage (bytes)=414711808
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=140750829423462787
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=6553600000
```

### The result of the time command
```
real	2m15.925s
user	0m6.008s
sys	0m0.369s
```

### The command and output
> hdfs dfs -ls /user/goldengate/tgen
```
Found 3 items
-rw-r--r--   3 goldengate goldengate          0 2018-07-27 18:37 /user/goldengate/tgen/_SUCCESS
-rw-r--r--   3 goldengate goldengate 3276800000 2018-07-27 18:37 /user/goldengate/tgen/part-m-00000
-rw-r--r--   3 goldengate goldengate 3276800000 2018-07-27 18:37 /user/goldengate/tgen/part-m-00001
```

> hadoop fsck -blocks /user/goldengate
```
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-9-19.us-east-2.compute.internal:50070
FSCK started by goldengate (auth:SIMPLE) from /172.31.9.19 for path /user/goldengate at Fri Jul 27 18:39:51 UTC 2018
...Status: HEALTHY
 Total size:	6553600000 B
 Total dirs:	3
 Total files:	3
 Total symlinks:		0
 Total blocks (validated):	98 (avg. block size 66873469 B)
 Minimally replicated blocks:	98 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		3
 Number of racks:		1
FSCK ended at Fri Jul 27 18:39:51 UTC 2018 in 5 milliseconds


The filesystem under path '/user/goldengate' is HEALTHY
``` 

