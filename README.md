# Hospital Management System
A full-stack web application designed to streamline hospital administrative and clinical operations. This project showcases expertise in building scalable, responsive web applications using ASP.NET Core Blazor, C#, Microsoft SQL Server, HTML/CSS, and JavaScript.

## Documentation

### Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Architecture](#architecture)
4. [Technologies Used](#technologies-used)
5. [Installation Guide](#installation-guide)
6. [Usage Instructions](#usage-instructions)
7. [Screenshots](#screenshots)
8. [Contributing](#contributing)
9. [License](#license)

---

## Introduction

The **Hospital Management System** is a comprehensive web application designed to manage the administrative and clinical aspects of a hospital. It aims to streamline processes like patient registration, appointment scheduling, medical records management, billing, and more. This system enhances efficiency, reduces paperwork, and improves patient care by providing quick access to critical information.

---

## Features

- **Patient Management**
  - Register new patients
  - Update patient information
  - View patient medical history

- **Doctor Management**
  - Add and manage doctor profiles
  - Schedule doctor appointments
  - Assign doctors to patients

- **Appointment Scheduling**
  - Book appointments for patients
  - View and manage appointment calendar
  - Send appointment reminders via email/SMS

- **Medical Records Management**
  - Electronic Health Records (EHR)
  - Secure storage of patient data
  - Access control for sensitive information

- **Billing and Invoicing**
  - Generate bills for services rendered
  - Process payments
  - Insurance claim management

- **Staff Management**
  - Manage hospital staff details
  - Assign roles and permissions
  - Attendance and payroll system

- **Inventory Management**
  - Track medical supplies and equipment
  - Manage stock levels
  - Generate purchase orders

- **Reporting and Analytics**
  - Generate reports on hospital operations
  - Data visualization dashboards
  - Export reports in various formats (PDF, Excel)

- **User Authentication and Authorization**
  - Secure login system
  - Role-based access control (Admin, Doctor, Nurse, Receptionist)

- **Responsive Design**
  - Accessible on desktops, tablets, and mobile devices
  - Cross-browser compatibility

---

## Architecture

The system is built using a layered architecture to separate concerns and enhance scalability.

### Layers

1. **Presentation Layer**
   - **Description**: User interface components that interact with users.
   - **Technologies**: HTML5, CSS3, JavaScript, Bootstrap

2. **Business Logic Layer**
   - **Description**: Core application logic that processes data between the UI and data layers.
   - **Technologies**: C#, ASP.NET MVC

3. **Data Access Layer**
   - **Description**: Handles all database operations.
   - **Technologies**: Entity Framework, LINQ

4. **Database Layer**
   - **Description**: Stores all persistent data required by the application.
   - **Technologies**: Microsoft SQL Server


## Technologies Used

- **Frontend**
  - HTML5
  - CSS3
  - JavaScript
  - Bootstrap

- **Backend**
  - C#
  - ASP.NET MVC Framework
  - Entity Framework (ORM)

- **Database**
  - Microsoft SQL Server

- **Development Tools**
  - Visual Studio 2019 or later
  - SQL Server Management Studio
  - Git for version control

---

## Installation Guide

### Prerequisites

- **Operating System**: Windows 10 or later
- **Software**:
  - [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/)
  - [SQL Server 2017](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) or later
  - [SQL Server Management Studio](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms)
  - [.NET Framework 4.7.2](https://dotnet.microsoft.com/download/dotnet-framework/net472)
  - [Git](https://git-scm.com/downloads)

### Steps

1. **Clone the Repository**

   Open Command Prompt or Git Bash and run:

   ```bash
   git clone https://github.com/ashrithvm/Medical-Facility-Management-System.git
   ```

2. **Restore NuGet Packages**

   - Open the solution file `HospitalManagementSystem.sln` in Visual Studio.
   - Right-click on the solution in the **Solution Explorer** and select **Restore NuGet Packages**.

3. **Configure the Database**

   - Open `Web.config` file.
   - Locate the `<connectionStrings>` section.
   - Update the `connectionString` to match your SQL Server instance.

   ```xml
   <connectionStrings>
     <add name="HospitalDBEntities" connectionString="data source=YOUR_SERVER_NAME;initial catalog=HospitalDB;integrated security=True;" providerName="System.Data.SqlClient" />
   </connectionStrings>
   ```

4. **Create the Database**

   - Open **Package Manager Console** in Visual Studio (Tools > NuGet Package Manager > Package Manager Console).
   - Run the following command to apply migrations and create the database:

     ```powershell
     Update-Database
     ```

5. **Build and Run the Application**

   - Press **F5** or click on **Start Debugging** to run the application.
   - The application should open in your default web browser.

---

## Usage Instructions

### Accessing the Application

- **URL**: `http://localhost:[port]/`
- Replace `[port]` with the port number displayed in Visual Studio when the application runs.

### Default Login Credentials

- **Administrator**
  - **Username**: `admin@hospital.com`
  - **Password**: `Admin@123`

- **Doctor**
  - **Username**: `doctor@hospital.com`
  - **Password**: `Doctor@123`

- **Staff**
  - **Username**: `staff@hospital.com`
  - **Password**: `Staff@123`

> **Note**: Please change the default passwords after the first login for security purposes.

### Navigating the Application

- **Dashboard**
  - View overall hospital statistics.
  - Access quick links to different modules.

- **Patients Module**
  - Add new patients.
  - Search and update patient information.
  - View medical histories.

- **Appointments Module**
  - Schedule new appointments.
  - View and manage existing appointments.
  - Send reminders.

- **Doctors Module**
  - Manage doctor profiles and schedules.
  - Assign doctors to patients.

- **Billing Module**
  - Generate invoices.
  - Process payments.
  - Manage insurance claims.

- **Reports Module**
  - Generate and export operational reports.
  - View analytics dashboards.

### Security Roles

- **Admin**
  - Full access to all modules and settings.

- **Doctor**
  - Access to patient records, appointments, and medical notes.

- **Staff**
  - Limited access to patient registration, appointment scheduling, and billing.

