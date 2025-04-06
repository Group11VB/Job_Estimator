# Job_Estimator
📄 Project Documentation: Job Estimator (VB.NET)
📘 1. Project Overview
The Job Estimator is a desktop application developed in VB.NET using Windows Forms. It allows businesses or freelancers to quickly calculate and generate estimates for various jobs or services. It streamlines the quotation process and ensures pricing consistency.
________________________________________
🧩 2. Objectives
•	Automate job cost estimation.
•	Save customer data and estimate history.
•	Provide printable and exportable estimates.
•	Reduce manual errors in calculations.
________________________________________
🛠️ 3. Technologies Used
Component	Technology
Programming Language	VB.NET
IDE	Microsoft Visual Studio
UI Framework	Windows Forms (.NET)
Database	Microsoft SQL Server 
________________________________________
🧱 4. System Modules
A. Login Module
•	Secure login for admin
B. Customer Management
•	Add, update, or delete customer records.
C. Job Entry Module
•	    First Name 
•	    Surname 
•	    Date 
•	    Address
•	    Phone 
 Email
•	 Copper Pipes 
•	  Chrome Pipe 
•	 Plastic Pipe 
•	 Labour 
•	 Travel 
•	 Username 
•	Password 
•	Rate per hour or material cost configurations.
D. Estimator Logic
•	Calculates total cost:
Total Cost = (Labor Hours × Hourly Rate) + Material Costs + Miscellaneous
•	Adds taxes and discounts based on user input.
•	Auto-generates reference number for tracking.
E. Estimate Output
•	Displays a summary of job estimate.
•	Option to:
o	Save
F. Settings/Configuration
•	Hourly rate settings.
•	Tax/Discount configurations.
•	Company branding for reports.
________________________________________
📊 5. Database Schema (Simplified)
Database:
CREATE DATABASE Estimator 
Tables:
CREATE TABLE Job (
    Job_ID INT IDENTITY(1,1) PRIMARY KEY,
    Firstname VARCHAR(50) NOT NULL,
    Surname VARCHAR(50) NOT NULL,
    DOB DATE NOT NULL,
    Address TEXT NOT NULL,
    Phone VARCHAR(15) NOT NULL,
    Email VARCHAR(100) NOT NULL,
    Discount DECIMAL(10,2) DEFAULT 0.00,
    Tax DECIMAL(10,2) DEFAULT 0.00,
    SubTotal DECIMAL(10,2) DEFAULT 0.00,
    Total DECIMAL(10,2) DEFAULT 0.00,
    Coppies_Pipes INT DEFAULT 0,
    Chrome_Pipe INT DEFAULT 0,
    Plastic_Pipe INT DEFAULT 0,
    Labour DECIMAL(10,2) DEFAULT 0.00,
    Travel DECIMAL(10,2) DEFAULT 0.00,
    Receipt VARCHAR(50) NULL
);
GO
CREATE TABLE Login (
    Username VARCHAR(50) PRIMARY KEY,
    Password VARCHAR(255) NOT NULL
);
GO
📸 6. Sample Screenshots
Login Screen
![image](https://github.com/user-attachments/assets/31eeae25-5ba2-4e73-994c-e172219b73a6)

•	Add New Estimate 
![image](https://github.com/user-attachments/assets/55804391-f9bb-423d-a153-f5affa766e18)

•	Estimate Report Preview
 ![image](https://github.com/user-attachments/assets/49fb345e-a6d8-4bd6-a92d-a6678682a497)

________________________________________
✅ 7. Testing and Validation
•	Unit tested calculator logic.
•	Manual UI testing for workflows.
•	Sample test cases for cost computation with edge cases (e.g., zero values, extreme numbers).
________________________________________
👨‍💼 8. Conclusion
The Job Estimator in VB.NET simplifies the process of estimating job costs for small businesses and freelancers. With an intuitive interface, quick calculations, and professional report outputs, the application enhances productivity and professionalism in service delivery.
Appendix
Source Code: 

Tools Used: Microsoft Visual Studio, SQL Server Management Studio

