---
title: "MkDocs + GitHub Pages 公開ガイド"
tags:
  - 概要
status: "公開中"
---

# MkDocs + GitHub Pages 公開ガイド

=== "本文"

    このサイトは、Markdownで書いたドキュメントを **MkDocs** でサイト化し、
    **GitHub Pages** で無料公開するまでの手順を、自分で再現できるレベルでまとめたものです。

    ## 全体の流れ

    ![全体の流れ](images/overview.svg)

    1. ローカルPCで Markdown ファイルを編集する
    2. GitHubのリポジトリに `git push` する
    3. push をきっかけに **GitHub Actions** が自動でビルドする
    4. ビルド結果が `gh-pages` ブランチに送られる
    5. **GitHub Pages** がそのブランチの内容を世界に公開する

    一度この仕組みを作ってしまえば、以降は **Markdownを編集してpushするだけ** で
    サイトが自動更新されます。手動でのアップロード作業は不要です。

    ## 章の構成

    <div class="docs-card-grid" markdown>
    <a class="docs-card" href="01-setup/01-python-setup/"><strong>1. Python環境の準備</strong><br>MkDocsを動かすための土台づくり</a>
    <a class="docs-card" href="01-setup/02-mkdocs-install/"><strong>2. mkdocsのインストールとサイト作成</strong><br>サイトの雛形を作る</a>
    <a class="docs-card" href="02-github-publish/03-github-repo/"><strong>3. GitHubリポジトリの作成とpush</strong><br>コードをGitHubに置く</a>
    <a class="docs-card" href="02-github-publish/04-github-actions/"><strong>4. GitHub Actionsによる自動デプロイ</strong><br>push→公開を自動化する</a>
    <a class="docs-card" href="02-github-publish/05-github-pages/"><strong>5. GitHub Pagesの公開設定</strong><br>公開のスイッチを入れる</a>
    <a class="docs-card" href="03-local-dev/06-local-preview/"><strong>6. ローカルでのプレビュー方法</strong><br>公開前に手元で確認する</a>
    <a class="docs-card" href="04-customization/07-customization/"><strong>7. サイトデザインのカスタマイズ</strong><br>配色・ナビゲーション・コードブロックを整える</a>
    <a class="docs-card" href="04-customization/08-mermaid-and-revision-date/"><strong>8. 図解(Mermaid)と改定履歴</strong><br>設計書向けに図と改定履歴の管理方法を追加する</a>
    </div>

    ## このサイトのその他の機能

    - [タグ一覧](tags.md) で機能横断にページを探せます
    - `llms.txt`（[{{ extra.site_base_url }}llms.txt]({{ extra.site_base_url }}llms.txt)）でサイト全体の構成をAIが一括で読み取れます
    - フォルダ構成は `awesome-pages` プラグインにより自動でナビゲーションに反映されます（`mkdocs.yml`の手動編集は不要）

    ## このサイトの公開先（実例）

    {{ extra.site_base_url }}

    同じ手順で、自分のリポジトリ名（`{{ extra.repo_name }}`）・GitHubユーザー名（`{{ extra.github_user }}`）を
    置き換えれば同様に公開できます。

=== "改定履歴"

    | 更新日 | 更新者 | 更新内容 |
    |---|---|---|
    | 2026-06-20 | 岡洋介 | 初版作成 |
