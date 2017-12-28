zookeeper
=========

![](http://zookeeper.apache.org/images/zookeeper_small.gif)

Apache [ZooKeeper][1] is an effort to develop and maintain an open-source server
which enables highly reliable distributed coordination.


## docker-compose.yml

```yaml
zookeeper:
  image: zookeeper
  ports:
    - "2181:2181"
  volumes:
    - ./data:/data
    - ./datalog:/datalog
  restart: always
```

## Standalone Mode

```bash
$ docker-compose up -d
$ docker-compose exec zookeeper zkCli.sh
>>> help
>>> create /hello world
>>> get /hello
>>> delete /hello
>>> quit
```

Click [this][2] to learn more.

## Cluster Mode [TODO]

[1]: http://zookeeper.apache.org/
[2]: https://zookeeper.apache.org/doc/trunk/zookeeperStarted.html