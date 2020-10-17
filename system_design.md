
# System Design

 Overview:
 https://www.youtube.com/watch?v=-W9F__D3oY4

- Scaling
  - Vertical
    - Bigger machine (bump specs)
    - Single point of failure
    - Consistent
    - Hardware limit
  - Horizontal
    - More machines
    - Needs a load balancer
    - Resilient
    - Data inconsistency, network calls
    - Scales well
  - Hybrid
    - best of both
 
 - High level design steps
    - Optimize processes and increase throughput (vertical)
    - caching and pre-compute
    - Resilience (backup)
    - Horizontal scaling
    - Mircroservices and Pools
    - Distributed system (partitions)
    - Fault tolerance
    - Load balancer
    - Decoupling
    - Logging and metrics
    - Extensible architecture
  
  - Load balancing
    - consistent hashing 
    - reducing impact on horizontal scaling
    - skewed distribution
    - replica service id's to create at least log(x) distrubution points
    - Software: ELB, HAProxy | Hardware: F5

- Message/Task queue
  - heartbeats
  - persistence
  - load balancing

- Monolith
  - less moving parts
  - deployment maybe single but not depcoupled
  - less duplication
  - local exec speed
  - point of failure
  - team size
  
- Microservices
  - easier to scale
  - parallel development
  - decoupled deployments
  
- Database
  - horizontal partitioning (sharding)
  - vertical partitioning
  - consistency
  - availability
    - heirarchical sharding
    - indexing

- Caching
  - LRU
  - thrashing
  - consistency
  - global cache
  - write-through: data is written in cache & DB; I/O completion is confirmed only when data is written in both places
  - write-around: data is written in DB only; I/O completion is confirmed when data is written in DB
  - write-back: data is written in cache first; I/O completion is confirmed when data is written in cache; data is written to DB asynchronously (background job)
 
  
