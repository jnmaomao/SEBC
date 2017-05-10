# Report the latest available version of the API
```
[root@cmnode yum.repos.d]# curl -u jnmaomao:cloudera "http://ec2-54-200-82-91.us-west-2.compute.amazonaws.com:7180/api/version"
v16
```

# Report the CM version
```
[root@cmnode yum.repos.d]# curl -u jnmaomao:cloudera "http://ec2-54-200-82-91.us-west-2.compute.amazonaws.com:7180/api/v16/cm/version"
{
  "version" : "5.11.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170412-1249",
  "gitHash" : "70cb1442626406432a6e7af5bdf206a384ca3f98",
  "snapshot" : false
}
```

# List all CM users
```
[root@cmnode yum.repos.d]# curl -u jnmaomao:cloudera "http://ec2-54-200-82-91.us-west-2.compute.amazonaws.com:7180/api/v16/users"
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "jnmaomao",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}

```
# Report the database server in use by CM
```
[root@cmnode yum.repos.d]# curl -u jnmaomao:cloudera "http://ec2-54-200-82-91.us-west-2.compute.amazonaws.com:7180/api/v16/cm/scmDbInfo"
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```
