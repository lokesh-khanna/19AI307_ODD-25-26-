# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.

## AIM:
To write character data into a file using the FileWriter class in Java.

## ALGORITHM :
1.Import java.io.FileWriter and java.io.IOException.
2.Take user input using Scanner.
3.Create a FileWriter object with the desired file name.
4.Use write() method to write text into the file.
5.Close the FileWriter and handle exceptions using try-catch.




## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: LOKESH KHANNA R
RegisterNumber:212222040088
*/
```

## SOURCE CODE:
```
import java.io.*;

public class FileWriteExample {
    public static void main(String[] args) {
        try {
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            String filename = br.readLine();
            String content = br.readLine();

            FileWriter fw = new FileWriter(filename);
            fw.write(content);
            fw.close();

            System.out.println("File written successfully.");
        } catch (IOException e) {
            System.out.println("An error occurred.");
        }
    }
}
```






## OUTPUT:

<img width="1239" height="395" alt="image" src="https://github.com/user-attachments/assets/4727331b-2892-48f5-a880-f08e71aa5c70" />


## RESULT:

The program successfully writes the entered text into output.txt using FileWriter.

