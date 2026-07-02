[![Enroll on Udemy](https://img.shields.io/badge/Udemy-A435F0?style=for-the-badge&logo=udemy&logoColor=white)](https://dub.sh/djAI-ghb)

# Build AI Employees with Django — Agentic AI for Developers

A complete AI-powered customer support system built with Django, Claude API & RAG (Retrieval-Augmented Generation).
Three AI agents collaborate autonomously to handle customer queries, make refund 
decisions, detect fraud, and search real company documents & policies — all streaming live 
to a monitoring dashboard.

---

## What's Inside

**Maya** — AI support agent that handles customer queries, checks orders, 
verifies delivery status, searches company documents, and decides when to escalate.

**Manager Agent** — Reviews escalated cases and makes refund decisions. 
Consults the risk agent when fraud is suspected.

**Risk Agent** — Analyses customer patterns and returns a fraud verdict 
to the manager.

**RAG System** — Agents search real company PDF documents before answering 
policy questions. No hallucination. Real answers from real documents.

**Live Dashboard** — Staff can watch every agent decision, tool call, 
and escalation stream in real time.

---

## Tech Stack

- Python 3.14
- Django 6.0
- Anthropic Claude API
- ChromaDB (RAG / Vector Database)
- MySQL
- Server Sent Events (SSE)
- Bootstrap 5
- Railway (Deployment)

---

## Watch Demo

🚀 [Watch Now](https://youtu.be/qyq0YGo10sU)

---

## Want to Build This Yourself?

This project is the outcome of my Django + Agentic AI course on Udemy.
You'll build every single piece of this from scratch — agents, tools, 
RAG, dashboard, SSE streaming, and full deployment.

👉 [Enroll on Udemy](https://dub.sh/djAI-ghb)

[![Enroll on Udemy](https://img.shields.io/badge/Udemy-A435F0?style=for-the-badge&logo=udemy&logoColor=white)](https://dub.sh/djAI-ghb)

---

## Setup Instructions

### 1. Create a Project Folder and Clone the Repo

```bash
mkdir coolbreeze-ai
cd coolbreeze-ai
git clone https://github.com/dev-rathankumar/coolbreeze-ai-public.git .
```

### 2. Create and Activate Virtual Environment

**Mac/Linux:**
```bash
python3 -m venv env
source env/bin/activate
```

**Windows:**
```bash
python -m venv env
env\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Create `.env` File

Create a file called `.env` in the project root and add the following:

```dotenv
SECRET_KEY=your-secret-key-here
DEBUG=True

ANTHROPIC_API_KEY=your-anthropic-api-key
ANTHROPIC_MODEL=claude-sonnet-4-6

ALLOWED_HOSTS=127.0.0.1,localhost
```

> **Note:** You'll need an Anthropic API key to run the AI agents.
> New accounts may receive $5 free credits — enough to fully explore this project.
> Get your key at [console.anthropic.com](https://console.anthropic.com)


### 5. Run Migrations

```bash
python manage.py migrate
```

### 6. Load Demo Data

```bash
python manage.py loaddata demo_data.json
```

### 7. Create Superuser (Admin Access)

```bash
python manage.py createsuperuser
```

### 8. Load Documents into ChromaDB (RAG)

```bash
python manage.py shell
```

```python
from support.rag import load_documents
load_documents()
exit()
```

### 9. Run the Server

```bash
python manage.py runserver
```

### 10. Open in Browser
```
Customer Orders:    http://127.0.0.1:8000/orders/
Live Streaming Dashboard:  http://127.0.0.1:8000/support/dashboard/
Admin Panel:        http://127.0.0.1:8000/admin/
```
**Demo Login Credentials:**

| Username | Password | Role |
|----------|----------|------|
| techwithrathan | techwithrathan | Customer |
| fraud_test | techwithrathan | Test fraud detection |
| admin | your superuser password | Staff dashboard |

---

## Troubleshooting

**ChromaDB downloads embedding model on first run (~79MB) — this is normal.**

**Anthropic API error?**
Make sure your `ANTHROPIC_API_KEY` is valid and has available credits.

**Demo data not loading?**
Make sure you ran `python manage.py migrate` before `loaddata`.

---
## Want to Build This Yourself?

Cloning this repo gives you the finished project — but building it 
yourself is a completely different experience.

When you build it from scratch, you'll be able to:

- Explain exactly how the agent loop works in an interview
- Describe how tool calling enables agents to make decisions
- Walk through how RAG retrieves the right document chunks
- Show how SSE streams live agent activity to the dashboard

That's the difference between having a project and understanding a project.

**This course teaches you to build every single piece of this from scratch.**
You'll understand every line of code deeply enough to explain it, extend it,
and build your own version. LangChain edition included as a free update.

[![Enroll on Udemy](https://img.shields.io/badge/Udemy-A435F0?style=for-the-badge&logo=udemy&logoColor=white)](https://dub.sh/djAI-ghb)


