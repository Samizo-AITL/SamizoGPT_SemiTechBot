# SamizoGPT - 半導体技術Bot | Semiconductor Tech Bot

ChatGPT APIを活用した、半導体技術支援用のチャットボット構築テンプレートです。  
This is a template for building a semiconductor technical support chatbot using the ChatGPT API.

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

## 📄 ライセンス | License

このプロジェクトは MITライセンス です。  
This project is licensed under the MIT License.
