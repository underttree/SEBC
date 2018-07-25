# 1. Check vm.swappiness on all your nodes
 sudo sysctl -w vm.swappiness=1
> vm.swappiness = 1

 cat /proc/sys/vm/swappiness 
> 0

# 2. Show the mount attributes of your volume(s)
 cat /etc/fstab 

>\#

>\# /etc/fstab

>\# Created by anaconda on Fri Mar 23 17:41:14 2018

>\#

>\# Accessible filesystems, by reference, are maintained under '/dev/disk'

>\# See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info

>\#

>UUID=50a9826b-3a50-44d0-ad12-28f2056e9927 /                       xfs     defaults,noatime        0 0`


3. If you have ext-based volumes, list the reserve space setting
using XFS

4. Disable transparent hugepage support
# cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never
# cat /sys/kernel/mm/transparent_hugepage/defrag
[always] madvise never

# cat /etc/rc.d/rc.local 
#!/bin/bash
# THIS FILE IS ADDED FOR COMPATIBILITY PURPOSES
#
# It is highly advisable to create own systemd services or udev rules
# to run scripts during boot instead of using this file.
#
# In contrast to previous versions due to parallel execution during boot
# this script will NOT be run after all other services.
#
# Please note that you must run 'chmod +x /etc/rc.d/rc.local' to ensure
# that this script will be executed during boot.

touch /var/lock/subsys/local

echo never > /sys/kernel/mm/transparent_hugepage/enabled
echo never > /sys/kernel/mm/transparent_hugepage/defrag 

# chmod +x /etc/rc.d/rc.local
# ls -l /etc/rc.d/rc.local 
-rwxr-xr-x. 1 root root 587 Jul 23 21:29 /etc/rc.d/rc.local


5. List your network interface configuration


6. Show that forward and reverse host lookups are correctly resolved
# cat /etc/hosts
127.0.0.1   localhost localhost.localdomain localhost4 localhost4.localdomain4
::1         localhost localhost.localdomain localhost6 localhost6.localdomain6

172.31.33.182	ip-172-31-33-182.us-east-2.compute.internal     sebc01node
172.31.45.181	ip-172-31-45-181.us-east-2.compute.internal     sebc02node
172.31.36.243	ip-172-31-36-243.us-east-2.compute.internal	sebc03node
172.31.41.192	ip-172-31-41-192.us-east-2.compute.internal	sebc04node
172.31.34.134	ip-172-31-34-134.us-east-2.compute.internal	sebc05node


7. Show the nscd service is running
# systemctl status nscd
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: inactive (dead)

8. Show the ntpd service is running
# systemctl status ntpd
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Mon 2018-07-23 22:29:35 UTC; 5s ago
  Process: 17862 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 17863 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─17863 /usr/sbin/ntpd -u ntp:ntp -g

Jul 23 22:29:35 sebc01node ntpd[17863]: Listen and drop on 0 v4wildcard 0.0.0....23
Jul 23 22:29:35 sebc01node ntpd[17863]: Listen and drop on 1 v6wildcard :: UDP 123
Jul 23 22:29:35 sebc01node ntpd[17863]: Listen normally on 2 lo 127.0.0.1 UDP 123
Jul 23 22:29:35 sebc01node ntpd[17863]: Listen normally on 3 eth0 172.31.33.18...23
Jul 23 22:29:35 sebc01node ntpd[17863]: Listen normally on 4 lo ::1 UDP 123
Jul 23 22:29:35 sebc01node ntpd[17863]: Listen normally on 5 eth0 fe80::861:5c...23
Jul 23 22:29:35 sebc01node ntpd[17863]: Listening on routing socket on fd #22 ...es
Jul 23 22:29:35 sebc01node ntpd[17863]: 0.0.0.0 c016 06 restart
Jul 23 22:29:35 sebc01node ntpd[17863]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
Jul 23 22:29:35 sebc01node ntpd[17863]: 0.0.0.0 c011 01 freq_not_set
Hint: Some lines were ellipsized, use -l to show in full.