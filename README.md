# CAR PARKING

# project 

# new 

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

static int totalSlots, availableSlots;
static ArrayList<String> parkedCars = new ArrayList<String>();

(Complete code is available in the Java file.)

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
