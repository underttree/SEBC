# Create a precious directory in HDFS; copy the ZIP course file into it.

hdfs dfs -mkdir /user/underttree/precious
hdfs dfs -put SEBC-master.zip /user/underttree/precious
hdfs dfs -ls /user/underttree/precious
Found 1 items
-rw-r--r--   3 root supergroup     474919 2018-07-24 19:28 /user/underttree/precious/SEBC-master.zip


# Enable snapshots for precious

sudo -u hdfs hdfs dfsadmin -allowSnapshot /user/underttree/precious
Allowing snaphot on /user/underttree/precious succeeded

hdfs lsSnapshottableDir
drwxr-xr-x 0 root supergroup 0 2018-07-24 19:28 0 65536 /user/underttree/precious


# Create a snapshot called sebc-hdfs-test

hdfs dfs -createSnapshot /user/underttree/precious sebc-hdfs-test
Created snapshot /user/underttree/precious/.snapshot/sebc-hdfs-test

[root@ip-172-31-33-182 ~]# hdfs dfs -ls /user/underttree/precious/.snapshot/sebc-hdfs-test
Found 1 items
-rw-r--r--   3 root supergroup     474919 2018-07-24 19:28 /user/underttree/precious/.snapshot/sebc-hdfs-test/SEBC-master.zip


# Delete the ZIP file
# Delete the directory
sudo -u hdfs hdfs dfs -rm /user/underttree/precious/SEBC-master.zip
18/07/24 19:48:41 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-33-182.us-east-2.compute.internal:8020/user/underttree/precious/SEBC-master.zip' to trash at: hdfs://ip-172-31-33-182.us-east-2.compute.internal:8020/user/hdfs/.Trash/Current/user/underttree/precious/SEBC-master.zip

sudo -u hdfs hdfs dfs -rmdir /user/underttree/precious/
rmdir: The directory /user/underttree/precious cannot be deleted since /user/underttree/precious is snapshottable and already has snapshots

hdfs dfs -ls /user/underttree/
Found 3 items
drwxr-xr-x   - root supergroup          0 2018-07-24 19:48 /user/underttree/precious
drwxr-xr-x   - root supergroup          0 2018-07-24 18:50 /user/underttree/tengigafile
drwxrwxrwx   - root supergroup          0 2018-07-24 19:14 /user/underttree/tengigasort


# Restore the deleted file
hdfs dfs -cp /user/underttree/precious/.snapshot/sebc-hdfs-test/SEBC-master.zip /user/underttree/precious/
 
