# Jenkins- Cluster or Distributed Jenkins

``Node`` this is a special environment that contains customize workspace to achieve our goal of task. There can be several node in one whole application which are created to serve their purpose in managing the appplication. This nodes are also known as `Slave or Worker Node`. 

``Master Node`` this node is created to maintain all the slave node at one place this is the sole purpose of master node.

`` Distribute Cluster ``  Cluster is something that holds both the `Master node` and `Worker Node`
cluster is responsible for providing various environment required to  manage the application.

For this we need atleast instances one which conatains `Master node` and other instance will contain the `Worker Node`.

Only two  same job can run simultaneously when you try to perform the third job it will be in queue. this is applicable to slave node only on master we can run jobs simultaneously. 

Number of jobs depends on the amount of resources we have  with us. If we want to run 4000 job at a time we can run in master node but for this to achieve  we require large amount of resources to handle all this jobs all together.

` Executor ` means how many parallel job you want to run you can set this up according to your needs.

`Create Node Cluster` go to jenkins dashboard select manage jenkins then click on node and give a suitable node to create the cluster you should remember your  node name as it require when you setup the master and slave cluster. You can also add the number of executor there.

``Agent`` This programs main function is to connect the master and slave via ssh or remote connection as master can give the command to run continuously the jobs on slave node, For this we need a medium and this medium is called as a `Agent` and this whole program is known as  `Permanent Agent` this  keep the slave node wake up.

` Remote Root Directory` it is always mandatory to give the directory where your jobs related required files will be stored. iF  you fail to provide any directory your slave node will not be able to start and you will see the `red cross mark`.

Select the launch method how to launch the job either by controller or command line execution you have to select the launcher as per your job requirements. 
