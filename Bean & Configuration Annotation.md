`@Bean` is used when you want to make a spring bean
out of a non `@Component` class

Basically, make  an existing third-party  class available to spring framework

```
@Configuration  
public class SportConfig {  
    @Bean  
    public Coach swimCoach(){  
        return new SwimCoach();  
    }   
}
```
By default `@Bean` uses className as id

For custom ID write
```
@Configuration  
public class SportConfig {  
    @Bean("aquatic")  
    public Coach swimCoach(){  
        return new SwimCoach();  
    }   
}
```
Use this beanID in the [[Qualifier Annotation|qualifier]]
