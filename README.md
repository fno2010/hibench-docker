# HiBench Suite

An [HiBench Suite](https://github.com/intel-hadoop/HiBench) container image. The image is based on [Apache Spark image](https://github.com/fno2010/spark-docker).

# Usage

```
docker run -ti -d --name hibench fno2010/hibench

docker exec -ti hibench bash

root@09e511ea1b41:/# master 0.0.0.0 &
root@09e511ea1b41:/# worker 0.0.0.0 $(hostname) &
root@09e511ea1b41:/# config-hibench $(hostname)
root@09e511ea1b41:/# $HIBENCH_HOME/bin/workloads/micro/wordcount/prepare/prepare.sh
root@09e511ea1b41:/# $HIBENCH_HOME/bin/workloads/micro/wordcount/spark/run.sh
```
