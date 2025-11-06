# Airbnb Clone Backend – Use Case Diagram

## 🎯 Objective
This document provides a **Use Case Diagram** that visualizes how different actors interact with the **Airbnb Clone Backend System**.  
It highlights the core functionalities available to each user type — Guests, Hosts, and Admins — based on the project’s defined features and modules.

---

## 👥 System Actors
1. **Guest (User)**
   - Can register, log in, browse properties, make bookings, and leave reviews.

2. **Host**
   - Can list properties, manage availability, view bookings, and respond to booking requests.

3. **Admin**
   - Has elevated privileges to monitor and manage users, properties, and transactions.

4. **Payment Gateway (External System)**
   - Handles payment processing, refunds, and transaction verification.

---

## ⚙️ Main Use Cases

### 👤 For Guest:
- Register an account  
- Log in / Log out  
- Search for properties  
- View property details  
- Make a booking  
- Cancel a booking  
- Make a payment  
- Leave a review  
- Update personal profile  

---

### 🏠 For Host:
- Register as host  
- Add new property listing  
- Edit or delete property  
- Manage availability (calendar)  
- View incoming bookings  
- Approve or reject booking requests  
- View total revenue and statistics  

---

### 🧠 For Admin:
- Log in to the admin dashboard  
- Manage users (activate, deactivate, or delete)  
- Manage all properties and bookings  
- View analytics and reports  
- Handle complaints and disputes  
- Monitor suspicious activity  

---

### 💳 Payment Gateway (External):
- Process payments securely  
- Handle refunds for cancellations  
- Send payment confirmation to system  

---

## 🖼️ Use Case Diagram Overview

📁 **File:** `use-case-diagram/airbnb-usecase.png`

The diagram shows the interactions between the following actors:
- **Guest**, **Host**, **Admin**, and **Payment Gateway**
  
Each actor interacts with specific **use cases** (represented as ovals) inside the **Airbnb System boundary box**.

---

## 🧩 Key Relationships
| Actor | Interacts With | Notes |
|--------|----------------|-------|
| Guest | Booking, Payment, Review | Can make and manage bookings |
| Host | Property Management, Booking Approval | Controls listings |
| Admin | System Monitoring, Reports | Has access to everything |
| Payment Gateway | Payment Processing | External API integration |

---

## 🧾 Summary
The Use Case Diagram ensures a clear understanding of **how users interact** with the Airbnb backend system.  
It serves as the foundation for system design, API planning, and testing workflows.

---

**Author:** Mostafa Khamis  
**Repository:** [alx-airbnb-project-documentation](https://github.com/MostafaKhamis/alx-airbnb-project-documentation)

