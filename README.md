#  EcoScape Backend

EcoScape is a full-stack eco-tourism platform that enables users to explore, book, and manage environmentally friendly accommodations.

This repository contains the **backend application built with Spring Boot**, designed to deliver secure, scalable, and real-world booking functionality.

---

##  Purpose

The backend provides the core system responsible for:

* secure authentication and authorization
* managing listings and availability
* handling booking logic with validation
* processing payments via Stripe
* sending automated email notifications

---

##  Tech Stack

* Java 17
* Spring Boot
* Spring Security + JWT
* PostgreSQL
* JPA / Hibernate
* Stripe API
* Java Mail (SMTP)
* Maven

---

##  Architecture

The system follows a layered architecture:

* **Controller Layer** → handles HTTP requests and responses
* **Service Layer** → contains business logic and validations
* **Repository Layer** → interacts with the database
* **Configuration Layer** → security, JWT, Stripe, and Mail

---

##  Authentication & Authorization

* Stateless authentication using JWT
* Role-based access control:

  * USER
  * HOST
  * ADMIN
* Secured endpoints using Spring Security
* Centralized authentication handling

✔ Ensures secure and scalable session management

---

##  Core Features

###  Listings Management

* Create, update, and delete listings
* Support for amenities and sustainability features
* Advanced filtering and search

---

###  Availability System

* Prevents overlapping date ranges
* Automatically updates after booking or cancellation
* Handles splitting and merging of availability periods

---

###  Booking System

* Full booking lifecycle:

  * create
  * update
  * cancel (user & host)

* Validation includes:

  * date validation
  * guest limits
  * user input validation

* Price calculation:

  * nightly price
  * cleaning fee
  * service fee

---

###  Payment Integration (Stripe)

* PaymentIntent flow implemented
* Secure backend validation of payments
* Payments linked to bookings

---

###  Email System

* Booking confirmation emails
* Cancellation notifications
* Update notifications

---

##  API Documentation

All endpoints are documented using Postman:

 https://documenter.getpostman.com/view/40897736/2sAYk7SjT2

---

## ▶️ Run the Project

```bash
mvn clean install
mvn spring-boot:run
```

---

##  Team & Contribution

This project was developed as part of a team collaboration.

### My Contribution

I was responsible for key backend features, with a focus on:

* **Booking System**

  * implementing booking lifecycle (create, update, cancel)
  * validation of booking rules and business logic
  * price calculation logic

* **Payment Integration (Stripe)**

  * implementing PaymentIntent flow
  * connecting payments with bookings
  * handling secure payment validation

* **Email System (Java Mail)**

  * sending booking confirmation emails
  * handling cancellation and update notifications

I also contributed to:

* backend logic and service layer implementation
* API integration and validation
* improving system reliability and user experience

---

##  Future Improvements

* improve global exception handling
* enhance endpoint security
* implement Stripe webhook validation
* introduce logging and monitoring
* async email processing

---

##  Notes

This repository contains only the backend part of the system.
The frontend (React) is developed separately and consumes this API.
