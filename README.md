# 🔗 URL Shortener Web App

This is a full-stack **URL Shortener Application** built using **Node.js (Express)** for the backend and **React.js (Vite)** for the frontend. The app allows users to register, log in, and generate short URLs that redirect to the original long links.

---

## 🚀 Features

- 🔐 User Authentication (Register/Login)
- ✂️ URL Shortening with unique short codes
- 📜 Dashboard to manage your shortened URLs
- 📈 Redirect handling and data storage
- 🧠 Modular codebase using MVC structure

---

## 🛠️ Tech Stack

**Frontend:**
- React + Vite
- Tailwind CSS (optional)
- Axios
- Redux Toolkit

**Backend:**
- Node.js
- Express.js
- MongoDB (Mongoose)
- JWT for auth

---

## 📁 Project Structure

```
URL_SHORTENER/
├── BACKEND/        # Express backend
├── FRONTEND/       # React frontend
```

---

## 🧑‍💻 How to Run Locally

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/RajGauravTiwari
/URL_SHORTENER.git
cd URL_SHORTENER
```

---

### 2️⃣ Set Up the Backend

```bash
cd BACKEND
npm install
```

- Create a `.env` file inside `/BACKEND` folder and add the following:
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

- Run the backend:
```bash
node app.js
```

---

### 3️⃣ Set Up the Frontend

```bash
cd ../FRONTEND
npm install
npm run dev
```

- Make sure your backend is running on port 5000 and frontend on 5173 (default).

---

## 🖥️ Usage

1. Register or log in with your account.
2. Enter a long URL to generate a shortened link.
3. Copy and share the shortened link.
4. Visit your dashboard to view or manage all your URLs.

---

## 🤝 Contributing

Feel free to open issues or submit PRs!

---


## 🙌 Acknowledgements

- MongoDB
- Express
- React + Vite
- Redux Toolkit
