# CAR PARKING PROJECT 🎗️

Parking System – Java Console Application

This is a simple Parking Management System built using Java.
It allows users to:

- Park a car
- Remove a parked car
- View the list of currently parked cars
- Track available vs total parking slots

The project runs completely on the console using Java’s "Scanner" for user input.

---

📌 Features

1. Park a Car

- User enters a license plate number.
- Program checks if any slots are available.
- Car is added to the parked list.

2. Remove a Car

- User enters the license plate of the car they want to remove.
- The program verifies if the car exists in the parking lot.

3. View Parked Cars

- Displays all currently parked cars.

4. Exit

- Stops the application.

---

🛠️ Technologies Used

- Java
- ArrayList for storing parked cars
- Switch-case for menu navigation
- Scanner for user input

---

📂 How to Run the Program

1. Install JDK (Java Development Kit).
2. Save the file as "ParkingSystem.java".
3. Compile the program:
javac ParkingSystem.java
4. Run the program:
java ParkingSystem

---

📜 Code Preview

import java.util.ArrayList;
import java.util.Scanner;
public class ParkingSystem {

    static int totalSlots, availableSlots;
    static ArrayList<String> parkedCars = new ArrayList<String>();

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the total number of parking slots:");
        totalSlots = sc.nextInt();
        availableSlots = totalSlots;

        while (true) {
            System.out.println("\nWhat would you like to do?");
            System.out.println("1. Park a car");
            System.out.println("2. Remove a car");
            System.out.println("3. View parked cars");
            System.out.println("4. Exit");
            int choice = sc.nextInt();

            switch (choice) {
                case 1:
                    parkCar();
                    break;
                case 2:
                    removeCar();
                    break;
                case 3:
                    viewParkedCars();
                    break;
                case 4:
                    System.exit(0);
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        }
    }

    public static void parkCar() {
        if (availableSlots == 0) {
            System.out.println("Sorry, there are no available parking slots.");
            return;
        }

        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the license plate number of the car:");
        String licensePlate = sc.nextLine();
        parkedCars.add(licensePlate);
        availableSlots--;
        System.out.println("Car parked successfully. Available slots: " + availableSlots);
    }

    public static void removeCar() {
        if (availableSlots == totalSlots) {
            System.out.println("There are no parked cars.");
            return;
        }

        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the license plate number of the car to be removed:");
        String licensePlate = sc.nextLine();
        if (parkedCars.contains(licensePlate)) {
            parkedCars.remove(licensePlate);
            availableSlots++;
            System.out.println("Car removed successfully. Available slots: " + availableSlots);
        } else {
            System.out.println("The car is not parked here.");
        }
    }

    public static void viewParkedCars() {
        if (availableSlots == totalSlots) {
            System.out.println("There are no parked cars.");
            return;
        }

        System.out.println("Parked cars:");
        for (String licensePlate : parkedCars) {
            System.out.println(licensePlate);
        }
    }
}


---

✅ Future Enhancements (Optional)

- Store data in a file
- Add timestamps for parked cars
- Add slot numbers
- Create a GUI version

---

📄 License

This project is free to use and modify.

---

Feel free to contribute or raise issues!




