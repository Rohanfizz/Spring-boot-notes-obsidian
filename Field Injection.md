Field injection is NOT recommended by sprint.io as it makes the code harder to unit test.
It is used in legacy projects.

In this, you directly add `@Autowired` annotation on the private field

for ex-
```
public class DemoController{
	
	@Autowired             // <- Field injection
	private Coach myCoach;

	//no need for constructors or setters

	@GetMapping('/dailyWorkout')
	public String getDailyWorkout(){
		return myCoach.getDailyWorkout();
	}
}
```