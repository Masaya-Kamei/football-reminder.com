# 規約まわりの記録と宿題

`terms/index.html` を改訂するときに最初に見るファイル。⚠️ このリポジトリは push した時点で公開される（GitHub Pages）ので、ここに書くのは**公開資料へのリンクと確認結果だけ**。

## 宿題（次の改訂で見るもの）

- **規約そのものの宿題は無し**（2026-09-21 時点）
- ⏳ サイトの `README.md` が `/` `/terms/` `/privacy/` しか挙げていない。実際には `/tokushoho/`（特定商取引法に基づく表示）と `/review-access/` もある（2026-09-21 に気づいた / 次にこのリポジトリを触るときに直す）

## 確認済みの前提（同じ調べ直しを繰り返さないための記録）

### Google Play の販売者・決済（2026-09-21 確認）

| 論点 | 結論 | 一次資料 |
|---|---|---|
| 日本で Google はどの役割か | **マーケットプレイス サービス プロバイダ**（代理人ではない）。日本の窓口は Google Asia Pacific Pte. Ltd.。売買契約は運営者とユーザーの間で直接成立する | [supported-locations](https://play.google.com/supported-locations/)（英語正文の該当セクションで日本の位置を確認） |
| MoR（最終販売責任を負う商業者）になる国・地域 | EU / EEA + 英国 + モナコ・サンマリノ・バチカン・仏海外領土など。**スイスは非該当**（Apple 側のスイスと混同しない） | [DDA 3.4 がリンクする対象国一覧](https://support.google.com/googleplay/android-developer/answer/7645364) |
| 決済の根拠 | 「Google Play でコンテンツを購入するには、Google Payments アカウントを所有し、**Googleペイメント購入者利用規約**に同意している必要がある」。日本語正文の呼称は「Googleペイメント購入者利用規約」、英語正文は `Google Payments Terms of Service` | [Google Play 利用規約](https://play.google.com/intl/ja_jp/about/play-terms/index.html) |
| DDA の版ずれ | **影響なし**。規約が拠る DDA 3.1 / 3.4 の日本語正文は 2024-02-05 版と 2025-09-15 版で一字一句同じ（差分は税・源泉徴収 3.3 / 3.6、アイコンの色 5.3、書式のみ）。そもそも規約に DDA へのリンクも版の記載も無い | [現行版](https://play.google/intl/ALL_jp/developer-distribution-agreement.html) / [アーカイブ](https://play.google/intl/ALL_jp/developer-distribution-agreement/archive.html) |

## 改訂のときの手順

1. 公開ページ（`https://football-reminder.com/terms/`）とローカルの `terms/index.html` に差分が無いことを先に確かめる
2. 日本語セルと英語セルを**両方**直す（表は日本語 60 行台 / 英語 190 行台）
3. HTML のタグ整合をパーサで検証する
4. push = 即時公開。アプリ側リポジトリ（`football-reminder`）の `docs/store/public-business-info.md` に注記があるときは、同じ回に現行文面へ合わせる
