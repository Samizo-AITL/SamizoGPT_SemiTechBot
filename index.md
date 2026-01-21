---
layout: default
title: SamizoGPT – SemiTech Bot
# math: katex   # 必要ページだけ
# mermaid: true  # フローチャート図など出すとき
---

---

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

---

## 🔗 公式リンク | Official Links

| 言語 / Language | GitHub Pages 🌐 | GitHub 💻 |
|-----------------|----------------|-----------|
| 🇯🇵 Japanese | [![GitHub Pages JP](https://img.shields.io/badge/GitHub%20Pages-日本語版-brightgreen?logo=github)](https://samizo-aitl.github.io/SamizoGPT_SemiTechBot/) | [![GitHub Repo JP](https://img.shields.io/badge/GitHub-日本語版-blue?logo=github)](https://github.com/Samizo-AITL/SamizoGPT_SemiTechBot) |
| 🇺🇸 English | [![GitHub Pages EN](https://img.shields.io/badge/GitHub%20Pages-English-brightgreen?logo=github)](https://samizo-aitl.github.io/SamizoGPT_SemiTechBot/en/) | [![GitHub Repo EN](https://img.shields.io/badge/GitHub-English-blue?logo=github)](https://github.com/Samizo-AITL/SamizoGPT_SemiTechBot/tree/main/en) |

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

## 👤 **執筆者情報 | Author**

| 📌 項目 / Item | 内容 / Details |
|------|------|
| **氏名 / Name** | 三溝 真一（Shinichi Samizo） |
| **経験領域 / Expertise** | 半導体デバイス（ロジック・メモリ・高耐圧混載）<br>インクジェット薄膜ピエゾアクチュエータ<br>プリントヘッド製品化・BOM管理・ISO教育 |
| **💻 GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL) |

---

## 📄 **ライセンス / License**

- **JP:** 本教材は [**MIT License**](https://opensource.org/licenses/MIT) に基づき、**教育・非営利での再利用・編集・派生**を歓迎します。  
- **EN:** Licensed under **[MIT License](https://opensource.org/licenses/MIT)**. Free to **reuse, modify, and fork** for education/non-profit.

---

## 💬 **フィードバック | Feedback**
> 改善提案や議論はGitHub Discussionsからお願いします。  
> *Propose improvements or start discussions via GitHub Discussions.*

[![💬 GitHub Discussions](https://img.shields.io/badge/💬%20GitHub-Discussions-brightgreen?logo=github)](https://github.com/Samizo-AITL/SamizoGPT_SemiTechBot/discussions)

