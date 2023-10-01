Spring will not initialize the beans on the startup itself, rather it will
initialize a bean on demand.

This improves startup time.

2 Methods,
1. Explicitly on a @Component by using [[Lazy Annotation]] 
2. Globally by using [[Application Properties file]] 
	1. `spring.main.lazy-initialization=true`