# Docker Hadoop Cluster
  
En este experimento vamos a montar y configurar un cluster de hadoop utilizando
docker.

## Imagen Base
  
La imagen base es esta: https://github.com/rvegas/hadoop-docker y la está 
publicada en docker aquí: https://hub.docker.com/r/rvegas/hadoop-cluster

## Diagrama simple de representación

https://docs.google.com/drawings/d/1Q0CHf9XtFwPb6fvqXWF9_okxjjT5S_UPnh-28Sod3kI/edit

## Requerimientos
  
Necesitarás:
- `Docker`
- `docker-compose`

## Instrucciones
  
Después de clonar, ejecuta:  
```bash
docker-compose up --build -d
```
  
Te encontrarás con 2 contenedores:
```
Creating network "hadoop_cluster_default" with the default driver
Creating hadoop_cluster_master_1 ... done
Creating hadoop_cluster_slave_1  ... done
```

## How to finish the excercise?
  
Simply find the hostname of the slave instance by running:
  
```bash
docker exec -it hadoop_cluster_slave_1 /bin/hostname
```
  
After that, go inside the master instance by running:
  
```bash
docker exec -it hadoop_cluster_master_1 /bin/bash
```
  
You'll have a prompt active for the master instance in which you 
can update the `slaves` file which defines what other nodes are 
available in the network to use as slaves. If you're capable of 
using [vi](https://en.wikipedia.org/wiki/Vi) simply run:
  
```bash
vi /usr/local/hadoop/etc/hadoop/slaves
```
  
In there you should add 1 line per slave instance, in this case, 
it should end up looking like this:
  
```
master
e230ab201f
```
  
Keep in mind that the master's hostname is `master` and that the 
slave's hostname is the one that you found out in the first command 
of this section.
  
After doing all this, run this to make both `yarn` and `hdfs` reload 
the possible slaves and start both a nodemanager and a datanode on 
each of the slaves instances:

```
/usr/local/hadoop/sbin/start-dfs.sh
/usr/local/hadoop/sbin/start-yarn.sh
```
  
If you've followed all of the steps carefully, you should see 2 datanodes 
and 2 nodemanagers on these hadoop UI pages:  
  
- http://localhost:50070/dfshealth.html#tab-datanode
- http://localhost:8088/cluster/nodes

## Scaling the cluster up and down
  
If you want to add more slaves to the cluster, simply go to your host 
machine and run:
  
```bash
docker-compose scale slave=2
```
  
Simply state the number of slave machines that you need in total, and 
then for each, find out their hostnames and add them to the master's 
slave configuration file, along with a call to `dfs` and `yarn` start 
scripts.