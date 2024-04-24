## **Hi! :wave:, I'm Muhammad Fiqo Anugrah and this is my repo for Tutorial 8 Adpro C**


> REFLECTION

**a. How many data your publlsher program will send to the message broker in one
run?**

The publisher program is designed to send five separate messages (data entries) to the message broker during a single execution. This is evidenced by the presence of five publish_event calls within the main function, each configured with distinct data.

**b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?**

Yes, the URL "amqp://guest:guest@localhost:5672" being the same in both the publisher and subscriber programs indicates that both applications are configured to connect to the same AMQP server using identical settings.

amqp:// specifies the protocol used, which is AMQP.
guest:guest represents the default login credentials being used. In this context, 'guest' is the username, and 'guest' is also the password.
localhost:5672 is the host address and port used to connect to the AMQP server. In this case, the connection is made to the same machine (localhost) on the standard AMQP port (5672).
This uniformity in the connection URL ensures that both the publisher and subscriber are interacting with the same message queue, facilitating effective communication and message exchange within the same local environment.

## Running RabbitMQ as message broker : 
![image](https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/bb8dfa25-1b1e-498f-ab37-8fde8b2d1859)

## we should at least have one connection as shown:
It means we have one subscriber making connection to the message broker
![image](https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/2454d11a-e65c-4f31-b41b-07ead29c8fe4)

Now try to run the publisher again, ‘cargo run’ in the directory publisher. Pay attention on the
subscriber console on the right. I find some thing like this:
![image](https://github.com/fiqoanugrah/tutorial-8-publisher/assets/87713462/d969ce95-c9b2-4d57-8af6-12f46b0fd748)
when I run ‘cargo run’ on publisher (I run the publisher), the publisher sent 5
event to the message broker. Those event later consumed and processed by the subscriber. 

