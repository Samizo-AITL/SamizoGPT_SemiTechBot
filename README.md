# 🧠 **SamizoGPT - 半導体技術Bot | Semiconductor Tech Bot**

[![Samizo-AITLポータルサイトに戻る](https://img.shields.io/badge/Samizo--AITL%20ポータルサイトに戻る-brightgreen)](https://samizo-aitl.github.io/) [![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

**半導体エンジニアや学生**のための、**技術質問対応チャットボット**の構築テンプレートです。  
**設計・プロセス・テスト・不良解析**など、開発現場での技術的な質問に **ChatGPT API** を活用して**対話形式で回答**します。

This is a customizable **chatbot template** designed to assist **semiconductor engineers and students**.  
It uses the **ChatGPT API** to provide interactive answers to technical questions in areas such as **device design**, **fabrication process**, **testing**, and **failure analysis**.

> ⚠️ **注意 / Note:**  
> 本プロジェクトは、**ChatGPT API** と **プロンプトテンプレート**を使った **チャットボット構築の雛形**です。  
> 現在は「**API呼び出し＋プロンプト応答**」の最小構成であり、以下のような **本格的なBotアプリ機能は整備中**です：
> 
> - **セッション管理・対話履歴保存**  
> - **GUIチャット画面**（例：Streamlit）  
> - **テンプレートの動的切り替え**  
> - **教材連携（Edusemi など）**
>
> 現時点では「**プロンプト駆動型の技術Botテンプレート集**」としてご利用ください。

🌐 [**English Version**](./README_en.md) — Click here for the English version

---

## 📁 **フォルダ構成 | Folder Structure**

```plaintext
SamizoGPT_SemiTechBot/
├── docs/
├── prompt_templates/
│   └── semi_tech_support.md
│   └── semi_failure_analysis.md
├── samples/
│   └── faq_failure_analysis.md
├── api-scripts/
│   └── flask_semi_bot.py
├── config/
│   └── semi_settings.yaml
├── .gitignore
└── README.md
```

---

## 🚀 **起動方法 | How to Run**

### 🔧 **依存パッケージのインストール | Install Dependencies**

```bash
pip install openai flask pyyaml
```

### ▶️ **Flask アプリの起動 | Run the Flask App**

```bash
cd api-scripts
python flask_semi_bot.py
```

---

## 🔗 **API利用例 | API Usage Example**

### `curl` を使った例 | Using `curl`

```bash
curl -X POST http://127.0.0.1:5000/chat \
     -H "Content-Type: application/json" \
     -d '{"message": "ゲート酸化膜が薄くなると何が起こる？"}'
```

---

## ⚠️ **注意事項 | Notes**

- `config/semi_settings.yaml` にご自身の **OpenAI APIキー**を設定してください。  
  Please set your **OpenAI API key** in `config/semi_settings.yaml`.
- セキュリティのため、このファイルは `.gitignore` に追加しておくことを推奨します。  
  For security, we recommend adding this file to `.gitignore`.

---

## 📄 **ボットテンプレート一覧 | Bot Templates**

以下はこのプロジェクトに含まれる **チャットボット用プロンプトテンプレート**です：

| **ファイル名** | **説明** | **Description (EN)** |
|----------------|----------|-----------------------|
| [`semi_tech_support.md`](./prompt_templates/semi_tech_support.md) | **半導体の設計・プロセス・テスト・信頼性**に関する質問に幅広く対応 | General support for **semiconductor design, process, test, and reliability** |
| [`semi_failure_analysis.md`](./prompt_templates/semi_failure_analysis.md) | **信頼性試験や不良解析**に特化し、**工程・構造・原因・対策**を丁寧に解説 | Specialized in **reliability and failure analysis**, with engineering-focused responses |

---

## 📘 **FAQ応答例（Botの使用例） | Example Bot Answers**

**不良解析Botの実際の応答例**を以下にまとめています。  
教育や動作確認にご活用ください：

📄 [`faq_failure_analysis.md`](./samples/faq_failure_analysis.md)

---

## 👤 **執筆者情報 / Author**

**三溝 真一（Shinichi Samizo）**  
- **信州大学大学院 電気電子工学 修了**  
- 元 **セイコーエプソン**株式会社 技術者（1997年〜）

📌 **経験領域**：  
- **半導体デバイス（ロジック・メモリ・高耐圧混載）**  
- **インクジェット薄膜ピエゾアクチュエータ**  
- **PrecisionCoreプリントヘッド製品化・BOM管理・ISO教育**

📬 **連絡先**  
- ✉️ [shin3t72@gmail.com](mailto:shin3t72@gmail.com)  
- 🐦 [https://x.com/shin3t72](https://x.com/shin3t72)  
- 💻 [https://samizo-aitl.github.io/](https://samizo-aitl.github.io/)

---

## 📄 **ライセンス | License**

このプロジェクトは **MITライセンス** です。  
This project is licensed under the **MIT License**.

---
