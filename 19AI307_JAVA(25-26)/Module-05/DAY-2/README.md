# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList) into a file.

## AIM:
To write a Java program to serialize a collection of objects (like ArrayList) into a file.

## ALGORITHM :
1.Start the program.
2.Import the necessary package 'java.util'
3.Read the number of students and collect each student’s id, name, and marks into a list.
4.Serialize (save) the list of Student objects into a file using ObjectOutputStream.
5.Deserialize (load) the list back from the file using ObjectInputStream.
6.Display each deserialized Student’s details on the screen.
7.End the program after closing all input resources.




## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: LOKESH KHANNA R
RegisterNumber:  212222040088
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); // consume newline

        
        for(int i=0;i<n;i++)
        {
            int id=scanner.nextInt();
            String name=scanner.next();
            double marks=scanner.nextDouble();
            
            students.add(new Student(id,name,marks));
        }
        
        String filename="students.dat";
        serializeStudents(students,filename);
        List<Student> deserializedStudents=deserializeStudents(filename);
        
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}
```





## OUTPUT:
<img width="1244" height="760" alt="image" src="https://github.com/user-attachments/assets/337d9b8e-3531-443d-9bce-db103fe055fe" />



## RESULT:
The program has been executed successfully and the desired output has been obtained.

