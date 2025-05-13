### How much data will the publisher program send to the message broker in one run?

The publisher program will send 5 events to the message broker in one run. This is evident from the `main` function in `publisher/src/main.rs`, where 5 `UserCreatedEventMessage` instances are created and published to the message broker using the `publish_event` method.

---

### What does it mean that the URL "amqp://guest:guest@localhost:5672" is the same as in the subscriber program?

The URL "amqp://guest:guest@localhost:5672" is a connection string that specifies the AMQP (Advanced Message Queuing Protocol) server to connect to. In this case, it means that both the publisher and subscriber programs are connecting to the same AMQP server, which is running on `localhost` (i.e., the same machine) and listening on port `5672`. The `guest` username and password are used for authentication.

---

### RabbitMQ Screenshot

![RabbitMQ Management](static/img/Screenshot%202025-05-13%20at%2013-18-01%20RabbitMQ%20Management.png)

---

### Subscriber Console Screenshot

![Subscriber Console](static/img/Screenshot%202025-05-13%20132506.png)

---

### Spike Explanation

The spike in the RabbitMQ Management screenshot is related to running the publisher because it represents the sudden increase in message publishing activity when the publisher program is executed.

When the publisher program runs, it sends 5 `UserCreatedEventMessage` instances to the message broker, which causes a spike in the RabbitMQ queue. This spike is visible in the RabbitMQ Management screenshot, which shows the message queue activity over time.

![RabbitMQ Management](static/img/Screenshot%202025-05-13%20at%2013-31-40%20RabbitMQ%20Management.png)