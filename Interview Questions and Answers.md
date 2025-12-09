# 💬 Apache Kafka Interview Questions & Answers

Beginner + Intermediate + Advanced (30 Questions Total)

# 🟡 Beginner Level – 10 Questions
1. What is Apache Kafka?

Answer:
Apache Kafka is a distributed event streaming platform used for building real-time data pipelines and streaming applications. It allows high-throughput, low-latency publishing and subscribing of data streams.

2. What is a Kafka Topic?

Answer:
A topic is a category or feed name in Kafka to which records are stored and from which consumers read data.

3. What is a Producer in Kafka?

Answer:
A producer is a client application that sends (writes) data to Kafka topics.

4. What is a Consumer in Kafka?

Answer:
A consumer is a client application that reads (subscribes to) messages from Kafka topics.

5. What is a Kafka Broker?

Answer:
A broker is a Kafka server that stores data and serves client requests for read/write operations.

6. What is a Partition in Kafka?

Answer:
A topic is divided into partitions for scalability and parallelism. Each partition is an ordered, immutable sequence of messages.

7. What is an Offset?

Answer:
Offset is the unique identifier for each record within a Kafka partition.

8. What is a Consumer Group?

Answer:
A consumer group is a collection of consumers that work together to read data from partitions for load balancing.

9. What does Replication mean in Kafka?

Answer:
Replication ensures data availability by copying partitions across multiple brokers.

10. What is Zookeeper in Kafka (older versions)?

Answer:
Zookeeper manages metadata, cluster coordination, and broker leadership elections for Kafka (pre-KIP-500).

# 🔵 Intermediate Level – 10 Questions
11. What is a Kafka Cluster?

Answer:
A cluster is a group of Kafka brokers working together for distributed storage and fault tolerance.

12. What is the difference between Kafka and a Traditional Message Queue?

Answer:

Kafka	Traditional MQ
Pull model	Push model
High throughput	Limited throughput
Distributed & scalable	Single-node or limited scaling
Retains data for time	Deletes after delivery
13. What is Kafka Streams?

Answer:
Kafka Streams is a Java library that enables real-time stream processing directly within applications.

14. What is Schema Registry?

Answer:
It stores and enforces data schemas for Kafka messages to ensure compatibility and structure.

15. What is Log Compaction?

Answer:
Log compaction ensures Kafka keeps the latest version of each key, useful for changelog-style data.

16. Explain At-Least-Once vs Exactly-Once Delivery in Kafka.

Answer:

At-least-once: Messages may be delivered more than once but never lost.

Exactly-once: Guaranteed single delivery via idempotent producers + transactions.

17. What is a Rebalance in Kafka?

Answer:
A rebalance redistributes partitions across consumers when group membership changes.

18. What is Kafka Connect?

Answer:
Kafka Connect is a framework that integrates Kafka with external systems (databases, S3, Elasticsearch).

19. What is Producer Acknowledgment (acks)?

Answer:
It controls reliability of message delivery:

acks=0 → fire and forget

acks=1 → leader ack

acks=all → leader + replicas ack

20. What is Retention Policy in Kafka?

Answer:
Defines how long Kafka stores data (time-based or size-based).

# 🔴 Advanced Level – 10 Questions
21. What is Kafka’s Internal Architecture Based On?

Answer:
Kafka uses a distributed commit log, partitioning, replication, zero-copy transfers, and sequential disk I/O.

22. Explain Leader & Follower Replicas.

Answer:

Leader replica: Handles all reads/writes.

Follower replicas: Replicate the leader's data asynchronously.

23. What is ISR (In-Sync Replicas)?

Answer:
ISR is the set of replicas fully synced with the leader. Only ISR members are eligible to become leaders.

24. What is Idempotent Producer?

Answer:
It ensures messages are not duplicated by assigning a producer ID and sequence numbers.

25. What is a Transactional Producer?

Answer:
Enables atomic writes across multiple partitions, achieving exactly-once semantics.

26. What is Backpressure in Kafka Streams?

Answer:
When the processing is slower than incoming data, Kafka Streams pauses consumption to prevent overload.

27. What is KTable vs KStream?

Answer:

KStream: Real-time, unbounded data stream.

KTable: Table view of latest key-value states (changelog stream).

28. What is Partition Reassignment?

Answer:
It redistributes partitions across brokers to maintain balance and avoid hotspots.

29. What is Kafka’s Exactly-Once Semantics (EOS)?

Answer:
EOS ensures messages are processed once without duplication using transactions + idempotency.

30. What is Tiered Storage in Kafka?

Answer:
Allows storing older Kafka data on cheaper cloud/object storage while keeping recent data on local disks.
