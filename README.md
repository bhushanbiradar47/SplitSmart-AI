# SplitSmart AI 💸

### AI-Powered Group Expense Splitting & Settlement Platform

**Live Demo:** https://split-smart-ai-three.vercel.app

## 📌 Overview

SplitSmart AI is an intelligent group expense management platform designed to make sharing expenses easier, faster and more transparent.

Whether it's a trip with friends, a shared apartment or a group outing, SplitSmart AI helps users record expenses, calculate individual shares, track balances and simplify settlements.

With AI-powered expense interpretation, users can enter expenses in natural language instead of filling out complicated forms.

## 🎯 Problem Statement

Managing shared expenses among friends and groups often leads to confusion, manual calculations and disagreements about who owes whom.

SplitSmart AI addresses these challenges through automated expense splitting, transparent balance tracking and AI-assisted expense entry.

## ✨ Key Features

- **Group Management:** Create expense groups and add members.
- **Smart Expense Splitting:** Automatically calculate equal shares with precise rounding.
- **AI Expense Interpretation:** Convert natural-language expense descriptions into structured expense details using Groq AI.
- **Balance Tracking:** View how much each member paid, owes and should receive.
- **Settlement Suggestions:** Simplify payments by calculating optimized settlement suggestions.
- **Expense Management:** Add, edit, delete, search and filter expenses.
- **Dashboard:** View group spending, transactions and member-wise breakdowns.
- **User Authentication:** Secure signup and login using Supabase Auth.
- **PayPal Sandbox Integration:** Demonstrate payment order creation, buyer approval and payment capture.

## 🤖 AI Integration

SplitSmart AI uses **Groq AI** to interpret natural-language expense entries.

For example:

> "Dinner cost ₹1200, paid by Rahul."

The AI extracts structured information such as the expense description, amount and payer.

Python validates the extracted information and performs the actual expense calculations. Users can review the interpreted details before saving.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| Flask | Web application framework |
| Groq AI | Natural-language expense interpretation |
| Supabase | Database and authentication |
| PostgreSQL | Data storage |
| PayPal Sandbox | Payment integration demonstration |
| HTML, CSS, JavaScript | Frontend development |
| Vercel | Application deployment |

## 🏗️ Architecture

1. Users interact with the Flask-powered web interface.
2. Supabase Auth handles user authentication.
3. Flask communicates with Supabase to store and retrieve expense data.
4. Groq AI interprets natural-language expense inputs.
5. Python validates inputs and calculates expense shares and balances.
6. PayPal Sandbox demonstrates the payment approval and capture workflow.

## 🚀 Run Locally

### Prerequisites

- Python 3.10 or later
- Git
- Supabase account
- Groq API key
- PayPal Developer Sandbox account

### Installation

Clone the repository:

```bash
git clone https://github.com/bhushanbiradar47/SplitSmart-AI
cd SplitSmart-AI
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
.\venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Create a `.env` file in the project root and configure:

```env
SUPABASE_URL=
SUPABASE_SECRET_KEY=
SUPABASE_PUBLISHABLE_KEY=
GROQ_API_KEY=
PAYPAL_CLIENT_ID=
PAYPAL_CLIENT_SECRET=
PAYPAL_BASE_URL=
SECRET_KEY=
FLASK_DEBUG=false
SESSION_COOKIE_SECURE=false
```

Fill in the values using your own service credentials. Never commit your `.env` file or expose API keys.

Configure the required Supabase database tables using the project's database schema.

Start the application:

```bash
python app.py
```

Open:

```text
http://127.0.0.1:5000/
```

## 💳 PayPal Integration

The project integrates PayPal Sandbox to demonstrate:

- Creating payment orders.
- Redirecting buyers for approval.
- Capturing approved payments.
- Recording payment status and capture details.

**Note:** PayPal is configured in Sandbox mode. Transactions are simulated and do not transfer real money or automatically settle group debts.

## 🔐 Security

- Environment variables are used for sensitive credentials.
- `.env` is excluded from Git using `.gitignore`.
- Flask sessions are configured with secure cookie options for HTTPS deployment.
- Authentication is handled through Supabase Auth.

## 🌐 Deployment

The application is deployed on Vercel.

**Live Application:** https://split-smart-ai-three.vercel.app

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

**Built for the PayPal AI Hackathon 2026.**
