# Spark Unified Stack and Core Concepts

## Spark Core:
- Central to the Spark stack, providing scheduling, distributing, and monitoring of applications across clusters.
- Scales from one to thousands of nodes and supports multiple cluster managers (e.g., Hadoop YARN, Apache Mesos, or standalone with its own scheduler).

## Components of the Spark Stack:
- Components like Spark SQL, Streaming, MLlib, and GraphX sit on top of the Spark Core, inheriting its performance improvements and fault tolerance.
- These components interoperate seamlessly, allowing for easy integration like software libraries.

## Key Libraries:
- **Spark SQL**: Allows SQL and HiveQL queries within Spark, integrated with its core programming languages (Python, Scala, Java).
- **Spark Streaming**: Supports real-time data processing, with an API similar to Spark Core’s, ensuring scalability and fault tolerance.
- **MLlib**: Provides scalable machine learning algorithms that run across clusters.
- **GraphX**: Offers graph processing APIs for graph-parallel computations.

## Advantages Over MapReduce:
- Spark builds upon MapReduce with faster in-memory processing and a more unified, flexible framework.
- MapReduce had limitations in complex use cases, whereas Spark can handle batch processing, real-time streaming, and machine learning.

## Code Efficiency:
- Spark reduces code complexity significantly compared to MapReduce, due to its tightly integrated libraries and minimal overhead.

## Resilient Distributed Dataset (RDD):
- Spark’s core data abstraction, representing distributed collections of elements processed in parallel across a cluster.
- Supports two main operations:
  - **Transformations**: Lazy operations (e.g., filter, map) that define a computation but do not execute until an action is called.
  - **Actions**: Triggers evaluation of transformations, returning values (e.g., count, reduce).

## Lazy Evaluation and Fault Tolerance:
- Spark creates a Directed Acyclic Graph (DAG) for transformations, which is evaluated only when an action is invoked.
- Fault tolerance is provided by reconstructing lost data through the lineage of transformations.

## Caching:
- Spark enables caching of RDDs in memory for faster processing. If memory is insufficient, data spills to disk.
