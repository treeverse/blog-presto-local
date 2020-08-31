## Presto Environment

### About

This environment will allow you to run Presto (Using docker-compose).
 
It Includes the following:

   * MariaDB
   * Hive 3.x 
   * Presto

### Prerequisite
 
Update the following configuration files with your AWS credentials:

* `etc/s3.properties`
* `hive/conf/hdfs-site.xml`
* `hive/conf/hive-site.xml`

### Running

```sh
$ docker-compose up -d
```

### using Presto CLI

```sh
$ docker-compose exec presto presto-cli --catalog s3 --schema default
```

### Running Hive Server (optional)

```sh
$ docker-compose exec -d hive hiveserver2 
```

This will start Hive server in the background.

You could use `beeline` to connect to the server after it's up and running

```sh
$ docker-compose exec hive beeline -u jdbc:hive2://localhost:10000
```
