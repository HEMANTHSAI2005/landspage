# 🎓 College Appointment System - Backend API

This is the backend API for a **College Appointment System** built using Node.js, Express, and MongoDB. It enables students to book appointments with professors, and allows professors to manage their availability and bookings.

## ✨ Features

- 🔐 User Authentication (JWT-based)
- 👨‍🏫 Professors can:
  - Define available appointment slots
  - View and manage appointments
- 👨‍🎓 Students can:
  - View professor availability
  - Book and cancel appointments
- 🗂 Role-based access control
- ✅ End-to-End automated test case
- 📬 Postman-ready API with complete routes

---

## 📁 Project Structure

college-appointment-system/
│
├── controllers/ # Business logic for auth, students, professors
│ ├── authController.js
│ ├── professorController.js
│ └── studentController.js
│
├── middleware/ # Authentication middleware
│ └── authMiddleware.js
│
├── models/ # Mongoose schemas
│ ├── User.js
│ └── Appointment.js
│
├── routes/ # API route handlers
│ ├── authRoutes.js
│ ├── professorRoutes.js
│ ├── studentRoutes.js
│ └── appointmentRoutes.js
│
├── tests/ # Automated E2E test
│ └── appointment.test.js
│
├── .env # Environment variables
├── app.js # Express app configuration
├── server.js # Server entry point
├── README.md # Project documentation
└── package.json # Dependencies and scripts

yaml
Copy
Edit

---

## ⚙️ Tech Stack

- **Backend:** Node.js, Express.js
- **Database:** MongoDB (with Mongoose ODM)
- **Authentication:** JWT
- **Testing:** Jest / Supertest
- **API Testing:** Postman

---

## 🚀 Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/your-username/college-appointment-system.git
cd college-appointment-system
2. Install dependencies
bash
Copy
Edit
npm install
3. Set up environment variables
Create a .env file in the root directory:

env
Copy
Edit
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
⚠️ Replace the values with your actual credentials.

4. Start the development server
bash
Copy
Edit
npm run dev
🧪 Running Automated Test
An end-to-end test is written to validate the full user flow (student registration, professor availability, booking, cancellation).

bash
Copy
Edit
npm run test
📮 API Endpoints
🔐 Auth
Method	Endpoint	Description
POST	/api/auth/register	Register a user (student or professor)
POST	/api/auth/login	Login and receive JWT

👨‍🏫 Professors
Method	Endpoint	Description
POST	/api/professors/availability	Define available time slots
GET	/api/professors/appointments	View all booked appointments
DELETE	/api/professors/cancel/:id	Cancel an appointment

👨‍🎓 Students
Method	Endpoint	Description
GET	/api/students/availability/:professorId	View available slots of a professor
POST	/api/students/book	Book an appointment
GET	/api/students/appointments	View your appointments

Authentication token (JWT) is required for protected routes.

📹 Deliverables
✅ API source code

✅ One end-to-end automated test

✅ Video 1: Automated test execution

✅ Video 2: Codebase & database explanation

✅ Video 3: Postman demo of full user flow

🧠 Author
Hemanth Sai
LinkedIn • GitHub

📝 License
This project is for evaluation purposes as part of an internship assignment. Not for commercial use.

yaml
Copy
Edit

---

Let me know if you'd like me to create the `appointment.test.js` file or generate a Postman Collection next.
