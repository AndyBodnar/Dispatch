# 🚛 DISPATCH PLATFORM

**Powered by Trumbull Trucking**

A high-octane, cloud-based logistics and dispatch management system built to streamline load assignment, improve driver communication, and scale fleet operations with power and precision.

---

## 🧫 Overview

**Dispatch Platform** is a modular dispatch and logistics management system made up of independently deployable services and apps. It includes:

* 🧑‍🎼 **Admin Dashboard** – Web interface for dispatchers to create and manage loads
* 📱 **Driver App** – Mobile interface for drivers to receive loads and update statuses
* ⚙️ **API** – Core REST backend managing loads, users, auth, and statuses
* 🔔 **Push Notification Service** – Sends alerts to drivers using Firebase or similar
* ⏱️ **Scheduler Service** – Handles time-based load pushes and cron-style operations

---

## 🧱 Monorepo Structure

```bash
dispatch-platform/
├── api/                 # Backend REST API
├── admin-dashboard/     # React web frontend for dispatchers
├── driver-app/          # Flutter or React Native mobile app for drivers
├── push-service/        # Notification microservice
├── scheduler-service/   # Background job & load scheduler
├── docs/                # Diagrams, branding assets, notes
├── scripts/             # Dev tooling, CI/CD hooks
└── README.md            # You're reading it
```

---

## ✨ Features

### Admin Dashboard

* Add/edit/delete loads
* Assign loads to drivers (now or scheduled)
* View driver activity and load statuses
* Map integration for pickup/dropoff visualization

### Driver App

* Login and view assigned loads
* Load details: pickup, dropoff, notes, documents
* Accept/reject and update status (En Route → Delivered)
* Upload photos or proof of delivery
* Receive push notifications

### Core API

* RESTful API with secure auth (JWT)
* Load lifecycle management
* File upload support
* Role-based access (Driver vs Admin)

### Notification Service

* Sends push or in-app alerts for load activity
* Integrates with Firebase Cloud Messaging (FCM) or OneSignal
* Queue or webhook triggered

### Scheduler

* Scheduled load pushing
* Background cleanup or reminders
* Cron-like job execution

---

## 🚀 Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/YOUR_USERNAME/dispatch-platform.git
cd dispatch-platform
```

### 2. Set up modules (each can be bootstrapped independently)

For example:

```bash
cd api
npm install
npm run dev
```

Or:

```bash
cd driver-app
flutter pub get
flutter run
```

---

## 🛠️ Tech Stack

| Module               | Stack                          |
| -------------------- | ------------------------------ |
| API                  | Node.js (NestJS) or Express.js |
| Admin Dashboard      | React + Tailwind CSS           |
| Driver App           | Flutter or React Native        |
| Notification Service | Node.js + FCM/OneSignal        |
| Scheduler Service    | Node.js or Python + cron       |
| DB                   | PostgreSQL                     |
| Maps & Geolocation   | Google Maps API                |

---

## 🔐 Authentication

Uses secure JWT-based auth for both Admin and Driver roles. Tokens expire after X time. Refresh tokens optional for mobile.

---

## 🧪 Testing

* Unit tests for API routes
* E2E testing for load assignment
* Manual testing checklist in `/docs`
* CI/CD ready with GitHub Actions or custom hooks

---

## 🗸 Roadmap

* [x] Define project architecture
* [x] Set up monorepo with module structure
* [ ] Scaffold initial backend API
* [ ] Build out React admin panel
* [ ] Create Driver App UI
* [ ] Add push notifications
* [ ] Enable scheduled load pushes
* [ ] Launch MVP

---

## 🤘 Credits

Built by Andy Bodnar for [Trumbull Trucking](#) — redefining digital logistics, one load at a time.

---

## 📜 License

MIT License (or update if commercial/private)
