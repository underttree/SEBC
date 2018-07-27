#  Challenge 4 - HDFS Testing

### The full teragen command and output
> time sudo -u goldengate hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Ddfs.blocksize=67108864 -Dmapreduce.map.memory.mb=768 -Dmapred.map.tasks=8 65536000 /user/goldengate/tgen 
```
18/07/27 19:15:08 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-9-19.us-east-2.compute.internal/172.31.9.19:8032
18/07/27 19:15:08 INFO terasort.TeraSort: Generating 65536000 using 8
18/07/27 19:15:08 INFO mapreduce.JobSubmitter: number of splits:8
18/07/27 19:15:08 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
18/07/27 19:15:09 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1532714394430_0193
18/07/27 19:15:09 INFO impl.YarnClientImpl: Submitted application application_1532714394430_0193
18/07/27 19:15:09 INFO mapreduce.Job: The url to track the job: http://ip-172-31-9-19.us-east-2.compute.internal:8088/proxy/application_1532714394430_0193/
18/07/27 19:15:09 INFO mapreduce.Job: Running job: job_1532714394430_0193
18/07/27 19:15:20 INFO mapreduce.Job: Job job_1532714394430_0193 running in uber mode : false
18/07/27 19:15:20 INFO mapreduce.Job:  map 0% reduce 0%
18/07/27 19:15:35 INFO mapreduce.Job:  map 3% reduce 0%
18/07/27 19:15:37 INFO mapreduce.Job:  map 10% reduce 0%
18/07/27 19:15:38 INFO mapreduce.Job:  map 11% reduce 0%
18/07/27 19:15:40 INFO mapreduce.Job:  map 16% reduce 0%
18/07/27 19:15:41 INFO mapreduce.Job:  map 18% reduce 0%
18/07/27 19:15:43 INFO mapreduce.Job:  map 22% reduce 0%
18/07/27 19:15:44 INFO mapreduce.Job:  map 23% reduce 0%
18/07/27 19:15:47 INFO mapreduce.Job:  map 24% reduce 0%
18/07/27 19:15:48 INFO mapreduce.Job:  map 15% reduce 0%
18/07/27 19:15:49 INFO mapreduce.Job:  map 17% reduce 0%
18/07/27 19:15:50 INFO mapreduce.Job:  map 18% reduce 0%
18/07/27 19:15:53 INFO mapreduce.Job:  map 19% reduce 0%
18/07/27 19:15:55 INFO mapreduce.Job:  map 21% reduce 0%
18/07/27 19:15:56 INFO mapreduce.Job:  map 24% reduce 0%
18/07/27 19:15:58 INFO mapreduce.Job:  map 26% reduce 0%
18/07/27 19:15:59 INFO mapreduce.Job:  map 29% reduce 0%
18/07/27 19:16:01 INFO mapreduce.Job:  map 31% reduce 0%
18/07/27 19:16:02 INFO mapreduce.Job:  map 33% reduce 0%
18/07/27 19:16:05 INFO mapreduce.Job:  map 34% reduce 0%
18/07/27 19:16:06 INFO mapreduce.Job:  map 36% reduce 0%
18/07/27 19:16:07 INFO mapreduce.Job:  map 38% reduce 0%
18/07/27 19:16:15 INFO mapreduce.Job:  map 41% reduce 0%
18/07/27 19:16:18 INFO mapreduce.Job:  map 43% reduce 0%
18/07/27 19:16:21 INFO mapreduce.Job:  map 45% reduce 0%
18/07/27 19:16:22 INFO mapreduce.Job:  map 47% reduce 0%
18/07/27 19:16:23 INFO mapreduce.Job:  map 48% reduce 0%
18/07/27 19:16:24 INFO mapreduce.Job:  map 50% reduce 0%
18/07/27 19:16:25 INFO mapreduce.Job:  map 52% reduce 0%
18/07/27 19:16:25 INFO mapreduce.Job: Task Id : attempt_1532714394430_0193_m_000001_1, Status : FAILED
Error: org.apache.hadoop.ipc.RemoteException(java.io.IOException): File /user/goldengate/tgen/_temporary/1/_temporary/attempt_1532714394430_0193_m_000001_1/part-m-00001 could only be replicated to 0 nodes instead of minReplication (=1).  There are 3 datanode(s) running and no node(s) are excluded in this operation.
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

18/07/27 19:16:25 INFO mapreduce.Job: Task Id : attempt_1532714394430_0193_m_000005_0, Status : FAILED
Error: org.apache.hadoop.ipc.RemoteException(java.io.IOException): File /user/goldengate/tgen/_temporary/1/_temporary/attempt_1532714394430_0193_m_000005_0/part-m-00005 could only be replicated to 0 nodes instead of minReplication (=1).  There are 3 datanode(s) running and no node(s) are excluded in this operation.
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

18/07/27 19:16:26 INFO mapreduce.Job:  map 40% reduce 0%
18/07/27 19:16:26 INFO mapreduce.Job: Task Id : attempt_1532714394430_0193_m_000002_1, Status : FAILED
Error: org.apache.hadoop.ipc.RemoteException(java.io.IOException): File /user/goldengate/tgen/_temporary/1/_temporary/attempt_1532714394430_0193_m_000002_1/part-m-00002 could only be replicated to 0 nodes instead of minReplication (=1).  There are 3 datanode(s) running and no node(s) are excluded in this operation.
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

18/07/27 19:16:27 INFO mapreduce.Job:  map 38% reduce 0%
18/07/27 19:16:39 INFO mapreduce.Job:  map 41% reduce 0%
18/07/27 19:16:42 INFO mapreduce.Job:  map 43% reduce 0%
18/07/27 19:16:45 INFO mapreduce.Job:  map 44% reduce 0%
18/07/27 19:16:46 INFO mapreduce.Job:  map 48% reduce 0%
18/07/27 19:16:48 INFO mapreduce.Job:  map 50% reduce 0%
18/07/27 19:16:49 INFO mapreduce.Job:  map 53% reduce 0%
18/07/27 19:16:49 INFO mapreduce.Job: Task Id : attempt_1532714394430_0193_m_000006_0, Status : FAILED
Error: org.apache.hadoop.ipc.RemoteException(java.io.IOException): File /user/goldengate/tgen/_temporary/1/_temporary/attempt_1532714394430_0193_m_000006_0/part-m-00006 could only be replicated to 0 nodes instead of minReplication (=1).  There are 3 datanode(s) running and no node(s) are excluded in this operation.
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

18/07/27 19:16:50 INFO mapreduce.Job:  map 44% reduce 0%
18/07/27 19:16:52 INFO mapreduce.Job:  map 47% reduce 0%
18/07/27 19:16:53 INFO mapreduce.Job: Task Id : attempt_1532714394430_0193_m_000005_1, Status : FAILED
Error: org.apache.hadoop.ipc.RemoteException(java.io.IOException): File /user/goldengate/tgen/_temporary/1/_temporary/attempt_1532714394430_0193_m_000005_1/part-m-00005 could only be replicated to 0 nodes instead of minReplication (=1).  There are 3 datanode(s) running and no node(s) are excluded in this operation.
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

18/07/27 19:16:53 INFO mapreduce.Job: Task Id : attempt_1532714394430_0193_m_000001_2, Status : FAILED
Error: org.apache.hadoop.ipc.RemoteException(java.io.IOException): File /user/goldengate/tgen/_temporary/1/_temporary/attempt_1532714394430_0193_m_000001_2/part-m-00001 could only be replicated to 0 nodes instead of minReplication (=1).  There are 3 datanode(s) running and no node(s) are excluded in this operation.
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

18/07/27 19:16:54 INFO mapreduce.Job:  map 38% reduce 0%
18/07/27 19:17:24 INFO mapreduce.Job:  map 40% reduce 0%
18/07/27 19:17:27 INFO mapreduce.Job:  map 42% reduce 0%
18/07/27 19:17:30 INFO mapreduce.Job:  map 44% reduce 0%
18/07/27 19:17:34 INFO mapreduce.Job:  map 46% reduce 0%
18/07/27 19:17:37 INFO mapreduce.Job:  map 48% reduce 0%
18/07/27 19:17:40 INFO mapreduce.Job:  map 50% reduce 0%
18/07/27 19:19:24 INFO mapreduce.Job:  map 53% reduce 0%
18/07/27 19:19:27 INFO mapreduce.Job:  map 55% reduce 0%
18/07/27 19:19:30 INFO mapreduce.Job:  map 57% reduce 0%
18/07/27 19:19:33 INFO mapreduce.Job:  map 59% reduce 0%
18/07/27 19:19:37 INFO mapreduce.Job:  map 60% reduce 0%
18/07/27 19:19:40 INFO mapreduce.Job:  map 63% reduce 0%
18/07/27 19:19:55 INFO mapreduce.Job:  map 64% reduce 0%
18/07/27 19:19:57 INFO mapreduce.Job:  map 68% reduce 0%
18/07/27 19:19:58 INFO mapreduce.Job:  map 69% reduce 0%
18/07/27 19:20:00 INFO mapreduce.Job:  map 72% reduce 0%
18/07/27 19:20:01 INFO mapreduce.Job:  map 74% reduce 0%
18/07/27 19:20:03 INFO mapreduce.Job:  map 77% reduce 0%
18/07/27 19:20:04 INFO mapreduce.Job:  map 79% reduce 0%
18/07/27 19:20:06 INFO mapreduce.Job:  map 82% reduce 0%
18/07/27 19:20:07 INFO mapreduce.Job:  map 84% reduce 0%
18/07/27 19:20:09 INFO mapreduce.Job:  map 87% reduce 0%
18/07/27 19:20:10 INFO mapreduce.Job:  map 89% reduce 0%
18/07/27 19:20:12 INFO mapreduce.Job:  map 90% reduce 0%
18/07/27 19:20:13 INFO mapreduce.Job:  map 91% reduce 0%
18/07/27 19:20:15 INFO mapreduce.Job:  map 93% reduce 0%
18/07/27 19:20:18 INFO mapreduce.Job:  map 94% reduce 0%
18/07/27 19:20:19 INFO mapreduce.Job:  map 96% reduce 0%
18/07/27 19:20:22 INFO mapreduce.Job:  map 99% reduce 0%
18/07/27 19:20:24 INFO mapreduce.Job:  map 100% reduce 0%
18/07/27 19:20:24 INFO mapreduce.Job: Job job_1532714394430_0193 completed successfully
18/07/27 19:20:24 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=988247
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=682
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=32
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=16
	Job Counters 
		Launched map tasks=8
		Other local map tasks=4
		Total time spent by all maps in occupied slots (ms)=141913
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=141913
		Total vcore-seconds taken by all map tasks=141913
		Total megabyte-seconds taken by all map tasks=145318912
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Input split bytes=682
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=2319
		CPU time spent (ms)=154830
		Physical memory (bytes) snapshot=1987780608
		Virtual memory (bytes) snapshot=10900586496
		Total committed heap usage (bytes)=2399666176
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=140750829423462787
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=6553600000
```

