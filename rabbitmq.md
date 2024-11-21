# RabbitMQ

RabbitMQ is a popular open-source message broker that facilitates communication between different applications or services. It is widely used for message queuing, supporting asynchronous communication, and providing reliability in message delivery.

This guide provides an introduction to RabbitMQ with Python examples to demonstrate how to set up and use RabbitMQ for messaging tasks such as publishing and consuming messages.

---

## Index

- [Prerequisites](#prerequisites)  
  Installation and setup instructions for RabbitMQ and Python.

- [Basic Concepts](#basic-concepts)  
  Overview of core RabbitMQ concepts like producers, consumers, and queues.

- [RabbitMQ Example in Python](#rabbitmq-example-in-python)  
  Example code to send and receive messages using RabbitMQ in Python.

- [Advanced RabbitMQ Concepts](#advanced-rabbitmq-concepts)  
  Information on durable queues, persistent messages, and routing.

---

## Prerequisites

To get started with RabbitMQ and Python, you need to install:

- **RabbitMQ server**: RabbitMQ server should be running on your machine or accessible on a network. You can follow the installation guide for RabbitMQ on [official documentation](https://www.rabbitmq.com/).
  
- **Pika library**: Pika is a Python library that provides an interface to RabbitMQ. Install it using pip:
  ```bash
  pip install pika
  ```

---

## Basic Concepts

- **Producer**: A program that sends messages to a queue.
- **Consumer**: A program that retrieves and processes messages from a queue.
- **Queue**: A buffer that stores messages until they are consumed.
- **Exchange**: Routes messages to the appropriate queue.

---

## RabbitMQ Example in Python

Below is a simple example where we demonstrate how to set up a RabbitMQ producer and consumer using the Pika library.

### Producer (Sending Messages)

```python
import pika

# Connect to RabbitMQ server
connection = pika.BlockingConnection(pika.ConnectionParameters('localhost'))
channel = connection.channel()

# Declare a queue named 'hello'
channel.queue_declare(queue='hello')

# Send a message to the 'hello' queue
channel.basic_publish(exchange='',
                      routing_key='hello',
                      body='Hello World!')

print(" [x] Sent 'Hello World!'")

# Close the connection
connection.close()
```

In this example:
- We create a connection to the RabbitMQ server running on `localhost`.
- We declare a queue named `hello`. If the queue doesn't exist, it will be created.
- We send the message `"Hello World!"` to the `hello` queue using the `basic_publish` method.
- Finally, we close the connection after sending the message.

### Consumer (Receiving Messages)

```python
import pika

# Connect to RabbitMQ server
connection = pika.BlockingConnection(pika.ConnectionParameters('localhost'))
channel = connection.channel()

# Declare a queue named 'hello'
channel.queue_declare(queue='hello')

# Callback function to process messages
def callback(ch, method, properties, body):
    print(f" [x] Received {body.decode()}")

# Start consuming messages from the 'hello' queue
channel.basic_consume(queue='hello', on_message_callback=callback, auto_ack=True)

print(' [*] Waiting for messages. To exit press CTRL+C')
channel.start_consuming()
```

In this example:
- We connect to the RabbitMQ server and declare the `hello` queue again.
- The `callback` function is defined to handle the received messages. It simply prints out the received message (`body.decode()`).
- The `basic_consume` method is used to start listening for messages from the `hello` queue. When a message is received, the `callback` function is triggered.
- `auto_ack=True` automatically acknowledges the message, indicating it has been processed.

---

## Advanced RabbitMQ Concepts

### Durable Queues
By default, queues in RabbitMQ are not durable. This means if RabbitMQ crashes, all messages in the queue are lost. To make queues durable, you can specify the `durable=True` parameter when declaring the queue.

```python
channel.queue_declare(queue='hello', durable=True)
```

### Persistent Messages
To ensure that messages are not lost if RabbitMQ crashes, you can make them persistent by setting the `delivery_mode=2` property when publishing the message.

```python
channel.basic_publish(exchange='',
                     routing_key='hello',
                     body='Hello World!',
                     properties=pika.BasicProperties(
                         delivery_mode=2,  # Make message persistent
                     ))
```

### Exchanges and Routing
RabbitMQ supports different types of exchanges (direct, topic, fanout, and headers) for routing messages to queues. You can use different exchanges to control how messages are routed.

Example using a **direct exchange**:

```python
# Producer using a direct exchange
channel.exchange_declare(exchange='logs', exchange_type='direct')
channel.basic_publish(exchange='logs', routing_key='info', body='This is an info message')

# Consumer using a direct exchange
channel.exchange_declare(exchange='logs', exchange_type='direct')
channel.queue_declare(queue='info_logs')
channel.queue_bind(exchange='logs', queue='info_logs', routing_key='info')
```
