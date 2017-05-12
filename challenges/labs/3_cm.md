## The command and output for hdfs dfs -ls /user
```
[hdfs@masternode ~]$ hdfs dfs -ls /user
Found 7 items
drwxr-xr-x   - chen   shanghai          0 2017-05-12 02:24 /user/chen
drwxrwxrwx   - mapred hadoop            0 2017-05-12 02:17 /user/history
drwxrwxr-t   - hive   hive              0 2017-05-12 02:17 /user/hive
drwxrwxr-x   - hue    hue               0 2017-05-12 02:18 /user/hue
drwxrwxr-x   - impala impala            0 2017-05-12 02:20 /user/impala
drwxrwxr-x   - oozie  oozie             0 2017-05-12 02:18 /user/oozie
drwxr-xr-x   - zhou   beijing           0 2017-05-12 02:24 /user/zhou
```

## The command and output from the CM API call ../api/v14/hosts
```
[hdfs@masternode ~]$ curl -u admin:admin 'http://cmnode.com:7180/api/v14/hosts'
{
  "items" : [ {
    "hostId" : "91ff4c7a-135c-485c-b3f1-8482bc600bcc",
    "ipAddress" : "172.31.47.238",
    "hostname" : "cmnode.com",
    "rackId" : "/default",
    "hostUrl" : "http://cmnode.com:7180/cmf/hostRedirect/91ff4c7a-135c-485c-b3f1-8482bc600bcc",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "66810647-2d41-4efa-b75f-a6af1ed6b1d2",
    "ipAddress" : "172.31.44.186",
    "hostname" : "datanode1.com",
    "rackId" : "/default",
    "hostUrl" : "http://cmnode.com:7180/cmf/hostRedirect/66810647-2d41-4efa-b75f-a6af1ed6b1d2",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "a4810e19-8d3e-47fb-b1d7-7397691fd258",
    "ipAddress" : "172.31.32.176",
    "hostname" : "datanode2.com",
    "rackId" : "/default",
    "hostUrl" : "http://cmnode.com:7180/cmf/hostRedirect/a4810e19-8d3e-47fb-b1d7-7397691fd258",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "d90f14d8-99a4-48d9-9866-107c7710fca3",
    "ipAddress" : "172.31.38.243",
    "hostname" : "datanode3.com",
    "rackId" : "/default",
    "hostUrl" : "http://cmnode.com:7180/cmf/hostRedirect/d90f14d8-99a4-48d9-9866-107c7710fca3",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "31031ac7-de18-49e5-9fce-40470d6b63de",
    "ipAddress" : "172.31.41.25",
    "hostname" : "masternode.com",
    "rackId" : "/default",
    "hostUrl" : "http://cmnode.com:7180/cmf/hostRedirect/31031ac7-de18-49e5-9fce-40470d6b63de",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  } ]
}
```

## The command and output from the CM API call ../api/v6/clusters/<githubName>/services
```
[hdfs@masternode ~]$ curl -u admin:admin 'http://cmnode.com:7180/api/v14/hosts'
{
  "items" : [ {
    "hostId" : "91ff4c7a-135c-485c-b3f1-8482bc600bcc",
    "ipAddress" : "172.31.47.238",
    "hostname" : "cmnode.com",
    "rackId" : "/default",
    "hostUrl" : "http://cmnode.com:7180/cmf/hostRedirect/91ff4c7a-135c-485c-b3f1-8482bc600bcc",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "66810647-2d41-4efa-b75f-a6af1ed6b1d2",
    "ipAddress" : "172.31.44.186",
    "hostname" : "datanode1.com",
    "rackId" : "/default",
    "hostUrl" : "http://cmnode.com:7180/cmf/hostRedirect/66810647-2d41-4efa-b75f-a6af1ed6b1d2",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "a4810e19-8d3e-47fb-b1d7-7397691fd258",
    "ipAddress" : "172.31.32.176",
    "hostname" : "datanode2.com",
    "rackId" : "/default",
    "hostUrl" : "http://cmnode.com:7180/cmf/hostRedirect/a4810e19-8d3e-47fb-b1d7-7397691fd258",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "d90f14d8-99a4-48d9-9866-107c7710fca3",
    "ipAddress" : "172.31.38.243",
    "hostname" : "datanode3.com",
    "rackId" : "/default",
    "hostUrl" : "http://cmnode.com:7180/cmf/hostRedirect/d90f14d8-99a4-48d9-9866-107c7710fca3",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "31031ac7-de18-49e5-9fce-40470d6b63de",
    "ipAddress" : "172.31.41.25",
    "hostname" : "masternode.com",
    "rackId" : "/default",
    "hostUrl" : "http://cmnode.com:7180/cmf/hostRedirect/31031ac7-de18-49e5-9fce-40470d6b63de",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  } ]
}[hdfs@masternode ~]$ curl -u admin:admin 'http://cmnode.com:7180/api/v6/clusters/jnmaomao/services'
{
  "items" : [ {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://cmnode.com:7180/cmf/serviceRedirect/hive",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hive"
  }, {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://cmnode.com:7180/cmf/serviceRedirect/zookeeper",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://cmnode.com:7180/cmf/serviceRedirect/hue",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue"
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://cmnode.com:7180/cmf/serviceRedirect/oozie",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://cmnode.com:7180/cmf/serviceRedirect/yarn",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://cmnode.com:7180/cmf/serviceRedirect/hdfs",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS"
  }, {
    "name" : "impala",
    "type" : "IMPALA",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://cmnode.com:7180/cmf/serviceRedirect/impala",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "IMPALA_ASSIGNMENT_LOCALITY",
      "summary" : "DISABLED"
    }, {
      "name" : "IMPALA_CATALOGSERVER_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "IMPALA_IMPALADS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "IMPALA_STATESTORE_HEALTH",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Impala"
  } ]
}
```