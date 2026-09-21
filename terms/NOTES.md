# サイトの記録と宿題

**このサイト（`terms/` / `privacy/` / `tokushoho/` / `review-access/` / トップ）を改訂するときに最初に見るファイル。** 中身は規約まわりが中心。⚠️ このリポジトリは push した時点で公開される（GitHub Pages）ので、ここに書くのは**公開資料へのリンクと確認結果だけ**。

## 宿題（次の改訂で見るもの）

- ⏳ **第 7 条（規約の変更）に「表記・呼称の訂正を除く」旨のただし書きが無い**。条文は例外なく「効力発生日を定めて相当な期間前に周知」と読めるので、次に規約を実質的に改訂するときに合わせて整える（2026-09-21）
- ⏳ サイトの `README.md` が `/` `/terms/` `/privacy/` しか挙げていない。実際には `/tokushoho/`（特定商取引法に基づく表示）と `/review-access/` もある（2026-09-21 に気づいた / 次にこのリポジトリを触るときに直す）

## 確認済みの前提（同じ調べ直しを繰り返さないための記録）

### Google Play の販売者・決済（2026-09-21 確認）

| 論点 | 結論 | 一次資料 |
|---|---|---|
| 日本で Google はどの役割か | **マーケットプレイス サービス プロバイダ**（代理人ではない）。日本の窓口は Google Asia Pacific Pte. Ltd.。売買契約は運営者とユーザーの間で直接成立する | [supported-locations](https://play.google.com/supported-locations/)（英語正文で日本がどのセクションにあるかを見る。DDA 3.1 →[ヘルプ 10532353](https://support.google.com/googleplay/android-developer/answer/10532353)→ このページ、の順でたどる） |
| ⚠️ ユーザー向け Play 利用規約（日本語）の表記 | こちらは売買契約の相手を「**Google Digital Inc.** または提供元」と書いている。**デベロッパー↔Google の関係（MSP = Google Asia Pacific Pte. Ltd.）とは別の話**なので、混同しない | [Google Play 利用規約](https://play.google.com/intl/ja_jp/about/play-terms/index.html) |
| MoR（最終販売責任を負う商業者）になる国・地域 | EU / EEA + 英国 + モナコ・サンマリノ・バチカン・仏海外領土・ジブラルタルなど。**スイスも日本も非該当**（Apple 側のスイスと混同しない） | [DDA 3.4 がリンクする対象国一覧](https://support.google.com/googleplay/android-developer/answer/7645364) |
| 決済の根拠 | 「Google Play でコンテンツを購入するには、Google Payments アカウントを所有し、**Googleペイメント購入者利用規約**に同意している必要がある」。日本語正文の呼称は「Googleペイメント購入者利用規約」、英語正文は `Google Payments Terms of Service` | [Google Play 利用規約](https://play.google.com/intl/ja_jp/about/play-terms/index.html) |
| DDA の版ずれ | **影響なし**。規約が拠る DDA 3.1 / 3.4 の日本語正文は 2024-02-05 版と 2025-09-15 版で一字一句同じ（差分は税・源泉徴収 3.3 / 3.6、アイコンの色 5.3、書式のみ）。そもそも規約に DDA へのリンクも版の記載も無い | [現行版](https://play.google/intl/ALL_jp/developer-distribution-agreement.html) / [アーカイブ](https://play.google/intl/ALL_jp/developer-distribution-agreement/archive.html) |

## 改訂のときの手順

1. 公開ページ（`https://football-reminder.com/terms/`）とローカルの `terms/index.html` に差分が無いことを先に確かめる
2. 日本語セルと英語セルを**両方**直す（表は日本語 60 行台 / 英語 190 行台）
3. 🔴 **`最終更新日` と `Last updated` を両方更新する**（日本語 13 行目 / 英語 142 行目。本文だけ直して日付が据え置きになりやすい）
4. **第 7 条（規約の変更）の周知が要るかを判断し、判断したことをここに残す** — 効力発生日を定めて相当な期間前に周知（重要な変更はアプリ内通知）が要るのは**権利義務が変わるとき**。表記・呼称の訂正はこれに当たらない
5. HTML のタグ整合をパーサで検証する
6. push = 即時公開。アプリ側リポジトリ（`football-reminder`）の `docs/store/public-business-info.md` に注記があるときは、同じ回に現行文面へ合わせる

### 周知の判断の記録

- **2026-09-21（Google の役割の訂正）**: 第 7 条の事前周知は**不要**と判断した。「販売者 = 運営者」「売買契約はユーザーと運営者の間」という**実体は変わっておらず**、Google の役割名（代理人 / マーケットプレイス サービス プロバイダ）の誤記を一次資料に合わせただけのため。最終更新日のみ更新した
