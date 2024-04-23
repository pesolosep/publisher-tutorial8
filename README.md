- Muhammad Faishal Adly Nelwan
- 2206030754/Advanced Programming C


# How many data your publisher program will send to the message broker in one run?
The publisher program will send 5 messages to the broker in one run. This is due to the code calling 5 `publish_event` methods, each publishing a `UserCreatedEventMessage`.

# The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

The URL `amqp://guest:guest@localhost:5672` is the same in both the **publisher** and **subscribe** programs, which means they are connected to the same message broker instance running on localhost with port 5672.

Therefore, both the publisher and subscriber interact with the same message broker, making it possible for them to be sending and receiving messages from the same queue.

# Running RabbitMQ as message broker
![alt text](<docs/running RabbitMQ.jpg>)

# Sending and processing event
![alt text](image-1.png)
![alt text](image.png)
By using a message broker (in this case RabbitMQ), every time we run the Subscriber and Publisher programs using `cargo run`, the Publisher sends data to the message broker, which is then received by the Subscriber. From the illustration provided, it appears that the Publisher sends data once to the message broker and then the Subscriber receives this data. In other words, in this process, the Publisher acts as the data sender, while the Subscriber acts as the receiver.

# Monitoring chart based on publisher.
![alt text](docs/monitoringchart.jpg)
The chart in the image depicts the activity of the `publisher` in sending its messages. We can determine whether the load on the publisher in sending messages is heavy or light by monitoring the message rates. This helps in understanding the amount of sending and processing that is occurring.
