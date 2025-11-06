# Airbnb Clone – Data Flow Diagram (DFD)

## 🎯 Objective
This document explains the **Data Flow Diagram (DFD)** for the Airbnb Clone Backend System.  
The diagram illustrates how data moves between users, the system processes, and the database.

---

## 📊 Diagram Overview
The DFD represents the core modules of the system:
- **User Management**
- **Property Management**
- **Booking System**
- **Payment Processing**
- **Review & Feedback**

Each module shows how data flows between **external entities**, **processes**, **data stores**, and **outputs**.

---

## 🧩 Level 0 (Context Diagram)
At Level 0, the Airbnb System is represented as a single process interacting with external entities:

- **Entities:**
  - User (Guest)
  - Host
  - Admin
  - Payment Gateway

- **Processes:**
  - Airbnb System (Main backend)

- **Data Flows:**
  - User → Login/Registration Data → Airbnb System
  - Airbnb System → Booking Confirmation → User
  - Airbnb System ↔ Payment Gateway → Payment Requests/Responses
  - Host → Property Data → Airbnb System
  - Admin ↔ Airbnb System → Reports/Logs

---

## 🧠 Level 1 (Detailed DFD)
At Level 1, the system is expanded into 5 main processes:

### 1. **User Authentication**
- **Input:** Registration details, Login credentials  
- **Process:** Validate and store user data  
- **Output:** Authenticated session token, error messages  
- **Data Store:** `User` table

---

### 2. **Property Management**
- **Input:** Property details (title, description, price, availability)  
- **Process:** Validate data, link property to host, store property info  
- **Output:** Property listing confirmation  
- **Data Store:** `Property` table

---

### 3. **Booking System**
- **Input:** Booking request (user ID, property ID, dates)  
- **Process:** Check availability, calculate cost, create booking record  
- **Output:** Booking confirmation or rejection  
- **Data Store:** `Booking` table

---

### 4. **Payment Processing**
- **Input:** Payment details (amount, booking ID, user ID)  
- **Process:** Send payment request to gateway, receive confirmation  
- **Output:** Payment success/failure message  
- **Data Store:** `Payment` table  
- **External Entity:** Payment Gateway

---

### 5. **Review & Feedback**
- **Input:** User review data (rating, comment, booking ID)  
- **Process:** Validate and store feedback  
- **Output:** Review published  
- **Data Store:** `Review` table

---

## 📤 Output Summary
| Process | Input | Output | Data Store |
|----------|--------|---------|-------------|
| User Authentication | Login/Register Data | Token / Error | User |
| Property Management | Property Info | Listing Created | Property |
| Booking System | Booking Data | Confirmation | Booking |
| Payment Processing | Payment Info | Receipt | Payment |
| Review & Feedback | Review Data | Public Review | Review |

---

## 🖼️ Diagram File
The visual DFD has been exported as:

📄 **File:** `data-flow.png`  
📁 **Directory:** `data-flow-diagram/`

---

## 👨‍💻 Author
**Mostafa Khamis**  
Repository: [alx-airbnb-project-documentation](https://github.com/MostafaKhamis/alx-airbnb-project-documentation)

