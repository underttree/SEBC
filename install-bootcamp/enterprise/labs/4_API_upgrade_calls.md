#  CM Lab
##  Upgrade Cloudera Manager

Report the latest available version of the API

> curl -u admin http://18.217.160.49:7180/api/version
```
v14
```

Report the CM version

> curl -u admin http://18.217.160.49:7180/api/v14/cm/version
```
{
  "version" : "5.9.3",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170627-1506",
  "gitHash" : "23506bb4e114dd460bdac64c57a672e6be631907",
  "snapshot" : false
}
```

List all CM users

> curl -u admin http://18.217.160.49:7180/api/v14/users

```
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  }, {
    "name" : "underttree",
    "roles" : [ "ROLE_LIMITED" ]
  } ]
}
```

Report the database server in use by CM

> curl -u admin http://18.217.160.49:7180/api/v14/cm/scmDbInfo

```
{
  "scmDbType" : "POSTGRESQL",
  "embeddedDbUsed" : false
}
```
