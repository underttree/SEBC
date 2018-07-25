# CM Lab
## Use the API

### Browse or use curl on the endpoint ./api/v2/cm/deployment

```
{
  "timestamp": "2018-07-25T19:05:17.252Z",
  "clusters": [
    {
      "name": "sebc_cluster",
      "version": "CDH5",
      "services": [
        {
          "name": "zookeeper",
          "type": "ZOOKEEPER",
          "config": {
            "roleTypeConfigs": [],
            "items": []
          },
          "roles": [
            {
              "name": "zookeeper-SERVER-713a23725568919644e555f9efc6a278",
              "type": "SERVER",
              "hostRef": {
                "hostId": "d546180d-99b7-4267-b04f-1a187866eb26"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "8usfdzt8aet51h49fcrpa8asz"
                  },
                  {
                    "name": "serverId",
                    "value": "1"
                  }
                ]
              }
            },
            {
              "name": "zookeeper-SERVER-71b0e6000c7c19a3180e5875002874c1",
              "type": "SERVER",
              "hostRef": {
                "hostId": "c81b9b6a-df11-4899-80c9-068a6009ba1a"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "2hcacdcif2iuuogzv53mrerq8"
                  },
                  {
                    "name": "serverId",
                    "value": "2"
                  }
                ]
              }
            },
            {
              "name": "zookeeper-SERVER-79c47fb76d62ff54b62f8c6f4ab9e851",
              "type": "SERVER",
              "hostRef": {
                "hostId": "38420cc3-0a1f-438b-a77c-c26e2ebfd85a"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "3rq8sjzy38ql9gs7y904rzisc"
                  },
                  {
                    "name": "serverId",
                    "value": "3"
                  }
                ]
              }
            }
          ],
          "displayName": "ZooKeeper"
        },
        {
          "name": "hdfs",
          "type": "HDFS",
          "config": {
            "roleTypeConfigs": [
              {
                "roleType": "DATANODE",
                "items": [
                  {
                    "name": "datanode_java_heapsize",
                    "value": "1073741824"
                  },
                  {
                    "name": "dfs_data_dir_list",
                    "value": "/dfs/dn"
                  },
                  {
                    "name": "dfs_datanode_du_reserved",
                    "value": "4293706956"
                  },
                  {
                    "name": "dfs_datanode_max_locked_memory",
                    "value": "4294967296"
                  },
                  {
                    "name": "rm_cpu_shares",
                    "value": "400"
                  },
                  {
                    "name": "rm_io_weight",
                    "value": "200"
                  }
                ]
              },
              {
                "roleType": "GATEWAY",
                "items": [
                  {
                    "name": "dfs_client_use_trash",
                    "value": "true"
                  }
                ]
              },
              {
                "roleType": "JOURNALNODE",
                "items": [
                  {
                    "name": "dfs_journalnode_edits_dir",
                    "value": "/dfs/jn"
                  }
                ]
              },
              {
                "roleType": "NAMENODE",
                "items": [
                  {
                    "name": "dfs_name_dir_list",
                    "value": "/dfs/nn"
                  },
                  {
                    "name": "dfs_namenode_servicerpc_address",
                    "value": "8022"
                  },
                  {
                    "name": "fs_trash_interval",
                    "value": "240"
                  },
                  {
                    "name": "namenode_java_heapsize",
                    "value": "2700083200"
                  }
                ]
              },
              {
                "roleType": "SECONDARYNAMENODE",
                "items": [
                  {
                    "name": "fs_checkpoint_dir_list",
                    "value": "/dfs/snn"
                  },
                  {
                    "name": "secondary_namenode_java_heapsize",
                    "value": "2700083200"
                  }
                ]
              }
            ],
            "items": [
              {
                "name": "dfs_ha_fencing_cloudera_manager_secret_key",
                "value": "jwsuhcjsDhdzg2yS0IZbosCgti3YQq"
              },
              {
                "name": "dfs_ha_fencing_methods",
                "value": "shell(true)"
              },
              {
                "name": "fc_authorization_secret_key",
                "value": "AAeCIXeFDiCiEMNiYDegEpcfYy7hC3"
              },
              {
                "name": "http_auth_signature_secret",
                "value": "XnbY5ELlowbOBSfdvzq7Wgd6jp3qih"
              },
              {
                "name": "rm_dirty",
                "value": "false"
              },
              {
                "name": "rm_last_allocation_percentage",
                "value": "20"
              },
              {
                "name": "zookeeper_service",
                "value": "zookeeper"
              }
            ]
          },
          "roles": [
            {
              "name": "hdfs-BALANCER-d8ca5f0e0198b962d49a318f24b41838",
              "type": "BALANCER",
              "hostRef": {
                "hostId": "1cf29fe7-9b14-43c5-8f05-cdb003c8f8a6"
              },
              "config": {
                "items": []
              }
            },
            {
              "name": "hdfs-DATANODE-71b0e6000c7c19a3180e5875002874c1",
              "type": "DATANODE",
              "hostRef": {
                "hostId": "c81b9b6a-df11-4899-80c9-068a6009ba1a"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "7mdpqy5b88b9pxn0mja7gf2b"
                  }
                ]
              }
            },
            {
              "name": "hdfs-DATANODE-79c47fb76d62ff54b62f8c6f4ab9e851",
              "type": "DATANODE",
              "hostRef": {
                "hostId": "38420cc3-0a1f-438b-a77c-c26e2ebfd85a"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "4748zslphlvccpv8gqf82apbm"
                  }
                ]
              }
            },
            {
              "name": "hdfs-DATANODE-d8ca5f0e0198b962d49a318f24b41838",
              "type": "DATANODE",
              "hostRef": {
                "hostId": "1cf29fe7-9b14-43c5-8f05-cdb003c8f8a6"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "nv12m3sekrp87octh9j07hv7"
                  }
                ]
              }
            },
            {
              "name": "hdfs-FAILOVERCONTROLLER-713a23725568919644e555f9efc6a278",
              "type": "FAILOVERCONTROLLER",
              "hostRef": {
                "hostId": "d546180d-99b7-4267-b04f-1a187866eb26"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "1wv0yjjttc9iu0z2ovm22tb8f"
                  }
                ]
              }
            },
            {
              "name": "hdfs-FAILOVERCONTROLLER-71b0e6000c7c19a3180e5875002874c1",
              "type": "FAILOVERCONTROLLER",
              "hostRef": {
                "hostId": "c81b9b6a-df11-4899-80c9-068a6009ba1a"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "99ky8ek5dg8piyvi19d7q0wzm"
                  }
                ]
              }
            },
            {
              "name": "hdfs-JOURNALNODE-713a23725568919644e555f9efc6a278",
              "type": "JOURNALNODE",
              "hostRef": {
                "hostId": "d546180d-99b7-4267-b04f-1a187866eb26"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "byg37yqllwargu8a5ysvlcsvp"
                  }
                ]
              }
            },
            {
              "name": "hdfs-JOURNALNODE-71b0e6000c7c19a3180e5875002874c1",
              "type": "JOURNALNODE",
              "hostRef": {
                "hostId": "c81b9b6a-df11-4899-80c9-068a6009ba1a"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "950pxu540mwb1hhigkw5yx7mz"
                  }
                ]
              }
            },
            {
              "name": "hdfs-JOURNALNODE-d8ca5f0e0198b962d49a318f24b41838",
              "type": "JOURNALNODE",
              "hostRef": {
                "hostId": "1cf29fe7-9b14-43c5-8f05-cdb003c8f8a6"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "9qemaa7t19o1u6md7fj5l9ag9"
                  }
                ]
              }
            },
            {
              "name": "hdfs-NAMENODE-713a23725568919644e555f9efc6a278",
              "type": "NAMENODE",
              "hostRef": {
                "hostId": "d546180d-99b7-4267-b04f-1a187866eb26"
              },
              "config": {
                "items": [
                  {
                    "name": "autofailover_enabled",
                    "value": "true"
                  },
                  {
                    "name": "dfs_federation_namenode_nameservice",
                    "value": "mybootcamp"
                  },
                  {
                    "name": "dfs_namenode_quorum_journal_name",
                    "value": "mybootcamp"
                  },
                  {
                    "name": "namenode_id",
                    "value": "52"
                  },
                  {
                    "name": "role_jceks_password",
                    "value": "2wdkqb3n8ype5vjgh9kfdbe4m"
                  }
                ]
              }
            },
            {
              "name": "hdfs-NAMENODE-71b0e6000c7c19a3180e5875002874c1",
              "type": "NAMENODE",
              "hostRef": {
                "hostId": "c81b9b6a-df11-4899-80c9-068a6009ba1a"
              },
              "config": {
                "items": [
                  {
                    "name": "autofailover_enabled",
                    "value": "true"
                  },
                  {
                    "name": "dfs_federation_namenode_nameservice",
                    "value": "mybootcamp"
                  },
                  {
                    "name": "dfs_namenode_quorum_journal_name",
                    "value": "mybootcamp"
                  },
                  {
                    "name": "namenode_id",
                    "value": "57"
                  },
                  {
                    "name": "role_jceks_password",
                    "value": "asfkkqhzu2g3oznph733p48lp"
                  }
                ]
              }
            }
          ],
          "displayName": "HDFS"
        },
        {
          "name": "hive",
          "type": "HIVE",
          "config": {
            "roleTypeConfigs": [
              {
                "roleType": "HIVEMETASTORE",
                "items": [
                  {
                    "name": "hive_metastore_java_heapsize",
                    "value": "1928331264"
                  },
                  {
                    "name": "hive_metastore_server_max_message_size",
                    "value": "192833126"
                  }
                ]
              },
              {
                "roleType": "HIVESERVER2",
                "items": [
                  {
                    "name": "hiveserver2_java_heapsize",
                    "value": "2700083200"
                  },
                  {
                    "name": "hiveserver2_spark_driver_memory",
                    "value": "966367641"
                  },
                  {
                    "name": "hiveserver2_spark_executor_cores",
                    "value": "4"
                  },
                  {
                    "name": "hiveserver2_spark_executor_memory",
                    "value": "3289749913"
                  },
                  {
                    "name": "hiveserver2_spark_yarn_driver_memory_overhead",
                    "value": "102"
                  },
                  {
                    "name": "hiveserver2_spark_yarn_executor_memory_overhead",
                    "value": "553"
                  }
                ]
              }
            ],
            "items": [
              {
                "name": "hive_metastore_database_host",
                "value": "ip-172-31-45-181.us-east-2.compute.internal"
              },
              {
                "name": "hive_metastore_database_password",
                "value": "hive"
              },
              {
                "name": "hive_metastore_database_port",
                "value": "5432"
              },
              {
                "name": "hive_metastore_database_type",
                "value": "postgresql"
              },
              {
                "name": "mapreduce_yarn_service",
                "value": "yarn"
              },
              {
                "name": "zookeeper_service",
                "value": "zookeeper"
              }
            ]
          },
          "roles": [
            {
              "name": "hive-GATEWAY-713a23725568919644e555f9efc6a278",
              "type": "GATEWAY",
              "hostRef": {
                "hostId": "d546180d-99b7-4267-b04f-1a187866eb26"
              },
              "config": {
                "items": []
              }
            },
            {
              "name": "hive-GATEWAY-71b0e6000c7c19a3180e5875002874c1",
              "type": "GATEWAY",
              "hostRef": {
                "hostId": "c81b9b6a-df11-4899-80c9-068a6009ba1a"
              },
              "config": {
                "items": []
              }
            },
            {
              "name": "hive-GATEWAY-79c47fb76d62ff54b62f8c6f4ab9e851",
              "type": "GATEWAY",
              "hostRef": {
                "hostId": "38420cc3-0a1f-438b-a77c-c26e2ebfd85a"
              },
              "config": {
                "items": []
              }
            },
            {
              "name": "hive-GATEWAY-d497e2ea500b79265e9407d7e3e975bc",
              "type": "GATEWAY",
              "hostRef": {
                "hostId": "7a347707-0a67-42b9-95df-ba4d0e80f223"
              },
              "config": {
                "items": []
              }
            },
            {
              "name": "hive-GATEWAY-d8ca5f0e0198b962d49a318f24b41838",
              "type": "GATEWAY",
              "hostRef": {
                "hostId": "1cf29fe7-9b14-43c5-8f05-cdb003c8f8a6"
              },
              "config": {
                "items": []
              }
            },
            {
              "name": "hive-HIVEMETASTORE-d497e2ea500b79265e9407d7e3e975bc",
              "type": "HIVEMETASTORE",
              "hostRef": {
                "hostId": "7a347707-0a67-42b9-95df-ba4d0e80f223"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "3alixl6cnq7fo6qekrls0j6hr"
                  }
                ]
              }
            },
            {
              "name": "hive-HIVESERVER2-713a23725568919644e555f9efc6a278",
              "type": "HIVESERVER2",
              "hostRef": {
                "hostId": "d546180d-99b7-4267-b04f-1a187866eb26"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "b928031om2ccmcfaz6s2lawss"
                  }
                ]
              }
            }
          ],
          "displayName": "Hive"
        },
        {
          "name": "oozie",
          "type": "OOZIE",
          "config": {
            "roleTypeConfigs": [
              {
                "roleType": "OOZIE_SERVER",
                "items": [
                  {
                    "name": "oozie_database_host",
                    "value": "ip-172-31-45-181.us-east-2.compute.internal"
                  },
                  {
                    "name": "oozie_database_password",
                    "value": "oozie"
                  },
                  {
                    "name": "oozie_database_type",
                    "value": "postgresql"
                  },
                  {
                    "name": "oozie_database_user",
                    "value": "oozie"
                  }
                ]
              }
            ],
            "items": [
              {
                "name": "hive_service",
                "value": "hive"
              },
              {
                "name": "mapreduce_yarn_service",
                "value": "yarn"
              },
              {
                "name": "zookeeper_service",
                "value": "zookeeper"
              }
            ]
          },
          "roles": [
            {
              "name": "oozie-OOZIE_SERVER-d497e2ea500b79265e9407d7e3e975bc",
              "type": "OOZIE_SERVER",
              "hostRef": {
                "hostId": "7a347707-0a67-42b9-95df-ba4d0e80f223"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "92u8oez4uuc6jb8en49oornaw"
                  }
                ]
              }
            }
          ],
          "displayName": "Oozie"
        },
        {
          "name": "hue",
          "type": "HUE",
          "config": {
            "roleTypeConfigs": [],
            "items": [
              {
                "name": "database_host",
                "value": "ip-172-31-45-181.us-east-2.compute.internal"
              },
              {
                "name": "database_password",
                "value": "hue"
              },
              {
                "name": "database_port",
                "value": "5432"
              },
              {
                "name": "database_type",
                "value": "postgresql"
              },
              {
                "name": "hive_service",
                "value": "hive"
              },
              {
                "name": "hue_webhdfs",
                "value": "hdfs-NAMENODE-713a23725568919644e555f9efc6a278"
              },
              {
                "name": "oozie_service",
                "value": "oozie"
              },
              {
                "name": "zookeeper_service",
                "value": "zookeeper"
              }
            ]
          },
          "roles": [
            {
              "name": "hue-HUE_SERVER-d497e2ea500b79265e9407d7e3e975bc",
              "type": "HUE_SERVER",
              "hostRef": {
                "hostId": "7a347707-0a67-42b9-95df-ba4d0e80f223"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "8qkfairm5yp2aduwirg7397gd"
                  },
                  {
                    "name": "secret_key",
                    "value": "0NUcN12Cp4pwftZV86sw6O2cW9aTBd"
                  }
                ]
              }
            }
          ],
          "displayName": "Hue"
        },
        {
          "name": "yarn",
          "type": "YARN",
          "config": {
            "roleTypeConfigs": [
              {
                "roleType": "GATEWAY",
                "items": [
                  {
                    "name": "mapred_reduce_tasks",
                    "value": "6"
                  },
                  {
                    "name": "mapred_submit_replication",
                    "value": "1"
                  }
                ]
              },
              {
                "roleType": "NODEMANAGER",
                "items": [
                  {
                    "name": "rm_cpu_shares",
                    "value": "1600"
                  },
                  {
                    "name": "rm_io_weight",
                    "value": "800"
                  },
                  {
                    "name": "yarn_nodemanager_heartbeat_interval_ms",
                    "value": "100"
                  },
                  {
                    "name": "yarn_nodemanager_local_dirs",
                    "value": "/yarn/nm"
                  },
                  {
                    "name": "yarn_nodemanager_log_dirs",
                    "value": "/yarn/container-logs"
                  },
                  {
                    "name": "yarn_nodemanager_resource_cpu_vcores",
                    "value": "3"
                  },
                  {
                    "name": "yarn_nodemanager_resource_memory_mb",
                    "value": "1024"
                  }
                ]
              },
              {
                "roleType": "RESOURCEMANAGER",
                "items": [
                  {
                    "name": "yarn_scheduler_maximum_allocation_mb",
                    "value": "4618"
                  },
                  {
                    "name": "yarn_scheduler_maximum_allocation_vcores",
                    "value": "3"
                  }
                ]
              }
            ],
            "items": [
              {
                "name": "hdfs_service",
                "value": "hdfs"
              },
              {
                "name": "rm_dirty",
                "value": "false"
              },
              {
                "name": "rm_last_allocation_percentage",
                "value": "80"
              },
              {
                "name": "yarn_service_cgroups",
                "value": "false"
              },
              {
                "name": "yarn_service_lce_always",
                "value": "false"
              },
              {
                "name": "zk_authorization_secret_key",
                "value": "nwWqmcxWkzVq5UFIGlE74WKRdaMRFW"
              },
              {
                "name": "zookeeper_service",
                "value": "zookeeper"
              }
            ]
          },
          "roles": [
            {
              "name": "yarn-JOBHISTORY-d8ca5f0e0198b962d49a318f24b41838",
              "type": "JOBHISTORY",
              "hostRef": {
                "hostId": "1cf29fe7-9b14-43c5-8f05-cdb003c8f8a6"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "5ot61o3knwzuzi15tqvidv8vy"
                  }
                ]
              }
            },
            {
              "name": "yarn-NODEMANAGER-71b0e6000c7c19a3180e5875002874c1",
              "type": "NODEMANAGER",
              "hostRef": {
                "hostId": "c81b9b6a-df11-4899-80c9-068a6009ba1a"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "287bez8dof5eenczgydtbnkt0"
                  }
                ]
              }
            },
            {
              "name": "yarn-NODEMANAGER-79c47fb76d62ff54b62f8c6f4ab9e851",
              "type": "NODEMANAGER",
              "hostRef": {
                "hostId": "38420cc3-0a1f-438b-a77c-c26e2ebfd85a"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "342676mwl3kgn9r3xh8thsz6n"
                  }
                ]
              }
            },
            {
              "name": "yarn-NODEMANAGER-d8ca5f0e0198b962d49a318f24b41838",
              "type": "NODEMANAGER",
              "hostRef": {
                "hostId": "1cf29fe7-9b14-43c5-8f05-cdb003c8f8a6"
              },
              "config": {
                "items": [
                  {
                    "name": "role_jceks_password",
                    "value": "c01egwezrf7tvav9hgqs8dsrc"
                  }
                ]
              }
            },
            {
              "name": "yarn-RESOURCEMANAGER-713a23725568919644e555f9efc6a278",
              "type": "RESOURCEMANAGER",
              "hostRef": {
                "hostId": "d546180d-99b7-4267-b04f-1a187866eb26"
              },
              "config": {
                "items": [
                  {
                    "name": "rm_id",
                    "value": "50"
                  },
                  {
                    "name": "role_jceks_password",
                    "value": "4j7sdigdjej8lgz78wa5knlop"
                  }
                ]
              }
            }
          ],
          "displayName": "YARN (MR2 Included)"
        }
      ]
    }
  ],
  "hosts": [
    {
      "hostId": "d546180d-99b7-4267-b04f-1a187866eb26",
      "ipAddress": "172.31.33.182",
      "hostname": "ip-172-31-33-182.us-east-2.compute.internal",
      "rackId": "/default",
      "config": {
        "items": []
      }
    },
    {
      "hostId": "7a347707-0a67-42b9-95df-ba4d0e80f223",
      "ipAddress": "172.31.34.134",
      "hostname": "ip-172-31-34-134.us-east-2.compute.internal",
      "rackId": "/default",
      "config": {
        "items": []
      }
    },
    {
      "hostId": "c81b9b6a-df11-4899-80c9-068a6009ba1a",
      "ipAddress": "172.31.36.243",
      "hostname": "ip-172-31-36-243.us-east-2.compute.internal",
      "rackId": "/default",
      "config": {
        "items": []
      }
    },
    {
      "hostId": "38420cc3-0a1f-438b-a77c-c26e2ebfd85a",
      "ipAddress": "172.31.41.192",
      "hostname": "ip-172-31-41-192.us-east-2.compute.internal",
      "rackId": "/default",
      "config": {
        "items": []
      }
    },
    {
      "hostId": "1cf29fe7-9b14-43c5-8f05-cdb003c8f8a6",
      "ipAddress": "172.31.45.181",
      "hostname": "ip-172-31-45-181.us-east-2.compute.internal",
      "rackId": "/default",
      "config": {
        "items": []
      }
    }
  ],
  "users": [
    {
      "name": "__cloudera_internal_user__mgmt-EVENTSERVER-d497e2ea500b79265e9407d7e3e975bc",
      "roles": [
        "ROLE_USER"
      ],
      "pwHash": "29fd211e764bc572461a4c8ec5e1237be1fec25eb72683ec33fbf01d0cbc8f44",
      "pwSalt": -6699896547837809000,
      "pwLogin": true
    },
    {
      "name": "__cloudera_internal_user__mgmt-HOSTMONITOR-d497e2ea500b79265e9407d7e3e975bc",
      "roles": [
        "ROLE_USER"
      ],
      "pwHash": "5049cb6f7429ec6d61ef4d41d36349d3aaf1164f8fcd15e1a94af29b7dbba77f",
      "pwSalt": -134653699704742660,
      "pwLogin": true
    },
    {
      "name": "__cloudera_internal_user__mgmt-REPORTSMANAGER-d497e2ea500b79265e9407d7e3e975bc",
      "roles": [
        "ROLE_USER"
      ],
      "pwHash": "341c8e6e5811c397c49b77e2b7b4a823a817641a46c8a76aacca16f3505aa22d",
      "pwSalt": -2096960380373282000,
      "pwLogin": true
    },
    {
      "name": "__cloudera_internal_user__mgmt-SERVICEMONITOR-d497e2ea500b79265e9407d7e3e975bc",
      "roles": [
        "ROLE_USER"
      ],
      "pwHash": "d2e17d4674f3c7d85e1cb4cc494910eaed4df40adc51f99a71474b33964a4417",
      "pwSalt": -3178820367975300000,
      "pwLogin": true
    },
    {
      "name": "admin",
      "roles": [
        "ROLE_ADMIN"
      ],
      "pwHash": "81f98f1c03052fb19968933cd4b369ba0c5c86d038ac75508ef2cd7c2a182726",
      "pwSalt": 7338357857108235000,
      "pwLogin": true
    },
    {
      "name": "minotaur",
      "roles": [
        "ROLE_CONFIGURATOR"
      ],
      "pwHash": "a0a84b8dd0a50ff0951c0beee5b541f52a67f2e98d1d636ef765a29590e4b2c1",
      "pwSalt": -5743310487918849000,
      "pwLogin": true
    },
    {
      "name": "underttree",
      "roles": [
        "ROLE_LIMITED"
      ],
      "pwHash": "3bfc01f377236dc8ff65d5a670995a93673861ffd3872dbff268d9fa1831e44e",
      "pwSalt": -4131997262191543000,
      "pwLogin": true
    }
  ],
  "versionInfo": {
    "version": "5.9.3",
    "buildUser": "jenkins",
    "buildTimestamp": "20170627-1506",
    "gitHash": "23506bb4e114dd460bdac64c57a672e6be631907",
    "snapshot": false
  },
  "managementService": {
    "name": "mgmt",
    "type": "MGMT",
    "config": {
      "roleTypeConfigs": [
        {
          "roleType": "HOSTMONITOR",
          "items": [
            {
              "name": "firehose_non_java_memory_bytes",
              "value": "1610612736"
            }
          ]
        },
        {
          "roleType": "REPORTSMANAGER",
          "items": [
            {
              "name": "headlamp_database_host",
              "value": "ip-172-31-45-181.us-east-2.compute.internal"
            },
            {
              "name": "headlamp_database_name",
              "value": "rman"
            },
            {
              "name": "headlamp_database_password",
              "value": "rman"
            },
            {
              "name": "headlamp_database_type",
              "value": "postgresql"
            },
            {
              "name": "headlamp_database_user",
              "value": "rman"
            }
          ]
        },
        {
          "roleType": "SERVICEMONITOR",
          "items": [
            {
              "name": "firehose_non_java_memory_bytes",
              "value": "1610612736"
            }
          ]
        }
      ],
      "items": []
    },
    "roles": [
      {
        "name": "mgmt-ALERTPUBLISHER-d497e2ea500b79265e9407d7e3e975bc",
        "type": "ALERTPUBLISHER",
        "hostRef": {
          "hostId": "7a347707-0a67-42b9-95df-ba4d0e80f223"
        },
        "config": {
          "items": [
            {
              "name": "role_jceks_password",
              "value": "a21ffrvxmzs5mgevd6g5036n7"
            }
          ]
        }
      },
      {
        "name": "mgmt-EVENTSERVER-d497e2ea500b79265e9407d7e3e975bc",
        "type": "EVENTSERVER",
        "hostRef": {
          "hostId": "7a347707-0a67-42b9-95df-ba4d0e80f223"
        },
        "config": {
          "items": [
            {
              "name": "role_jceks_password",
              "value": "1p309q372jmm145ni2u15ht5s"
            }
          ]
        }
      },
      {
        "name": "mgmt-HOSTMONITOR-d497e2ea500b79265e9407d7e3e975bc",
        "type": "HOSTMONITOR",
        "hostRef": {
          "hostId": "7a347707-0a67-42b9-95df-ba4d0e80f223"
        },
        "config": {
          "items": [
            {
              "name": "role_jceks_password",
              "value": "3v4jons6yqkgzpj14ata5raro"
            }
          ]
        }
      },
      {
        "name": "mgmt-REPORTSMANAGER-d497e2ea500b79265e9407d7e3e975bc",
        "type": "REPORTSMANAGER",
        "hostRef": {
          "hostId": "7a347707-0a67-42b9-95df-ba4d0e80f223"
        },
        "config": {
          "items": [
            {
              "name": "role_jceks_password",
              "value": "djamfxc5jqbap1gp3tbvla2qc"
            }
          ]
        }
      },
      {
        "name": "mgmt-SERVICEMONITOR-d497e2ea500b79265e9407d7e3e975bc",
        "type": "SERVICEMONITOR",
        "hostRef": {
          "hostId": "7a347707-0a67-42b9-95df-ba4d0e80f223"
        },
        "config": {
          "items": [
            {
              "name": "role_jceks_password",
              "value": "3wa6akrk4e57rr0768wai3zlt"
            }
          ]
        }
      }
    ],
    "displayName": "Cloudera Management Service"
  },
  "managerSettings": {
    "items": [
      {
        "name": "CLUSTER_STATS_START",
        "value": "10/26/2012 11:00"
      },
      {
        "name": "CUSTOM_BANNER_HTML",
        "value": "SEBC"
      },
      {
        "name": "CUSTOM_HEADER_COLOR",
        "value": "BROWN"
      },
      {
        "name": "PUBLIC_CLOUD_STATUS",
        "value": "ON_PUBLIC_CLOUD"
      },
      {
        "name": "REMOTE_PARCEL_REPO_URLS",
        "value": "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
      }
    ]
  }
}
```