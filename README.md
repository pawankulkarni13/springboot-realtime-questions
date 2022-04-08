# springboot-realtime-questions
- how would you test a private method using Junit ?
> Generally a unit test is intended to exercise the public interface of a class or unit. Therefore, private methods are implementation detail that you would not expect to test explicitly. In the Spring Framework you can test private methods using this method:
ReflectionTestUtils.invokeMethod(). 
1.Don't test private methods.
2.Give the methods package access.
3.Use a nested test class.
4.Use reflection.

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

- Different ways to run method after startup in spring boot ?
> 
  1. Using CommandLineRunner interface
  2. With ApplicationRunner interface
  3. Spring boot Application events
  4. @Postconstruct annotation on a method
  5. The InitializingBean Interface
  6. Init attribute of @bean annotation

- Difference Between OpenFeign vs FeignClient ?
> Feign makes writing web service clients easier by providing annotation support that allows us to implement our clients with just interfaces.
> Spring Cloud OpenFeign integrates the predecessor project into the Spring Cloud ecosystem.

- How do you trace a API call which internally makes multiple API calls. ?
> Can use Spring Cloud Sleuth tracing with unique id and span ids for individual/multiple API calls.

- Can we have private methods with @Async implementations ?
> No, Methods annotated with '@Async' must be overridable.

- Difference between JPA vs Hibernate.
> The major difference between Hibernate and JPA is that Hibernate is a framework while JPA is API specifications. Hibernate is the implementation of all the JPA guidelines.

- 

- Given millions of records of a custom object/Person/Employee. Consider the  
- Spring Boot Github
- https://github.com/orgs/spring-projects/repositories?type=all
