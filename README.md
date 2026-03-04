# 🚕 Call Taxi Booking System

A Java console-based taxi booking application that simulates how taxis are 
allocated to customers based on availability, distance, and total earnings.

The system automatically assigns the most suitable taxi using predefined 
allocation rules and maintains booking history for each taxi.

This project demonstrates Object-Oriented Programming (OOP), modular package
design, and basic system design concepts.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📌 PROJECT OVERVIEW
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

The Call Taxi Booking System allows customers to book taxis between 
predefined locations arranged linearly.

Locations available in the system:

A → B → C → D → E → F

The application performs the following tasks:

• Accept taxi booking requests
• Allocate taxis based on availability and proximity
• Calculate fare according to travel distance
• Maintain booking history
• Track total earnings of each taxi

The system simulates how real taxi services efficiently allocate resources.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⚙️ TECH STACK
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

• Java
• Object-Oriented Programming (OOP)
• Java Collections Framework (ArrayList)
• Console-based User Interface
• Package-based Project Architecture


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🏗 PROJECT ARCHITECTURE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

The project follows a layered architecture:

Main → Service → Model → Utility


Main Layer
Handles user interaction and menu options.

Service Layer
Contains taxi allocation logic and booking operations.

Model Layer
Defines data objects such as Taxi and Booking.

Utility Layer
Provides helper functions such as fare and distance calculation.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📂 PACKAGE STRUCTURE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TaxiBooking
│
└── src
    │
    ├── com.taxibooking.main
    │       Main.java
    │
    ├── com.taxibooking.model
    │       Taxi.java
    │       Booking.java
    │
    ├── com.taxibooking.service
    │       TaxiService.java
    │
    └── com.taxibooking.util
            TaxiUtils.java


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📊 SYSTEM ASSUMPTIONS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Number of taxis          : 4 (scalable)
Available locations      : A, B, C, D, E, F
Distance between points  : 15 km
Travel time per segment  : 1 hour
Initial taxi position    : A


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🚖 TAXI ALLOCATION RULES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. If a taxi is available at the pickup location at the requested time,
   it will be allocated immediately.

2. If no taxi is available at the pickup location, the nearest available
   taxi will be allocated.

3. If multiple taxis are equally near, the taxi with the lowest total
   earnings will be selected.

4. Taxis charge fare only for the distance from pickup to drop location.

5. If no taxi is available, the booking request will be rejected.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
💰 FARE CALCULATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Minimum charge for first 5 km  : ₹100
After first 5 km               : ₹10 per km

Distance between route points  : 15 km


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
✨ FEATURES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✔ Automatic taxi allocation
✔ Distance-based fare calculation
✔ Taxi earnings tracking
✔ Booking history display
✔ Clean modular package structure
✔ Object-Oriented implementation


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📌 EXAMPLE WORKFLOW
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Customer Input
--------------
Customer ID  : 1
Pickup Point : A
Drop Point   : B
Pickup Time  : 9


System Output
-------------
Taxi-1 is allotted.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📄 DISPLAY TAXI DETAILS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Taxi-1 Total Earnings: Rs.200

BookingID  CustomerID  From  To  PickupTime  DropTime  Amount
1          1           A     B   9           10        200


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
▶️ HOW TO RUN THE PROJECT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Compile the program:

javac Main.java


Run the program:

java Main


Or run directly from IDE:

Right Click → Main.java → Run As → Java Application


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🚀 FUTURE IMPROVEMENTS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

• Add Graphical User Interface using Java Swing / JavaFX
• Store booking data in MySQL database
• Implement real-time taxi tracking
• Convert the application into a Spring Boot REST API
• Develop a web or mobile booking interface


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
👨‍💻 AUTHOR
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Developed as a Java practice project to demonstrate
Object-Oriented Programming and system design concepts.
