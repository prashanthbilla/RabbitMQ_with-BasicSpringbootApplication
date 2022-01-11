# RabbitMQ_with-BasicSpringbootApplication
How to use RabbitMQ with Publisher and Consumer Example

Install RabbitMQ in windows :
-----------------------------
1. Download and install ERlang http://erlang.org/download/otp_win64_22.3.exe
2. Downlaod and install RabbitMQ https://github.com/rabbitmq/rabbitmq-server/releases/download/v3.8.8/rabbitmq-server-3.8.8.exe
3. Go to RabbitMQ Server install Directory C:\Program Files\RabbitMQ Server\rabbitmq_server-3.8.3\sbin
4. Run command rabbitmq-plugins enable rabbitmq_management
5. Open browser and enter http://localhost:15672/ to redirect to RabbitMQ Dashboard
6. Also we can Open it with IP Address http://127.0.0.1:15672
7. Login page default username and password is guest 
8. After successfully login you should see RabbitMQ Home page

## Working and Functionality:

  * I have created two Spring boot applications
  * One will act as a message producer and one will act as a message consumer
  * In both applications, we can configure the RocketMq Queue, Exchange and Bind these queue and exchange in MQConfig class.
  * Consumer Application consumes the messege throgh @RabbitLestener with the help of queue name
  * If Consumer Application server will down, the messages are going into the queue, we can see the messages in our RabbitMQ Dashboard and If Consumer Application server will up then consumer application will consumes the messages in the queue.
  * I will show you entire workflow of our apllication through below diagram.
   
![RabbitMQDiagram](https://user-images.githubusercontent.com/85600714/148936117-f4d8866f-e20f-419a-a6ad-4b050b55e2d2.png)
