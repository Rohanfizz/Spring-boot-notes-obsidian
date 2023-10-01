Watch section 2 video 2
It also has AutoWiring

All the steps
1. Constructor Injection- Creating the class and interface
2. Create Demo rest controller
3. Create constructor in your classes for injections
```
//define a private field for dependency  
private Coach myCoach;  
//define a constructor for dependency injection  
@Autowired  
public DemoController(Coach theCoach){  
    myCoach = theCoach;  
}
```

5. Add @GetMapping for `/dailyWorkout` 

![[Pasted image 20230921012516.png]]