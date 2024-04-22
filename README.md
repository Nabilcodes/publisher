a. How many data your publisher program will send to the message broker in one
run? 

The data that will sent to the message broker can be found listed on the main 
function. It sent to the the publisher some event with the corresponding ID from
1 to 5. Therefore there are 5 message to be sent to the message broker.

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber
program, what does it mean?

The url denotes similar thing, which is to specify the message queueing service 
resource and how to access it (with what username, password, and port). Whats different
was the role, in which in this case, the program was publishing messages to the service,
and the other was receiving message from the service. Same url means they were 
communicating with the same service, and the service was accessed by the same user.

Screenshot of accessing local rabbitmq service

![image](https://github.com/Nabilcodes/publisher/assets/71275597/a04ee0cd-a788-4403-a269-3f8c6566d5d6)

Screenshot of two console, the left was from the publisher program, and the right is from
the subscriber program, sending messages from the former to the latter by using rabbitmq
as intermediaries.

![image](https://github.com/Nabilcodes/publisher/assets/71275597/6bbe98dc-1c79-4cb4-95c1-f968f90deb03)

Screenshot of rabbitmq web app interface and the publisher program console on it's right. Notice that
the chart titled message rate describe the amount of message sent per second on any particular time
(shown in the horizontal axis, 15:41:40 for example). The line colored in yellow show the movement of 
the message rate through time. When the publisher sent message in more frequency, the graph spiked up,
and conversely when the publisher sent less message, the graph goes down, making a triangle-like figure.
The line colored in purple shows the rate of consumer acknowledgement, which is a sign for the message 
queue from the consumer that the message was processed successfully. 

The difference of the two graph created by the two line show the different behavior resulted from 
different rate of publisher sending messages and the capability of the consumer processing it. When 
the message published was more intense and irregular, the resulting consumer acknowledgment doesn't 
follows the corresponding publisher graph, depicting its limited processing capacity. But when the 
messages were a lot less intense, the graph of the consumer seemed to follow the shape of the publisher 
messages sent, as we can see on the right part of the chart.

![image](https://github.com/Nabilcodes/publisher/assets/71275597/d7d639b7-4e14-4719-b101-0f932bedb1bb)


