# Airbnb Clone – System Process Flowchart

## 🎯 Objective
This document explains the **Flowchart** for a key backend process in the Airbnb Clone system.  
The flowchart visualizes the workflow, decisions, and data flow for the selected process.

---

## 🧩 Selected Process
**Property Booking Process** – chosen as it involves multiple steps and interactions between the user, system, and database.

---

## 🔄 Flowchart Steps

1. **User selects property and dates**
2. **System checks availability**
   - If **available**, proceed
   - If **not available**, notify user and end process
3. **User confirms booking**
4. **System calculates total cost**
5. **User submits payment**
6. **Payment processed via Payment Gateway**
   - If **payment successful**, booking confirmed
   - If **payment failed**, notify user and end process
7. **System updates Booking and Payment tables**
8. **Confirmation sent to User**
9. **End of process**

---

## 🖼️ Flowchart File
The visual flowchart has been exported as:

📄 **File:** `property-booking-flowchart.png`  
📁 **Directory:** `flowcharts/`

---

## 👨‍💻 Author
**Mostafa Khamis**  
Repository: [alx-airbnb-project-documentation](https://github.com/MostafaKhamis/alx-airbnb-project-documentation)

