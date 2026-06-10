FinBuddy is an intelligent, AI-powered financial assistant that helps users manage their money, grow their investments, and achieve financial freedom. Powered by GPT-5.1 and a multi-agent architecture, it provides personalized financial coaching 24/7.

🌟 Features
💰 Money Management
Automatic Transaction Tracking - Extract transactions from SMS, receipts, and bank statements
Smart Categorization - AI-powered expense classification (Needs, Essentials, Spends, Bills)
Spending Analysis - Visual breakdowns and trend analysis
Budget Recommendations - Personalized savings strategies
📈 Investment Planning
Risk Profiling - Comprehensive assessment of your risk tolerance
Portfolio Analysis - Track stocks, mutual funds, FDs, PPF, NPS
Stock Research - Real-time market data and analysis
SIP Planning - Goal-based investment recommendations
💳 Financial Products
Credit Card Matching - Find the best cards for your spending patterns
Tax Optimization - Old vs New regime comparison and 80C optimization
Loan Eligibility - EMI calculator and eligibility assessment
🤖 AI-Powered Agents
13 Specialized Agents across 3 orchestrators
Natural Language Interface - Ask questions in plain English
Context-Aware Responses - Personalized based on your financial profile
Real-time Streaming - Instant responses with streaming support
🖥️ Premium Dashboard Experience
Home Overview - Bento-grid layout with Financial Health Score and Cash Flow analysis.
Transactions Hub - Smart table with recurring payment detection and subscription management.
Investment Advisory - Split-view analysis: "Growth Generators" (Stocks/MFs) vs "Safety Net" (FDs/RDs).
Market Intelligence - AI-curated news feed with sentiment analysis and emerging trends.
Financial Toolkit - App-store style access to Tax, Loan, and Credit Card tools.
🏗️ Architecture
┌─────────────────────────────────────────────────────────────────┐
│                        Frontend (Next.js)                        │
│  ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐   │
│  │Dashboard│ │Transact │ │ Invest  │ │AI Chat  │ │ Credit  │   │
│  └────┬────┘ └────┬────┘ └────┬────┘ └────┬────┘ └────┬────┘   │
└───────┼──────────┼──────────┼──────────┼──────────┼──────────┘
        │          │          │          │          │
        ▼          ▼          ▼          ▼          ▼
┌─────────────────────────────────────────────────────────────────┐
│                    Backend API (FastAPI)                         │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │                    Agent Service                         │   │
│  │ ┌─────────────┐ ┌─────────────┐ ┌─────────────────────┐ │   │
│  │ │Orchestrator1│ │Orchestrator2│ │   Orchestrator 3    │ │   │
│  │ │   Money     │ │ Investment  │ │ Financial Products  │ │   │
│  │ │ Management  │ │             │ │                     │ │   │
│  │ └─────┬───────┘ └─────┬───────┘ └─────────┬───────────┘ │   │
│  │       │               │                   │             │   │
│  │ ┌─────┴─────┐   ┌─────┴─────┐      ┌─────┴─────┐       │   │
│  │ │ 6 Agents  │   │ 4 Agents  │      │ 3 Agents  │       │   │
│  │ └───────────┘   └───────────┘      └───────────┘       │   │
│  └─────────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────────┘
        │                    │                    │
        ▼                    ▼                    ▼
┌─────────────┐      ┌─────────────┐      ┌─────────────┐
│ PostgreSQL  │      │    Redis    │      │  ChromaDB   │
│  Database   │      │    Cache    │      │Vector Store │
└─────────────┘      └─────────────┘      └─────────────┘
🛠️ Tech Stack
Backend
Python 3.11+
FastAPI - Modern, fast web framework
SQLAlchemy - Async ORM with PostgreSQL
Redis - Caching and session management
Celery - Background task processing
LangChain - Agent orchestration
OpenAI GPT-5.1 - Language model
ChromaDB - Vector storage
Frontend
Next.js 14 - React framework
TypeScript - Type safety
Tailwind CSS - Styling
Redux Toolkit - State management
Framer Motion - Animations
Recharts - Data visualization
📦 Installation
Prerequisites
Python 3.11+
Node.js 18+
Docker & Docker Compose
OpenAI API key (with GPT-5.1 access)
1. Clone the Repository
git clone https://github.com/yourusername/finbuddy.git
cd finbuddy
2. Set Up Environment Variables
# Copy example env file
cp .env.example .env

