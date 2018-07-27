#  Challenge 1: Install a MySQL server

### the YUM repo configuration to install MariaDB 5.5 server

```
[maria55]
name = MariaDB 5.5 repo
baseurl = http://yum.mariadb.org/5.5/rhel7-amd64
gpgkey	= https://yum.mariadb.org/RPM-GPG-KEY-MariaDB
gpgcheck= 1
enabled = 1
```