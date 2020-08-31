## Presto-standalone

### About

To run presto-standalone
update the configuration file `s3.properties` with your AWS credentials

Run the following commands:

```sh
$ docker pull ahanaio/prestodb-sandbox
$ docker run -d -p 8080:8080 -v $PWD/catalog:/opt/presto-server/etc/catalog --name presto ahanaio/prestodb-sandbox
$ docker exec -it presto  presto-cli 
```

