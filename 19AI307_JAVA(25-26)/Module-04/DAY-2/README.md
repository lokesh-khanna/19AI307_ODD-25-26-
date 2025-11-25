# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.

The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.

Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.

Hidden Clue:
Use Singleton to manage shared access.

Count and log each print job submission.

Validate that state is preserved across all accesses.

Input Format:
First line: Integer n – number of print jobs

Next n lines: Each line contains the department name submitting the print job.

Output Format:
For each job, print:


[Department] submitted a print job. Total Jobs in Queue: [count]

## AIM:
To simulate a shared print spooler using the Singleton pattern so all print jobs go through one global manager that maintains a single job count

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Implement a Singleton class with a private constructor and a static getInstance() method.

4. Maintain a single jobCount variable in the Singleton.

5. Read number of print jobs.

6. For each job, get the same Singleton instance and submit the job.

7. Print the department name and updated job count.




## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: NIXAN DASS A
RegisterNumber:  212222040109
*/
```

## SOURCE CODE:

```
import java.util.*;

class PrintSpoolerManager {
    private static PrintSpoolerManager instance;
    private int jobCount = 0;

    private PrintSpoolerManager() {}

    public static PrintSpoolerManager getInstance() {
        if (instance == null) {
            instance = new PrintSpoolerManager();
        }
        return instance;
    }

    public int submitJob(String department) {
        jobCount++;
        return jobCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String dept = sc.nextLine();
            PrintSpoolerManager spooler = PrintSpoolerManager.getInstance();
            int total = spooler.submitJob(dept);
            System.out.println(dept + " submitted a print job. Total Jobs in Queue: " + total);
        }
    }
}
```





## OUTPUT:

<img width="1203" height="447" alt="image" src="https://github.com/user-attachments/assets/7b241ff4-9970-40b7-9571-d7e89a818ca6" />


## RESULT:

The singleton ensures all departments share one spooler manager and the job count increases globally for every submission.
