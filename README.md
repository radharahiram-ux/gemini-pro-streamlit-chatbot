@<img width="1440" height="1120" alt="image" src="https://github.com/user-attachments/assets/58faf8f8-834a-47ca-bdab-8d8efe8f3e4d" />
<div align="center">

<img src="https://img.shields.io/badge/Gemini-Pro-4285F4?style=for-the-badge&logo=google&logoColor=white" />
<img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" />
<img src="https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge" />

<br/><br/>

# 🤖 Gemini Pro Chatbot

### A sleek, conversational AI chatbot powered by Google Gemini Pro & Streamlit

<br/>

[✨ Live Demo](#-getting-started) · [🐛 Report Bug](../../issues) · [💡 Request Feature](../../issues)

<br/>

</div>

---

## 📸 Preview

```
┌─────────────────────────────────────────────┐
│  🤖  Gemini Pro Chatbot                      │
├─────────────────────────────────────────────┤
│                                             │
│  🧑 You                                     │
│  ┌─────────────────────────────────────┐   │
│  │ What is the theory of relativity?   │   │
│  └─────────────────────────────────────┘   │
│                                             │
│  🤖 Assistant                               │
│  ┌─────────────────────────────────────┐   │
│  │ The theory of relativity, developed │   │
│  │ by Albert Einstein, consists of...  │   │
│  └─────────────────────────────────────┘   │
│                                             │
│  ┌─────────────────────────────────────┐   │
│  │  Ask me anything...          [Send] │   │
│  └─────────────────────────────────────┘   │
└─────────────────────────────────────────────┘
```

---

## ✨ Features

- 💬 &nbsp; **Multi-turn conversations** — Gemini remembers context across the session
- ⚡ &nbsp; **Streaming responses** — Replies appear as they're generated
- 🧠 &nbsp; **Powered by Gemini Pro** — Google's most capable text model
- 🎨 &nbsp; **Clean chat UI** — Native Streamlit chat components
- 🔒 &nbsp; **Secure API key** — Loaded from `.env`, never hardcoded
- 📦 &nbsp; **Minimal setup** — Only 3 dependencies, runs in minutes

---

## 🗂️ Project Structure

```
gemini-pro-chatbot/
│
├── 📄 main.py                  # App entry point
├── 📄 requirements.txt         # Python dependencies
├── 📄 .env.example             # API key template
├── 📄 .gitignore               # Keeps secrets out of git
│
└── 📁 .streamlit/
    ├── config.toml             # Server configuration
    └── credentials.toml        # Streamlit credentials
```

---

## 🚀 Getting Started

### Prerequisites

- Python **3.9+**
- A **Google Gemini API key** → [Get one free at Google AI Studio](https://makersuite.google.com/app/apikey)

---

### 1 · Clone the repo

```bash
git clone https://github.com/YOUR_USERNAME/gemini-pro-chatbot.git
cd gemini-pro-chatbot
```

### 2 · Create a virtual environment

```bash
python -m venv venv

# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate
```

### 3 · Install dependencies

```bash
pip install -r requirements.txt
```

### 4 · Set your API key

```bash
cp .env.example .env
```

Open `.env` and replace the placeholder:

```env
GOOGLE_API_KEY=your_actual_api_key_here
```

### 5 · Run the app

```bash
streamlit run main.py
```

Open your browser at **http://localhost:8501** 🎉

---

## 📦 Dependencies

| Package | Version | Purpose |
|---|---|---|
| `streamlit` | 1.30.0 | Web UI framework |
| `google-generativeai` | 0.3.2 | Gemini Pro API SDK |
| `python-dotenv` | 1.0.1 | Load `.env` variables |

---

## ⚙️ Configuration

Edit `.streamlit/config.toml` to change server settings:

```toml
[server]
port = 8501          # Change port if needed
headless = true      # Set false to auto-open browser
enableCORS = false

[theme]
base = "dark"        # "light" or "dark"
```

---

## 🔐 Security

> ⚠️ **Never commit your `.env` file to GitHub.**

The included `.gitignore` already excludes it. Always use `.env.example` as a template with placeholder values when sharing your project.

---

## 📖 How It Works

```
User types message
       │
       ▼
Streamlit chat_input()
       │
       ▼
Appended to st.session_state.messages
       │
       ▼
google-generativeai SDK sends full history to Gemini Pro
       │
       ▼
Response streamed back token by token
       │
       ▼
Displayed in st.chat_message("assistant")
```

---

## 🛠️ Troubleshooting

| Problem | Fix |
|---|---|
| `API key not valid` | Check `.env` has the correct key with no extra spaces |
| `ModuleNotFoundError` | Run `pip install -r requirements.txt` inside your venv |
| `Port already in use` | Change port in `config.toml` or run `streamlit run main.py --server.port 8502` |
| `CORS error` | Set `enableCORS = false` in `config.toml` |

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the project
2. Create your branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push: `git push origin feature/amazing-feature`
5. Open a Pull Request

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for more information.

---

<div align="center">

Made with ❤️ using [Streamlit](https://streamlit.io) and [Google Gemini](https://deepmind.google/technologies/gemini/)

</div>
