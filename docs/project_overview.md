# 📊 Project Overview - SamizoGPT_SemiTechBot

This document outlines the structure, purpose, and components of the **SamizoGPT_SemiTechBot** project.

---

## 🎯 Purpose

To build a customizable, ChatGPT API-based chatbot focused on **semiconductor technical support**, including process, design, testing, and failure analysis.

日本語版の目的：
ChatGPT APIを活用し、半導体プロセス／設計／信頼性／不良解析に関する技術的な質問に応答できる、再利用性の高いチャットボットを構築する。

---

## 🧱 Project Structure

```
SamizoGPT_SemiTechBot/
├── SamizoGPT-v1x/
│   └── prompt_templates/
│       ├── semi_tech_support.md
│       └── semi_failure_analysis.md
├── api-scripts/
│   └── flask_semi_bot.py
├── config/
│   └── semi_settings.yaml
├── docs/
│   └── usage_guide.md
│   └── project_overview.md ← このファイル
├── .gitignore
└── README.md
```

---

## 🧠 Prompt Templates

| Template File | Description |
|---------------|-------------|
| `semi_tech_support.md` | General semiconductor support: process, design, testing, reliability |
| `semi_failure_analysis.md` | Specialized in failure mode diagnosis and reliability issues |

---

## 🔌 API Integration

- Flask-based web API endpoint: `POST /chat`
- Uses OpenAI's `gpt-4` model
- Settings are managed in `config/semi_settings.yaml` (excluded from Git)

---

## 🚀 Future Expansion Plans

- [ ] Add Streamlit GUI frontend
- [ ] Multi-template switching via UI
- [ ] Integrate Markdown/PDF knowledge base (LangChain, etc.)
- [ ] Education bot extension via Edusemi/EduController projects
- [ ] GitHub Pages for documentation

---

## 📜 License

This project is licensed under the MIT License.
