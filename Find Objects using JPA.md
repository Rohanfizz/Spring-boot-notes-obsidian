Steps
1. Add new method to DAO interface
```
Student findById(Integer id);
```

1. Add new method to DAO implementation
```
@Override  
public Student findById(Integer id) {  
    return entityManager.find(Student.class,id);  
}
```

1. Update main app
```
private void readStudent(StudentDAO studentDAO) {  
    //create a student object  
    Student newStudent = new Student("Ashutosh","Negi","ashutoshnegi195@gmail.com");  
    //save the student  
    studentDAO.save(newStudent);  
    //display the id of saved student  
    int currId = newStudent.getId();  
    System.out.println(currId);  
    //retrieve student based on id: primary key  
    System.out.println(studentDAO.findById(currId));  
}
```