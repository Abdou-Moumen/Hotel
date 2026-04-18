# 🏨 Hotel Booking Platform | Luxury Stay Management System

[![Laravel](https://img.shields.io/badge/Laravel-11.x-FF2D20?style=flat-square&logo=laravel&logoColor=white)](https://laravel.com/)
[![PHP](https://img.shields.io/badge/PHP-8.2+-777BB4?style=flat-square&logo=php&logoColor=white)](https://php.net/)
[![Blade](https://img.shields.io/badge/Blade-Template-FF2D20?style=flat-square&logo=laravel&logoColor=white)](https://laravel.com/docs/blade)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat-square&logo=mysql&logoColor=white)](https://mysql.com/)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-7952B3?style=flat-square&logo=bootstrap&logoColor=white)](https://getbootstrap.com/)

> **A full-featured hotel booking and management platform** — delivering a seamless experience for guests and staff from reservation to checkout.

---

## 🖼️ Screenshots

<table>
  <tr>
    <td align="center"><img src="hotel_images/Page1.png" width="340" alt="Homepage"/><br/><sub><b>Homepage</b></sub></td>
    <td align="center"><img src="hotel_images/Page2.png" width="340" alt="Room Listing"/><br/><sub><b>Room Listing</b></sub></td>
  </tr>
  <tr>
    <td align="center"><img src="hotel_images/Page3.png" width="340" alt="Room Details"/><br/><sub><b>Room Details</b></sub></td>
    <td align="center"><img src="hotel_images/Page4.png" width="340" alt="Booking Form"/><br/><sub><b>Booking Form</b></sub></td>
  </tr>
  <tr>
    <td align="center"><img src="hotel_images/Page5.png" width="340" alt="Guest Dashboard"/><br/><sub><b>Guest Dashboard</b></sub></td>
    <td align="center"><img src="hotel_images/Page6.png" width="340" alt="Admin Panel"/><br/><sub><b>Admin Panel</b></sub></td>
  </tr>
  <tr>
    <td align="center"><img src="hotel_images/Page7.png" width="340" alt="Reservations Management"/><br/><sub><b>Reservations Management</b></sub></td>
    <td align="center"><img src="hotel_images/Page8.png" width="340" alt="Reports & Analytics"/><br/><sub><b>Reports & Analytics</b></sub></td>
  </tr>
</table>

---

## 📋 Overview

This platform provides a complete solution for hotel operations — from online room browsing and booking to back-office reservation management. Guests enjoy a smooth booking experience while admins maintain full control over rooms, availability, and payments.

**Built by:** [Your Team Name]

---

## 🎯 Key Features

### 🛎️ Guest Side
- Browse available rooms with filters (type, price, capacity, amenities)
- View detailed room pages with photo galleries and descriptions
- Book rooms with real-time availability checking
- Receive booking confirmation via email
- Manage reservations (view, modify, cancel)
- Secure account registration and login

### 🏢 Admin Side
- Full room management (create, edit, delete, set availability)
- View and manage all guest reservations
- Update booking statuses (Pending, Confirmed, Checked-in, Checked-out, Cancelled)
- Upload and manage room photo galleries
- Generate occupancy and revenue reports
- Manage guest accounts and profiles

### 🔐 Security Features
- Role-based authentication (Guest, Receptionist, Admin)
- Secure password hashing with bcrypt
- CSRF protection on all forms
- Validated file uploads for room images
- Session-based authentication with Laravel Sanctum

---

## 🛠️ Tech Stack

| Layer | Technology | Download Link |
|-------|-------------|----------------|
| **Framework** | Laravel 11 | [laravel.com](https://laravel.com/) |
| **PHP** | PHP 8.2+ | [php.net](https://php.net/downloads) |
| **Templating** | Blade | Built into Laravel |
| **Database** | MySQL 8.0 | [mysql.com/downloads](https://dev.mysql.com/downloads/) |
| **CSS Framework** | Bootstrap 5.3 | [getbootstrap.com](https://getbootstrap.com/) |
| **Dependency Mgr** | Composer | [getcomposer.org](https://getcomposer.org/download/) |
| **Dev Tools** | Node.js & npm | [nodejs.org](https://nodejs.org/) |
| | Git | [git-scm.com](https://git-scm.com/downloads) |
| | Laragon/XAMPP | [laragon.org](https://laragon.org/download/) |

---

## 📥 Installation Guide

### 1. Install a Local Server Environment (Choose ONE)

**Option A: Laragon (Recommended for Windows)**
```bash
# Download from laragon.org
# Install and start Laragon
# It includes PHP, MySQL, Composer, and Node.js automatically
```

**Option B: XAMPP**
```bash
# Download from apachefriends.org
# Install and start Apache + MySQL modules
# Install PHP 8.2+ separately if needed
```

---

### 2. Clone the Repository

```bash
git clone https://github.com/your-username/hotel-platform.git
cd hotel-platform
```

---

### 3. Install PHP Dependencies

```bash
composer install
```

---

### 4. Install JavaScript Dependencies

```bash
npm install
npm run build
```

---

### 5. Environment Setup

```bash
# Copy the example environment file
cp .env.example .env

# Generate the application key
php artisan key:generate
```

Then open `.env` and configure your database:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=hotel_db
DB_USERNAME=root
DB_PASSWORD=
```

---

### 6. Database Setup

```bash
# Run migrations
php artisan migrate

# Seed with sample data (optional)
php artisan db:seed
```

---

### 7. Storage Link (for room images)

```bash
php artisan storage:link
```

---

### 8. Run the Application

```bash
php artisan serve
```

Visit **http://localhost:8000** in your browser.

---

## 📁 Project Structure

```
hotel-platform/
├── app/
│   ├── Http/
│   │   ├── Controllers/
│   │   │   ├── RoomController.php
│   │   │   ├── BookingController.php
│   │   │   ├── GuestController.php
│   │   │   └── AdminController.php
│   │   └── Middleware/
│   └── Models/
│       ├── Room.php
│       ├── Booking.php
│       └── User.php
├── database/
│   ├── migrations/
│   └── seeders/
├── public/
│   └── hotel_images/        ← Page1.png ... Page8.png
├── resources/
│   └── views/
│       ├── layouts/
│       ├── rooms/
│       ├── bookings/
│       └── admin/
├── routes/
│   └── web.php
└── storage/
    └── app/public/
```

---

## 🗄️ Database Schema

```
users          — id, name, email, password, role, timestamps
rooms          — id, name, type, description, price_per_night, capacity, status, timestamps
bookings       — id, user_id, room_id, check_in, check_out, status, total_price, timestamps
room_images    — id, room_id, image_path, is_primary, timestamps
```

---

## 👤 Default Admin Credentials

After seeding the database:

```
Email:    admin@hotel.com
Password: password
```

> ⚠️ Change these immediately in a production environment.

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add your feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
