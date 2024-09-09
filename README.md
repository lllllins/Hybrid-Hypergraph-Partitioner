# Hybrid-Hypergraph-Partitioner
HHP: A Hybrid Partitioner for Large-scale Hypergraph

Due to blind review requirements, we are currently providing executable files for the program.
# Environment requirements
C++17

Boost
# File Structure
```tree
.
├── HHP
│ ├── HHP_offline            //offline part in HHP
│ ├── HHP_online             //online part in HHP
│ ├── HHP_offLine.graph      //subgraph for offline
│ ├── HHP_onLine.graph       //subgraph for online
│ ├── offLine_information    //Stateful info for online part(generate after offline part)
│ └── HHP_Partition_Result   //HHP result(Each two rows represent the vertices and edges in a partition)
```
Hypgergraph format
we use the neighbor matrix format.
```
v1 : e1
v2 : e1, e2, e3, e4
v3 : e1, e4
```
# How to run
Each program needs an option to set the number of partitions(default k = 64).
```
./HHP_offline -k 128
./HHP_online -k 128
```
Also can modify the run.sh for partitions.
Make sure each subgraph is ready.

Due to github limitations, we shared some experimental dataset through [this](https://drive.google.com/drive/folders/1DmRHmbJyh5Ybtnha46MGRdijXCoeRjto?usp=drive_link) .
