# Airbnb Clone – Backend Feature Requirements

## 1️⃣ User Authentication

**Objective:** Allow users to securely register, log in, and manage their accounts.

**Endpoints:**
- `POST /api/auth/register/` – Register a new user
- `POST /api/auth/login/` – User login
- `POST /api/auth/logout/` – User logout
- `GET /api/auth/profile/` – Get user profile
- `PUT /api/auth/profile/` – Update user profile

**Input Specifications:**
- `register`:
  - `username` (string, required, unique)
  - `email` (string, required, valid email format)
  - `password` (string, required, min 8 characters)
- `login`:
  - `email` or `username` (string, required)
  - `password` (string, required)

**Output Specifications:**
- Success: JSON with user details and auth token
- Failure: JSON with error message and status code

**Validation Rules:**
- Email must be unique
- Password must contain at least 1 uppercase, 1 lowercase, 1 number
- Required fields cannot be empty

**Performance Criteria:**
- API response time ≤ 500ms
- Handle up to 1000 concurrent login requests

---

## 2️⃣ Property Management

**Objective:** Allow hosts to create, update, view, and delete property listings.

**Endpoints:**
- `GET /api/properties/` – List all properties
- `GET /api/properties/{id}/` – View a specific property
- `POST /api/properties/` – Create a new property
- `PUT /api/properties/{id}/` – Update property details
- `DELETE /api/properties/{id}/` – Delete property

**Input Specifications:**
- `title` (string, required)
- `description` (string, required)
- `location` (string, required)
- `price_per_night` (decimal, required, >0)
- `host_id` (integer, required, foreign key to User)

**Output Specifications:**
- Success: JSON with property details
- Failure: JSON with error message

**Validation Rules:**
- Price must be a positive number
- Location and title must not exceed 255 characters
- Only the host who owns the property can update/delete it

**Performance Criteria:**
- API response time ≤ 600ms
- Support pagination for property lists (default 10 per page)

---

## 3️⃣ Booking System

**Objective:** Allow users to book properties and manage their bookings.

**Endpoints:**
- `POST /api/bookings/` – Create a booking
- `GET /api/bookings/` – List all user bookings
- `GET /api/bookings/{id}/` – View booking details
- `PUT /api/bookings/{id}/cancel/` – Cancel a booking

**Input Specifications:**
- `property_id` (integer, required)
- `user_id` (integer, required)
- `start_date` (date, required, YYYY-MM-DD)
- `end_date` (date, required, YYYY-MM-DD)
- `guests` (integer, required, >0)

**Output Specifications:**
- Success: JSON with booking details, status = "confirmed"
- Failure: JSON with error message, e.g., "Property not available"

**Validation Rules:**
- `end_date` must be after `start_date`
- Cannot book past dates
- Maximum guests must not exceed property capacity

**Performance Criteria:**
- Booking API response time ≤ 700ms
- Handle up to 500 concurrent bookings

---

## Notes
- All APIs must return appropriate HTTP status codes (200, 201, 400, 404, 500)
- All endpoints require authentication except `register` and `login`
- APIs must follow RESTful conventions

