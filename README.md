#  EcoScape Backend

EcoScape is a full-stack eco-tourism platform that enables users to explore, book, and manage environmentally friendly accommodations.

This repository contains the backend application built with Spring Boot, designed to deliver secure, scalable, and real-world booking functionality.

---

##  Purpose

The backend aims to provide a complete system that:

* ensures secure authentication and authorization  
* manages listings and availability dynamically  
* handles complex booking logic with validation  
* processes payments through Stripe  
* communicates with users via automated email  

---

##  Tech Stack

* Java / Spring Boot  
* Spring Security + JWT  
* PostgreSQL  
* JPA / Hibernate  
* Stripe API  
* Java Mail (SMTP)  

---

##  Architecture Overview

The system follows a layered architecture:

* **Controller Layer** → handles HTTP requests and responses  
* **Service Layer** → contains business logic and validations  
* **Repository Layer** → interacts with the database  
* **Configuration Layer** → security, JWT, Stripe, Mail  

---

##  Authentication & Authorization

* Stateless authentication using JWT  
* Role-based access control:
  * USER  
  * HOST  
  * ADMIN  
* Secure request filtering via Spring Security  
* Centralized user retrieval through `AuthenticationService`  

✔ Ensures secure and scalable session handling  
⚠️ Potential improvement: refresh tokens & stricter endpoint protection  

---

##  Core Features

### Listings Management

* Create, update, delete listings  
* Includes amenities, sustainability features, and rules  
* Advanced search filtering  

---

###  Availability System

* Prevents overlapping date ranges  
* Dynamically updates after booking/cancellation  
* Splits and merges date ranges  

---

###  Booking System

* Full lifecycle:
  * create  
  * update  
  * cancel (user & host)  
* Strong validation:
  * dates  
  * guest limits  
  * contact information  
* Price calculation:
  * nightly rate  
  * cleaning fee  
  * service fee  

---

###  Payment Integration (Stripe)

* PaymentIntent flow implemented  
* Secure backend validation  
* Payments linked to bookings  

---

###  Email System

* Booking confirmation  
* Cancellation notifications  
* Update notifications  

---

##  API Documentation

All endpoints are documented via Postman:

https://documenter.getpostman.com/view/40897736/2sAYk7SjT2  

---

## ▶️ Run the Project

```bash
mvn clean install
mvn spring-boot:run
```
--- 

# Backend Analysis
## Strengths
* Clean layered architecture
* Strong business logic and validation
* Advanced availability management
* Secure authentication with JWT
* Integration with external services (Stripe & Email)

---

##  Improvements
* Implement global exception handling
* Improve endpoint security (reduce public access)
* Add logging and monitoring
* Use async email processing
* Implement Stripe webhook verification

---

## Author

**Shams AlSaffar**
