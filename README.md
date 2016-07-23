cloud-native-apps
------------------

Step-by-step guide to build [12-Factor](http://12factor.net/) cloud native apps with *Spring Cloud*, *Netflix OSS*, 
*Grails* and *AngularJS*

### Features
Spring Cloud focuses on providing good out of box experience for typical use cases and extensibility mechanism to cover others.

* Distributed/versioned configuration
* Service registration and discovery
* Routing
* Service-to-service calls
* Load balancing
* Circuit Breakers
* Global locks
* Leadership election and cluster state
* Distributed messaging

### Infrastructure Services 

* **Netflix Eureka:** Service registry & discovery
* **Netflix Hystrix:** Resiliency - Circuit breaker, Fallback, Concurrency, RxJava 
* **Netflix Hystrix Dashboard:** Monitoring and metrics dashboard
* **Netflix Turbine:** Aggregate hystrix streams
* **Netflix Ribbon:** Client-side load-balancing
* **Netflix Zuul:** Reverse proxy for API gateway
* **Spring Cloud Config:** Centralized configuration
* **Spring Cloud Bus:** PubSub messaging over RabbitMQ
* **Spring Cloud Security:** SSO for APIs - OAuth/JWT  
* **Logging:** Centralized logging - Logstash, ES, Kibana (LEK)
* **Swagger:** API Docs 


![](./deckset/images/system-landscape.png)
### Application Services 

### Start on Local Machine

Starting  Order
> RabbitMQ -> Euraka -> Config -> (Producer, GORM, ...), -> (Zuul,  Turbine, Hystrix Dashboard)

Start up Eureka
```
cd eureka
spring run .
```

Start up Config server
```
cd config
spring run .
```

Start up Producer Service
```
cd producer
spring run .
```

Start up Aggregate Application
```
cd app
spring run .
```

Start up API Gateway
```
cd zuul
spring run .
```

Start up Monitoring Application
```
cd hystrix-dashboard
spring run .
```