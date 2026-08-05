# GROWX-Inc 案件ポータル

LP案件の確認用リンク一覧です。リンクを開くと現在のLPが表示されます。

## はじめてこのページを見る人へ

- **LPを確認したいだけの人**：下の一覧表のURLをクリックするだけでOKです。GitHubの操作は一切不要です
- **LPの新規作成・修正を依頼したい人**：リポジトリを直接触らず、**Claudeに依頼**してください（例：「lp-test-linksに〇〇案件のリンクを発行して」）
- **リポジトリを直接操作するのは管理者（濵田・山口）とClaudeのみ**です

## 🚫 変更禁止リポジトリ

以下は**変更・削除・設定変更を一切禁止**します。先方共有済みのものは公開URLが生きているため、触るとお客様に影響が出ます。

| リポジトリ | 理由 |
|---|---|
| qr-lp | 先方共有済み・公開URL維持 |
| google-review | 先方共有済み・公開URL維持 |
| hybridseal-warp-lp | 先方共有済み・公開URL維持 |
| lp-test-hama | 進行中案件のため変更禁止 |
| lp-test-gota | 進行中案件のため変更禁止 |

## LP案件一覧

| 案件名 | テスト用公開リンク | ステータス | 担当 |
|---|---|---|---|
| lp-test-links（案件集約） | https://github.com/GROWX-Inc/lp-test-links | 現役（新規案件はここに集約） | チーム |
| lp-test-hama | https://growx-inc.github.io/lp-test-hama/ | 進行中・変更禁止 | 濵田 |
| lp-test-gota | （リンク準備中） | 進行中・変更禁止 | 山口 |
| qr-lp | https://growx-inc.github.io/qr-lp/ | **先方共有済み・公開維持・触らない** | - |
| hybridseal-warp-lp | https://growx-inc.github.io/hybridseal-warp-lp/ | **先方共有済み・公開維持・触らない** | - |
| google-review | https://growx-inc.github.io/google-review/ | **先方共有済み・公開維持・触らない** | - |
| lp-monster | https://growx-inc.github.io/lp-monster/ | 終了（アーカイブ済・リンク維持） | - |
| cho-lp-test | （公開ページなし） | 終了（アーカイブ済） | - |

ステータスの意味：**進行中・変更禁止**＝制作中だが現在は変更しない ／ **先方共有済み・公開維持**＝クライアントにURL共有済み。絶対に触らない ／ **終了**＝案件終了（リンクは維持）

## 運用ルール（打ち止め方式・確定済み）

1. **新規LP案件は原則 [lp-test-links](https://github.com/GROWX-Inc/lp-test-links) のサブフォルダ**で管理する（`lp-test-links/{案件フォルダ}/`）
2. 独立リポジトリを作る場合は、名前を必ず**「lp-」始まり**にする。修正ログ自動記録は「lp-」始まりのリポジトリだけが対象。逆に、ログ対象にしないリポ（デザイン作業用など）は「lp-」始まりを**禁止**（`design-` 始まり推奨）
3. 終了した案件のリポジトリは**削除せずアーカイブ**する（アーカイブしてもテスト用公開リンクは維持される）
4. PRタイトルは `【フォルダ名】要約`、PR本文の「プロンプト:」欄は `{フォルダ名}｜` 始まりの**1行**で書く

## 社内用リンク

- [skills-library](https://github.com/GROWX-Inc/skills-library) … 完成したスキル・プロンプトの保管庫。CLAUDE.mdテンプレートの正は `templates/` 配下
- [sandbox-exec](https://github.com/GROWX-Inc/sandbox-exec) … 【練習用】Claude Codeの実験場（現役）
- [sandbox-exec2](https://github.com/GROWX-Inc/sandbox-exec2) … 実験場（棚卸し中・山口さん確認待ち）
- [claude-skills](https://github.com/GROWX-Inc/claude-skills) … 旧スキル置き場（skills-libraryへの統合を検討中・山口さん確認待ち）

---

この一覧表は、新規案件の作成時・案件の終了時にClaudeが自動更新します（最終更新：2026-08-05）
