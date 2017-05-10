## What is ubertask optimization?
"ubertask" optimization, which runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.

## Where in CM is the Kerberos Security Realm value displayed?
Click the Administration -> Security to display the Security page. Click the Kerberos Credentials links and the currently configured Kerberos principals are display.

## Which CDH service(s) host a property for enabling Kerberos authentication?
Every CDH service(s) host a own Kerberos principals

## How do you upgrade the CM agents?
I will upgrading CM5 using packages,if cluster is running,I will stop it first and update CM server, after CM server update successed,on the web UI ,I can update agent by Select Yes, I would like to upgrade the Cloudera Manager Agent packages now and click Continue.Select the release of the Cloudera Manager Agent to install. Normally, this is the Matched Release for this Cloudera Manager Server

## Give the tsquery statement used to chart Hue's CPU utilization?
```
select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=Hue
```

## Name all the roles that make up the Hive service
```
A.Hive Metastore Server
B.HiveServer2
C.Hive Gateway
D.WebHCat Server
```

## What steps must be completed before integrating Cloudera Manager with Kerberos?
```
Step 1: already have a working Kerberos key distribution center (KDC) and realm setup
Step 2: you've installed the following Kerberos client packages on all cluster hosts and hosts that will be used to access the cluster
Step 3: Get or Create a Kerberos Principal for the Cloudera Manager Server
Step 4: Enabling Kerberos Using the Wizard
```