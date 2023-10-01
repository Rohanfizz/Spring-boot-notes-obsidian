- A project management tool for application
- When building project, you may need .jar files,
- Maven downloads and  installs the .jar files etc instead of downloading manually.  

1. POM.xml
	1. Project Object Model File
	2. This is basically the "shopping list" for .jar files
	3. It has Following components
		1. Project Meta Data
		2. Dependencies
			1. Every dependency has a GAV, GroupID ArtifactID and Version which are dependency coordinates, used to uniquely identify the dependency.
			2. You can go to http://search.maven.org for getting GAVs for different dependencies.
		3. Plugins  