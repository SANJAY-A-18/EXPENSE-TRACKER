# 💼 Expense Tracker — Receipt Parser & AI Chatbot

A full-stack Expense Tracker web app featuring receipt OCR parsing, family/group expense management, AI-powered insights, and a conversational chatbot for querying financial data. Primarily designed for Indian users with INR support, but easily adaptable.

---

## 🚀 Features

- Single-page frontend (HTML/CSS/Vanilla JS) with registration, login, and family/profile management
- Manual expense entry and receipt image uploads with OCR-based extraction
- Summary reports, monthly comparisons, family aggregates, and CSV/PDF export
- Light/dark mode toggle for better user experience
- Backend REST API with authentication, expense CRUD, and reporting
- Receipt parsing using EasyOCR plus lightweight NLP for shop, date, category, and amount extraction
- AI-powered insights leveraging LangChain + local LLM (e.g., Ollama/Mistral) and Chroma for embeddings
- Scheduled report generation and email delivery

---

## 🛠 Tech Stack

- **Frontend:** HTML5, CSS3, Vanilla JavaScript, Fetch API
- **Backend:** Python (FastAPI), SQL (any RDBMS), DAO pattern
- **OCR/NLP:** EasyOCR, scikit-learn, regex
- **AI:** LangChain, Ollama/Mistral (or any LLM), ChromaDB
- **Data Handling:** Pandas, Matplotlib, FPDF (PDF generation)

---

## ⚙️ Quick Start

### Backend (Unix / macOS)
```bash
git clone <backend-repo-url>
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Set environment variables or create .env (DB URL, SECRET_KEY, etc.)
uvicorn api:app --reload
```

### Backend (Windows - PowerShell)
```powershell
git clone <backend-repo-url>
cd backend
python -m venv venv
.\venv\Scripts\Activate.ps1
pip install -r requirements.txt

# Set environment variables / .env for DB URL, SECRET_KEY, etc.
uvicorn api:app --reload
```

> Notes:
> - For Command Prompt, activate with `venv\Scripts\activate.bat`
> - Replace `api:app` with your ASGI app if different (like `main:app`)

### Frontend
- Open `index.html` in a browser or serve via static server (e.g., `live-server` or `python -m http.server`)
- Update API base URL in frontend JS (`app.js`) if needed

### Receipt Parser (Local)
```bash
cd receipt-parser
python -m venv venv
source venv/bin/activate  # or on Windows PowerShell: .\venv\Scripts\Activate.ps1
pip install -r requirements.txt

# Minimal installation
pip install easyocr scikit-learn pandas
python test_receipt.py --image path/to/receipt.jpg
```

### Chatbot (LLM Backend)

1. Start and configure Ollama (or other LLM provider), pull required models:
```bash
ollama pull mistral
ollama pull nomic-embed-text
```

2. Install Python dependencies and run chatbot backend:
```bash
pip install -r requirements.txt
uvicorn app:app --reload
```

3. Access chatbot UI via `cb.html` or run console client `chat.py` if available.

---

## 💡 Usage

- Register or login, create/join family groups  
- Add expenses manually or upload receipts for OCR parsing  
- Generate and export reports (CSV/PDF)  
- Ask the AI chatbot questions on spend patterns, insights, and advice  

---

## 📁 Project Structure Example

BACK_END/ # FastAPI backend: api.py, dao.py, models, etc.
FRONT_END/ # index.html, cb.html, css/, js/
RECEIPT_PARSER/ # Receipt OCR and NLP scripts and utils
CHAT_BOT/ # Chatbot service, embeddings, datasets
README.md

---

## 🚧 Future Enhancements

- Multilingual OCR + PDF invoice support  
- Personalized AI-driven financial recommendations  
- Mobile app (React Native, Flutter)  
- Production deployment guides, CI/CD pipelines, security hardening  

---

## 🪪 License

MIT License

---

## 👤 Author

Sanjay A

---

### ⭐ If you find this project helpful, please star it on GitHub!
