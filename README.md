#  Football Ticket Booking System - Database Project

##  Overview
This project is a relational database system for managing football match ticket bookings.  
It allows users (fans and ticket managers) to view matches, book tickets, and track payment status.

The system is built using PostgreSQL and follows proper database normalization with relationships between Users, Matches, and Bookings tables.

---

##  Features
- User management (Football Fans & Ticket Managers)
- Match listing with ticket pricing and status
- Ticket booking system with seat allocation
- Payment tracking (Pending, Confirmed, Cancelled, Refunded)
- Relational integrity using Primary & Foreign Keys

---

##  Database Schema

### 1. Users Table
- user_id (PK)
- full_name
- email
- role
- phone_number

### 2. Matches Table
- match_id (PK)
- fixture
- tournament_category
- base_ticket_price
- match_status

### 3. Bookings Table
- booking_id (PK)
- user_id (FK → Users.user_id)
- match_id (FK → Matches.match_id)
- seat_number
- payment_status
- total_cost

---

##  Relationships
- One User → Many Bookings  
- One Match → Many Bookings  
- Each Booking links one User with one Match

---

##  Technologies Used
- PostgreSQL
- SQL (DDL & DML)
- Beekeeper Studio (Database Management Tool)
- DrawSQL / ERD Design Tool

---

##  Sample Queries Included
This project includes SQL queries for:
- Filtering matches by category and status
- Searching users using pattern matching (ILIKE)
- Handling NULL values using COALESCE
- INNER JOIN between tables
- LEFT JOIN to include all users
- Aggregate filtering using AVG()
- Pagination using OFFSET & LIMIT

---

##  How to Run This Project

1. Create database:
```sql
CREATE DATABASE ticket_booking_system;