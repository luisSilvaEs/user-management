# **User Management Mini-App Challenge**

## **Overview**

Build a minimal full-stack app that lets users:

- Register a new account
- Log in
- View a table of all registered users (only after login)

You’ll use the existing backend (FastAPI, MongoDB, Beanie) and create a simple frontend (React or plain HTML/JS). The goal is to interact with authentication, user creation, protected routes, and data fetching.

---

## **Features**

### 1. Registration Form

- Fields: Name, Email, Password
- POSTs to `/users/create_user`
- Shows success or error message

### 2. Login Form

- Fields: Email, Password
- POSTs to `/users/login`
- Stores the returned token (in memory or localStorage)
- Shows error on failure

### 3. User List Table (Protected)

- After login, fetches `/users/list_users` (or similar endpoint)
- Displays a table: Name, Email, Registration Date
- Only accessible if logged in (token required in header)

---

## **Backend Touchpoints**

- User registration (`/users/create_user`)
- User login (`/users/login`)
- Fetching users (`/users/list_users` or create a new endpoint if needed)
- Token-based authentication (JWT or similar)

---

## **Stretch Goals (Optional)**

- Add a “Delete” button for each user (admin only)
- Add a “Logout” button
- Add basic form validation

---

## **Tech Stack**

- **Backend:** Use the provided FastAPI backend (no changes required unless you want to add endpoints)
- **Frontend:** Your choice (React, Vue, or plain HTML/JS)

---

## **Getting Started**

1. **Clone the backend repo and run it locally**
2. **Create a new frontend folder/project**
3. **Implement the forms and table as described**
4. **Ask for help here whenever you get stuck!**

---

## **Submission**

- Push your code to a GitHub repo (or share your folder)
- Include a short README with setup instructions

---

## **Example UI**

```bash
+-------------------+      +-------------------+
|   Register Form   |      |     Login Form    |
+-------------------+      +-------------------+
| Name:  _________  |      | Email:  ________  |
| Email: _________  |      | Password: ______  |
| Pass:  _________  |      | [Login]           |
| [Register]        |      +-------------------+
+-------------------+

After login:
+------------------------------------------+
|         Registered Users Table           |
+------------------------------------------+
| Name      | Email         | Registered   |
|-----------|---------------|--------------|
| Alice     | a@b.com       | 2025-07-03   |
| Bob       | bob@x.com     | 2025-07-02   |
+------------------------------------------+
```
