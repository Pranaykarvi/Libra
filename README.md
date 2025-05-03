# 📈 Libra – AI-Powered Stock Prediction & Visualization Platform

![Banner](https://your-custom-image-or-banner-link.com)

**Libra** is an end-to-end, full-stack web application that enables users to:
- Visualize **real-time and historical stock prices**
- Predict **future stock trends** using deep learning
- Analyze **sentiment** from news and tweets
- Chat with a built-in **AI stock assistant**
- Manage portfolios, alerts, and more

---

## 🚀 Features

### 🧑‍💻 User System
- Secure authentication with **JWT** & **Google OAuth**
- PostgreSQL for user data
- Redis for session handling and caching
- Personalized dashboard with saved preferences

### 📊 Stock Data Visualization
- Interactive charts (candlesticks, volume, moving averages)
- WebSocket-powered **real-time updates**
- Multi-stock comparisons
- Filters for 1D, 1W, 1M, YTD, etc.

### 🤖 AI-Powered Stock Prediction
- **LSTM** and **Transformer** models for time-series prediction
- Show predicted trends with confidence intervals
- Display evaluation metrics: MSE, MAE, etc.
- Optional retraining via user data uploads (admin)

### 📰 News & Tweet Sentiment Analysis
- Scrape real-time financial news and tweets
- Use **FinBERT** or RoBERTa to detect sentiment
- Overlay sentiment analysis with stock charts

### 📥 Personal Tools
- ⭐️ Custom Watchlist
- 📈 Portfolio Tracker (simulated trading)
- 📧 Weekly Performance Emails
- 🔔 Price Alerts via Email or UI

### 💬 AI Stock Chatbot
- Ask about stock trends, news summaries, or predictions
- Get help navigating the site
- Learn how predictions were made (basic XAI)
- Powered by OpenAI or fine-tuned model

### 🧠 Explainable AI
- Visual feature attributions (via SHAP, Grad-CAM)
- Transparent insight into prediction logic

---

## 🛠️ Tech Stack

| Layer           | Tools |
|----------------|-------|
| Frontend        | Next.js, TailwindCSS, Chart.js, V0.dev |
| Backend         | FastAPI / Django |
| Authentication  | JWT, OAuth2 |
| Database        | PostgreSQL, Prisma / SQLAlchemy |
| Caching         | Redis |
| ML Model        | PyTorch (LSTM, Transformer) |
| Chatbot         | OpenAI API or HuggingFace |
| Model Serving   | FastAPI API / TorchServe |
| Deployment      | Docker, Vercel (frontend), Render/Fly.io (backend) |

---

## 🗂️ Project Structure
```
/libra
├── frontend/ # Next.js frontend
│ ├── pages/
│ ├── components/
│ └── charts/
├── backend/ # FastAPI/Django backend
│ ├── routes/
│ ├── auth/
│ ├── services/
│ └── chatbot/
├── ml_model/ # Model training + serving
│ ├── train_model.ipynb
│ ├── model.pt
│ └── predict.py
├── chatbot/ # Chatbot logic
│ └── chat_handler.py
├── scripts/ # Data fetchers and cron jobs
│ └── data_scraper.py
├── docker-compose.yml # Dev orchestration
└── README.md
```
---
## ⚙️ Local Setup

### Requirements
- Node.js & npm
- Python 3.8+
- Docker & Docker Compose
- PostgreSQL & Redis running locally

### 🔧 Getting Started

```bash
# Clone the repo
git clone https://github.com/yourusername/libra.git
cd libra

# Start Docker services
docker-compose up --build

# Frontend setup
cd frontend
npm install
npm run dev

# Backend setup
cd backend
pip install -r requirements.txt
uvicorn main:app --reload

```
---

## 🌐 Deployment

- **Frontend**: [Vercel](https://vercel.com/)
- **Backend**: [Render](https://render.com/), [Fly.io](https://fly.io/), or AWS EC2
- **Model API**: TorchServe or self-hosted FastAPI route

---

## 🤝 Contributing

We welcome PRs! To contribute:

1. Fork the repository
2. Create a new branch: `git checkout -b feature-name`
3. Commit your changes
4. Open a pull request

---

## 📄 License

Licensed under the MIT License. See `LICENSE` for details.

---

