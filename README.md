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