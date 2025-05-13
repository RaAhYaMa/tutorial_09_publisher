### How much data will the publisher program send to the message broker in one run?

The publisher program will send 5 events to the message broker in one run. This is evident from the `main` function in `publisher/src/main.rs`, where 5 `UserCreatedEventMessage` instances are created and published to the message broker using the `publish_event` method.

---

### What does it mean that the URL "amqp://guest:guest@localhost:5672" is the same as in the subscriber program?

The URL "amqp://guest:guest@localhost:5672" is a connection string that specifies the AMQP (Advanced Message Queuing Protocol) server to connect to. In this case, it means that both the publisher and subscriber programs are connecting to the same AMQP server, which is running on `localhost` (i.e., the same machine) and listening on port `5672`. The `guest` username and password are used for authentication.