# Edit with your values
nano .env
Required environment variables:

# OpenAI
OPENAI_API_KEY=your-api-key-here
OPENAI_MODEL=gpt-5.1

# Database
DATABASE_URL=postgresql+asyncpg://postgres:postgres@localhost:5432/finbuddy

# Redis
REDIS_URL=redis://localhost:6379/0

# JWT
JWT_SECRET_KEY=your-secret-key-here
3. Start Database Services
docker-compose up -d
4. Set Up Backend
cd backend

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run migrations (when available)
# alembic upgrade head

# Start server
uvicorn app.main:app --reload --port 8000
5. Set Up Frontend
cd frontend

# Install dependencies
npm install

# Start development server
npm run dev
6. Access the Application
Frontend: http://localhost:3000
Backend API: http://localhost:8000
API Docs: http://localhost:8000/docs
🤖 Agent System
Orchestrator 1: Money Management
Agent	Purpose
OCR Agent	Extract transactions from SMS, receipts, PDFs
Watchdog Agent	Detect anomalies and fraudulent transactions
Categorize Agent	Classify transactions into categories
Investment Detector	Identify recurring payments and SIPs
Money Growth Agent	Provide budgeting and savings advice
News Agent	Personal finance news and updates
Orchestrator 2: Investment
Agent	Purpose
Analysis Agent	Risk profiling and investment readiness
Stock Agent	Equity research and analysis
Investment Agent	Portfolio planning and recommendations
Market News Agent	Real-time market updates
Orchestrator 3: Financial Products
Agent	Purpose
Credit Card Agent	Card recommendations and comparison
ITR Agent	Tax calculation and optimization
Loan Agent	Eligibility and EMI calculation
📁 Project Structure
finbuddy/
├── backend/
│   ├── app/
│   │   ├── api/
│   │   │   ├── v1/
│   │   │   │   └── endpoints/
│   │   │   └── websocket/
│   │   ├── core/
│   │   ├── models/
│   │   ├── schemas/
│   │   └── services/
│   ├── agents/
│   │   ├── block_1/
│   │   ├── block_2/
│   │   ├── block_3/
│   │   ├── orchestrators/
│   │   ├── prompts/
│   │   └── tools/
│   └── requirements.txt
├── frontend/
│   ├── src/
│   │   ├── app/
│   │   │   ├── dashboard/
│   │   │   └── login/
│   │   ├── components/
│   │   ├── lib/
│   │   └── store/
│   └── package.json
├── docker-compose.yml
├── .env.example
└── README.md
🔒 Security
JWT-based authentication with refresh tokens
Password hashing with bcrypt
CORS configuration
Rate limiting
Input validation with Pydantic
🧪 Testing
# Backend tests
cd backend
pytest

# Frontend tests
cd frontend
npm test
📊 API Documentation
Once the backend is running, access the interactive API docs at:

Swagger UI: http://localhost:8000/docs
ReDoc: http://localhost:8000/redoc
🚀 Deployment
Docker (Recommended)
docker-compose -f docker-compose.prod.yml up -d
Manual
Set up PostgreSQL, Redis, and ChromaDB
Configure environment variables
Run backend with Gunicorn
Build and serve frontend with nginx
🤝 Contributing
Fork the repository
Create a feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request
📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

🙏 Acknowledgments
OpenAI for GPT-5.1
LangChain for agent orchestration
FastAPI for the amazing framework
The open-source community
Built with ❤️ for financial freedom# Finbuddy_AI_Based_Financial_Assistant
