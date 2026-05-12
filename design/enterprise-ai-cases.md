# 大企業の生成AI運用事例

> 最終更新: 2026-05-12
> 用途: 第1回（v3）「機密情報の境界線」パートで紹介する素材
> 参照日時点：2026-05-12

## まず使う5事例（研修トップ5）

| # | 事例 | 役割 |
|---|------|------|
| 1 | [メルカリ「AI活用基本ポリシー」](https://about.mercari.com/ai-policy/) | 「禁止ではなくガードレール」のアンカー |
| 2 | [パナソニック コネクト「ConnectAI」](https://news.panasonic.com/jp/press/jn250707-2) | 年44.8万時間削減・**事故ゼロ16カ月** |
| 3 | [LINEヤフー「生成AI活用義務化」](https://www.lycorp.co.jp/ja/news/release/008806/) | 11,000人に「ゼロベースで資料を作らない」を義務化 |
| 4 | [DeNA「AI活用100本ノック」](https://dena.ai/) | 100事例をPDFで公開・**研修後のお土産**として配れる |
| 5 | [サムスン電子 ChatGPT漏洩3事例](https://pc.watch.impress.co.jp/docs/news/yajiuma/1490904.html) | コード貼付・装置情報・会議録音の漏洩。「やってしまった」筆頭 |

---

## A. 運用ガイドライン・社内ルール

### メルカリ
- [AI活用基本ポリシー](https://about.mercari.com/ai-policy/) / [AIガバナンス](https://about.mercari.com/ai-governance/)
- [社員95%がAI業務利用](https://careers.mercari.com/mercan/articles/49836/)
- 「禁止せず明瞭に」「ブロッカーを作らない」が方針。社内ガイドライン・セキュリティガイドライン・相談窓口を整備。

### パナソニック コネクト
- [ConnectAI 2025年プレスリリース](https://news.panasonic.com/jp/press/jn250707-2)
- [2024年プレスリリース](https://news.panasonic.com/jp/press/jn240625-1)
- 全社員に独自AIアシスタント配布。**2年目で年44.8万時間削減**（1年目18.6万）。導入16カ月で漏洩・著作権事故ゼロ。

### 日立製作所
- [Generative AIセンター](https://pc.watch.impress.co.jp/docs/news/1500523.html)
- グループ32万人が業務利用。法務・知財・品質保証など部門横断でガイドライン策定。相談窓口あり。

### サイバーエージェント
- [ChatGPTオペレーション変革室](https://www.cyberagent.co.jp/news/detail/id=28668)
- [OpenAI公式事例](https://openai.com/index/cyberagent/)
- 広告運用23万時間/月のうち30%（約7万時間）削減目標。当初は学習されないAPI経由のみ。現在はChatGPT Enterprise全社展開、MAU率93%。

### リクルート
- [AI活用指針](https://www.recruit.co.jp/blog/culture/20241028_5252.html)
- [社内コミュニティAI Update](https://techblog.recruit.co.jp/article-4698/)
- 全社展開には文化醸成も必要、という観点の事例。

### 伊藤忠商事
- [生成AI研究ラボ](https://www.itochu.co.jp/ja/news/press/2023/230512.html)
- 商社という保守的業界でも、Azure OpenAIベースで約4,200人にセキュアなChatGPT環境提供。投資業務にも活用。

### 三菱UFJ銀行・MUFG
- [MUFG DX戦略](https://www.mufg.jp/profile/strategy/dx/articles/0133/index.html)
- 稟議書・社内文書要約・FAQ自動応答で月22万時間相当の削減試算。

### LINEヤフー
- [SeekAI（RAG社内検索）](https://www.lycorp.co.jp/ja/news/release/008806/)
- [生成AI活用義務化発表](https://www.lycorp.co.jp/ja/news/release/018121/)
- 11,000人に「まずAIに聞く」「ゼロベースで資料を作らない」「任意会議は議事録で」を義務化。

### 公的ガイドライン
- [経産省 AI事業者ガイドライン](https://www.meti.go.jp/press/2024/04/20240419004/20240419004.html)
- [総務省 1.1版 PDF](https://www.soumu.go.jp/main_content/001002576.pdf)
- [IPA テキスト生成AIガイドライン](https://www.ipa.go.jp/jinzai/ics/core_human_resource/final_project/2024/generative-ai-guideline.html)

---

## B. 機密情報の扱い方（公式情報）

### ChatGPT 法人プラン
- [OpenAI公式ヘルプ：データ利用](https://help.openai.com/ja-jp/articles/5722486-how-your-data-is-used-to-improve-model-performance)
- Team・Enterprise・API は既定で入力・出力が学習に使われない。個人版は明示的オプトアウト必要。

### Gemini for Google Workspace
- [Google公式FAQ](https://knowledge.workspace.google.com/admin/gemini/gemini-for-google-workspace-faq)
- Workspace有償ライセンス下では学習に使われず、人間レビューなし。

### NotebookLM
- [SoftBank解説](https://www.softbank.jp/biz/blog/cloud-technology/articles/202510/gemini-security/)
- Workspace版は学習なし。個人アカウントとの違いに注意。マイナンバー・カード番号は入れない、顧客名は「顧客A」のように匿名化。

### Microsoft 365 Copilot
- [Microsoft公式Q&A](https://learn.microsoft.com/ja-jp/answers/questions/3954098/)
- 法人ライセンスはテナント境界内で処理、基盤LLMの学習に使われない。画面に「Protected」アイコン表示。

### Anthropic Claude
- [プラン別データ取扱](https://code.claude.com/docs/ja/data-usage)
- [2025年8月規約改定の解説](https://www.lifehacker.jp/article/2508-anthropic-training-ai-claude-user-conversations/)
- 2025年8月以降、Free/Pro/Maxは既定で学習対象（オプトアウト可）。Team/Enterprise/APIは契約上学習なし。EnterpriseはZero Data Retentionオプション。

### GitHub Copilot for Business/Enterprise
- [freee社の導入記](https://developers.freee.co.jp/entry/github-copilot-governance)
- [ZOZO社の導入記](https://techblog.zozo.com/entry/introducing_github_copilot)
- Business以上はプロンプト保持なし、自社コードは学習に使われない。

### 伏せ字・抽象化テクニック
- 顧客名 → 「顧客A」「お客様B」
- 住所 → 「東京都内」「関東地方」
- 固有商品名 → 「製品X」「サービスY」
- 契約金額 → 「数千万円」「3桁万円」
- 学習設定に関わらず実施推奨。

---

## C. 効果・事故事例

### 成功事例

- **パナソニック コネクト**：年44.8万時間削減・事故ゼロ（A項目に詳細）
- **DeNA「AI活用100本ノック」**：[100事例PDF公開](https://dena.ai/)・[プレス](https://dena.com/jp/news/5279/)。エンジニア・ビジネス・クリエイター職の100事例。「DARS」AI活用度指標も。
- **リクルート「AIかべうち君」**：新規事業提案のエントリーが前年比3倍以上
- **三菱UFJ信託銀行×カサナレ**：[問い合わせ業務50%削減](https://prtimes.jp/main/html/rd/p/000000052.000114769.html)、年6.5万時間削減
- **LINEヤフー SeekAI**：年80万時間削減目標、CSテスト98%正答率

### 事故事例

- **サムスン電子（2023年4月）**：[解禁から3週間で3件漏洩](https://pc.watch.impress.co.jp/docs/news/yajiuma/1490904.html)
  - ①半導体ソースコードをデバッグ目的でペースト
  - ②不良装置のコードを修正依頼
  - ③会議録音をアップロードして議事録化
  - 最終的にChatGPT利用を全面禁止に。
- **JPモルガン・チェース等の米大手金融機関**：[2023年2月に一斉禁止](https://www.nikkei.com/article/DGXZQOGN22EA40S3A220C2000000/)
  - JPM・Goldman・Citi・Wells Fargo・BofA・Deutsche Bankなど
  - 規制対応・顧客情報漏洩懸念が背景

---

## 研修での使い方（第1回・機密情報パート 10分）

| 時間 | 内容 | 使う事例 |
|------|------|---------|
| 1〜2分 | 3段階ルール（安全／注意／禁止）を復習 | — |
| 3〜4分 | 「やってしまった」を見せる | サムスン3事例 |
| 3〜4分 | 「使い倒している」を見せる | メルカリ＋LINEヤフー＋パナソニック |
| 1〜2分 | 自分の会社で考えるための2軸＋お土産 | 学習されない設定／伏せ字テク／DeNA100本ノックURL |

緊張 → 希望 → 自分事、の3段。

## 注意事項

- 三菱UFJ・サムスンは2023年情報。「2023年時点」と明示する
- AIサービスのデータ取扱仕様は変わりやすい（特にAnthropicは2025年8月に大変更）。実施前に最新版の公式ヘルプを再確認
- 引用URLは2026-05-12時点で実在確認済み
