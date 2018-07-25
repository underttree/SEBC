sudo -u hdfs hdfs dfs /user/underttree 

hadoop jar /opt/cloudera/parcels/CDH-5.9.3-1.cdh5.9.3.p0.4/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen 5000000 /user/underttree/500mbfile

sudo -u hdfs hadoop distcp hdfs://18.222.54.165/user/underttree/500mbfile hdfs://40.70.201.41/thiagoabb/target

18/07/24 22:28:31 INFO tools.DistCp: Input Options: DistCpOptions{atomicCommit=false, syncFolder=false, deleteMissing=false, ignoreFailures=false, overwrite=false, append=false, useDiff=false, useRdiff=false, fromSnapshot=null, toSnapshot=null, skipCRC=false, blocking=true, numListstatusThreads=0, maxMaps=20, mapBandwidth=100, sslConfigurationFile='null', copyStrategy='uniformsize', preserveStatus=[], preserveRawXattrs=false, atomicWorkPath=null, logPath=null, sourceFileListing=null, sourcePaths=[hdfs://18.222.54.165/user/underttree/500mbfile], targetPath=hdfs://40.70.201.41/thiagoabb/target, targetPathExists=true, filtersFile='null'}
18/07/24 22:28:32 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-33-182.us-east-2.compute.internal/172.31.33.182:8032
18/07/24 22:28:32 INFO tools.SimpleCopyListing: Paths (files+dirs) cnt = 4; dirCnt = 1
18/07/24 22:28:32 INFO tools.SimpleCopyListing: Build file listing completed.
18/07/24 22:28:32 INFO Configuration.deprecation: io.sort.mb is deprecated. Instead, use mapreduce.task.io.sort.mb
18/07/24 22:28:32 INFO Configuration.deprecation: io.sort.factor is deprecated. Instead, use mapreduce.task.io.sort.factor
18/07/24 22:28:33 INFO tools.DistCp: Number of paths in the copy list: 4
18/07/24 22:28:33 INFO tools.DistCp: Number of paths in the copy list: 4
18/07/24 22:28:33 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-33-182.us-east-2.compute.internal/172.31.33.182:8032
18/07/24 22:28:34 INFO mapreduce.JobSubmitter: number of splits:3
18/07/24 22:28:34 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1532463226902_0572
18/07/24 22:28:35 INFO impl.YarnClientImpl: Submitted application application_1532463226902_0572
18/07/24 22:28:35 INFO mapreduce.Job: The url to track the job: http://ip-172-31-33-182.us-east-2.compute.internal:8088/proxy/application_1532463226902_0572/
18/07/24 22:28:35 INFO tools.DistCp: DistCp job-id: job_1532463226902_0572
18/07/24 22:28:35 INFO mapreduce.Job: Running job: job_1532463226902_0572
18/07/24 22:28:54 INFO mapreduce.Job: Job job_1532463226902_0572 running in uber mode : false
18/07/24 22:28:54 INFO mapreduce.Job:  map 0% reduce 0%
18/07/24 22:29:15 INFO mapreduce.Job:  map 33% reduce 0%
18/07/24 22:29:18 INFO mapreduce.Job:  map 67% reduce 0%
18/07/24 22:29:19 INFO mapreduce.Job:  map 100% reduce 0%
18/07/24 22:38:20 INFO mapreduce.Job: Task Id : attempt_1532463226902_0572_m_000002_0, Status : FAILED
Error: java.io.IOException: File copy failed: hdfs://18.222.54.165/user/underttree/500mbfile/part-m-00001 --> hdfs://40.70.201.41/thiagoabb/target/500mbfile/part-m-00001
	at org.apache.hadoop.tools.mapred.CopyMapper.copyFileWithRetry(CopyMapper.java:284)
	at org.apache.hadoop.tools.mapred.CopyMapper.map(CopyMapper.java:252)
	at org.apache.hadoop.tools.mapred.CopyMapper.map(CopyMapper.java:50)
	at org.apache.hadoop.mapreduce.Mapper.run(Mapper.java:145)
	at org.apache.hadoop.mapred.MapTask.runNewMapper(MapTask.java:787)
	at org.apache.hadoop.mapred.MapTask.run(MapTask.java:341)
	at org.apache.hadoop.mapred.YarnChild$2.run(YarnChild.java:164)
	at java.security.AccessController.doPrivileged(Native Method)
	at javax.security.auth.Subject.doAs(Subject.java:415)
	at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1912)
	at org.apache.hadoop.mapred.YarnChild.main(YarnChild.java:158)
Caused by: java.io.IOException: Couldn't run retriable-command: Copying hdfs://18.222.54.165/user/underttree/500mbfile/part-m-00001 to hdfs://40.70.201.41/thiagoabb/target/500mbfile/part-m-00001
	at org.apache.hadoop.tools.util.RetriableCommand.execute(RetriableCommand.java:101)
	at org.apache.hadoop.tools.mapred.CopyMapper.copyFileWithRetry(CopyMapper.java:280)
	... 10 more
Caused by: org.apache.hadoop.ipc.RemoteException(java.io.IOException): File /thiagoabb/target/.distcp.tmp.attempt_1532463226902_0572_m_000002_0 could only be replicated to 0 nodes instead of minReplication (=1).  There are 3 datanode(s) running and 3 node(s) are excluded in this operation.
	at org.apache.hadoop.hdfs.server.blockmanagement.BlockManager.chooseTarget4NewBlock(BlockManager.java:1626)
	at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.getAdditionalBlock(FSNamesystem.java:3351)
	at org.apache.hadoop.hdfs.server.namenode.NameNodeRpcServer.addBlock(NameNodeRpcServer.java:683)
	at org.apache.hadoop.hdfs.server.namenode.AuthorizationProviderProxyClientProtocol.addBlock(AuthorizationProviderProxyClientProtocol.java:214)
	at org.apache.hadoop.hdfs.protocolPB.ClientNamenodeProtocolServerSideTranslatorPB.addBlock(ClientNamenodeProtocolServerSideTranslatorPB.java:495)
	at org.apache.hadoop.hdfs.protocol.proto.ClientNamenodeProtocolProtos$ClientNamenodeProtocol$2.callBlockingMethod(ClientNamenodeProtocolProtos.java)
	at org.apache.hadoop.ipc.ProtobufRpcEngine$Server$ProtoBufRpcInvoker.call(ProtobufRpcEngine.java:617)
	at org.apache.hadoop.ipc.RPC$Server.call(RPC.java:1073)
	at org.apache.hadoop.ipc.Server$Handler$1.run(Server.java:2141)
	at org.apache.hadoop.ipc.Server$Handler$1.run(Server.java:2137)
	at java.security.AccessController.doPrivileged(Native Method)
	at javax.security.auth.Subject.doAs(Subject.java:415)
	at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1912)
	at org.apache.hadoop.ipc.Server$Handler.run(Server.java:2135)

	at org.apache.hadoop.ipc.Client.call(Client.java:1502)
	at org.apache.hadoop.ipc.Client.call(Client.java:1439)
	at org.apache.hadoop.ipc.ProtobufRpcEngine$Invoker.invoke(ProtobufRpcEngine.java:230)
	at com.sun.proxy.$Proxy15.addBlock(Unknown Source)
	at org.apache.hadoop.hdfs.protocolPB.ClientNamenodeProtocolTranslatorPB.addBlock(ClientNamenodeProtocolTranslatorPB.java:413)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:57)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:606)
	at org.apache.hadoop.io.retry.RetryInvocationHandler.invokeMethod(RetryInvocationHandler.java:256)
	at org.apache.hadoop.io.retry.RetryInvocationHandler.invoke(RetryInvocationHandler.java:104)
	at com.sun.proxy.$Proxy16.addBlock(Unknown Source)
	at org.apache.hadoop.hdfs.DFSOutputStream$DataStreamer.locateFollowingBlock(DFSOutputStream.java:1811)
	at org.apache.hadoop.hdfs.DFSOutputStream$DataStreamer.nextBlockOutputStream(DFSOutputStream.java:1607)
	at org.apache.hadoop.hdfs.DFSOutputStream$DataStreamer.run(DFSOutputStream.java:771)

