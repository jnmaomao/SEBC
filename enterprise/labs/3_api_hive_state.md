```
[root@cmnode ~]# curl -u jnmaomao:cloudera -X GET "http://ec2-54-200-82-91.us-west-2.compute.amazonaws.com:7180/api/v12/clusters/jnmaomao/services/hive"
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://cmnode.com:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://cmnode.com:7180/cmf/serviceRedirect/hive/instances",
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


[root@cmnode ~]# curl -u jnmaomao:cloudera -X POST "http://ec2-54-200-82-91.us-west-2.compute.amazonaws.com:7180/api/v12/clusters/jnmaomao/services/hive/commands/stop"
{
  "id" : 671,
  "name" : "Stop",
  "startTime" : "2017-05-10T03:43:17.459Z",
  "endTime" : "2017-05-10T03:43:17.459Z",
  "active" : false,
  "success" : false,
  "resultMessage" : "At least one role must be started.",
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}

[root@cmnode ~]# curl -u jnmaomao:cloudera -X GET "http://ec2-54-200-82-91.us-west-2.compute.amazonaws.com:7180/api/v12/clusters/jnmaomao/services/hive"
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://cmnode.com:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://cmnode.com:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STOPPED",
  "healthSummary" : "DISABLED",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "DISABLED",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "DISABLED",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "STOPPED"
}

[root@cmnode ~]# curl -u jnmaomao:cloudera -X POST "http://ec2-54-200-82-91.us-west-2.compute.amazonaws.com:7180/api/v12/clusters/jnmaomao/services/hive/commands/start"
{
  "id" : 672,
  "name" : "Start",
  "startTime" : "2017-05-10T03:44:08.519Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```