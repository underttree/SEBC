# Challenge Setup

### List the cloud provider you are using
```
Amazon Web Service (AWS)
```

### List your instances by IP address and DNS name
Public IP & DNS Name
```
18.188.18.116 ec2-18-188-18-116.us-east-2.compute.amazonaws.com
13.58.42.237 ec2-13-58-42-237.us-east-2.compute.amazonaws.com
18.221.87.135 ec2-18-221-87-135.us-east-2.compute.amazonaws.com
18.191.189.111 ec2-18-191-189-111.us-east-2.compute.amazonaws.com
52.14.28.78 ec2-52-14-28-78.us-east-2.compute.amazonaws.com
```

Private IP & DNS Name
```
172.31.9.19 ip-172-31-9-19.us-east-2.compute.internal
172.31.4.67 ip-172-31-4-67.us-east-2.compute.internal
172.31.15.174 ip-172-31-15-174.us-east-2.compute.internal
172.31.2.59 ip-172-31-2-59.us-east-2.compute.internal
172.31.12.34 ip-172-31-12-34.us-east-2.compute.internal
```

### List the Linux release you are using
> cat /etc/redhat-release
```
Red Hat Enterprise Linux Server release 7.5 (Maipo)
```

### List the file system capacity for the first node
> df -h
```
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda2       30G  1.3G   29G   5% /
devtmpfs        7.8G     0  7.8G   0% /dev
tmpfs           7.8G     0  7.8G   0% /dev/shm
tmpfs           7.8G   17M  7.8G   1% /run
tmpfs           7.8G     0  7.8G   0% /sys/fs/cgroup
tmpfs           1.6G     0  1.6G   0% /run/user/1000
```

### List the command and output for yum repolist enabled
> yum repolist enabled
```
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
repo id                                           repo name                                             status
!rhui-REGION-client-config-server-7/x86_64        Red Hat Update Infrastructure 2.0 Client Configuratio      2
!rhui-REGION-rhel-server-releases/7Server/x86_64  Red Hat Enterprise Linux Server 7 (RPMs)              20,693
!rhui-REGION-rhel-server-rh-common/7Server/x86_64 Red Hat Enterprise Linux Server 7 RH Common (RPMs)       233
repolist: 20,928
```

### List the /etc/passwd entries for goldengate and caldecott
```
goldengate:x:2150:1006::/home/goldengate:/bin/bash
caldecott:x:2250:1005::/home/caldecott:/bin/bash
```

### List the /etc/group entries for tunnel and bridge
```
tunnel:x:1005:
bridge:x:1006:
```