18/07/24 22:38:21 INFO mapreduce.Job:  map 67% reduce 0%
18/07/24 22:38:23 INFO mapreduce.Job: Task Id : attempt_1532463226902_0572_m_000001_0, Status : FAILED
Error: java.io.IOException: File copy failed: hdfs://18.222.54.165/user/underttree/500mbfile/part-m-00000 --> hdfs://40.70.201.41/thiagoabb/target/500mbfile/part-m-00000
	at org.apache.hadoop.tools.mapred.CopyMapper.copyFileWithRetry(CopyMapper.java:284)
	at org.apache.hadoop.tools.mapred.CopyMapper.map(CopyMapper.java:252)
	at org.apache.hadoop.tools.mapred.CopyMapper.map(CopyMapper.java:50)
	at org.apache.hadoop.mapreduce.Mapper.run(Mapper.java:145)
	at org.apache.hadoop.mapred.MapTask.runNewMapper(MapTask.java:787)
	at org.apache.hadoop.mapred.MapTask.run(MapTask.java:341)
	at org.apache.hadoop.mapred.YarnChild$2.run(YarnChild.java:164)
	at java.security.AccessController.doPrivileged(Native Method)
	at javax.security.auth.Subject.doAs(Subject.java:415)
	at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1912)
	at org.apache.hadoop.mapred.YarnChild.main(YarnChild.java:158)
