# Functions

## Required Libraries

```python
import pika
import os
```

## Connecting to RabbitMQ service

```python
con_params = pika.URLParameters(os.environ["AMQP_URL"])
connection = pika.BlockingConnection(parameters=con_params)
```

## Establishing Channel

```python
channel = connection.channel()
```

## Creating An Exchange

```python
exchange = channel.exchange_declare(exchange="Exchange Name")
```

## Publishing To An Exchange

```python
channel.basic_publish(
    exchange="Exchange Name",
    routing_key="Routing Key",
    body="Message",
)
```

## Declaring Queue

```python
channel.queue_declare(queue="Queue Name")
```

## Binding Queue To Exchange

```python
channel.queue_bind(
    queue= "Queue Name",
    routing_key= "Routing Key",
    exchange="Exchange Name",
)
```

## Setup Callback Function For Queue

```python
channel.basic_consume(
    "Queue Name", Function Name, auto_ack=False
)
```

## Acknowledge Message

```python
channel.basic_ack(method_frame.delivery_tag, False)
```

## Closing Channel and Connection

```python
channel.close()
connection.close()
```

## Start Consuming Message

```python
channel.start_consuming()
```

## Creating Topic Exchange

```python
channel.exchange_declare(
    exchange="Exchange Name", exchange_type="topic"
)
```

## De-Serialize JSON message object

```python
message = json.loads(JsonMessageObject)
```

