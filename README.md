# 💰 FinBuddy – AI-Powered Financial Assistant Coach

FinBuddy is an intelligent AI-powered financial assistant designed to help users manage expenses, optimize investments, improve savings habits, and achieve long-term financial goals. Built with a multi-agent AI architecture powered by GPT-5.1, FinBuddy delivers personalized financial guidance, portfolio insights, budgeting recommendations, and financial product suggestions through a modern and interactive dashboard.

## 🚀 Key Features

### 💳 Smart Money Management

* Automatic transaction extraction from SMS, receipts, and bank statements
* AI-powered expense categorization and spending analysis
* Personalized budgeting and savings recommendations
* Cash flow tracking and financial health monitoring

### 📈 Investment Planning

* Risk profiling and investment readiness assessment
* Portfolio analysis across stocks, mutual funds, FDs, PPF, and NPS
* SIP planning and goal-based investment recommendations
* AI-assisted stock research and market intelligence

### 🏦 Financial Products

* Credit card recommendation engine
* Tax optimization and old vs new regime comparison
* Loan eligibility assessment and EMI calculations

### 🤖 Multi-Agent AI Architecture

* 13 specialized AI agents coordinated through 3 orchestrators
* Context-aware financial conversations
* Natural language interaction
* Real-time streaming responses

### 📊 Premium Analytics Dashboard

* Financial Health Score tracking
* Smart transaction management
* Subscription and recurring payment detection
* Investment performance monitoring
* AI-curated financial news and sentiment analysis

## 🛠️ Tech Stack

### Backend

* Python 3.11+
* FastAPI
* SQLAlchemy
* PostgreSQL
* Redis
* Celery
* LangChain
* OpenAI GPT-5.1
* ChromaDB

### Frontend

* Next.js 14
* TypeScript
* Tailwind CSS
* Redux Toolkit
* Framer Motion
* Recharts

### Infrastructure

* Docker & Docker Compose
* JWT Authentication
* WebSockets
* REST APIs

## 🏗️ System Architecture

Frontend (Next.js) → FastAPI Backend → Multi-Agent AI Layer → PostgreSQL / Redis / ChromaDB

The platform uses three dedicated orchestrators:

1. **Money Management Orchestrator**

   * Transaction Analysis
   * Expense Categorization
   * Fraud Detection
   * Budget Planning

2. **Investment Orchestrator**

   * Risk Assessment
   * Portfolio Analysis
   * Stock Research
   * Market Intelligence

3. **Financial Products Orchestrator**

   * Credit Card Matching
   * Tax Optimization
   * Loan Advisory

## 🔒 Security Features

* JWT Authentication
* Password Hashing (bcrypt)
* Input Validation (Pydantic)
* Rate Limiting
* Secure API Design
* CORS Protection

## 🎯 Project Highlights

* Multi-Agent AI Financial Assistant
* Full-Stack Production Architecture
* Real-Time Financial Analytics
* Personalized Financial Coaching
* Modern Dashboard Experience
* Scalable Microservice-Friendly Design

Built with ❤️ to make financial planning smarter, simpler, and more accessible.

