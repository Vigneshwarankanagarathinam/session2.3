Session 2: Hadoop Framework Description
Assignment 3
•	Hadoop mainly provides a distributed storage (HDFS) and distributed computation engine (MapReduce) to solve certain problems of Big Data World. 
•	Both of these core components have some set of processes (daemons).

1.	HDFS
HDFS in Hadoop 1.x mainly has 3 daemons which are Name Node, Secondary Name Node and Data Node.
(i)	Name Node:
•	There is only single instance of this process runs on a cluster and that is on a master node.
•	It is responsible for manage metadata about files distributed across the cluster.
•	This process is a heart of HDFS, if it is down HDFS is not accessible any more.
(ii)	Secondary Name Node:
•	For this also, only single instance of this process runs on a cluster.
•	This process can run on a master node (for smaller clusters) or can run on a separate node (in larger clusters) depends on the size of the cluster.
(iii)	Data Node:
•	There are many instances of this process running on various slave nodes (referred as Data nodes).
•	It is responsible for storing the individual file blocks on the slave nodes in Hadoop cluster.

2.	MapReduce – Distributed Computation
MapReduce component is responsible for distributed computing on Hadoop Cluster. Basically it uses two daemons named Job Tracker and Task Tracker. 
(i)	Job Tracker:
•	Any MapReduce job is submitted to Job Tracker first.
•	Job Tracker checks for the location various file blocks used in MapReduce processing.
(ii)	Task Tracker:
•	This process has multiple instances running on the slave nodes (typically runs on the slave nodes where Data Node process is running).
•	It receives the job information from Job Tracker daemon and initiates a task on that slave node.
