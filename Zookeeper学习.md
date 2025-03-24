#  Zookeeper学习

##  1.概念

* Zookeeper是Apache Hadoop项目下的一个子项目，是一个树形目录服务。简称zk。

* Zookeeper是一个分布式的、开源的分布式应用程序的协调服务。

* Zookeeper提供的主要功能包括：

  * 配置管理

  * 分布式锁

  * 集群管理(注册中心)

    ​

##  2.安装

###  2.1 下载安装

####  1.环境准备

Zookeeper服务是用Java创建的，需要安装jdk7以上版本，以下是安装在Linux环境下。

####  2.上传

进入Apache官网下载https://zookeeper.apache.org/releases.html，去将下载的Zookeeper放到/opt/Zookeeper目录下

![74282066987](C:\Users\32542\AppData\Local\Temp\1742820669875.png)

​		![74282071518](C:\Users\32542\AppData\Local\Temp\1742820715185.png)

（待完善）

## 3.命令操作

### 3.1 数据模型

* Zookeeper是一个树形目录服务，其数据模型和Unix的文件系统目录树类似
* 它的每一个节点都被称为:ZNode,，每个节点都会保存自己的数据和节点信息。
* 节点可以拥有子节点，同时也允许少量(1MB)数据存储在该节点下。
* 节点可以分为四大类：
  * PERSISTENT 持久化顺序节点
  * EPHEMERAL 临时节点：-e
  * PERSISTENT_SEQUENTIAL 持久化顺序节点：-s
  * EPHEMERAL_SEQUENTIAL 临时顺序节点：-es

### 3.2服务端常用命令

``` she
./zkServer.sh start  # 启动Zookeeper服务
./zkServer.sh status  # 查看Zookeeper服务状态
./zkServer.sh stop  # 停止Zookeeper服务
./zkServer.sh restart  # 重启Zookeeper服务
```

