# SamizoGPT - Semiconductor Tech Bot

A customizable chatbot template for semiconductor engineers and students.  
This bot uses the ChatGPT API to provide interactive answers to technical questions related to device design, fabrication process, testing, and failure analysis.

🏠 [日本語版はこちら](./README.md) — 日本語のREADMEはこちら

---

## 📁 Folder Structure
```
SamizoGPT_SemiTechBot/
├── SamizoGPT-v1x/              # Prompt templates
│   └── prompt_templates/
│       └── semi_tech_support.md
├── api-scripts/                # Flask app for API interaction
│   └── flask_semi_bot.py
├── config/                     # Configuration files (API key excluded)
│   └── semi_settings.yaml
├── .gitignore                  # File exclusion (e.g., API keys)
└── README_en.md                # English version of this file
```
---

## 🚀 How to Run

### 🔧 Install Dependencies

```bash
pip install openai flask pyyaml
```

## ▶️ Run the Flask App
```
cd api-scripts
python flask_semi_bot.py
```

## 🔗 API Usage Example
```
curl -X POST http://127.0.0.1:5000/chat \
     -H "Content-Type: application/json" \
     -d '{"message": "What happens when the gate oxide gets thinner?"}'
```

---

## ⚠️ Notes

- You must set your OpenAI API key in `config/semi_settings.yaml`.
- For security, it is recommended to include this file in `.gitignore`.

---

## 📄 License

This project is released under the MIT License.  
Free for use, modification, and educational deployment.

---

## 🤖 Bot Templates

The following prompt templates are included in this project:

| File | Description |
|------|-------------|
| `semi_tech_support.md` | General support for semiconductor design, process, test, and reliability |
| `semi_failure_analysis.md` | Specialized support for reliability testing and failure analysis with detailed engineering responses |

---

## 👤 Author

**Shinichi Samizo**  
- M.S. in Electrical and Electronic Engineering, Shinshu University  
- Former engineer at Seiko Epson Corporation (since 1997)  

**Expertise**:  
- Semiconductor devices (logic, memory, high-voltage mixed-signal)  
- Thin-film piezo actuators  
- PrecisionCore printhead product development

📫 [GitHub: Samizo-AITL](https://github.com/Samizo-AITL)  
📩 Email: [shin3t72@gmail.com](mailto:shin3t72@gmail.com)

---
