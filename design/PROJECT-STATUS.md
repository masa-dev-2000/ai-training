# プロジェクト状態書（他端末での作業引き継ぎ用）

> 最終更新: 2026-04-04

## プロジェクト概要

AI研修（初級編 全8回）の設計・教材作成・助成金対応を行うプロジェクト。
受講企業ごとに助成金申請をサポートする外部訓練機関としてサービス提供する。

## 現在のフェーズ

**カリキュラムv2が確定し、第1回の教材は実装・テスト済み。第2回以降の設計・教材作成に入る段階。**

## 完了済みのこと

### カリキュラム設計
- [x] v1カリキュラム作成 → `curriculum/beginner-curriculum.md`
- [x] v2カリキュラム確定 → `curriculum/beginner-curriculum-v2.md`（**こちらが最新**）
- [x] 5つの業務スキル（伝える/書く/調べる/考える/まとめる）で全8回を構成
- [x] 業種別3グループ（A:公共福祉 / B:技術専門 / C:顧客対応）でお題を差し替える設計

### 第1回 教材
- [x] 設計書 → `design/session-01-design.md`
- [x] HTML講義資料 → `materials/session-01/presentation.html`
  - ライトテーマ、タイマー、講師メモ、コピーボタン、全画面、ログ機能
  - URLパラメータでの業種切替は**未実装**（JSON読み込み対応がまだ）
- [x] 振り返りページ → `materials/session-01/recap.html`
- [x] テスト実施2回 → 分析レポート作成済み

### 業種別お題セット
- [x] topics-A.json（公共・福祉系） → `materials/topics/topics-A.json`
- [x] topics-B.json（技術・専門系） → `materials/topics/topics-B.json`
- [x] topics-C.json（顧客対応系） → `materials/topics/topics-C.json`
- [ ] presentation.htmlのJSON読み込み対応（`?type=A`で切替）→ **未実装**

### 助成金対応
- [x] 要件整理 → `design/subsidy-requirements.md`
- [x] カリキュラム設計戦略 → `design/subsidy-curriculum-design.md`
- [ ] 計画届テンプレート → **未作成**
- [ ] 出席管理テンプレート → **未作成**
- [ ] 補講運用ガイド → **未作成**

### ナレッジベース
- [x] 講師用FAQ → `design/knowledge-base-faq.md`（Markdown原本）
- [x] HTMLページ → `knowledge-base.html`（GitHub Pages公開済み）

### GitHub
- リポジトリ: `masa-dev-2000/ai-training`（Public）
- GitHub Pages: https://masa-dev-2000.github.io/ai-training/
- Issue: 37件（大半クローズ済み）

## 未着手のこと

| # | タスク | 優先度 |
|---|--------|--------|
| 1 | **第2回の設計書＆講義資料** | 高 |
| 2 | **presentation.htmlのJSON読み込み対応** | 高 |
| 3 | 第3〜8回の設計書＆講義資料 | 中 |
| 4 | 計画届テンプレート | 中 |
| 5 | 出席管理テンプレート | 中 |
| 6 | 補講運用ガイド | 中 |
| 7 | 契約書・見積書テンプレート | 低 |
| 8 | 外部講師要件確認書 | 低 |

## 主な設計判断（決定済み）

| 判断事項 | 決定内容 |
|---------|---------|
| カリキュラム構成 | 5つの業務スキル × 全8回 |
| 業種対応 | 3グループ（公共福祉/技術専門/顧客対応）で演習お題を差替 |
| お題差替方式 | JSON外部化（`?type=A`でURLパラメータ切替） |
| 教材形式 | バニラHTML単一ファイル（CDN不使用） |
| デプロイ先 | GitHub Pages |
| 助成金コース | 事業展開等リスキリング支援コース（2026年度まで） |
| 申請主体 | 各受講企業が申請。講師は外部訓練機関＋申請サポート |
| 補講方式 | アーカイブ視聴＋個別ライブ30分 |
| テーマ | ライトテーマ（白背景） |
| 横文字方針 | 使わない。使う場合は日本語説明を添える |
| AIの例え | 「優秀だけど口が軽い新人」 |
| OK/NG分類 | 3段階（安全/注意/禁止） |

## ファイル構成

> 設計思想・変更経緯の詳細は `design/DESIGN-HISTORY.md` を参照。

```
ai-training/
├── CLAUDE.md                              ← プロジェクトルール
├── index.html                             ← ホームページ
├── knowledge-base.html                    ← ナレッジベース（講師用）
├── curriculum/
│   ├── beginner-curriculum.md             ← v1（旧版）
│   └── beginner-curriculum-v2.md          ← v2（最新・確定版）
├── design/
│   ├── PROJECT-STATUS.md                  ← このファイル（状態書）
│   ├── session-01-design.md               ← 第1回 設計書
│   ├── session-01-analysis.md             ← テスター1 分析
│   ├── session-01-analysis-tester2.md     ← テスター2 分析
│   ├── subsidy-requirements.md            ← 助成金要件
│   ├── subsidy-curriculum-design.md       ← 助成金対応設計
│   ├── curriculum-v2-proposal.md          ← v2提案書（経緯記録）
│   ├── DESIGN-HISTORY.md                 ← 設計思想・変更履歴（★ 足跡記録）
│   └── knowledge-base-faq.md             ← ナレッジベース原本
├── materials/
│   ├── session-01/
│   │   ├── presentation.html              ← 第1回 講義資料
│   │   └── recap.html                     ← 第1回 振り返り
│   └── topics/
│       ├── topics-A.json                  ← 公共・福祉系お題
│       ├── topics-B.json                  ← 技術・専門系お題
│       └── topics-C.json                  ← 顧客対応系お題
└── .github/workflows/pages.yml           ← GitHub Pages デプロイ
```

## テスター講義からの主要フィードバック

### テスター1（社会福祉協議会職員・初中級）
- 「AIにインタビューさせる」手法が最も響いた
- 議事録自動化・Googleフォーム連携に強い関心
- PCメモリ不足でGeminiが開けない問題が発生

### テスター2（経営者・設計業・中級）
- 情報漏洩リスク＋学習設定の話が最大の学び
- 43分で終了（90分想定の半分）→ 中級者には簡単すぎた
- 「AI＝優秀だけど暴露リスクのある新人」の例えが響いた
- AI間の比較（ChatGPT/Gemini/Claude/Perplexity）に強い関心

### 講師のしゃべり方フィードバック
- テスター1→2で結論ファーストと例えの具体化が改善
- まだ残る課題：1文が長い、不要な謝罪、参加者レベルに合わせた調整
- 詳細 → 分析レポート参照
