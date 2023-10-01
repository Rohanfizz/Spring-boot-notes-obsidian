- Default scope of a bean is singleton
	- Creates single instance of a bean
- Prototype Scope
	- A new object instance for each injection
```
@Scope(ConfigurableBeanFactory.SCOPE_PROTOTYPE)  
public class CricketCoach implements Coach{
```

![[Pasted image 20230923015934.png]]
#### Prototype Beans and Destroy Lifecycle
**For "prototype" scoped beans, Spring does not call the destroy method. Gasp!**
