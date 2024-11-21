# Kafka

Apache Kafka is a distributed streaming platform that allows for the publishing, subscribing, storing, and processing of real-time data streams. It is widely used to build high-performance and scalable messaging systems. Kafka is commonly employed for monitoring, log analysis, event processing, and many other real-time use cases.

This guide provides an introduction to Kafka, including Python examples to demonstrate how to set up and use Kafka for sending and receiving messages.

---

## Table of Contents

- [Prerequisites](#prerequisites)  
  Installation and setup of Kafka and Python.

- [Basic Concepts](#basic-concepts)  
  Overview of key Kafka concepts such as producers, consumers, and topics.

- [Kafka Example in Python](#kafka-example-in-python)  
  Code example to send and receive messages using Kafka in Python.

- [Advanced Kafka Concepts](#advanced-kafka-concepts)  
  Information on partitioning, topics, offsets, and message processing.

---

## Prerequisites

To start working with Kafka and Python, you will need:

- **Install Kafka**:  
  You can follow the official documentation to install Apache Kafka on your machine or use a hosted Kafka service like Confluent Cloud.

  Kafka Installation:
  1. Download and extract Apache Kafka from [Apache Kafka Download](https://kafka.apache.org/downloads).
  2. Start Zookeeper (required by Kafka):
     ```bash
     bin/zookeeper-server-start.sh config/zookeeper.properties
     ```
  3. Then, start Kafka:
     ```bash
     bin/kafka-server-start.sh config/server.properties
     ```

- **Kafka-Python Library**: Kafka-Python is a library that provides an interface for interacting with Kafka using Python. Install it using the following command:
  ```bash
  pip install kafka-python
  ```

---

## Basic Concepts

- **Producer**: The producer is responsible for sending messages to a Kafka topic.
- **Consumer**: The consumer is responsible for reading messages from one or more Kafka topics.
- **Topic**: The topic is a communication channel where messages are sent by producers and consumed by consumers.
- **Partition**: Kafka divides each topic into partitions, allowing data distribution in a parallel and scalable way.
- **Offset**: The offset is the identifier of a message within a partition. The consumer uses the offset to track processed messages.

---

## Kafka Example in Python

Below is a simple example demonstrating how to set up a producer and a consumer in Kafka using the Kafka-Python library.

### Producer (Sending Messages)

```python
from kafka import KafkaProducer

# Connect to Kafka server
producer = KafkaProducer(bootstrap_servers='localhost:9092')

# Send a message to the 'test' topic
producer.send('test', b'Hello, Kafka!')

# Wait for all messages to be sent
producer.flush()

print("Message sent successfully!")

# Close the producer
producer.close()
```

In this example:
- We create a Kafka producer that connects to the server at `localhost:9092`.
- We send a simple message (`b'Hello, Kafka!'`) to the `test` topic.
- We use `flush()` to ensure all messages are sent before closing the connection.

### Consumer (Receiving Messages)

```python
from kafka import KafkaConsumer

# Connect to Kafka server
consumer = KafkaConsumer('test', bootstrap_servers='localhost:9092')

# Consume messages
for message in consumer:
    print(f"Received message: {message.value.decode('utf-8')}")

# Close the consumer
consumer.close()
```

In this example:
- We create a Kafka consumer for the `test` topic, connecting to the server at `localhost:9092`.
- The consumer continuously listens for messages on the topic and prints any received messages.
- The loop will continue until the consumer is closed.

---

## Advanced Kafka Concepts

### Partitioning
Kafka topics can be partitioned to improve performance and scalability. Each partition is handled by different consumers, enabling parallelism and load balancing. Kafka uses **partitioning keys** to determine which partition a message is sent to or consumed from.

Example of sending messages to specific partitions:

```python
# Send a message with a specific key, which can be used to determine the partition
producer.send('test', key=b'key1', value=b'Hello, Kafka!')
```

### Consumer with Offsets

In Kafka, each consumer maintains the **offset** of the messages it has read. It can start reading from a specific offset or process messages in the order they are received. By default, Kafka automatically stores the offset, but you can also control it manually.

Example of manual offset management:

```python
consumer = KafkaConsumer('test', 
                         bootstrap_servers='localhost:9092',
                         enable_auto_commit=False)

for message in consumer:
    print(f"Received message: {message.value.decode('utf-8')}")
    
    # Manually commit the offset
    consumer.commit()
```

### Stream Processing with Kafka Streams

Kafka Streams is a library that enables real-time stream processing. You can combine, filter, and transform data streams directly in Kafka.

To use Kafka Streams with Python, you can integrate Kafka with other stream processing libraries like Apache Flink or Apache Spark.
