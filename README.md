# 🛒 Walmartart – AI-Powered Gamified Dashboard for Sustainability

A unified digital ecosystem to reduce food waste, empower associates, and engage eco-conscious customers through gamification and AI — built for Walmart’s sustainability initiatives.

---

## 🎯 Core Features

- **Perishable Rescue Alerts**  
  Real-time inventory alerts + AI-suggested actions (discount, donate, reposition).

- **Personal Sustainability Tracker**  
  Employee goal setting (e.g., carpooling, recycling), with gamified progress and badges.

- **Rescue Deals**  
  Highlight discounted near-expiry items with impact stats (e.g., "50L water saved").

- **Social Hub**  
  Friend challenges and storewide leaderboards. Become an “Eco-Influencer”.

- **Rewards Marketplace**  
  Redeem points for sustainable goods, donations, or Walmart cash.

---

## 🧩 Tech Stack

| Layer         | Technology                          |
|---------------|-------------------------------------|
| Frontend      | React.js, D3.js, Redux              |
| Backend       | Node.js (Express), FastAPI (ML)     |
| ML/AI         | Scikit-learn, joblib-loaded models  |
| Database      | PostgreSQL, Redis (cache/session)   |
| DevOps        | Docker, Railway/Heroku, Vercel      |
| Integrations  | Walmart Inventory, MSP, EDSP APIs   |

---

## 📂 Folder Breakdown

### `/client`
- React frontend app
- Recharts/D3 visualizations
- Redux store for points, badges, and rewards

### `/server`
- `index.js`: Sets up Express app
- `/routes`: API endpoints (`/alerts`, `/rewards`, `/goals`, etc.)
- `/ml`: ML model loader (joblib via Python microservice bridge)

### `/db/schema.sql`
- Tables: `users`, `items`, `actions`, `points`, `badges`

### `.env`
```
PORT=5000
DATABASE_URL=postgres://...
WALMART_API_KEY=...
REDIS_URL=redis://...
```

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/your-username/smart-retail.git
cd smart-retail
```

### 2. Set up backend
```bash
cd server
npm install
node index.js
```

### 3. Set up frontend
```bash
cd client
npm install
npm start
```

### 4. Set up DB
```bash
psql < db/schema.sql
```

---

## ⚙️ Development Notes

- Use mock Walmart API responses if real endpoints aren't accessible
- ML models saved as `.joblib` files; served via FastAPI/Python in `/ml`
- Badges and reward rules configurable from admin panel (TBD)

---

## 📈 Success Metrics

- ⏱️ 30% faster food rescue actions
- 🧑‍🤝‍🧑 2x increase in employee sustainability goal completion
- 🌱 3x more customer engagement with near-expiry "rescue deals"
- ♻️ 40% waste reduction in pilot stores

---

## 👥 Contributors
- Team RetailHack 2025
- Inspired by Walmart’s My Sustainability Plan (MSP)
