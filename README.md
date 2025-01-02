# AI Chat Platform

A lightweight, real-time AI chat platform built with **FastAPI** and **Groq AI**, offering natural language interactions with state-of-the-art AI models.

## 🎯 Overview
This platform provides a robust backend for AI-powered conversations, featuring session persistence, real-time responses, and a clean API interface.

## 🚀 Features
- **AI Conversations** – Natural language interactions powered by Groq AI
- **FastAPI Backend** – High-performance async API with automatic OpenAPI docs
- **Persistent Chats** – Session-based conversation history with context retention
- **CORS Support** – Secure cross-origin access for web integration
- **.env Config** – Secure environment variable management
- **Real-time Processing** – Immediate response handling
- **Error Handling** – Robust error management and graceful fallbacks

## 🛠️ Tech Stack
- **Backend Framework**: FastAPI (Python 3.8+)
- **AI Provider**: Groq AI API
- **Data Validation**: Pydantic v2
- **Server**: Uvicorn (ASGI)
- **Development**: Python virtual environment

## 📦 Installation & Setup

### Prerequisites
- Python 3.8 or higher
- pip package manager
- Git

### Setup Steps
```bash
# Clone the repository
git clone https://github.com/your-repo/ai-chat-platform.git
cd ai-chat-platform

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # Windows: `venv\Scripts\activate`

# Install dependencies
pip install -r requirements.txt
```

### 🔧 Configuration
1. Create a `.env` file in the project root:
```env
GROQ_API_KEY=your_groq_api_key
CORS_ORIGINS=["http://localhost:3000"]  # Add your frontend URLs
DEBUG=True  # Set to False in production
```

### 🚀 Running the Server
```bash
# Development mode
uvicorn main:app --host 0.0.0.0 --port 8000 --reload

# Production mode
uvicorn main:app --host 0.0.0.0 --port 8000 --workers 4
```

Access the API documentation at:
- OpenAPI UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`

## 🔌 API Reference

### Chat Endpoint
**POST /chat/**
Create or continue an AI conversation.

**Request Body:**
```json
{
    "message": "Hello AI!",
    "role": "user",
    "conversation_id": "12345"  // Optional
}
```

**Response:**
```json
{
    "response": "Hello! How can I assist you today?",
    "conversation_id": "12345",
    "created_at": "2024-03-21T10:30:00Z"
}
```

**Error Responses:**
- `400 Bad Request`: Invalid input
- `429 Too Many Requests`: Rate limit exceeded
- `500 Internal Server Error`: Server-side error

## 🔒 Security
- API key authentication
- Rate limiting
- Input validation
- CORS protection

## 📈 Roadmap
- [ ] User authentication & authorization
- [ ] PostgreSQL database integration
- [ ] WebSocket support for real-time chat
- [ ] Multiple AI model support
- [ ] Chat history visualization
- [ ] Docker containerization
- [ ] CI/CD pipeline
- [ ] Cloud deployment guides

## 🤝 Contributing
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🐛 Bug Reports
Report bugs by opening an issue. Include:
- Description of the bug
- Steps to reproduce
- Expected behavior
- Screenshots (if applicable)
- Environment details

## 📄 License
This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## 📬 Contact & Support
- **Developer**: Amjad Fertassi
- **Email**: amjadfertassi69@gmail.com
- **GitHub Issues**: [Report a bug](https://github.com/your-repo/ai-chat-platform/issues)

---
💡 *Empowering conversations with AI, one message at a time.*