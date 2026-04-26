# 🏨 Hotel Management System (LLD)

## 📌 Overview
This project focuses on designing a **Hotel Management System (HMS)** using Low-Level Design (LLD) principles. The system models real-world hotel operations including room booking, customer management, check-in/check-out, billing, and payments.

The goal is to build a scalable, modular, and extensible design suitable for handling real-world scenarios and concurrent users.

---

## 🎯 Objectives
- Design clean and maintainable class structures
- Handle real-world constraints like concurrent bookings
- Apply SOLID principles and design patterns
- Build extensible modules for future features

---

## 🧩 Core Features

### 1. Hotel Structure
- Hotel consists of multiple floors
- Each floor contains multiple rooms

#### Room Attributes:
- Room Number
- Room Type (Single, Double, Deluxe, Suite)
- Price per night
- Status:
  - Available
  - Booked
  - Occupied
  - Maintenance

---

### 2. User Roles

#### 👤 Customer
- Search rooms by:
  - Date range
  - Room type
  - Price range
- Book rooms
- Cancel bookings
- View booking history

#### 👨‍💼 Receptionist / Admin
- Add/update room details
- Manage bookings
- Perform check-in/check-out
- Generate bills
- Assign rooms

---

### 3. Booking Management

#### Booking Details:
- Booking ID
- Customer details
- Room(s)
- Check-in date
- Check-out date
- Booking status:
  - Confirmed
  - Cancelled
  - Completed

#### Rules:
- No overlapping bookings for the same room
- Multiple rooms can be booked together
- Booking can be modified before check-in

---

### 4. Check-In / Check-Out

#### ✅ Check-In
- Validate booking
- Assign room(s)
- Update room status → Occupied

#### 🚪 Check-Out
- Generate final bill
- Update room status → Available
- Mark booking as Completed

---

### 5. Billing & Payments

#### Bill Includes:
- Room charges (per night × duration)
- Additional services (optional)
- Taxes

#### Payment Modes:
- Cash
- Card
- UPI

#### Payment Status:
- Pending
- Completed
- Failed

---

### 6. Room Availability
- Track availability for a given date range
- Prevent double booking (handle concurrency)

---

### 7. Additional Services (Optional)
- Food ordering
- Laundry
- Spa

Each service:
- Has associated cost
- Added to final bill

---

### 8. Notifications
- Booking confirmation
- Cancellation updates
- Check-in reminders

---

## ⚙️ Functional Requirements
- Search available rooms
- Create booking
- Modify/cancel booking
- Check-in and check-out
- Generate bill
- Process payment

---

## 🚫 Non-Functional Requirements
- Scalable (support large number of rooms/users)
- Thread-safe (avoid race conditions)
- Extensible (add new services easily)
- Maintainable (clean architecture)

---

## 🔥 Edge Cases
- Overlapping bookings
- Partial payments
- Late check-out charges
- Room under maintenance
- Failed payment scenarios
- No-show bookings

---

## 💡 Design Considerations

### Key Entities:
- Hotel
- Floor
- Room
- Booking
- Customer
- Payment
- Bill
- Service

### Design Patterns:
- **Strategy Pattern** → Payment methods
- **Factory Pattern** → Room creation
- **Observer Pattern** → Notifications
- **Singleton (optional)** → Central management system

---

## 🚀 Bonus Enhancements
- Multi-hotel support
- Dynamic pricing (weekends, holidays)
- Loyalty/reward system
- Third-party integrations

---

## 🛠️ Tech Stack (Optional)
You can implement this design using:
- Java / PHP / Node.js
- MySQL / PostgreSQL
- REST APIs

---

## 📚 How to Use
1. Identify entities and relationships
2. Draw class diagrams
3. Implement core modules
4. Add concurrency handling
5. Extend with advanced features

---

## 🧠 Interview Tips
- Focus on clear class design
- Justify design patterns used
- Handle edge cases
- Think about scalability and concurrency

---

## 📌 Author
Shashank Gangwar