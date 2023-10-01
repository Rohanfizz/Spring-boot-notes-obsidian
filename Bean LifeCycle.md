![[Pasted image 20230923021641.png]] 

@PostConstruct & @PreDestroy example for a class default (singleton) scope class
```
//define our init method  
@PostConstruct  
public void doMyStartupStuff(){  
    System.out.println("We are in doStartupStuff for "+this.getClass().getSimpleName());  
}  

//define our destroy method  
@PreDestroy  
public void doMyCleanupStuff(){  
    System.out.println("We are in doMyCleanupStuff for "+this.getClass().getSimpleName());  
}
```
#### Prototype Beans and Destroy Lifecycle
**For "prototype" scoped beans, Spring does not call the destroy method. Gasp!**