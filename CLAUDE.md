# CLAUDE.md — tradingcomplete.github.io（広報部）

> Studio Compana の **公式LP・特商法・法務専用リポ**。GitHub Pages で `https://tradingcomplete.com` として公開中。

---

## 🏢 リポの位置付け

このリポは **Studio Compana 3リポ体制の「広報部」**:

```
GitHub/
├── 💻 trading-complete/             ← 本社（CEO秘書室・docs・アプリ本体）
├── 📣 tradingcomplete.github.io/    ← 当リポ（LP・法務）
└── ✍️ trading-articles/              ← コンテンツ制作部
```

**本社の経営要件定義書**: `../trading-complete/docs/business/Studio_Compana_運営要件定義書.md`

---

## 🎯 このリポの責任範囲

- 公式LP（`index.html`・188KB・GitHub Pages公開中）
- 特定商取引法に基づく表記（`tokutei.html`）
- 利用規約・プライバシーポリシー（`legal/index.html`）
- LP用画像資産（`images/feature-*.jpg` 等）
- ロゴ・favicon（Studio Compana の Cマーク）
- LP設計書（`TC_ホームページ設計書_v1_3.md`）
- SEO（`robots.txt` / `sitemap.xml`）

---

## 📌 重要ファイル

| ファイル | 役割 |
|---|---|
| `index.html` | 公式LP本体・SEO/構造化データ統合 |
| `tokutei.html` | 特商法表記（屋号・所在地等） |
| `legal/index.html` | 利用規約・プライバシーポリシー |
| ⭐ `TC_ホームページ設計書_v1_3.md` | LP設計の最新マスター（75KB） |
| `CNAME` | カスタムドメイン設定（tradingcomplete.com） |
| `sitemap.xml` / `robots.txt` | SEO設定 |

---

## 🚨 編集時の必須チェック

### 1. 屋号・住所の表記統一
全ファイルで以下を統一する（grep で確認）:
- 屋号: **Studio Compana**（個人事業主・「株式会社」NG）
- 代表者: 成瀬仁文（コンパナ）
- 所在地: 〒450-0002 愛知県名古屋市中村区名駅3-4-10 アルティメイト名駅1st 2階

### 2. 価格・リリース時期
最新の正は **本社の中核オファー要件定義書**:
- `../trading-complete/docs/marketing/Trading_Complete_中核オファー要件定義書_v1_0.md`
- 価格: Pro¥1,980/¥19,800年 / Premium¥2,980/¥29,800年
- 早期割引: 先着100名終身 Pro¥1,480 / Premium¥2,480
- リリース: 2026年夏

### 3. 決済プロバイダ表記
- 公開向け: 「外部決済サービスを利用」（具体名は本番切替時に追記）
- 本番切替時: PayPal・Square を tokutei.html に追記
- 詳細: `../trading-complete/docs/features/決済システム要件定義書_v3_10.md`

### 4. 「FX」キーワードの取り扱い
カードブランドの自動審査で減点対象になりうる。
- 推奨: 「トレード記録」「データ分析」「規律」「副業」
- 控えめに: 「FX」「金融」「投資」（必要最低限・誇張回避）
- 詳細: `../trading-complete/docs/REFERENCE.md` 教訓27

### 5. 投資助言にならない表現
- ✅ OK: 「過去データの分析」「統計上の傾向」「参考情報」
- ❌ NG: 「今エントリーすべき」「勝てるシグナル」「確実に儲かる」
- 詳細: 本社マーケドキュメントの「AI機能ガイドライン」

---

## 🔗 本社（trading-complete）への重要参照

| 知りたいこと | 参照先 |
|---|---|
| 経営全体方針 | `../trading-complete/docs/business/Studio_Compana_運営要件定義書.md` |
| 価格・プラン | `../trading-complete/docs/marketing/Trading_Complete_中核オファー要件定義書_v1_0.md` |
| 決済実装 | `../trading-complete/docs/features/決済システム要件定義書_v3_10.md` |
| ミッション・ビジョン | `../trading-complete/docs/marketing/Trading_Complete_ミッションステートメント_v1_3.md` |
| マーケ戦略 | `../trading-complete/docs/marketing/Trading_Complete_マーケティング戦略.md` |

---

## 🔄 LP変更時のクロスリポ波及

LPの主要セクションを変更したら、以下も連動更新が必要かチェック:

| LP変更 | 連動チェック |
|---|---|
| 価格セクション | 本社の中核オファー要件定義書 / v3.10 / TASKS.md |
| 機能紹介セクション | 本社の docs/機能一覧.md / OVERVIEW.md |
| 屋号・住所表記 | tokutei.html / legal/ / 本社CLAUDE.md / 運営要件定義書 §1 |
| ミッション・スローガン | 本社のミッションステートメント / 記事スキル mission.md |

詳細フローは本社の `/cross-update` スキルで支援。

---

## ⚙️ 公開・デプロイ

- GitHub Pages 自動デプロイ（main ブランチへのpush で即反映）
- カスタムドメイン: tradingcomplete.com（CNAME設定済）
- SSL: GitHub Pages デフォルト
- キャッシュ: ブラウザのみ（CDNなし）→ 重要変更後は強制リロード推奨

### push後の確認
1. https://tradingcomplete.com で表示確認（5〜10分のラグあり）
2. https://tradingcomplete.com/tokutei.html / `/legal/` も確認
3. OG画像・SEOメタタグが正しく出るか（[OGP確認ツール](https://www.opengraph.xyz/)等）

---

## 🚫 NG リスト（絶対やらない）

1. ❌ 「株式会社」「弊社」「当社」を使う（個人事業主のため）
2. ❌ 価格を直接書き換え（マスター更新後に同期）
3. ❌ 「FX」「投資」を多用（審査リスク）
4. ❌ 「勝てる」「儲かる」「必ず」等の投資助言表現
5. ❌ 本番Stripe/PayPal/Squareキーをコミット（このリポは公開リポ）
6. ❌ ユーザー個人情報を含むスクリーンショット掲載

---

## 📐 SEO最適化の指針

- 構造化データ（Organization / SoftwareApplication / FAQPage）を維持
- メタタグの description / keywords は「Studio Compana」を必ず含む
- 内部リンク: tokutei / legal への明示的リンクを各ページに
- robots.txt / sitemap.xml は変更時に必ず再確認

詳細: `TC_ホームページ設計書_v1_3.md` §9 「SEO運用ガイド」

---

## 🔮 リリース時の必須更新（2026年夏予定）

リリース時に同期すべき項目:
- [ ] `index.html` の `href="#"` 3箇所を本番アプリURLに差し替え
- [ ] `tokutei.html` の支払方法欄に PayPal・Square 追記
- [ ] 「2026年夏リリース予定」を「リリース中」「ご利用いただけます」に変更
- [ ] OG画像・description を「リリース済み」のメッセージに更新
- [ ] FAQ に「ログイン方法」「課金方法」「解約方法」を追加

詳細: 本社の `/release-go` スキル + `/cross-update` スキル

---

*Studio Compana — 広報部*
*このCLAUDE.mdは本社の経営要件定義書（v0.1）に基づき作成 / 2026-04-28*
