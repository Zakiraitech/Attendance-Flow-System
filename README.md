# 🕒 Attendance Flow

> *Smart Attendance. Better Workforce.*

Attendance Flow is a comprehensive, multi-tenant employee attendance management platform designed to streamline workforce tracking with advanced security, biometrics, and geolocation validation[cite: 6].

## ✨ Key Features

- **Multi-Tenant Architecture:** Complete organization-level data isolation and tenant scoping for secure multi-company environments[cite: 6, 10].
- **Five-Tier Role-Based Access Control (RBAC):** Granular server-side permissions for System Administrators, Support Staff, Organization Admins, Department Heads, and Employees[cite: 6, 15].
- **Facial Biometric Verification:** Employee face enrollment and 128-dimensional embedding verification (supporting browser ONNX, AWS, or Azure configurations)[cite: 6, 19, 20].
- **GPS Geofencing:** Server-side Haversine distance calculations to ensure employees are within authorized work location radii during clock-in/out[cite: 6, 18, 21].
- **Automated Attendance Workflows:** Duplicate shift prevention, late detection based on schedules, worked-hours tracking, and department-head submission locking[cite: 6, 20, 23].
- **Billing & Subscriptions:** Seamless Paystack checkout integration, manual bank transfer review workflows, and automated receipt generation[cite: 6, 22, 23].
- **Operations & Audit Logging:** Built-in threaded support ticketing system and detailed audit trails for sensitive administrative and security actions[cite: 6, 8, 25].

---

## 🛠️ Technology Stack

| Layer | Technology / Baseline |
| :--- | :--- |
| **Server** | PHP 8.x with PDO (Data Objects)[cite: 6] |
| **Database** | MySQL / compatible MariaDB (utf8mb4 encoding)[cite: 6, 8] |
| **Frontend** | HTML5, CSS3, Bootstrap 5, vanilla JavaScript[cite: 6] |
| **Biometrics** | Browser ONNX, AWS, or Azure (dependent on deployment configuration)[cite: 6] |
| **Payments** | Paystack API integration & Manual Bank Transfer review[cite: 6] |
| **Environment** | Local: XAMPP / Production: HTTPS-enabled shared or VPS PHP hosting[cite: 6] |
| **Timezone Policy** | UTC storage with display conversion to `Africa/Lagos`[cite: 4, 6] |

---

## 🚀 Quick Start Guide

1. **Prerequisites:** Ensure you have XAMPP installed with **PHP 8.x** and **MySQL/MariaDB** running[cite: 6, 8].
2. **Clone / Place Project:** Move the application directory into your web root (e.g., `C:\xampp\htdocs\attendance-flow`)[cite: 7, 8].
3. **Database Setup:** 
   - Create a dedicated MySQL database (e.g., `attendance_flow`) with `utf8mb4` character collation[cite: 8].
   - Import the canonical database schema provided in your project files[cite: 7, 8].
4. **Environment Configuration:** 
   - Copy `.env.example` to `.env`[cite: 7].
   - Configure your database credentials, base URL (`APP_URL`), mail settings, and Paystack API keys[cite: 9]. Make sure `APP_DEBUG=false` in production[cite: 9].
5. **Launch:** Open your local development URL in a modern web browser, complete the initial setup, and verify system health[cite: 7, 9].

---

## 🔒 Security & Compliance

- **Prepared Statements:** Uses PDO parameter binding exclusively to prevent SQL injection[cite: 24].
- **Password Hashing:** Implements native PHP `password_hash()` (Bcrypt)[cite: 24].
- **CSRF & XSS Protections:** Session-bound unpredictable tokens for state-changing requests and strict contextual output escaping[cite: 24].
- **Secure Sessions:** HTTPS-enforced environment configuration with `Secure`, `HttpOnly`, and properly configured `SameSite` cookie flags[cite: 15, 24, 25].

---

## 📄 License

Copyright © Ablaz Technologies Limited. All rights reserved. Subject to the specific license terms defined by the project owner[cite: 4, 7].
