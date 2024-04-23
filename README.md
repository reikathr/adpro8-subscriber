# Tutorial-8
---
#### Nama: Athira Reika
#### NPM: 2206031422
#### Kelas: Adpro B
---
### Refleksi
<ol>
<li>What is amqp?</li>
<p> Answer: AMQP stands for Advanced Message Queueing Protocol. It's an open standard application layer protocol used for passing messages between applications that uses subscriber-publisher model.
<li>What guest:guest@localhost:5672 means? what is the first guest, and what is the second guest, and what is localhost:5672 is for?</li>
<p>Answer: <code>guest:guest@localhost:5672</code> is the string that connects the application to an AMQP server. The first <code>guest</code> is the username to aunthenticate to the server and the second one is the password. <code>localhost:5672</code> means that the message broker will run locally on port 5672 which is AMQP's default port.
</ol>

Screenshot of my RabbitMQ after I ran the slower subscriber and executed the publisher 5 times. The queue reached 20 messages. This is because one single execution of publisher sends 5 messages. Because the subscriber is slow, the 20 messages from the 4 other executions have to wait in the queue to be processed by the subscriber.

![alt text](image.png)

Result after running publisher 5 times with 3 different consoles running subscriber:

Screenshot of publisher's terminal:

![alt text](image-5.png)

Screenshot of RabbitMQ. Message queue reduced more quickly because now the 25 messages being sent by the publisher are given to 3 different subscribers to be processed:

![alt text](image-1.png)

Screenshots of the 3 consoles running subscriber separately:

![alt text](image-2.png)

![alt text](image-3.png)

![alt text](image-4.png)

Improvements:
- fn get_handler_action() wasn't implemented before. It has to be implemented for the program to be able to run, but now it's unused and currently doesn't do anything, there should be a good implementation of it.
- the string used to access RabbitMQ ("amqp://guest:guest@localhost:5672") is better off being in a constant variable so that it's easy to look for and change when we want to run it on cloud instead of running it locally.