1. Download and implement the official MySQL repo
# vi /etc/yum.repos.d/mysql.repo 
[mysq-community]
name=MySQL 5.5 Community Server
baseurl=http://repo.mysql.com/yum/mysql-5.5-community/el/7/$basearch/
enabled=1
gpgcheck=0
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql

# yum install mysql
# yum install mysql-server


2. You should not need to build a /etc/my.cnf file to start your MySQL server
@ master (172.31.36.243	ip-172-31-36-243.us-east-2.compute.internal)
# vi /etc/my.cnf

[mysqld]
…
log-bin=mysql-bin
server-id=1001

# systemctl start mysqld

@slave (172.31.45.181	ip-172-31-45-181.us-east-2.compute.internal)
# vi /etc/my.cnf

[mysqld]
… 
server-id=1002



3. Start the mysqld service.
@ master, slave
# systemctl start mysqld


4. Use /usr/bin/mysql_secure_installation


5. On the master MySQL node, grant replication privileges for your replica node
@ master
# mysql -u root

> GRANT REPLICATION SLAVE ON *.* TO ‘repli’@‘ip-172-31-36-243.us-east-2.compute.internal' IDENTIFIED BY 'password';



6. In a second terminal session, log into the MySQL master and show its status


7. Login to the replica server and configure a connection to the master


8. Initiate slave operations on the replica




