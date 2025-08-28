# TrainTicketBookingApp
Online Railway Ticket Booking System

A **Java Servlet & JSP based web application** for online railway ticket booking.
This project allows **Admins** to manage trains & bookings, and **Customers** to search, book, and cancel tickets online.

🔹 Features

 👨‍💼 Admin Panel

* Add new trains with details (Train No, Name, Route, Price, Seats etc.)
* Update existing train details
* Delete trains from the system
* View all customer bookings

 👤 Customer Panel

* Register & Login to the system
* Search trains by source, destination & date
* Book tickets with seat availability check
* Cancel booked tickets using Booking ID
* View booking history (past & upcoming journeys)

---

🔹 System Diagrams

 1. Authentication (Common for Admin & Customer)

```
[Start] → [Login/Register Page] → (Admin / Customer Dashboard)
```

 2. Admin Part

* Add Train → Save in Database
* Update Train → Modify Existing Data
* Delete Train → Remove from Database
* View All Bookings → Fetch Customer Data

 3. Customer Part

* Search Train → Show Available Trains
* Book Ticket → Check Availability → Confirm or Reject
* Cancel Ticket → Update Status → Show Success
* View Booking History → Show All Bookings

 4. Overall System Flow

```
          ┌───────────────┐
          │   LOGIN PAGE  │
          └──────┬────────┘
                 │
      ┌──────────┴───────────┐
      │                      │
 ┌────▼─────┐           ┌────▼──────┐
 │  ADMIN   │           │ CUSTOMER  │
 └────┬─────┘           └────┬──────┘
      │                      │
 ┌────▼───────┐        ┌─────▼─────────┐
 │ Manage     │        │ Search Trains │
 │ Trains     │        └─────┬─────────┘
 │ View Bookings│            │
 └──────────────┘       ┌────▼──────┐
                        │ Book/Cancel│
                        │ View History│
                        └────────────┘
```

---

 🔹 Tech Stack

* **Frontend:** JSP, HTML, CSS
* **Backend:** Java Servlets
* **Database:** MySQL (JDBC for connectivity)
* **Server:** Apache Tomcat
* **Version Control:** Git & GitHub

---

 🔹 Project Setup (Eclipse + Tomcat)

1. Clone the repository:

   ```bash
   git clone https://github.com/<username>/RailwayTicketBookingApp.git
   ```
2. Open Eclipse → Import project as **Dynamic Web Project**.
3. Configure **Apache Tomcat Server** in Eclipse.
4. Setup MySQL database (create tables for users, trains, bookings).
5. Run the project on Tomcat → Access via `http://localhost:8080/RailwayTicketBookingApp/`

---

 🔹 Future Enhancements

* Online Payment Integration (UPI, NetBanking, Cards)
* Seat Selection with Coach View
* Email/SMS Booking Notifications
* Mobile App Version
