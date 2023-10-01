There are 2 options
1. Using `java -jar` and then the jar file name
	1. Open Git bash in the pom.xml folder
	2.  Run `./mvnw package`
	3. Change directory to /target as it contains the .jar file
	4. Get the name of the .jar file by `ls *.jar` 
	5. Run the jar file `java -jar fileName.jar` 
2. Using Spring Boot Maven Plugin
	1. Just run `./mvnw spring-boot:run` in the pom.xml directory


