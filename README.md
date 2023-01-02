# AI Chat Platform

A lightweight, real-time AI chat platform built with **FastAPI** and **Groq AI**.

## 🚀 Features
- **AI Conversations** – Natural language interactions.
- **FastAPI Backend** – Efficient & scalable API.
- **Persistent Chats** – Session-based conversation history.
- **CORS Support** – Secure cross-origin access.
- **.env Config** – Easy API key management.

## 🛠️ Tech Stack
- FastAPI (Python)
- Groq AI API
- Pydantic (Validation)
- Uvicorn (Server)

## 📦 Setup
```bash
git clone https://github.com/your-repo/ai-chat-platform.git
cd ai-chat-platform
python -m venv venv
source venv/bin/activate  # Windows: `venv\Scripts\activate`
pip install -r requirements.txt
```

### 🔧 Environment Variables:
Create a `.env` file:
```env
GROQ_API_KEY=your_groq_api_key
```

### 🚀 Run the Server:
```bash
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```
Access the API at `http://localhost:8000`.

## 📌 API Endpoint
**POST /chat/** – Send a message to AI.
```json
{
  "message": "Hello AI!",
  "role": "user",
  "conversation_id": "12345"
}
```
**Response:**
```json
{
  "response": "Hello! How can I assist?",
  "conversation_id": "12345"
}
```

## 📌 Roadmap
- [ ] User authentication
- [ ] Database storage
- [ ] Improved context retention
- [ ] Deployment

## 🤝 Contribute
Fork, branch, commit, and PR your improvements!

## 📄 License
**MIT License**

## 📬 Contact
For support, reach out to **Amjad** at `your-email@example.com`.

---
💡 *Simple. Fast. Intelligent.*
