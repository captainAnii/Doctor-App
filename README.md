<h1 align = "center"> Doctor-App </h1>
<p align="center">
  <a href="Java url">
    <img alt="Java" src="https://img.shields.io/badge/JavaVersion-8+-blue.svg" />
  </a>
  <a href="Maven url">
    <img alt="Maven" src="https://img.shields.io/badge/Maven-3.6.3-blue.svg" />
  </a>
  <a href="Spring Boot url">
    <img alt="Spring Boot" src="https://img.shields.io/badge/Spring%20Boot-2.5.0+-brightgreen.svg" />
  </a>
  <a href="MySQL url">
    <img alt="MySQL" src="https://img.shields.io/badge/MySQL-8.0+-blue.svg" />
  </a>
</p>
- This project is a web application that allows patients to book appointments with doctors. The system helps manage doctor availability, patient appointments, and provides an easy-to-use interface for users to schedule their appointments.

---
## Frameworks and Libraries Used
* Spring Boot
* Spring MVC
* Spring Data JPA
* MySQL (as the database)
---
---
## Dependencies
The following dependencies are required to run the project:

* Spring Web
* Spring Data JPA
* MySQL Driver
* Thymeleaf
* Spring Boot DevTools
* Validation
* Lombok
---
---
<br>

## Database Configuration
To connect to a MySQL database, update the application.properties file with the appropriate database URL, username, and password. The following properties need to be updated:
```
spring.datasource.driverClassName=com.mysql.cj.jdbc.Driver
spring.datasource.url = jdbc:mysql://localhost:3306/<DatabaseName>
spring.datasource.username = <userName>
spring.datasource.password = <password>
spring.jpa.show-sql = true
spring.jpa.hibernate.ddl-auto = update

spring.jpa.properties.hibernate.show_sql=true
spring.jpa.properties.hibernate.use_sql_comments=true
spring.jpa.properties.hibernate.format_sql=true

```
<br>
## Data Model

The Job data model is defined in the Job class, which has the following attributes:
<br>

* Doctor
```
id: Long
firstName: String
lastName: String
specialization: String
availableSlots: List<LocalDateTime>
```

* Patient
```
id: Long
firstName: String
lastName: String
email: String
phoneNumber: String
appointments: List<Appointment>
```
 
*Appointment
```
id: Long
doctor: Doctor
patient: Patient
appointmentDateTime: LocalDateTime
```

## Data Flow
1. The user visits the application's homepage and selects a doctor.
2. The application retrieves the available slots for the selected doctor.
3. The user selects a preferred appointment slot.
4. The application validates the appointment and checks for conflicts with existing appointments.
5. If the appointment is valid, it is saved in the database.
6. The user receives a confirmation of the appointment.

---

## API Endpoints

The following endpoints are available in the API:

* Doctor Controller:
```
GET /doctors: Get all doctors
GET /doctors/{id}: Get a specific doctor
POST /doctors: Create a new doctor
PUT /doctors/{id}: Update a doctor
DELETE /doctors/{id}: Delete a doctor
```

* Patient Controller:
```
GET /patients: Get all patients
GET /patients/{id}: Get a specific patient
POST /patients: Create a new patient
PUT /patients/{id}: Update a patient
DELETE /patients/{id}: Delete a patient
```

* Appointment Controller:
```
GET /appointments: Get all appointments
GET /appointments/{id}: Get a specific appointment
POST /appointments: Create a new appointment
PUT /appointments/{id}: Update an appointment
DELETE /appointments/{id}: Delete an appointment
``` 
<br>

## DataBase Used
* SQL database
```
We have used Persistent database to implement CRUD Operations.
```
---
<br>

## Project Summary
The Doctor Appointment Booking System is a web application that allows patients to book appointments with doctors. It utilizes Spring Boot and Spring MVC frameworks for handling requests and managing data persistence. The system provides endpoints for managing doctors, patients, and appointments. The data model includes entities for Doctor, Patient, and Appointment. The application validates appointment requests and ensures that there are no conflicts with existing appointments. The project utilizes MySQL as the database for storing data.


Author
👤 Aniket Yogesh Gosavi

GitHub: https://github.com/captainAnii

LinkedIn: https://www.linkedin.com/in/anikegosavi1999/

--- 
## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page]("url").
    
---
    
## Show your support

Give a ⭐️ if this project helped you!
    
---
    
## 📝 License

Copyright © 2023 [Aniket Gosavi](https://github.com/captainAnii).<br />

This project is [MIT]("url") licensed.
    
---
