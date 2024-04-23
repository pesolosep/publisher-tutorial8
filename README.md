- Muhammad Faishal Adly Nelwan
- 2206030754/Advanced Programming C


# How many data your publisher program will send to the message broker in one run?
The publisher program will send 5 messages to the broker in one run. This is due to the code calling 5 `publish_event` methods, each publishing a `UserCreatedEventMessage`.

# The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

The URL `amqp://guest:guest@localhost:5672` is the same in both the **publisher** and **subscribe** programs, which means they are connected to the same message broker instance running on localhost with port 5672.

Therefore, both the publisher and subscriber interact with the same message broker, making it possible for them to be sending and receiving messages from the same queue.

# Running RabbitMQ as message broker
![alt text](<docs/running RabbitMQ.jpg>)