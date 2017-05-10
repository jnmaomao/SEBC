```
curl -u 'jnmaomao:cloudera' http://ec2-54-200-82-91.us-west-2.compute.amazonaws.com:7180/api/v2/cm/deployment > 2_cluster_deployment.md

{
  "timestamp" : "2017-05-10T03:35:00.154Z",
  "clusters" : [ {
    "name" : "jnmaomao",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "2064646144"
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "206464614"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "2064646144"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2380634521"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "400"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "cmnode.com"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive_password"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-118f35856117f372d246eb909f881735",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0e43aa22f6eb20599"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-8358625ea753eefa7ca128aa77b6d490",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-06ace1500c334a93e"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-fe5c16ec90a14d05a55de7b12dd54760",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0d02a118a68dfb153"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-ffafaae29ae2c55a828bbd0347d6cc1e",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0e15eb41319a63b4c"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-8358625ea753eefa7ca128aa77b6d490",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-06ace1500c334a93e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "f4lwzahq8a3mbwuy7oj6sn3ah"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-8358625ea753eefa7ca128aa77b6d490",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-06ace1500c334a93e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3oh9u8q8ymbzjoaq4uoap5sin"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-118f35856117f372d246eb909f881735",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0e43aa22f6eb20599"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1w7tk6yspstvya36m97yjbyp9"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-fe5c16ec90a14d05a55de7b12dd54760",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0d02a118a68dfb153"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8v06iy7n3hpnrlxd7b4sdqmsu"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-ffafaae29ae2c55a828bbd0347d6cc1e",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0e15eb41319a63b4c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a4ie9lt0ihoalcjuygfsoitbv"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "cmnode.com"
        }, {
          "name" : "database_password",
          "value" : "password"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-8358625ea753eefa7ca128aa77b6d490"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-6b90ae13e57784d4c92b2bf02107ad9a",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-0421205e7da39bde5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4ynpnrun6nrmrbwa0p85qewze"
          }, {
            "name" : "secret_key",
            "value" : "uYfMQP2H0ZpqgHUHdtTOki3ctXtnqh"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "cmnode.com"
          }, {
            "name" : "oozie_database_password",
            "value" : "password"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-6b90ae13e57784d4c92b2bf02107ad9a",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-0421205e7da39bde5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1g2mvomja9nkrehup79tpabxi"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1600"
          }, {
            "name" : "rm_io_weight",
            "value" : "800"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "3253"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "3253"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "80"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "KrYgfPA3D2JWZbmKOkFgWLnI0iaEDY"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-8358625ea753eefa7ca128aa77b6d490",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-06ace1500c334a93e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2i2eml8nmnu6cdsgh90nk9gyc"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-118f35856117f372d246eb909f881735",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0e43aa22f6eb20599"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cbu65odcl0djkvd057j1tu2ja"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-fe5c16ec90a14d05a55de7b12dd54760",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0d02a118a68dfb153"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "jal5dfwx85hft6eqhcdsmal9"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-ffafaae29ae2c55a828bbd0347d6cc1e",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0e15eb41319a63b4c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5r5oq3ocgn1fwplg9s0qf48be"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-8358625ea753eefa7ca128aa77b6d490",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-06ace1500c334a93e"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "49"
          }, {
            "name" : "role_jceks_password",
            "value" : "7b2y5zgq8rbf71yiylwu1f71h"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3170683699"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "400"
          }, {
            "name" : "rm_io_weight",
            "value" : "200"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "2064646144"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "2064646144"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "T0sLQV695hoGBZnUk9OEqOkVtS97uZ"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "AkowISuSwioyUybCEODwYkLbGGtzfU"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "MXbbsvexBg0UHcqSK3h0Lb6DLYtYLD"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "20"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-8358625ea753eefa7ca128aa77b6d490",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-06ace1500c334a93e"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-118f35856117f372d246eb909f881735",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0e43aa22f6eb20599"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9icmw5rc9t0uimp026k3l937q"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-fe5c16ec90a14d05a55de7b12dd54760",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0d02a118a68dfb153"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "53bk744w4wbcsm7zyq1chl7y"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-ffafaae29ae2c55a828bbd0347d6cc1e",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0e15eb41319a63b4c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8ondmc6jgax73yivb40wpuqlm"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-8358625ea753eefa7ca128aa77b6d490",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-06ace1500c334a93e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2lsmir7jai8ejd00vxode1n0c"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-fe5c16ec90a14d05a55de7b12dd54760",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0d02a118a68dfb153"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9ss5u3rrj75e1jfyrwwrtnsau"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-8358625ea753eefa7ca128aa77b6d490",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-06ace1500c334a93e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d6197pc4ec4kcskzzogepodm0"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-118f35856117f372d246eb909f881735",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0e43aa22f6eb20599"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cdib7atshieq6cdxt5dre7qmv"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-fe5c16ec90a14d05a55de7b12dd54760",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0d02a118a68dfb153"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d5npaug6yptozouyppeede86"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-ffafaae29ae2c55a828bbd0347d6cc1e",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0e15eb41319a63b4c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ekqrmje3m2ld8qdwhco3hyg3a"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-8358625ea753eefa7ca128aa77b6d490",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-06ace1500c334a93e"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "jnmaomaoCluster1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "jnmaomaoCluster1"
          }, {
            "name" : "namenode_id",
            "value" : "52"
          }, {
            "name" : "role_jceks_password",
            "value" : "e06o0hv1fo48v415a2bmg4265"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-fe5c16ec90a14d05a55de7b12dd54760",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0d02a118a68dfb153"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "jnmaomaoCluster1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "jnmaomaoCluster1"
          }, {
            "name" : "namenode_id",
            "value" : "57"
          }, {
            "name" : "role_jceks_password",
            "value" : "5td6aiiajcoff1b0i41wq3jvk"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-0421205e7da39bde5",
    "ipAddress" : "172.31.36.96",
    "hostname" : "cmnode.com",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0d02a118a68dfb153",
    "ipAddress" : "172.31.37.33",
    "hostname" : "datanode1.com",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0e15eb41319a63b4c",
    "ipAddress" : "172.31.46.141",
    "hostname" : "datanode2.com",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0e43aa22f6eb20599",
    "ipAddress" : "172.31.33.237",
    "hostname" : "datanode3.com",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-06ace1500c334a93e",
    "ipAddress" : "172.31.36.73",
    "hostname" : "masternode.com",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-6b90ae13e57784d4c92b2bf02107ad9a",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "b6308d7a8767e0ae076a1310020847c1268d49eb03bb0460282689f4cc1d1eb5",
    "pwSalt" : -3353164401888149133,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-6b90ae13e57784d4c92b2bf02107ad9a",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "4cc92bd5ffd1d61f3c7bd6e2a4621981cd55e4dbcfc041bc433a474ffa54e7b4",
    "pwSalt" : -4608032355268256476,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-6b90ae13e57784d4c92b2bf02107ad9a",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "2b6e75bbce8a136bb91ef43415d3f974611eac37d323bdd83e66c19276f832bc",
    "pwSalt" : -8654158909768057372,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-6b90ae13e57784d4c92b2bf02107ad9a",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "97884e347fe230eb7be185bd1617a0157b8e60da9d80ebb3e40462b56087f00d",
    "pwSalt" : -701805990679600833,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "e9a488793f97dfa09c077e01a0f43e7c88387f775d466b44ba5af609369ba25a",
    "pwSalt" : 4186454734442384590,
    "pwLogin" : true
  }, {
    "name" : "jnmaomao",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "ac4c62c534189b9255aa135e5bd146b597d9fe48e33b3223b294bc37b0846f1e",
    "pwSalt" : 3572585545978028199,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "669f7362526a6ce865140b02ca0bab42e11883d02e34e18758d79f49b1e97949",
    "pwSalt" : -6282956656902551504,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.9.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170330-1814",
    "gitHash" : "822da28bff818f57fc1bfc3eafe3a550300ef1b0",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "cmnode.com"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman_password"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-6b90ae13e57784d4c92b2bf02107ad9a",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-0421205e7da39bde5"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "dwkkqxvq9qi44lsv5burvdteo"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-6b90ae13e57784d4c92b2bf02107ad9a",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-0421205e7da39bde5"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "8gzkysnzwdulbn205u5t8vdrr"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-6b90ae13e57784d4c92b2bf02107ad9a",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-0421205e7da39bde5"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "eh247uufzm07tpirtuh85lwvo"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-6b90ae13e57784d4c92b2bf02107ad9a",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-0421205e7da39bde5"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "cp5fg4o9vn0168o0s1k1jbdwx"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-6b90ae13e57784d4c92b2bf02107ad9a",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-0421205e7da39bde5"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4z4a5gj0fa6kabf8leatjn4b"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/22/2012 5:30"
    }, {
      "name" : "PARCEL_UPDATE_FREQ",
      "value" : "1"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/,http://ec2-54-245-167-85.us-west-2.compute.amazonaws.com/cdh5/parcels/5.8.3/,http://ec2-54-245-167-85.us-west-2.compute.amazonaws.com/beta/spark2/parcels/"
    } ]
  }
}
```