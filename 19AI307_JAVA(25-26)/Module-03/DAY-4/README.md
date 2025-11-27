# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.


 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".

Input:

temperature
botType (1 for SunBot, 2 for RainBot)Output:
Prediction as a string.

For example:

<img width="452" height="147" alt="image" src="https://github.com/user-attachments/assets/8e1c447a-5ad1-4e5e-9340-7c47414c07ee" />


## AIM:
To create a common interface WeatherBot and implement different bots to predict weather based on temperature.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Create an interface WeatherBot with a method predict(int temperature).
4.	Implement SunBot that predicts "HOT" if temperature > 30, else "MODERATE".
5.	Implement RainBot that predicts "COLD" if temperature < 20, else "WARM".
6.	In the main method, read temperature and bot type from the user.
7.	Create the appropriate bot object and call predict().
8.	Display the prediction.
9.	Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: LOKESH KHANNA R
RegisterNumber:  212222040088
*/
```

## SOURCE CODE:


```
import java.util.Scanner;

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    public String predict(int temperature) {
        return temperature > 30 ? "HOT" : "MODERATE";
    }
}

class RainBot implements WeatherBot {
    public String predict(int temperature) {
        return temperature < 20 ? "COLD" : "WARM";
    }
}

public class WeatherPrediction {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int temperature = scanner.nextInt();
        int botType = scanner.nextInt();
        WeatherBot bot;

        if (botType == 1) {
            bot = new SunBot();
        } else if (botType == 2) {
            bot = new RainBot();
        } else {
            System.out.println("Invalid bot type.");
            scanner.close();
            return;
        }

        System.out.println(bot.predict(temperature));
        scanner.close();
    }
}


```

## OUTPUT:

<img width="528" height="197" alt="image" src="https://github.com/user-attachments/assets/e4a4b457-2947-422d-826f-5068de6b4e34" />


## RESULT:
The program successfully predicts the weather based on the bot type and input temperature.

