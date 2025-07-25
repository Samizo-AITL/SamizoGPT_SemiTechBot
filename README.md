# SamizoGPT - 半導体技術Bot | Semiconductor Tech Bot

半導体エンジニアや学生のための、技術質問対応チャットボットの構築テンプレートです。  
設計・プロセス・テスト・不良解析など、開発現場での技術的な質問に ChatGPT API を活用して対話形式で回答します。

This is a customizable chatbot template designed to assist semiconductor engineers and students.  
It uses the ChatGPT API to provide interactive answers to technical questions in areas such as device design, fabrication process, testing, and failure analysis.

🌐 [English Version](./README_en.md) — Click here for the English version

---

## 📁 フォルダ構成 | Folder Structure

```
SamizoGPT_SemiTechBot/
├── SamizoGPT-v1x/              # プロンプトテンプレート | Prompt templates
│   └── prompt_templates/
│       └── semi_tech_support.md
├── api-scripts/                # Flask アプリ | Flask app for API
│   └── flask_semi_bot.py
├── config/                     # 設定ファイル（APIキーは除外推奨） | Config (exclude API key)
│   └── semi_settings.yaml
├── .gitignore                  # APIキーなどを除外 | Ignore sensitive files
└── README.md                   # 本ファイル | This file
```

---

## 🚀 起動方法 | How to Run

### 🔧 依存パッケージのインストール | Install Dependencies

```bash
pip install openai flask pyyaml
```

### ▶️ Flask アプリの起動 | Run the Flask App

```bash
cd api-scripts
python flask_semi_bot.py
```

---

## 🔗 API利用例 | API Usage Example

### `curl` を使った例 | Using `curl`

```bash
curl -X POST http://127.0.0.1:5000/chat \
     -H "Content-Type: application/json" \
     -d '{"message": "ゲート酸化膜が薄くなると何が起こる？"}'
```

---

## ⚠️ 注意事項 | Notes

- `config/semi_settings.yaml` にご自身の OpenAI APIキーを設定してください。  
  Please set your OpenAI API key in `config/semi_settings.yaml`.
- セキュリティのため、このファイルは `.gitignore` に追加しておくことを推奨します。  
  For security, we recommend adding this file to `.gitignore`.

---

## 📄 ボットテンプレート一覧 | Bot Templates

以下はこのプロジェクトに含まれるチャットボットテンプレートです：

| ファイル名 | 説明 | 説明（EN） |
|------------|------|-------------|
| `semi_tech_support.md` | 半導体の設計・プロセス・テスト・信頼性に関する質問に幅広く対応 | General support for semiconductor design, process, test, and reliability |
| `semi_failure_analysis.md` | 信頼性試験や不良解析に特化し、工程・構造・原因・対策を丁寧に解説 | Specialized in reliability and failure analysis, with engineering-focused responses |

---

## 📘 FAQ応答例（Botの使用例） | Example Bot Answers

不良解析Botの実際の応答例を以下にまとめています。教育や動作確認に活用できます：

📄 [`samples/faq_failure_analysis.md`](./samples/faq_failure_analysis.md)

---


## 👤 執筆者情報 / Author

**三溝 真一（Shinichi Samizo）**  
- 信州大学大学院 電気電子工学 修了  
- 元 セイコーエプソン株式会社 技術者（1997年〜）  

📌 **経験領域**：  
- 半導体デバイス（ロジック／メモリ／高耐圧混載）  
- 薄膜ピエゾアクチュエータ
- PrecisionCoreプリントヘッド製品化

📬 **連絡先**
- ✉️ Email: [shin3t72@gmail.com](mailto:shin3t72@gmail.com)  
- 🐦 X (Twitter): [https://x.com/shin3t72](https://x.com/shin3t72)  
- 💻 GitHub: [https://samizo-aitl.github.io/](https://samizo-aitl.github.io/)

---

## 📄 ライセンス | License

このプロジェクトは MITライセンス です。  
This project is licensed under the MIT License.

---