Caused by: java.io.IOException: Couldn't run retriable-command: Copying hdfs://18.222.54.165/user/underttree/500mbfile/part-m-00000 to hdfs://40.70.201.41/thiagoabb/target/500mbfile/part-m-00000
	at org.apache.hadoop.tools.util.RetriableCommand.execute(RetriableCommand.java:101)
	at org.apache.hadoop.tools.mapred.CopyMapper.copyFileWithRetry(CopyMapper.java:280)
	... 10 more
Caused by: org.apache.hadoop.ipc.RemoteException(java.io.IOException): File /thiagoabb/target/.distcp.tmp.attempt_1532463226902_0572_m_000001_0 could only be replicated to 0 nodes instead of minReplication (=1).  There are 3 datanode(s) running and 3 node(s) are excluded in this operation.
	at org.apache.hadoop.hdfs.server.blockmanagement.BlockManager.chooseTarget4NewBlock(BlockManager.java:1626)
	at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.getAdditionalBlock(FSNamesystem.java:3351)
	at org.apache.hadoop.hdfs.server.namenode.NameNodeRpcServer.addBlock(NameNodeRpcServer.java:683)
	at org.apache.hadoop.hdfs.server.namenode.AuthorizationProviderProxyClientProtocol.addBlock(AuthorizationProviderProxyClientProtocol.java:214)
	at org.apache.hadoop.hdfs.protocolPB.ClientNamenodeProtocolServerSideTranslatorPB.addBlock(ClientNamenodeProtocolServerSideTranslatorPB.java:495)
	at org.apache.hadoop.hdfs.protocol.proto.ClientNamenodeProtocolProtos$ClientNamenodeProtocol$2.callBlockingMethod(ClientNamenodeProtocolProtos.java)
	at org.apache.hadoop.ipc.ProtobufRpcEngine$Server$ProtoBufRpcInvoker.call(ProtobufRpcEngine.java:617)
	at org.apache.hadoop.ipc.RPC$Server.call(RPC.java:1073)
	at org.apache.hadoop.ipc.Server$Handler$1.run(Server.java:2141)
	at org.apache.hadoop.ipc.Server$Handler$1.run(Server.java:2137)
	at java.security.AccessController.doPrivileged(Native Method)
	at javax.security.auth.Subject.doAs(Subject.java:415)
	at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1912)
	at org.apache.hadoop.ipc.Server$Handler.run(Server.java:2135)

	at org.apache.hadoop.ipc.Client.call(Client.java:1502)
	at org.apache.hadoop.ipc.Client.call(Client.java:1439)
	at org.apache.hadoop.ipc.ProtobufRpcEngine$Invoker.invoke(ProtobufRpcEngine.java:230)
	at com.sun.proxy.$Proxy15.addBlock(Unknown Source)
	at org.apache.hadoop.hdfs.protocolPB.ClientNamenodeProtocolTranslatorPB.addBlock(ClientNamenodeProtocolTranslatorPB.java:413)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:57)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:606)
	at org.apache.hadoop.io.retry.RetryInvocationHandler.invokeMethod(RetryInvocationHandler.java:256)
	at org.apache.hadoop.io.retry.RetryInvocationHandler.invoke(RetryInvocationHandler.java:104)
	at com.sun.proxy.$Proxy16.addBlock(Unknown Source)
	at org.apache.hadoop.hdfs.DFSOutputStream$DataStreamer.locateFollowingBlock(DFSOutputStream.java:1811)
	at org.apache.hadoop.hdfs.DFSOutputStream$DataStreamer.nextBlockOutputStream(DFSOutputStream.java:1607)
	at org.apache.hadoop.hdfs.DFSOutputStream$DataStreamer.run(DFSOutputStream.java:771)

18/07/24 22:38:24 INFO mapreduce.Job:  map 33% reduce 0%
18/07/24 22:38:37 INFO mapreduce.Job:  map 67% reduce 0%
18/07/24 22:38:42 INFO mapreduce.Job:  map 100% reduce 0%
18/07/24 22:39:29 INFO mapreduce.Job:  map 0% reduce 0%
18/07/24 22:39:29 INFO mapreduce.Job: Job job_1532463226902_0572 failed with state KILLED due to: Application killed by user.
18/07/24 22:39:29 INFO mapreduce.Job: Counters: 0
18/07/24 22:39:29 ERROR tools.DistCp: Exception encountered 
java.io.IOException: DistCp failure: Job job_1532463226902_0572 has failed: Application killed by user.
	at org.apache.hadoop.tools.DistCp.execute(DistCp.java:193)
	at org.apache.hadoop.tools.DistCp.run(DistCp.java:141)
	at org.apache.hadoop.util.ToolRunner.run(ToolRunner.java:70)
	at org.apache.hadoop.tools.DistCp.main(DistCp.java:441)