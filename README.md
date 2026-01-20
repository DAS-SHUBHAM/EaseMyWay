# Pystay-EaseMyWay
✈️ Flight Booking System (Python + Tkinter + MySQL)

This is a desktop-based Flight Booking System developed using Python, Tkinter for the GUI, and MySQL for database management. The project provides user authentication (Sign Up & Login) and serves as a foundation for a complete flight reservation system.

📋 Prerequisites

Before setting up the project, ensure the following are installed on your system:

1️⃣ Software Requirements
Python 3.8 or higher
MySQL Server 8.0+
pip (Python package manager)
2️⃣ Python Libraries
Install the required Python packages using pip:
pip install mysql-connector-python
Tkinter comes pre-installed with Python. No separate installation is required.

📁 Project Structure
Flight-Booking-System/
│
├── SourceCode/
│   ├── index.py
│   ├── login.py
│   ├── SignUp.py
│   ├── homePage.py
│   ├── indexBg.png
│   ├── loginBg.png
│   ├── openeye.png
│   ├── closeye.png
│
├── README.md


⚠️ Important: Do not rename image files unless you update their paths in the code.

🛠️ Database Setup (MySQL)
Step 1: Start MySQL Server
Ensure that your MySQL server is running.
Step 2: Create Database
Login to MySQL and run:
CREATE DATABASE userdata;
Step 3: Use Database
USE userdata;
Step 4: Create Table
CREATE TABLE data (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(100) UNIQUE NOT NULL,
    password VARCHAR(100) NOT NULL
);

🔑 Database Configuration
Update the MySQL credentials in the Python files (login.py, SignUp.py) if required:
mysql.connector.connect(
    host="localhost",
    user="root",
    password="root",
    database="userdata"
)


Make sure the username and password match your MySQL configuration.
▶️ How to Run the Project
1️⃣ Navigate to the project directory:
cd Flight-Booking-System/SourceCode

2️⃣ Run the main file:
python index.py

3️⃣ Click JOIN NOW to navigate to the Sign Up / Login page.
🖼️ Image Path Configuration (Important)

The project uses absolute image paths.
If you clone this repository, update image paths in the code:
PhotoImage(file="D:\\Flight-Booking-System-Using-Python-and-MySQL\\SourceCode\\indexBg.png")
✅ Recommended (Better)
Use relative paths:
PhotoImage(file="SourceCode/indexBg.png")

⚠️ Common Issues & Solutions
❌ MySQL Connection Error
Ensure MySQL server is running
Verify username & password
Check if database userdata exists

❌ Images Not Displaying
Verify image paths
Ensure images are in the correct folder
Keep PhotoImage variables global

❌ Login Always Fails
Ensure user exists in the database
Check column names (username, password)
Confirm correct database is selected

🔐 Security Note
Passwords are currently stored in plain text.
For production use, it is highly recommended to implement password hashing (e.g., bcrypt or hashlib).

🚀 Future Enhancements
Password hashing & encryption
Flight search and booking modules
Admin dashboard
Improved UI/UX
Input validation & error handling

👨‍💻 Author
Shubham Das
