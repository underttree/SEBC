#  Challenge 3 - Install CDH 5.9.x (latest micro release)

### display tables in the default database
> Use default;
> Show tables;
```
INFO  : Compiling command(queryId=hive_20180727181111_cc1f26f4-ec6f-4688-83ec-0131c97c0f72): Show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20180727181111_cc1f26f4-ec6f-4688-83ec-0131c97c0f72); Time taken: 0.142 seconds
INFO  : Executing command(queryId=hive_20180727181111_cc1f26f4-ec6f-4688-83ec-0131c97c0f72): Show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180727181111_cc1f26f4-ec6f-4688-83ec-0131c97c0f72); Time taken: 0.02 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.285 seconds)
```
