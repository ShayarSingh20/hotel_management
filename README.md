# hotel_management

A simple Hotel Management System developed using Python and MySQL.
This project allows users to manage hotel customer records through a menu-driven console application.

Features

- Add new customer records
- Search for a customer record
- Update customer details
- Delete customer records
- View all customer records
- Generate a hotel bill/report
- Store data using MySQL database
- Calculate the number of days between check-in and check-out dates

 Technologies Used

- Python 3
- MySQL
- MySQL Connector/Python

 Project Structure

Hotel-Management-System/
│
├── hotel.py
├── README.md
└── database.sql

«"database.sql" contains the SQL commands required to create the database and table.»

Database Details

The project uses a MySQL database named:

"Hotel_Management"

The main table is:

hotel

Table Fields

Field| Description
"cno"| Customer number
"cname"| Customer name
"address"| Customer address
"roomno"| Room number
"mobileno"| Customer mobile number
"check_in"| Check-in date
"check_out"| Check-out date
"adv_pay"| Advance payment
"room_type"| Type of room

 Installation

1. Install Python

Download and install Python 3 from the official Python website.

2. Install MySQL

Install MySQL Server and MySQL Workbench if required.

3. Install MySQL Connector

Open Command Prompt/Terminal and run:

pip install mysql-connector-python

4. Create the Database

Open MySQL and run:

CREATE DATABASE xiiproject;

USE Hotel_Management;

CREATE TABLE hotel (
    cno INT PRIMARY KEY,
    cname VARCHAR(50),
    address VARCHAR(100),
    roomno INT,
    mobileno BIGINT,
    check_in DATE,
    check_out DATE,
    adv_pay FLOAT,
    room_type VARCHAR(30)
);

Database Configuration

The Python program connects to MySQL using:

def connect_db():
    return mysql.connector.connect(
        host='localhost',
        user='root',
        passwd='',
        database='xiiproject'
    )

If your MySQL username, password, or database name is different, update these values in the Python file.

How to Run

Run the Python program using:

python hotel.py

The following menu will appear:

        MAIN MENU
1. Add New Record
2. Search a Record
3. Update the Record
4. Delete the Record
5. View All Records
6. Generate Report
0. Exit

Enter the number corresponding to the operation you want to perform.

Billing Calculation

The program calculates the bill based on the number of days stayed.

The current room rate used in the program is:

₹4500 per day

The program calculates:

Total = Number of Days × 4500

Tax = Total × 10%

Net Amount = Total - Advance Payment + Tax

Room Categories

The program supports three room categories:

1. Duplex
2. Semi-Duplex
3. Standard

Sample Output

        MAIN MENU
1. Add New Record
2. Search a Record
3. Update the Record
4. Delete the Record
5. View All Records
6. Generate Report
0. Exit

Enter your choice: 1

Enter number of records to add: 1
Customer number: 101
Customer name: Rahul
Address: Delhi
Room number: 205
Mobile number: 9876543210
Check-in date (YYYY-MM-DD): 2026-09-20
Check-out date (YYYY-MM-DD): 2026-09-23
Advance payment: 5000
Room category (1: duplex, 2: semi-duplex, 3: standard): 1

Purpose of the Project

This project was created as a Class 12 Computer Science/Python project to demonstrate the use of:

- Python functions
- Conditional statements
- Loops
- Exception handling
- User input
- MySQL connectivity
- SQL "INSERT", "SELECT", "UPDATE", and "DELETE"
- SQL date functions
- Database management

Future Improvements

Possible improvements include:

- Add a graphical user interface (GUI)
- Add login/authentication
- Add different prices for different room categories
- Add automatic room availability checking
- Generate printable invoices
- Improve error handling and validation
- Store database credentials securely

Author

Shayar Singh (Jasrath)

If you found this project useful, consider giving the repository a star!