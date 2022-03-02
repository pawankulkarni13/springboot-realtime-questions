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

- What are Sterotype annotations ?
> Spring Annotations are a form of metadata that provides data about a program. Annotations are used to provide supplemental information about a program. It does not have a direct effect on the operation of the code they annotate. It does not change the action of the compiled program. @Component annotation is the main Stereotype Annotation. @Repository, @Service, and @Controller are specializations of @Component

- What are different annotations used in Spring Framework ?
> 6 Types of Spring Framework Annotations
1. Spring Core Annotations
2-Categories - DI-Related Annotation and Context Configuration Annotations
DI-Related Annotation
@Autowired
@Qualifier
@Primary
@Bean
@Lazy
@Required
@Value
@Scope
@Lookup
Context Configuration Annotations
@Profile
@Import
@ImportResource
@PropertySource

2. Spring Web Annotations
@RequestMapping
@RequestBody
@PathVariable
@RequestParam
Response Handling Annotations
  @ResponseBody
  @ExceptionHandler
  @ResponseStatus
@Controller
@RestController
@ModelAttribute
@CrossOrigin

3. Spring Boot Annotations
@SpringBootApplication
@EnableAutoConfiguration
Auto-Configuration Conditions
  @ConditionalOnClass, and @ConditionalOnMissingClass
  @ConditionalOnBean, and @ConditionalOnMissingBean
  @ConditionalOnProperty
  @ConditionalOnResource
  @ConditionalOnWebApplication and @ConditionalOnNotWebApplication
  @ConditionalExpression
  @Conditional

4. Spring Scheduling Annotations
@EnableAsync
@EnableScheduling
@Async
@Scheduled
@Schedules

5. Spring Data Annotations
Common Spring Data Annotations
  @Transactional
  @NoRepositoryBean
  @Param
  @Id
  @Transient
  @CreatedBy, @LastModifiedBy, @CreatedDate, @LastModifiedDate
Spring Data JPA Annotations
  @Query
  @Procedure
  @Lock
  @Modifying
  @EnableJpaRepositories
Spring Data Mongo Annotations
  @Document
  @Field
  @Query
  @EnableMongoRepositories

6. Spring Bean Annotations
@ComponentScan
@Configuration
Stereotype Annotations
  @Component
  @Service
  @Repository
  @Controller

- Spring Boot Github
- https://github.com/orgs/spring-projects/repositories?type=all
