# LLM Analyst Agent (Streamlit)

A Streamlit app that wraps a LangChain-powered agent to perform data analysis and storytelling. The agent can scrape websites, analyze uploaded files (CSV/JSON/PDF/images), generate interactive HTML data stories, and save artifacts to the working directory.

---

## 🚀 Quick Start

1. Clone the repo and open the project folder:

```bash
cd Data-Agent-Streamlit
```

2. Create and activate a virtual environment (Windows):

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install --upgrade pip
```

3. Install required packages:

```bash
pip install streamlit python-dotenv langchain langchain-experimental langchain_openai langsmith pydantic
```

4. Create a `.env` file in the project root with the following variables:

```env
AIPIPE_TOKEN=your_aipipe_token_here
STUDENT_SECRET=choose_a_secret
OPENAI_BASE_URL=https://your-openai-base-url
```

> Note: `.env` is included in `.gitignore`—do NOT commit secrets.

5. Run the app:

```bash
streamlit run app.py
```

Open the URL printed by Streamlit (usually http://localhost:8501).

---

## ⚙️ Usage

- Enter the **Secret** (value of `STUDENT_SECRET`) in the sidebar to unlock functionality.
- Type your analysis or data-story request using the chat input.
- Optionally upload files (CSV, JSON, PDF, images) for the agent to use.
- The agent will produce an interactive HTML data story and additional artifact files accessible in the app.

---

## 🔒 Security & Privacy

- Keep your API keys and secrets private. Never commit `.env` to source control.
- If you suspect a leak, rotate your tokens immediately.

---

## 🧭 Project Structure

- `app.py` — Main Streamlit application and agent orchestration
- `.gitignore` — Ignores `.env`

---

## ✨ Notes

- The agent uses the AIPIPE/OpenRouter-style endpoint and expects `AIPIPE_TOKEN` and `OPENAI_BASE_URL` to be set.
- Generated HTML and JSON artifacts are written to the working directory and can be previewed or downloaded from the Streamlit UI.

---

## 🙌 Contributing

Feel free to open issues or PRs. Keep changes focused and include tests or manual steps to reproduce.

---

## 📄 License

MIT © Harliv Singh
