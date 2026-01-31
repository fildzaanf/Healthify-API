# Healthify : Health Care System
Healthify is a digital health platform that provides consultation services with doctors, ordering medicines, and health information through articles or Chatbot integrated with Artificial Intelligence

## 📚 Documentation
* [Healthify - User](https://healthify-reactapp.vercel.app/)
* [Healthify - Doctor](https://healthify-doctor.vercel.app/login)
* [Healthify - Admin](https://healthify-admin.vercel.app/login)
* [Healthify GitHub Organization](https://github.com/Health-Care-System)
  
## 🚀 Tools and Technologies 
- Go Programming Language
- Echo Go Framework
- GORM for Object Relational Mapping
- MySQL for Relational Database
- JSON Web Token for Authentication
- Docker for Containerization
- CI/CD Pipeline using GitHub Actions
- Large Language Model (LLM) with Generative Pre-trained Transformer (GPT)
- ChatBot with Prompt Engineering
- Go Testify for Unit Test

## 🏛️ System Design and Architecture
- Domain-Driven Design (DDD)
- Model View Controller (MVC) Architecture
- REST API

## ✨ Features

* Admin Features

| Feature                          | Description                                                                                                              |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Authentication & Profile         | Handles login, profile retrieval, profile updates, password management, and OTP-based security verification              |
| User Management                  | Allows viewing all users, retrieving user details by ID, and deleting users from the system                              |
| Doctor Management                | Provides functionality to register new doctors, view all doctors, update doctor information, and delete doctors          |
| Consultation Payments Management | Enables managing doctor payment transactions, updating payment statuses, and retrieving transactions per doctor or user  |
| Medicines Management             | Supports adding, updating, viewing, and deleting medicines, including management of medicine images                      |
| Medicines Payment Management     | Facilitates viewing and updating checkout transactions for medicines                                                     |

* User Features

| Feature                  | Description                                                                                                        |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| Authentication & Profile | Enables user registration, login, OTP verification, profile viewing, profile updating, and password reset          |
| Doctor Management        | Allows users to browse doctors by specialization, check available doctors, and view detailed doctor profiles       |
| Medicines Managemnet     | Provides access to all medicines and detailed information per medicine                                             |
| Consultation Payments    | Supports creating doctor payment transactions, viewing all transactions, and retrieving transaction details by ID  |
| Consultation with Doctor | Allows creating chat rooms, viewing messages, and sending complaint messages                                       |
| Medicines Payments       | Enables creating medicine transactions, viewing and deleting transactions, and managing checkouts                  |
| Articles Management      | Provides access to all articles, viewing article details, and searching articles by title                          |
| Customer Service         | Facilitates contacting customer service for support and inquiries                                                  |
| Chatbot                  | Allows public users to interact with the AI Chatbot to obtain information and guidance                             |

* Doctor Features

| Feature                  | Description                                                                                                                |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------- |
| Authentication & Profile | Supports login, profile retrieval, profile updates, status management, password reset, and OTP verification.               |
| Articles Management      | Enables creating, viewing, updating, and deleting articles.                                                                |
| Consultation with Users  | Provides functionality to view all consultations, manage chat rooms, access specific chat rooms, and send advice messages. |
| Users Management         | Allows accessing managed users and updating their associated transactions.                                                 |
| Medicines Management     | Provides access to all medicines.                                                                                          |

## 📡 API Endpoints

### Admins

* Authentication & Profile

| Method | Endpoint                       | Description          |
| ------ | ------------------------------ | -------------------- |
| POST   | /api/v1/admins/login           | Login admin          |
| GET    | /api/v1/admins/profile         | Get admin profile    |
| PUT    | /api/v1/admins/profile         | Update admin profile |
| POST   | /api/v1/admins/get-otp         | Get OTP for password |
| POST   | /api/v1/admins/verify-otp      | Verify OTP           |
| POST   | /api/v1/admins/change-password | Reset password       |

* Users by Admin

| Method | Endpoint                     | Description    |
| ------ | ---------------------------- | -------------- |
| GET    | /api/v1/admins/users         | Get all users  |
| GET    | /api/v1/admins/user/:user_id | Get user by ID |
| DELETE | /api/v1/admins/user/:user_id | Delete user    |

* Doctors by Admin

| Method | Endpoint                         | Description      |
| ------ | -------------------------------- | ---------------- |
| POST   | /api/v1/admins/doctors/register  | Register doctor  |
| GET    | /api/v1/admins/doctors           | Get all doctors  |
| GET    | /api/v1/admins/doctor/:doctor_id | Get doctor by ID |
| PUT    | /api/v1/admins/doctor/:doctor_id | Update doctor    |
| DELETE | /api/v1/admins/doctor/:doctor_id | Delete doctor    |

* Consultation Doctor Payments by Admin

| Method | Endpoint                                       | Description                  |
| ------ | ---------------------------------------------- | ---------------------------- |
| PUT    | /api/v1/admins/doctor-payments/:transaction_id | Update payment status        |
| GET    | /api/v1/admins/doctor-payment/:user_id         | Get user payments            |
| GET    | /api/v1/admins/doctor-payments                 | Get all doctor payments      |
| GET    | /api/v1/admins/doctor-payment                  | Get doctor transaction by ID |

* Medicines by Admin

| Method | Endpoint                                    | Description           |
| ------ | ------------------------------------------- | --------------------- |
| POST   | /api/v1/admins/medicines                    | Create medicine       |
| GET    | /api/v1/admins/medicines                    | Get all medicines     |
| GET    | /api/v1/admins/medicines/:medicine_id       | Get medicine by ID    |
| PUT    | /api/v1/admins/medicines/:medicine_id       | Update medicine       |
| DELETE | /api/v1/admins/medicines/:medicine_id       | Delete medicine       |
| GET    | /api/v1/admins/medicines/:medicine_id/image | Get medicine image    |
| PUT    | /api/v1/admins/medicines/:medicine_id/image | Update medicine image |
| DELETE | /api/v1/admins/medicines/:medicine_id/image | Delete medicine image |

* Medicines Payment by Admin

| Method | Endpoint                                                | Description        |
| ------ | ------------------------------------------------------- | ------------------ |
| PUT    | /api/v1/admins/medicines-payments/checkout/:checkout_id | Update checkout    |
| GET    | /api/v1/admins/medicines-payments/checkout              | Get all checkouts  |
| GET    | /api/v1/admins/medicines-payments/checkout/:checkout_id | Get checkout by ID |

### Users

* Authentication & Profile

| Method | Endpoint                       | Description               |
| ------ | ------------------------------ | ------------------------- |
| POST   | /api/v1/users/register         | Register user             |
| POST   | /api/v1/users/login            | Login user                |
| POST   | /api/v1/users/OTP-verification | Verify OTP after register |
| GET    | /api/v1/users/profile          | Get user profile          |
| PUT    | /api/v1/users/profile          | Update user profile       |
| DELETE | /api/v1/users                  | Delete user               |
| POST   | /api/v1/users/get-otp          | Get OTP for password      |
| POST   | /api/v1/users/verify-otp       | Verify OTP                |
| POST   | /api/v1/users/change-password  | Reset password            |

* Doctors

| Method | Endpoint                         | Description                   |
| ------ | -------------------------------- | ----------------------------- |
| GET    | /api/v1/users/doctors/available  | Get available doctors         |
| GET    | /api/v1/users/doctors            | Get doctors by specialization |
| GET    | /api/v1/users/doctors/:doctor_id | Get doctor by ID              |

* Medicines

| Method | Endpoint                             | Description        |
| ------ | ------------------------------------ | ------------------ |
| GET    | /api/v1/users/medicines              | Get all medicines  |
| GET    | /api/v1/users/medicines/:medicine_id | Get medicine by ID |

* Consultation Doctor Payments

| Method | Endpoint                                      | Description                  |
| ------ | --------------------------------------------- | ---------------------------- |
| POST   | /api/v1/users/doctor-payments/:doctor_id      | Create doctor transaction    |
| GET    | /api/v1/users/doctor-payments                 | Get all doctor transactions  |
| GET    | /api/v1/users/doctor-payments/:transaction_id | Get doctor transaction by ID |

* Roomchats / Messages

| Method | Endpoint                                 | Description              |
| ------ | ---------------------------------------- | ------------------------ |
| POST   | /api/v1/users/chats/:transaction_id      | Create room chat         |
| GET    | /api/v1/users/chats/:roomchat_id         | Get room chat            |
| POST   | /api/v1/users/chats/:roomchat_id/message | Create complaint message |

* Medicines Payments by User

| Method | Endpoint                                               | Description                    |
| ------ | ------------------------------------------------------ | ------------------------------ |
| POST   | /api/v1/users/medicines-payments                       | Create medicine transaction    |
| GET    | /api/v1/users/medicines-payments                       | Get all medicine transactions  |
| GET    | /api/v1/users/medicines-payments/:medtrans_id          | Get medicine transaction by ID |
| DELETE | /api/v1/users/medicines-payments/:medtrans_id          | Delete medicine transaction    |
| POST   | /api/v1/users/medicines-payments/checkout              | Create checkout                |
| GET    | /api/v1/users/medicines-payments/checkout              | Get user checkouts             |
| GET    | /api/v1/users/medicines-payments/checkout/:checkout_id | Get checkout by ID             |

* Articles

| Method | Endpoint                           | Description              |
| ------ | ---------------------------------- | ------------------------ |
| GET    | /api/v1/users/articles             | Get all articles         |
| GET    | /api/v1/users/articles/:article_id | Get article by ID        |
| GET    | /api/v1/users/article              | Search articles by title |

* Customer Service

| Method | Endpoint                       | Description              |
| ------ | ------------------------------ | ------------------------ |
| POST   | /api/v1/users/customer-service | Contact customer service |

