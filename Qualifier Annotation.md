If you have multiple implementations of the same interface,
Spring boot will get confused in selecting any one of them.
One method is to give a qualifier

In the below example
1. TrackCoach is the qualifier using @Qualifier annotation
```
public DemoController(@Qualifier("trackCoach")Coach theCoach){//you can give it any method name  
    myCoach = theCoach;  
}
```

Qualifier has higher priority than [[Primary Annotation]] 
This is recommended in general.