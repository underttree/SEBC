# Challenge 2: Install Cloudera Manager 5.12.x (latest micro release)

### List repo files
> ls /etc/yum.repos.d
```
cloudera-manager.repo  redhat-rhui-client-config.repo  rhui-load-balancers.conf
mariadb55.repo         redhat-rhui.repo
```

### List the full command and its output using the scm_prepare_database.sh script
> /usr/share/cmf/schema/scm_prepare_database.sh --host 172.31.9.19 mysql scm scm scm
```
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!
``` 


