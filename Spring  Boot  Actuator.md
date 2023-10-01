- Used  to  monitor the health and  metrics of the  application
- How to use? Just add dependency to POM file
```
<dependency>  
    <groupId>org.springframework.boot</groupId>  
    <artifactId>spring-boot-starter-actuator</artifactId>  
</dependency>
```

- `/actuator/health` - Health information about application
- `/actuator/info` - Some preset  information like
	- ```info.app.name = My First Spring App  
		info.app.description = A crazy App!  
		info.app.version = 1.0.0```
- To expose all endpoints - `management.endpoints.web.exposure.include=*`
- What about [[Application Properties file|Security]]?
	- Add `spring-boot-starter-security` dependency!