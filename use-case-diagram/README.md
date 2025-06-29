# 📘 Airbnb Clone - Use Case Diagram Documentation

This document outlines the actors, use cases and system boundaries

---

## 🎭 1. Actors

| Actor                            | Description                                                                                                                |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Host**                         | Property owners who list and manage properties.<br>🔹 _Key Actions:_ Create listings, manage bookings, respond to reviews. |
| **Guest**                        | Users who search, book, and review properties.<br>🔹 _Key Actions:_ Search, book, pay, review.                             |
| **Admin**                        | System administrators who manage users and monitor system health.<br>🔹 _Key Actions:_ Manage users, resolve disputes.     |
| **Payment Gateway** _(External)_ | Third-party service (e.g., Stripe) for processing payments.                                                                |
| **Email Service** _(External)_   | Email notifications (e.g., SendGrid) for updates and alerts.                                                               |

---

## 🧩 2. Use Cases

### 👤 Host-Focused

- **Register**: Sign up as a host.
- **Login**: Authenticate and access the system.
- **Manage Profile**: Update photo, contact info, and preferences.
- **Manage Property**: Add, edit, or delete listings.
- **Respond to Review**: Reply to guest reviews.
- **Cancel Booking**: Cancel confirmed bookings (if policy allows).
- **Check Booking Status**: View the status of bookings.
- **Process Payout**: Receive payment after a booking is completed.

---

### 🧍 Guest-Focused

- **Register**: Sign up as a guest.
- **Login**: Authenticate and access the system.
- **Manage Profile**: Update photo, contact info, and preferences.
- **Search Property**: Filter listings by location, price, and amenities.
- **Create Booking**: Reserve a property for a given date range.
- **Make Payment**: Pay securely via integrated gateway.
- **Leave Review**: Rate and review a property after a stay.

---

### 🛡️ Admin-Focused

- **Login**: Authenticate and access the admin system.
- **Manage Users**: Suspend, delete, or review host/guest accounts.
- **Manage Profile**: Update profile information as an admin.
- **Manage Property**: Remove inappropriate or fraudulent listings.
- **Search Property**: Search listings for moderation or investigation.

---

### 🛰️ System-Level

- **Make Payment**: Performed by the guest through an external payment gateway.
- **Send Notification**: Email notifications for key events (booking, cancellation, payment) via external email service.

---

## 🚧 3. System Boundary

The system boundary clearly defines what is part of the internal system and what lies outside.

### ✅ Inside the System (Use Cases)

- User authentication and profile management
- Property listings creation and updates
- Property search and filtering
- Booking and cancellation
- Payment processing logic
- Review system
- Admin tools and dashboards
- Notification logic (sending trigger)

### 🚫 Outside the System (Actors)

- Hosts, Guests, and Admins (users who interact with the system)
- Payment Gateway (e.g., Stripe, PayPal)
- Email Service (e.g., SendGrid)
- Devices: Web browsers and mobile applications

---