### The result of the time command
```
real	5m18.614s
user	0m6.010s
sys	0m0.374s
```

### The command and output
> hdfs dfs -ls /user/goldengate/tgen
```
Found 9 items
-rw-r--r--   3 goldengate goldengate          0 2018-07-27 19:20 /user/goldengate/tgen/_SUCCESS
-rw-r--r--   3 goldengate goldengate  819200000 2018-07-27 19:16 /user/goldengate/tgen/part-m-00000
-rw-r--r--   3 goldengate goldengate  819200000 2018-07-27 19:17 /user/goldengate/tgen/part-m-00001
-rw-r--r--   3 goldengate goldengate  819200000 2018-07-27 19:19 /user/goldengate/tgen/part-m-00002
-rw-r--r--   3 goldengate goldengate  819200000 2018-07-27 19:16 /user/goldengate/tgen/part-m-00003
-rw-r--r--   3 goldengate goldengate  819200000 2018-07-27 19:16 /user/goldengate/tgen/part-m-00004
-rw-r--r--   3 goldengate goldengate  819200000 2018-07-27 19:20 /user/goldengate/tgen/part-m-00005
-rw-r--r--   3 goldengate goldengate  819200000 2018-07-27 19:20 /user/goldengate/tgen/part-m-00006
-rw-r--r--   3 goldengate goldengate  819200000 2018-07-27 19:20 /user/goldengate/tgen/part-m-00007
```

> sudo -u goldengate hadoop fsck -blocks /user/goldengate
```
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-9-19.us-east-2.compute.internal:50070
FSCK started by goldengate (auth:SIMPLE) from /172.31.12.34 for path /user/goldengate at Fri Jul 27 19:24:16 UTC 2018
.........Status: HEALTHY
 Total size:	6553600000 B
 Total dirs:	3
 Total files:	9
 Total symlinks:		0
 Total blocks (validated):	104 (avg. block size 63015384 B)
 Minimally replicated blocks:	104 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		3
 Number of racks:		1
FSCK ended at Fri Jul 27 19:24:16 UTC 2018 in 6 milliseconds


The filesystem under path '/user/goldengate' is HEALTHY
```
