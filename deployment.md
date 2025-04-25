# 🚀 Deployment Guide for Chainlit Chatbot

This guide helps you deploy the Chainlit Chatbot powered by the **Gemini API** using minimal tools: `uv`, Chainlit, and Gemini.

---

## 📦 Requirements

- Python 3.10+
- [uv](https://github.com/astral-sh/uv) installed globally  
- Gemini API Key

---

## 🖥️ Local Deployment (Dev Environment)

1. **Clone the repo**:
   ```bash
   git clone https://github.com/azfarsuhail/ChainLitChatbot.git
   cd ChainLitChatbot
   ```

2. **Install dependencies**:
   ```bash
   uv install
   ```

3. **Configure your Gemini API key**:

   Create a `.env` file (if not present) and add:

   ```env
   GEMINI_API_KEY=your_api_key_here
   ```

4. **Run locally with hot-reload**:
   ```bash
   uv run chainlit run main.py -w
   ```

---

## 🌐 Production Deployment (Simple & Server-Based)

### Option 1: **Using `uvicorn` directly**
For a more traditional ASGI deployment:

1. Replace `-w` with a production-grade command:

   ```bash
   uv run chainlit run main.py --host 0.0.0.0 --port 8000
   ```

2. Use `tmux`, `screen`, or `systemd` to keep it running.

---

### Option 2: **Docker (Optional)**

If you prefer containerized deployment:

1. **Dockerfile** (optional, not included by default)

   ```Dockerfile
   FROM python:3.10-slim

   WORKDIR /app

   COPY . /app

   RUN pip install --no-cache-dir chainlit

   CMD ["chainlit", "run", "main.py", "--host", "0.0.0.0", "--port", "8000"]
   ```

2. **Build and run**:
   ```bash
   docker build -t chainlit-chatbot .
   docker run -p 8000:8000 -e GEMINI_API_KEY=your_api_key_here chainlit-chatbot
   ```

---

## 🔐 Environment & Secrets

Always secure your Gemini API key using `.env` files or environment variables in production. Avoid hardcoding secrets in source files.

---

## ✅ Final Checklist Before Production

- [ ] Confirm `GEMINI_API_KEY` is set
- [ ] Run `uv install` with a clean environment
- [ ] Use proper logging and error handling
- [ ] Secure your server or container runtime
- [ ] Set up HTTPS (optional but recommended)

