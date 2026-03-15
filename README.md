# 🏩 Hotel Reservation System

[![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![JDBC](https://img.shields.io/badge/JDBC-Internal-blue?style=for-the-badge)](https://docs.oracle.com/javase/8/docs/technotes/guides/jdbc/)

A robust, console-based Java application designed to streamline hotel management operations. This project demonstrates core backend development principles, including database connectivity, CRUD operations, and structured software design.

---

## 🚀 Features

- **🏨 Room Reservation:** Capture guest details, room preference, and contact information seamlessly.
- **📋 Management Dashboard:** Real-time view of all active reservations with formatted tabular output.
- **🔍 Instant Lookup:** Quickly retrieve room numbers using reservation IDs and guest names.
- **✏️ Dynamic Updates:** Modify existing reservation details (guest name, room, contact) on the fly.
- **❌ Efficient Cancellation:** Remove outdated or cancelled reservations with simple ID-based deletion.
- **⏳ Graceful Shutdown:** User-friendly exit sequence with simulated processing.

---

## 🛠️ Tech Stack

- **Language:** Java 8+
- **Database:** MySQL
- **Driver:** JDBC (Java Database Connectivity)
- **Architecture:** Procedural with modular method breakdown for high readability.

---

## 🧩 Technical Highlights

- **Database Integration:** Implements JDBC for reliable communication between the Java application and MySQL.
- **SQL Mastery:** Utilizes optimized SQL queries for all CRUD (Create, Read, Update, Delete) operations.
- **Data Integrity:** Ensures data persistence and consistency across sessions using a relational database.
- **Error Handling:** Robust `try-catch` blocks to manage `SQLException` and `ClassNotFoundException`.
- **UI/UX:** Clean, intuitive console-driven menus with formatted tables for enhanced data visualization.

---

## 📂 Database Schema

The system relies on a `reservations` table within the `hotel_db` database:

```sql
CREATE TABLE reservations (
    reservation_id INT AUTO_INCREMENT PRIMARY KEY,
    guest_name VARCHAR(255) NOT NULL,
    room_number INT NOT NULL,
    contact_number VARCHAR(20) NOT NULL,
    reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

## ⚙️ Installation & Setup

### Prerequisites
- [JDK 8 or higher](https://www.oracle.com/java/technologies/downloads/)
- [MySQL Server](https://dev.mysql.com/downloads/installer/)
- [MySQL Connector/J](https://dev.mysql.com/downloads/connector/j/)

### Step-by-Step Guide

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/kalyanSadhukhan/Hotel-Reservation-System.git
   ```

2. **Database Configuration:**
   - Create a database named `hotel_db`.
   - Run the SQL command provided in the [Database Schema](#-database-schema) section.

3. **Environment Setup:**
   - Update the connection strings in `HotelReservationSystem.java`:
   ```java
   private static final String url = "jdbc:mysql://localhost:3306/hotel_db";
   private static final String username = "your_username";
   private static final String password = "your_password";
   ```

4. **Compile and Run:**
   ```bash
   javac HotelReservationSystem.java
   java -cp ".;lib/mysql-connector-j-x.x.x.jar" HotelReservationSystem
   ```
   *(Note: Ensure the MySQL connector is in your classpath)*

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git checkout origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📧 Contact

**Kalyan Sadhukhan** - [GitHub](https://github.com/kalyanSadhukhan)

Project Link: [https://github.com/kalyanSadhukhan/Hotel-Reservation-System](https://github.com/kalyanSadhukhan/Hotel-Reservation-System)

