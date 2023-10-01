- Created  by Spring Initializr
- I think its like .env file
- Initially its empty

Use these like
```
@Value("${name}")
@RestController  
public class FunRestController {  
    
    @Value("${team.name}")  
    private String name;  
  
    @GetMapping("/")  
    public String sayHello(){  
  
  
        return "Hello World" + name;  
    }  
  
}
```

[All Properties](https://docs.spring.io/spring-boot/docs/current/reference/html/application-properties.html#appendix.application-properties)

Some of the Spring Boot properties
1. Core properties
	1. `logging.file.name=my-craze-stuff.log` To send logs to a file
2. Web
	1. `server.port=7070`
	2. `server.servlet.context-path=/my-path` This will set the path to the endpoints as localhost/8080/my-path/all-endpoints
	3. Default http session timeout `server.servlet.session.timeout=15m`
3. [[Spring  Boot  Actuator|Actuator]]
	1. `management.endpoints.web.exposure.include=*`
	2. `management.endpoints.web.exposure.exclude=beans,mapping`
	3. `management.endpoints.web.base-path=/actuator`
4. Security
	1. `spring.security.user.name=admin`
	2. `spring.security.user.password=topsecret`
5. Data 
	1. JDBC URL `spring.datasource.url=jdbc:mysql://link`
	2. `spring.datasource.username=scott`
	3. `spring.datasource.password=tiger` 
6. [[Lazy Initialization]]
		1. `spring.main.lazy-initialization=true`
7. Logging sql statements
	1. `logging.level.org.hibernate.SQL=debug`
	2. `logging.level.org.hibernate.orm.jdbc.bind=trace`
8. [[Creating Tables]]