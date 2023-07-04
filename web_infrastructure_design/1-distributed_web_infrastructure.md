## For additional element, why you are adding it?

The new configuration is composed of two master-servers and one slave-servers. As the master-servers are going to be working based on a Active-Active set up, their configuration must be identical, therefore we need to add every additional element as the simple web infrastructure we had in the previous point. The load is going to be managed through a load-balancer, which distributes the queries according to a Robin-Round algorithm. Finally an additional server will be needed to serve a replica or slave server, this server can help in many aspects: redundancy, load distribution, scalability, and facilitates maintenance tasks.

## What distribution algorithm your load balancer is configured with and how it works
Our load-balancer is using a Round Robin algorithm. the queries requested are distributed to every server sequentially one after another, after sending the request to the last server, the algorithm startarts from the first server.
this will try to distribute equaly the load 50% in each

## Is your load-balancer enabling an Active-Active or Active-Passive setup, explain the difference between both
Our load-balancer is enabling an Active-Active set up. 
# difference between Active-Active and Active-Pasive:
the main difference between active-active and active-passive configurations is that in active-active, multiple servers are actively serving client requests simultaneously, while in active-passive, there is one active server and one passive server that takes over when the active server fails. Active-active provides load distribution and scalability, while active-passive focuses on failover and ensuring high availability in case of primary server failures.
## How a database Primary-Replica (Master-Slave) cluster works
A primary-replica (master-slave) database cluster is a configuration where one database server acts as the primary/master server, handling both read and write operations, while one or more replica/slave servers replicate the data from the primary server and handle read-only operations.By using a primary-replica cluster, you can achieve data redundancy, high availability, and scalability. The primary server handles write operations, while the replica servers provide additional read capacity and serve as backups in case the primary server fails. The replication process ensures that the data on the replicas stays synchronized with the primary server, providing a consistent view of the database across the cluster.
## What is the difference between the primary node and the replica node in regard to the application.
the primary node in a primary-replica database cluster handles both read and write operations and is the authoritative source of data. It ensures data consistency and plays a critical role in failover. The replica node(s) primarily serve read-only operations, maintain eventual consistency, and provide scalability and high availability by offloading the read workload from the primary node.

## Issues with the distributed web infrastructure

# Security issues.
The data transmitted over the network isnt encrypted using an SSL certificate so the network is not safe. There is no way of blocking unauthorized IPs since there isnt a firewall installed on any server.
# No monitoring.
We have no way of knowing the status of each server since they are not being monitored.
