# 

### The full teragen command and output
> time sudo -u goldengate hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Ddfs.blocksize=67108864 -Dmapreduce.map.memory.mb=768 -Dmapred.job.reduces=8 65536000 /user/goldengate/tgen
```
18/07/27 18:26:59 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-9-19.us-east-2.compute.internal/172.31.9.19:8032
18/07/27 18:26:59 INFO terasort.TeraSort: Generating 65536000 using 2
18/07/27 18:27:00 INFO mapreduce.JobSubmitter: number of splits:2
18/07/27 18:27:00 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1532714394430_0002
18/07/27 18:27:00 INFO impl.YarnClientImpl: Submitted application application_1532714394430_0002
18/07/27 18:27:00 INFO mapreduce.Job: The url to track the job: http://ip-172-31-9-19.us-east-2.compute.internal:8088/proxy/application_1532714394430_0002/
18/07/27 18:27:00 INFO mapreduce.Job: Running job: job_1532714394430_0002
18/07/27 18:27:07 INFO mapreduce.Job: Job job_1532714394430_0002 running in uber mode : false
18/07/27 18:27:07 INFO mapreduce.Job:  map 0% reduce 0%
18/07/27 18:27:18 INFO mapreduce.Job:  map 13% reduce 0%
18/07/27 18:27:21 INFO mapreduce.Job:  map 18% reduce 0%
18/07/27 18:27:24 INFO mapreduce.Job:  map 22% reduce 0%
18/07/27 18:27:27 INFO mapreduce.Job:  map 26% reduce 0%
18/07/27 18:27:30 INFO mapreduce.Job:  map 31% reduce 0%
18/07/27 18:27:33 INFO mapreduce.Job:  map 35% reduce 0%
18/07/27 18:27:36 INFO mapreduce.Job:  map 39% reduce 0%
18/07/27 18:27:39 INFO mapreduce.Job:  map 43% reduce 0%
18/07/27 18:27:42 INFO mapreduce.Job:  map 48% reduce 0%
18/07/27 18:27:45 INFO mapreduce.Job:  map 52% reduce 0%
18/07/27 18:27:48 INFO mapreduce.Job:  map 56% reduce 0%
18/07/27 18:27:51 INFO mapreduce.Job:  map 59% reduce 0%
18/07/27 18:27:54 INFO mapreduce.Job:  map 62% reduce 0%
18/07/27 18:27:57 INFO mapreduce.Job:  map 69% reduce 0%
18/07/27 18:28:00 INFO mapreduce.Job:  map 73% reduce 0%
18/07/27 18:28:03 INFO mapreduce.Job:  map 77% reduce 0%
18/07/27 18:28:06 INFO mapreduce.Job:  map 82% reduce 0%
18/07/27 18:28:09 INFO mapreduce.Job:  map 86% reduce 0%
18/07/27 18:28:12 INFO mapreduce.Job:  map 90% reduce 0%
18/07/27 18:28:15 INFO mapreduce.Job:  map 94% reduce 0%
18/07/27 18:28:17 INFO mapreduce.Job:  map 96% reduce 0%
18/07/27 18:28:18 INFO mapreduce.Job:  map 98% reduce 0%
18/07/27 18:28:22 INFO mapreduce.Job:  map 99% reduce 0%
18/07/27 18:28:23 INFO mapreduce.Job:  map 100% reduce 0%
18/07/27 18:28:23 INFO mapreduce.Job: Job job_1532714394430_0002 completed successfully
18/07/27 18:28:23 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=247312
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
		Total time spent by all maps in occupied slots (ms)=142451
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=142451
		Total vcore-seconds taken by all map tasks=142451
		Total megabyte-seconds taken by all map tasks=145869824
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Input split bytes=170
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=2400
		CPU time spent (ms)=102860
		Physical memory (bytes) snapshot=405118976
		Virtual memory (bytes) snapshot=2713071616
		Total committed heap usage (bytes)=471859200
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=140750829423462787
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=6553600000
```

### The result of the time command
```
real	1m26.290s
user	0m5.394s
sys	0m0.342s
```

### The command and output 
> hdfs dfs -ls /user/goldengate/tgen
```
Found 3 items
-rw-r--r--   3 goldengate goldengate          0 2018-07-27 18:28 /user/goldengate/tgen/_SUCCESS
-rw-r--r--   3 goldengate goldengate 3276800000 2018-07-27 18:28 /user/goldengate/tgen/part-m-00000
-rw-r--r--   3 goldengate goldengate 3276800000 2018-07-27 18:28 /user/goldengate/tgen/part-m-00001
```

> hadoop fsck -blocks /user/goldengate
```
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-9-19.us-east-2.compute.internal:50070
FSCK started by hdfs (auth:SIMPLE) from /172.31.9.19 for path /user/goldengate at Fri Jul 27 18:32:04 UTC 2018
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
FSCK ended at Fri Jul 27 18:32:04 UTC 2018 in 4 milliseconds


The filesystem under path '/user/goldengate' is HEALTHY
```
