# GROWX-Inc 案件ポータル

LP案件の確認用リンク一覧です。リンクを開くと現在のLPが表示されます。

## 運用ルール（打ち止め方式・確定済み）

1. **新規LP案件は原則 [lp-test-links](https://github.com/GROWX-Inc/lp-test-links) のサブフォルダ**で管理する（`lp-test-links/{案件フォルダ}/`）
2. 独立リポジトリを作る場合は、名前を必ず **「lp-」始まり**にする（例：`lp-kamakura`）。修正ログ自動記録は「lp-」始まりのリポジトリだけが対象
3. 終了した案件のリポジトリは**削除せずアーカイブ**する（アーカイブしても確認用のPagesリンクは維持される）
4. PRタイトルは `【フォルダ名】要約`、PR本文の「プロンプト:」欄は `{フォルダ名}｜` 始まりの**1行**で書く

## LP案件一覧

| 案件名 | 確認用URL | ステータス | 担当 |
|---|---|---|---|
| lp-test-links（案件集約） | https://github.com/GROWX-Inc/lp-test-links | 現役（新規案件はここに集約） | チーム |
| lp-test-hama | https://growx-inc.github.io/lp-test-hama/ | テスト公開（進行中） | 濵田 |
| lp-test-gota | （リンク準備中） | 進行中 | 山口 |
| lp-monster | https://growx-inc.github.io/lp-monster/ | 終了（アーカイブ済・リンク維持） | - |
| qr-lp | https://growx-inc.github.io/qr-lp/ | 終了確認中（アーカイブ候補・山口さん確認待ち） | - |
| cho-lp-test | （公開ページなし） | 終了（アーカイブ済） | - |
| hybridseal-warp-lp | https://growx-inc.github.io/hybridseal-warp-lp/ | 終了確認中（アーカイブ候補・山口さん確認待ち） | - |

ステータスの意味：**テスト公開**＝制作中・社内/先方確認用 ／ **公開済み**＝本番運用中 ／ **終了**＝案件終了（リンクは維持） ／ **終了確認中**＝終了かどうか確認中

## 社内用リンク

- [skills-library](https://github.com/GROWX-Inc/skills-library) … 完成したスキル・プロンプトの保管庫（社内メンバーのみ閲覧可）。CLAUDE.mdテンプレートの正は `templates/` 配下
- [sandbox-exec](https://github.com/GROWX-Inc/sandbox-exec) … 【練習用】Claude Codeの実験場（現役）
- [sandbox-exec2](https://github.com/GROWX-Inc/sandbox-exec2) … 実験場（棚卸し中・山口さん確認待ち）
- [claude-skills](https://github.com/GROWX-Inc/claude-skills) … 旧スキル置き場（skills-libraryへの統合を検討中・山口さん確認待ち）
- [google-review](https://github.com/GROWX-Inc/google-review) … Google口コミ表示の検証用（継続要否を確認中）

---

この一覧表は、新規案件の作成時・案件の終了時にClaudeが自動更新します（最終更新：2026-08-05）
