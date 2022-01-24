# springboot-realtime-questions

- If you need to parallely process multiple messages in RMQ using springboot, how do you achieve it ?
> Minimum number of listener invoker threads
> spring.rabbitmq.listener.simple.concurrency=5

- Spring boot application has multiple instances but only one instance should consume messages from RabbitMQ.
> RabbitMQ has a feature called - Single Active Consumer. Single active consumer allows to have only one consumer at a time consuming from a queue and to fail over to another registered consumer in case the active one is cancelled or dies.

- How do you run same instance of springboot application in local machine ?
> Change port of one SprintBoot App instance using server.port and run both.

- How do you create a specific bean if the Spring Context doesn't load them while starting up ? Note :You cannot use ApplicationContext to check specific bean
> We can use @ConditionalOnMissingBean. Similar to this we have @ConditionalOnMissingClass, @ConditionalOnClass and @Conditional annotations which help in check based on some condition/beans.

- What is difference between EnableDiscoveryClient and EnableEurekaClient ?

>There are multiple implementations of "Discovery Service" (eureka, consul, zookeeper). @EnableDiscoveryClient lives in spring-cloud-commons and picks the implementation on the classpath. @EnableEurekaClient lives in spring-cloud-netflix and only works for eureka. If eureka is on your classpath, they are effectively the same.

-

- Spring Boot Github
- https://github.com/orgs/spring-projects/repositories?type=all
