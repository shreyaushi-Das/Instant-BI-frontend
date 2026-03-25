# InstantBI — Frontend

> Conversational AI for Instant Business Intelligence Dashboards
> Built by **Team Issue 4**

---

## 📌 What is InstantBI?

InstantBI lets non-technical users generate fully interactive business dashboards using plain English. No SQL. No BI tools. Just type what you want to see.

> _"Show me monthly revenue for Q3 broken down by region"_
> → Instant dashboard. Done.

---

## ✨ Features

- 📁 **CSV / Excel Upload** — Upload your own data file and start querying instantly
- 💬 **Natural Language Queries** — Type questions in plain English, get charts back
- 📊 **Smart Chart Selection** — AI picks the right chart type automatically (bar, line, pie, etc.)
- 🧠 **AI Insights** — Get auto-generated business insights alongside every chart
- 📤 **Share Report** — Share your dashboard with a link
- 📥 **Download Report** — Export your dashboard as a report
- 💡 **Follow-up Questions** — Chat with your dashboard to filter or refine results

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | React (Vite) |
| Charts | Recharts |
| Styling | Tailwind CSS |
| Deployment | Vercel |
| AI | Google Gemini API |

---

## 🏗️ Architecture Overview

```
User types natural language query
            ↓
React frontend sends query + CSV schema to backend
            ↓
Python backend sends schema + query to Gemini API
            ↓
Gemini returns SQL query + chart type
            ↓
Backend runs SQL on SQLite (converted from uploaded CSV)
            ↓
Results sent back to frontend as JSON
            ↓
Recharts renders the dashboard
```

---

## ⚙️ Getting Started

### Prerequisites
- Node.js v18+
- npm or yarn

### Installation

```bash
# Clone the repo
git clone [your frontend repo link]
cd instantbi-frontend

# Install dependencies
npm install

# Create environment file
cp .env.example .env
```

### Environment Variables

Create a `.env` file in the root:

```env
VITE_BACKEND_URL=your_render_backend_url
```

### Run Locally

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

---

## 🎯 How to Use

1. **Upload** your CSV or Excel file
2. **Type** a natural language question about your data
3. **View** the auto-generated dashboard with charts
4. **Read** AI-generated insights below the charts
5. **Chat** with your dashboard to filter or refine
6. **Share or Download** your report

---

## 👥 Team Issue 4

| Role | Responsibility |
|------|---------------|
| React Developer | Frontend, charts, API integration |
| UI/UX Designer | Design, styling, user flow |
| SQL/Data Engineer | CSV processing, SQLite, data pipeline |
| Python Developer | FastAPI backend, Gemini integration |

---

## 📄 License

This project was built for the Qualifier Hackathon.
