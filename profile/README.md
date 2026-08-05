# GROWX-Inc GitHub 使用方法

このページは、GROWXでのGitHubの使い方をまとめた社内向けガイドです。**GitHubに詳しくなくても、このページだけ読めば大丈夫**なように書いています。

## GROWXでGitHubを使う目的（2つだけ）

1. **LP案件のテスト用公開リンクの発行・管理**（お客様に見せる確認用URLを作る）
2. **Claude用のスキル・プロンプトの保管**（社内の自動化資産を貯める）

この2つ以外の用途では使いません。

## まず覚えることは3つだけ

- **LPを確認したいだけの人** → 下の「LP案件一覧」のURLをクリックするだけ。GitHubの操作は一切不要
- **LPの新規作成・修正・リンク発行を依頼したい人** → リポジトリを直接触らず、**Claudeに依頼**する（例：「lp-test-linksに〇〇案件のリンクを発行して」）
- **リポジトリを直接操作するのは管理者（濵田・山口）とClaudeのみ**

## 🚫 変更禁止リポジトリ

以下は**変更・削除・設定変更を一切禁止**します。先方共有済みのものは公開URLが生きているため、触るとお客様に影響が出ます。

| リポジトリ | 理由 |
|---|---|
| qr-lp | 先方共有済み・公開URL維持 |
| google-review | 先方共有済み・公開URL維持 |
| hybridseal-warp-lp | 先方共有済み・公開URL維持 |
| lp-monster | 先方共有済み・公開URL維持 |
| lp-test-hama | 進行中案件のため変更禁止 |
| lp-test-gota | 進行中案件のため変更禁止 |
| lp-test-kamakura | 進行中案件のため変更禁止 |

## リポジトリ一覧：それぞれの役割と中身

GROWXの全リポジトリの役割の早見表です。ここに載っていないリポジトリは存在しません。

### ふだん使う4本

| リポジトリ | 役割 | 中身 |
|---|---|---|
| [lp-test-links](https://github.com/GROWX-Inc/lp-test-links) | **全LP案件のテストリンク置き場**。新規案件はすべてここ | 案件ごとのフォルダ（`{案件名}/index.html`）＋作業ルール（CLAUDE.md） |
| [skills-library](https://github.com/GROWX-Inc/skills-library) | **完成したスキル・プロンプトの保管庫（本番）** | `skills/`（Claude Code用スキル）、`prompts/`（コピペで使うプロンプト）、`templates/`（CLAUDE.md原本） |
| [sandbox-exec](https://github.com/GROWX-Inc/sandbox-exec) | **実験場（唯一）**。作りかけ・試行錯誤はここで。汚してOK | 個人・案件ごとのサブフォルダ（`AI MONSTERS/`、`hama/` など）。完成品はskills-libraryへ昇格 |
| [.github](https://github.com/GROWX-Inc/.github) | **このガイド自体**。組織トップに表示される特殊リポジトリ | `profile/README.md`（このページ） |

### 個別のLP案件リポジトリ（すべて変更禁止）

| リポジトリ | 状態 |
|---|---|
| lp-test-hama / lp-test-gota / lp-test-kamakura | 進行中の個別LP案件 |
| qr-lp / google-review / hybridseal-warp-lp / lp-monster | 先方共有済みLP（公開URL維持・絶対に触らない） |
| cho-lp-test | 終了（アーカイブ済） |

### 旧リポジトリ（移設完了・整理待ち）

| リポジトリ | 状態 |
|---|---|
| claude-skills | 中身はskills-libraryへ移設完了。アーカイブ待ち |
| sandbox-exec2 | 中身はsandbox-exec/hamaへ移設完了。整理待ち |

## LP案件一覧

| 案件名 | テスト用公開リンク | ステータス | 担当 |
|---|---|---|---|
| lp-test-links（案件集約） | https://github.com/GROWX-Inc/lp-test-links | 現役（新規案件はここに集約） | チーム |
| lp-test-hama | https://growx-inc.github.io/lp-test-hama/ | 進行中・変更禁止 | 濵田 |
| lp-test-gota | （リンク準備中） | 進行中・変更禁止 | 山口 |
| lp-test-kamakura | https://growx-inc.github.io/lp-test-kamakura/ | 進行中・変更禁止 | 濵田 |
| qr-lp | https://growx-inc.github.io/qr-lp/ | **先方共有済み・公開維持・触らない** | - |
| hybridseal-warp-lp | https://growx-inc.github.io/hybridseal-warp-lp/ | **先方共有済み・公開維持・触らない** | - |
| google-review | https://growx-inc.github.io/google-review/ | **先方共有済み・公開維持・触らない** | - |
| lp-monster | https://growx-inc.github.io/lp-monster/ | **先方共有済み・公開維持・触らない** | - |
| cho-lp-test | （公開ページなし） | 終了（アーカイブ済） | - |

ステータスの意味：**進行中・変更禁止**＝制作中だが現在は変更しない ／ **先方共有済み・公開維持**＝クライアントにURL共有済み。絶対に触らない ／ **終了**＝案件終了（リンクは維持）

## 運用ルール（打ち止め方式・確定済み）

1. **新規LP案件は原則 [lp-test-links](https://github.com/GROWX-Inc/lp-test-links) のサブフォルダ**で管理する（`lp-test-links/{案件フォルダ}/`）。リポジトリはこれ以上増やさない
2. 独立リポジトリを作る場合は、名前を必ず**「lp-」始まり**にする。修正ログ自動記録は「lp-」始まりのリポジトリだけが対象。逆に、ログ対象にしないリポ（デザイン作業用など）は「lp-」始まりを**禁止**（`design-` 始まり推奨）
3. 終了した案件のリポジトリは**削除せずアーカイブ**する（アーカイブしてもテスト用公開リンクは維持される）
4. PRタイトルは `【フォルダ名】要約`、PR本文の「プロンプト:」欄は `{フォルダ名}｜` 始まりの**1行**で書く
5. **このページの更新はClaudeの作業に組み込み済み**：テストリンクの発行・案件ステータスの変更・スキルやプロンプトの追加をClaudeに依頼すると、Claudeが作業の最後にこのページも更新する（人間が覚えておく必要はない）

---

最終更新：2026-08-05（このページはClaudeが作業のたびに自動更新します）
