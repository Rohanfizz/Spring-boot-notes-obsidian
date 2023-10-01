Set up the project  on spring initializr
1. Go to start.sprint.io
2. Add dependencies
	1. mysql-connector-j (JDBC Driver)
	2. spring-boot-starter-data-jpa (ORM)
3. Add a CommandLineRunner in Application file
```
//Executed after all spring beans have been loaded @Bean  
public CommandLineRunner commandLineRunner(String[] args){  
      
    return runner ->{  
       System.out.println("Hello World");  
    }  
}
```
4. DB connection from [[Application Properties file]]
```
spring.datasource.url=jdbc:mysql://localhost:3306/student_tracker  
spring.datasource.username=springstudent  
spring.datasource.password=springstudent
```