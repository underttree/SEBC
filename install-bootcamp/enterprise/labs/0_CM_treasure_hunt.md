# CM Monitoring Lab

## What is ubertask optimization?
Ubertask optimization means that “sufficiently small" jobs run sequentially at a single JVM. The definition of “Small” depends on values of mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces and mapreduce.job.ubertask.maxbytes. 
When the parameter mapreduce.job.ubertask.enable is enable, Ubertask optimization is available. You can find the property by an order bellow when you use Cloudera Manager. 

1. Click YARN (MR2 Included)
2. Chose Configuration tab
3. Chose Performance from Category at the left pane
4. See the property Enable Ubertask Optimization

## Where in CM is the Kerberos Security Realm value displayed?
It is displayed at Configuration page. You can find a property and a value by an order bellow:

1. Click Configuration from Management pull down at the top of CM home.
2. Chose Kerberos from Category at the left pane
3. See the Property Kerberos Security Realm value as a property “default_realm”

## Which CDH service(s) host a property for enabling Kerberos authentication?
Zookeeper has a property whose name is “enableSecurity”.

## How do you upgrade the CM agents?
Upgrading the CM agents is a part of upgrading CM, so generally you have to upgrade CM (including Manager, Agent, JDK etc…) if you want to upgrade the CM agent. 
You can see an order at [Upgrading Cloudera Manager 5 Using Packages](https://www.cloudera.com/documentation/enterprise/5-9-x/topics/cm_ag_ug_cm5.html#cmig_topic_9_4 "Upgrading Cloudera Manager 5 Using Packages")

## Give the tsquery statement used to chart Hue's CPU utilization?
```
SELECT cpu_percent WHERE roleType=HUE_SERVER;
```

## Name all the roles that make up the Hive service
- Hive Metastore Server
- Hive Server2
- Hive Gateway

## What steps must be completed before integrating Cloudera Manager with Kerberos?
I pick up some points. You can check details at [Enabling Kerberos Authentication Using the Wizard](https://www.cloudera.com/documentation/enterprise/5-9-x/topics/cm_sg_intro_kerb.html “Enabling Kerberos Authentication Using the Wizard”)

- Ensure you have secured communication between Cloudera Manager Server and Agents.
- You already have a working Kerberos key distribution center (KDC) and realm setup
- You've installed the following Kerberos client packages on all cluster hosts and hosts that will be used to access the cluster,
