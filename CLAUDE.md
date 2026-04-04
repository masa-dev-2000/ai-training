# AI Training - AI活用実践研修プロジェクト

## 概要

AI研修（初級編 全8回）の設計・教材作成・助成金対応を行うプロジェクト。
外部訓練機関として複数企業に提供し、各企業の助成金申請もサポートする。

## 最重要：作業開始前に読むべきファイル

| ファイル | 内容 |
|---------|------|
| **`design/PROJECT-STATUS.md`** | プロジェクト全体の状態・完了済み/未着手タスク・設計判断の記録 |
| **`curriculum/beginner-curriculum-v2.md`** | 最新のカリキュラム（v2確定版） |

**必ず上記2つを最初に読んでから作業を始めること。**

## 設計判断（要約）

- カリキュラム: 5つの業務スキル（伝える/書く/調べる/考える/まとめる）× 全8回
- 業種対応: 3グループ（A:公共福祉 / B:技術専門 / C:顧客対応）で演習お題をJSON差替
- 教材形式: バニラHTML単一ファイル、GitHub Pagesでデプロイ
- 助成金: 事業展開等リスキリング支援コース対応（2026年度まで）
- 横文字: 使わない方針。使う場合は日本語説明を添える
- テーマ: ライトテーマ（白背景）

## フォルダ構成

```
curriculum/           ← カリキュラム文書
design/               ← 設計書・分析レポート・状態書
  PROJECT-STATUS.md   ← ★ プロジェクト状態（最初に読む）
materials/
  session-01/         ← 第1回の教材
  topics/             ← 業種別お題セット（JSON）
```

詳細な構成は `design/PROJECT-STATUS.md` を参照。

## ルール

- Think in English, generate responses in Japanese.
- 設計ドキュメントはすべて日本語で記述
- 作業を始める前に `design/PROJECT-STATUS.md` を読む
- 設計判断を変更した場合は `design/PROJECT-STATUS.md` を更新する
- GitHubのIssueで改善点を管理している（`gh issue list`で確認可能）
