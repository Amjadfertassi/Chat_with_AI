# AI Chat Platform

Welcome to the **AI Chat Platform**! This platform enables real-time conversations with an AI assistant using **FastAPI** as the backend, integrated with **Groq AI** for responses.

## 🚀 Features
- **AI-powered Conversations** – Engage with an AI assistant using natural language.
- **FastAPI Backend** – Lightweight and efficient API handling.
- **Conversation Management** – Persistent conversation history.
- **CORS Middleware** – Secure cross-origin requests.
- **Environment Configuration** – API key handling via `.env` file.

## 🛠️ Tech Stack
### **Backend:**
- FastAPI (Python)
- Groq AI API
- Pydantic (Data Validation)
- dotenv (Environment Variable Management)
- Uvicorn (ASGI Server)

## 📦 Installation
Follow these steps to set up the AI Chat Platform locally:

### 1️⃣ Clone the Repository:


### 2️⃣ Create a Virtual Environment & Install Dependencies:
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt
```

### 3️⃣ Set Up Environment Variables:
Create a `.env` file in the root directory and configure:
```env
GROQ_API_KEY=your_groq_api_key
```

### 4️⃣ Run the Application:
```bash
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

The API should be running on `http://localhost:8000`.

## 📌 API Endpoints
### **POST /chat/**
Send a message to the AI assistant.
#### **Request Body:**
```json
{
  "message": "Hello AI!",
  "role": "user",
  "conversation_id": "12345"
}
```
#### **Response:**
```json
{
  "response": "Hello! How can I assist you today?",
  "conversation_id": "12345"
}
```

## 📌 Roadmap
- [ ] Implement user authentication.
- [ ] Add persistent database storage.
- [ ] Improve conversation context retention.
- [ ] Deploy to production.

## 🤝 Contributing
Contributions are welcome! If you'd like to contribute:
1. Fork the repository.
2. Create a new branch (`feature-branch`).
3. Commit your changes.
4. Open a pull request.

## 📄 License
This project is licensed under the **MIT License**.

## 📬 Contact
For questions or support, contact **Amjad** via email at `your-email@example.com`.

---
💡 *Built with passion and innovation!*
