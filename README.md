# springboot-realtime-questions

- If you need to parallely process multiple messages in RMQ using springboot, how do you achieve it ?
> # Minimum number of listener invoker threads
> spring.rabbitmq.listener.simple.concurrency=5

- Spring boot application has multiple instances but only one instance should consume messages from RabbitMQ.
> RabbitMQ has a feature called - Single Active Consumer. Single active consumer allows to have only one consumer at a time consuming from a queue and to fail over to another registered consumer in case the active one is cancelled or dies.

- 
