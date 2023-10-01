- Query language for retrieving objects
- Similar to SQL
- JPQL is based on the entity name and entity fields not on sql database table and columns
- STEPS
1. Add new method to DAO interface
```
List<Student> findAll();
```
2. Implement Method
```
@Override  
public List<Student> findAll() {  
    //Create query  
    TypedQuery<Student> theQuery = entityManager.createQuery("FROM Student order by id desc ",Student.class);  
    //Return results  
    return theQuery.getResultList();  
}
```
3. Main App
```
private void findAllStudents(StudentDAO studentDAO) {  
    // get a list of students  
    List<Student> theStudents = studentDAO.findAll();  
    // display list  of  students  
    for(Student tempStudent : theStudents){  
       System.out.println(tempStudent);  
    }
}
```

### How to make JPQL custom named parameters?
```
@Override  
public List<Student> findByLastName(String theLastName) {  
    TypedQuery<Student> theQuery = entityManager.createQuery("From Student WHERE lastName=:theData",Student.class);  
    theQuery.setParameter("theData",theLastName);  
    return theQuery.getResultList();  
}
```

Here 👆 we are querying for a student with a specific last name.