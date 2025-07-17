# 使用ガイド | Usage Guide

このリポジトリは、ChatGPT APIを使って構築した半導体技術ボットのテンプレート集です。Flask APIを介して呼び出すことで、技術者や学生の質問に応答するチャットボットを構築できます。

## Botの種類
- `semi_tech_support.md`：一般的な半導体設計・プロセス質問対応
- `semi_failure_analysis.md`：信頼性・不良解析専用の技術ボット

## 使用方法（Flask）
1. `config/semi_settings.yaml` にAPIキーを設定
2. `python flask_semi_bot.py` を実行
3. `/chat` にPOSTで質問を送信
