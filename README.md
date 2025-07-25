# Redisson - Valkey & Redis Java client.<br/>Real-Time Data Platform.
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.redisson/redisson/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.redisson/redisson)
[![JavaDoc](http://www.javadoc.io/badge/org.redisson/redisson.svg)](http://www.javadoc.io/doc/org.redisson/redisson)
[![License](http://img.shields.io/:license-apache-brightgreen.svg)](http://www.apache.org/licenses/LICENSE-2.0.html)

[Quick start](https://redisson.org/docs/getting-started/) | [Documentation](https://redisson.org/docs/) | [Changelog](https://github.com/redisson/redisson/blob/master/CHANGELOG.md) | [Code examples](https://github.com/redisson/redisson-examples) | [Report an issue](https://github.com/redisson/redisson/issues/new)

Redisson is the Java Client and Real-Time Data Platform for Valkey and Redis. Providing the most convenient and easiest way to work with Valkey or Redis. Redisson objects provide an abstraction layer between Valkey or Redis and your Java code, which allowing maintain focus on data modeling and application logic. 

Redisson greatly extends the capabilities of Valkey and Redis by providing additional services and data structures not natively available in either platform. This enhancement includes distributed Java collections, objects, and service implementations, which significantly boost distributed application development and reduce the learning curve for Java developers working with key-value databases.

## Features

* Thread-safe implementation
* JDK 1.8+ up to the latest version compatible
* Android compatible
* [Redis](https://redis.io) compatible - from 3.0 up to the latest version
* [Valkey](https://valkey.io) compatible - from 7.2.5 up to the latest version
* Supported deployment types
    * [Proxy](https://redisson.org/docs/configuration/#proxy-mode)
    * [Multi-Cluster](https://redisson.org/docs/configuration/#multi-cluster-mode)
    * [Multi-Sentinel](https://redisson.org/docs/configuration/#multi-sentinel-mode)
    * [Single](https://redisson.org/docs/configuration/#single-mode)
    * [Cluster](https://redisson.org/docs/configuration/#cluster-mode)
    * [Sentinel](https://redisson.org/docs/configuration/#sentinel-mode)
    * [Replicated](https://redisson.org/docs/configuration/#replicated-mode)
    * [Master and Slaves](https://redisson.org/docs/configuration/#master-slave-mode)
* Supports auto-reconnection  
* Supports failed to send command auto-retry  
* Supports OSGi  
* Supports SSL  
* Asynchronous connection pool  
* Lua scripting  
* [RediSearch](https://redisson.org/docs/data-and-services/services/#redisearch-service)
* [JSON datatype](https://redisson.org/docs/data-and-services/objects/#json-object-holder)
* [JSON Store](https://redisson.org/docs/data-and-services/collections/#json-store) 
* [Reactive Streams](https://redisson.org/docs/api-models/#reactive-api) API  
* [RxJava3](https://redisson.org/docs/api-models/#rxjava-api) API  
* [Asynchronous](https://redisson.org/docs/api-models/#synchronous-and-asynchronous-api) API  
* Local cache support including [Caffeine](https://github.com/ben-manes/caffeine)-based implementation
* [Cache API implementations](https://redisson.org/docs/cache-api-implementations)  
    Spring Cache, JCache API (JSR-107), Hibernate Cache, MyBatis Cache, Quarkus Cache, Micronaut Cache
* [Distributed Java objects](https://redisson.org/docs/data-and-services/objects)  
    Object holder, JSON holder, Binary stream holder, Geospatial holder, BitSet, PublishSubscribe, Bloom filter, HyperLogLog
* [Distributed Java counters](https://redisson.org/docs/data-and-services/counters)  
    AtomicLong, AtomicDouble, LongAdder, DoubleAdder
* [Distributed Java collections](https://redisson.org/docs/data-and-services/collections)  
    JSON Store, Map, Multimap, Set, List, SortedSet, ScoredSortedSet, LexSortedSet, Queue, Deque, Blocking Queue, Bounded Blocking Queue, Blocking Deque, Delayed Queue, Priority Queue, Priority Deque
* [Distributed Java locks and synchronizers](https://redisson.org/docs/data-and-services/locks-and-synchronizers)  
    Lock, FairLock, MultiLock, RedLock, ReadWriteLock, Semaphore, PermitExpirableSemaphore, CountDownLatch
* [Distributed services](https://redisson.org/docs/data-and-services/services)  
    Remote service, Live Object service, Executor service, Scheduler service, MapReduce service
* [Microservices integration](https://redisson.org/docs/microservices-integration)  
    Helidon, Micronaut, Quarkus
* [Integration with Spring framework](https://redisson.org/docs/integration-with-spring)  
    Spring Boot Starter, Spring Cache, Spring Session, Spring Transaction Manager, Spring Cloud Stream, Spring Data Redis
* [Web Session Management](https://redisson.org/docs/web-session-management)  
    Apache Tomcat Session, Spring Session, Micronaut Session
* [Transactions API](https://redisson.org/docs/transactions)
* [Redis pipelining](https://redisson.org/docs/pipelining) (command batches)
* Supports many popular codecs ([Kryo](https://github.com/EsotericSoftware/kryo), [Jackson JSON](https://github.com/FasterXML/jackson), [Avro](http://avro.apache.org/), [Smile](http://wiki.fasterxml.com/SmileFormatSpec), [CBOR](http://cbor.io/), [MsgPack](http://msgpack.org/), [Amazon Ion](https://amzn.github.io/ion-docs/), [LZ4](https://github.com/jpountz/lz4-java), [Snappy](https://github.com/xerial/snappy-java), [Protobuf](https://github.com/protocolbuffers/protobuf) and JDK Serialization)
* 2000+ unit tests  

## [Redisson PRO vs. Community Edition ➜](https://redisson.pro/feature-comparison.html)

<!--

## Comparing solutions
- [Redisson vs Spring Data Redis](https://redisson.org/articles/feature-comparison-redisson-vs-spring-data-redis.html)
- [Redisson vs Jedis](https://redisson.org/feature-comparison-redisson-vs-jedis.html)
- [Redisson vs Lettuce](https://redisson.org/feature-comparison-redisson-vs-lettuce.html)
- [Redis vs Apache Ignite](https://redisson.org/feature-comparison-redis-vs-ignite.html)
- [Redis vs Hazelcast](https://redisson.org/feature-comparison-redis-vs-hazelcast.html)
- [Redis vs Ehcache](https://redisson.org/feature-comparison-redis-vs-ehcache.html)

## Success stories

- [Moving from Hazelcast to Redis  /  Datorama](https://engineering.datorama.com/moving-from-hazelcast-to-redis-b90a0769d1cb)  
- [Migrating from Hazelcast to Redis  /  Halodoc](https://blogs.halodoc.io/why-and-how-we-move-from-hazelcast-to-redis-2/)
- [Distributed Locking with Redis (Migration from Hazelcast)  /  ContaAzul](https://carlosbecker.com/posts/distributed-locks-redis/)  
- [Migrating from Coherence to Redis](https://www.youtube.com/watch?v=JF5R2ucKTEg)  
-->
