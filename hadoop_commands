hduser@bmsce-OptiPlex-3060:~$ start-all.sh
This script is Deprecated. Instead use start-dfs.sh and start-yarn.sh
22/05/31 10:24:08 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Starting namenodes on [localhost]
localhost: starting namenode, logging to /usr/local/hadoop/logs/hadoop-hduser-namenode-bmsce-OptiPlex-3060.out
localhost: starting datanode, logging to /usr/local/hadoop/logs/hadoop-hduser-datanode-bmsce-OptiPlex-3060.out
Starting secondary namenodes [0.0.0.0]
The authenticity of host '0.0.0.0 (0.0.0.0)' can't be established.
ECDSA key fingerprint is SHA256:/yLgfi4ldgrCqmRYXV0L3IPgwUzgy+0xH+slY4ek7Kg.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
0.0.0.0: Warning: Permanently added '0.0.0.0' (ECDSA) to the list of known hosts.
0.0.0.0: secondarynamenode running as process 10393. Stop it first.
22/05/31 10:24:28 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
starting yarn daemons
resourcemanager running as process 10550. Stop it first.
localhost: nodemanager running as process 10878. Stop it first.
hduser@bmsce-OptiPlex-3060:~$ jps
18598 Jps
18198 DataNode
10550 ResourceManager
18038 NameNode
10393 SecondaryNameNode
10878 NodeManager
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -ls /
22/05/31 10:27:23 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -mkdir /skanda
22/05/31 10:27:53 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -ls /
22/05/31 10:28:31 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Found 1 items
drwxr-xr-x   - hduser supergroup          0 2022-05-31 10:27 /skanda
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -put /home/hduser/Desktop/demo.txt /skanda/sample.txt
22/05/31 10:32:27 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
put: `/home/hduser/Desktop/demo.txt': No such file or directory
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -put /home/bmsce/Desktop/demo.txt /skanda/sample.txt
22/05/31 10:35:06 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -ls /skanda/
22/05/31 10:35:32 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Found 1 items
-rw-r--r--   1 hduser supergroup         12 2022-05-31 10:35 /skanda/sample.txt
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -copyFromLocal /home/bmsce/Desktop/demo.txt /skanda/sample1.txt
22/05/31 10:36:18 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -ls /skanda/
22/05/31 10:36:22 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Found 2 items
-rw-r--r--   1 hduser supergroup         12 2022-05-31 10:35 /skanda/sample.txt
-rw-r--r--   1 hduser supergroup         12 2022-05-31 10:36 /skanda/sample1.txt
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -get /skanda/sample.txt  /home/bmsce/Desktop/copy.txt 
22/05/31 10:38:32 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
get: /home/bmsce/Desktop/copy.txt._COPYING_ (Permission denied)
hduser@bmsce-OptiPlex-3060:~$ sudo chmod 777 -R /home/bmsce/Desktop
[sudo] password for hduser: 
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -get /skanda/sample.txt  /home/bmsce/Desktop/copy.txt 
22/05/31 10:39:39 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
hduser@bmsce-OptiPlex-3060:~$ ls
hadoop-2.6.0  hadoop-2.6.0.tar.gz
hduser@bmsce-OptiPlex-3060:~$ ls /home/bmsce/Desktop/copy.txt
/home/bmsce/Desktop/copy.txt
hduser@bmsce-OptiPlex-3060:~$ ls /home/bmsce/Desktop/
 1BM19CS041   demo.txt              labtest.sh                                                                                               R-with-Hadoop-YouTube.mp4  'unix shell proramming'
 copy.txt     hadoop-2.6.0.tar.gz  'Program 20'                                                                                              share
 data         LAB-5                 RHadoop-Integrating-R-with-Hadoop-How-to-Integrate-R-Hadoop-R-Programming-Tutorial-Edureka-YouTube.mp4  'spark installation'
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -copyToLocal /skanda/sample.txt  /home/bmsce/Desktop/copy1.txt 
22/05/31 10:41:12 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
hduser@bmsce-OptiPlex-3060:~$ ls /home/bmsce/Desktop/
 1BM19CS041   data                  LAB-5         RHadoop-Integrating-R-with-Hadoop-How-to-Integrate-R-Hadoop-R-Programming-Tutorial-Edureka-YouTube.mp4  'spark installation'
 copy1.txt    demo.txt              labtest.sh    R-with-Hadoop-YouTube.mp4                                                                               'unix shell proramming'
 copy.txt     hadoop-2.6.0.tar.gz  'Program 20'   share
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -cat /skanda/sample.txt
22/05/31 10:42:17 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
hi
hey
wow

hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -mv /skanda /AAA
22/05/31 10:43:10 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -ls /AAA
22/05/31 10:43:27 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Found 2 items
-rw-r--r--   1 hduser supergroup         12 2022-05-31 10:35 /AAA/sample.txt
-rw-r--r--   1 hduser supergroup         12 2022-05-31 10:36 /AAA/sample1.txt
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -cp /AAA /BBB
22/05/31 10:44:24 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
hduser@bmsce-OptiPlex-3060:~$ hdfs dfs -ls /BBB
22/05/31 10:44:30 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Found 2 items
-rw-r--r--   1 hduser supergroup         12 2022-05-31 10:44 /BBB/sample.txt
-rw-r--r--   1 hduser supergroup         12 2022-05-31 10:44 /BBB/sample1.txt
