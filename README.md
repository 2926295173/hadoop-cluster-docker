## Run Hadoop Cluster within Docker Containers

### 3 Nodes Hadoop Cluster

##### 1. pull docker image

```
$ sudo docker pull aoian5173/hadoop5173:latest
```

##### 2. clone github repository

```
$ git clone https://github.com/2926295173/hadoop-cluster-docker
```

##### 3. run

```
$ sudo docker compose up
```

##### 4. start container
`$ exec `
**output:**

```
start hadoop-master container...
start hadoop-slave1 container...
start hadoop-slave2 container...
root@hadoop-master:~# 
```
- start 3 containers with 1 master and 2 slaves
- you will get into the /root directory of hadoop-master container


### Arbitrary size Hadoop cluster

##### 1. pull docker images and clone github repository

do 1~3 like section A

##### 2. rebuild docker image

```
sudo ./resize-cluster.sh 5
```
- specify parameter > 1: 2, 3..
- this script just rebuild hadoop image with different **slaves** file, which pecifies the name of all slave nodes

##### 3. run hadoop cluster 

do 5~6 like section A

