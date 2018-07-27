# Challenge 1: Install a MySQL server

### The db server command and output that report the server host
> Show VARIABLES Like 'hostname';
```
+---------------+-------------------------------------------+
| Variable_name | Value                                     |
+---------------+-------------------------------------------+
| hostname      | ip-172-31-9-19.us-east-2.compute.internal |
+---------------+-------------------------------------------+
1 row in set (0.00 sec)
```

### The db server command and output that report the server version
> Select Version();
```
+----------------------+
| Version()            |
+----------------------+
| 5.5.60-MariaDB-wsrep |
+----------------------+
1 row in set (0.01 sec)
```

### The db server command and output that list the databases
> Show Databases;
```
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
+--------------------+
8 rows in set (0.01 sec)
```
