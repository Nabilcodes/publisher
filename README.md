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