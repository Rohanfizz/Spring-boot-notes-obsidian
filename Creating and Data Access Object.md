Acts as an interface between CRUD app and DB

Important methods
- Save()
- findById()
- findAll()
- findByLastName()
- update()
- delete()
- deleteAll()

DAO needs JPA  Entity Manager,
JPA Entity Manager needs Data source (Both created by Spring boot based on maven.pom file and application.properties file)

DAO <-> Entity Manager <-> Data Source <-> DB

STEPS
1. Define DAO Interface

```
public interface StudentDAO {  
    void save(Student theStudent);  
}
```

2. Define DAOImplementation class as @Repository

```
  
@Repository  
public class StudentDAOImpl implements StudentDAO{  
  
    // define  field for  entity manager  
    private EntityManager entityManager;  
    //inject entity manager  
    @Autowired  
    public StudentDAOImpl(EntityManager entityManager){  
        this.entityManager = entityManager;  
    }  
    //implement save method  
    @Override  
    @Transactional //since we are performing  an update in DB  
    public void save(Student theStudent) {  
        //this will save student to DB  
        entityManager.persist(theStudent);  
    }  
}
```

3. Inject studentDAO in the Command line runner
	1. Pass studentDAO object in the arguments
	2. call `createStudentDAO(studentDAO)` in the runner lambda function
	3. Use IDE to create `createStudentDAO()` method
		1. create the student object
		2. save the student object
		3. display id of created student object 
```
	private void createStudent(StudentDAO studentDAO) {  
    // create the student object  
    System.out.println("Creating student object");  
    Student tempStudent = new Student("Paule","Doe","a@b.com");  
  
    //save the student object  
    System.out.println("Savint the student...");  
    studentDAO.save(tempStudent);  
  
    //display id of the saved student  
    System.out.println("Saved student's id is: "+tempStudent.getId());  
}
```