# Quick Start Guide

## 🚀 Get Running in 5 Minutes

### Prerequisites
- Node.js installed
- MongoDB Atlas account (free: mongodb.com/cloud/atlas)

### Setup

1. **Clone & Install**
   ```bash
   cd MINI-URL
   
   # Backend
   cd BACKEND && npm install && cd ..
   
   # Frontend
   cd FRONTEND && npm install && cd ..
   ```

2. **Configure Environment**
   
   **BACKEND/.env**
   ```env
   NODE_ENV=development
   MONGO_URI=mongodb+srv://your_user:your_password@cluster.mongodb.net/mini-url
   JWT_SECRET=your_super_secret_key_here
   PORT=3000
   FRONTEND_URL=http://localhost:5173
   ```

   **FRONTEND/.env**
   ```env
   VITE_API_BASE_URL=http://localhost:3000
   ```

3. **Start the App**
   
   Terminal 1 (Backend):
   ```bash
   cd BACKEND
   npm run dev
   ```
   
   Terminal 2 (Frontend):
   ```bash
   cd FRONTEND
   npm run dev
   ```

4. **Open Browser**
   - Navigate to: http://localhost:5173
   - Register → Login → Create Short URLs!

---

## 📋 What Each Endpoint Does

| Action | Endpoint | Method |
|--------|----------|--------|
| Register | `/api/auth/register` | POST |
| Login | `/api/auth/login` | POST |
| Create Short URL | `/api/create` | POST |
| Get My URLs | `/api/user/all-urls` | GET |
| Use Short URL | `/:id` | GET (redirect) |
| Delete URL | `/api/user/delete/:id` | DELETE |

---

## 🔧 Example Flow

1. **User visits app** → http://localhost:5173
2. **Register** → POST to `/api/auth/register`
3. **Login** → POST to `/api/auth/login` → JWT token in cookie
4. **Enter long URL** → POST to `/api/create` with auth header
5. **Get short URL** → Frontend displays: `http://localhost:3000/abc123`
6. **Share link** → Anyone can visit `http://localhost:3000/abc123` → redirects to original

---

## ⚠️ Troubleshooting

**Port already in use?**
```bash
# Change in BACKEND/.env
PORT=3001
```

**MongoDB connection failed?**
- Check username/password in MONGO_URI
- Whitelist your IP in MongoDB Atlas (0.0.0.0/0 for dev)

**Frontend can't reach backend?**
- Ensure backend is running on port 3000
- Check VITE_API_BASE_URL in FRONTEND/.env

---

See [DEPLOYMENT_GUIDE.md](./DEPLOYMENT_GUIDE.md) for production deployment.
