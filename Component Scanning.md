- By default spring will only scan the packages inside the application pacakge
- if you want to place some packages outside, you can do it by
```
//Explicitly list base packages to scan  
@SpringBootApplication(  
       scanBasePackages = {"com.luv2code.springcoredemo","com.luv2code.util"}  
)
```
In the Application.java