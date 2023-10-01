Just like [[Qualifier Annotation]] this is another annotation.
to specify which class to pick.
Just add
```
@Component
@Primary
public class CricketCoach implements Coach{...}
```
On top of the class you want to give priority

Points to remember-
1. Only 1 primary class can exist
2. If you use both [[Qualifier Annotation|@Qualifier]] and Primary, Qualifier will be given higher priority.
[[Qualifier Annotation]] is recommended in general.