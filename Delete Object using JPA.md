1. Create method in DAO implementation

`void delete(Integer id);`

2. Implement the method in the class

```
@Override  
@Transactional  
public void delete(Integer id) {  
    Student myStudent = entityManager.find(Student.class,id);  
    entityManager.remove(myStudent);  
}
```

3. Update the main app

```
private void deleteStudentById(StudentDAO studentDAO) {  
    //delete student of id 3  
    int studentId  = 3;  
    System.out.println("Deleting student with id: " + studentId);  
    studentDAO.delete(studentId);  
}
```

****
### Delete all the rows
1. Add method in DAO interface
`int deleteAll();`
2. Implement method in DAOImpl
```
@Override  
@Transactional  
public int deleteAll() {  
    int numRows = entityManager.createQuery("DELETE FROM Student").executeUpdate();  
    return numRows;  
}
```
3. Update the main App
```
private void deleteAllStudents(StudentDAO studentDAO) {  
    int numRows  = studentDAO.deleteAll();  
    System.out.println(numRows +" rows affected.");  
}
```
