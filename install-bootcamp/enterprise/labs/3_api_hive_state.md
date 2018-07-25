# CM Lab
## Use the API

###  statements that stop, start, and check the current state of your Hive service

Stop Hive service
>  curl -u admin -X POST http://18.217.160.49:7180/api/v12/clusters/cluster/services/hive/commands/stop

```
{
  "id" : 735,
  "name" : "Stop",
  "startTime" : "2018-07-25T19:25:00.855Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```

Start Hive Service
> curl -u admin -X POST http://18.217.160.49:7180/api/v12/clusters/cluster/services/hive/commands/start

```
{
  "id" : 739,
  "name" : "Start",
  "startTime" : "2018-07-25T19:30:29.543Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```

Check the current state of Hive Service
> curl -u admin http://18.217.160.49:7180/api/v12/clusters/cluster/services/hive

```
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-45-181.us-east-2.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-45-181.us-east-2.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
}
```