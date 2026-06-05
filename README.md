# Claude Code ハンズオン

Claude Code の基本操作からソフトウェア開発・チーム開発までを **60分 × 3回** で実践するハンズオンコースです。

実践教材として、PHP すら入っていない macOS から **Laravel 13 + [Prism](https://github.com/prism-php/prism)（LLM 統合パッケージ）による AI チャット Web アプリ**を、すべてプロンプトだけで構築・デバッグした実セッションを再現可能な形にまとめています。

## 📖 教材の閲覧

ブラウザで [`index.html`](index.html)（コースポータル）を開くと、各回の資料にアクセスできます（外部依存なしの静的 HTML）。

```bash
open index.html
```

| ファイル | 内容 |
|---|---|
| [`index.html`](index.html) | コースポータル（概要・各回へのリンク） |
| [`session1.html`](session1.html) | 第1回：Claude Code の基本 |
| [`session2.html`](session2.html) | 第2回：Claude Code を使ったソフトウェア開発 |
| [`session3.html`](session3.html) | 第3回：Claude Code を使ったチーム開発 |
| [`laravel-prism.html`](laravel-prism.html) | 第1回 実践教材（Laravel × Prism チャットアプリ構築） |
| [`HANDSON.md`](HANDSON.md) | 講義資料のソース（Markdown） |

以下は実践教材（Laravel × Prism チャットアプリ構築）の説明です。

## 🎯 学べること

- 曖昧な指示に対して Claude Code が**意図を確認**する振る舞い
- 前提ツール不足（PHP/Composer）の**自動検知と依存解決**
- 未知のパッケージ（Prism）の**ドキュメント／ソースからの仕様把握**
- エラー発生時の**ログ調査 → 根本原因特定 → 修正**の流れ
- API キーなど**機密情報の安全な扱い**

## 🧭 教材の構成

| # | ステップ | 内容 |
|---|---------|------|
| 0 | 環境とゴール | 前提環境・到達目標 |
| 1 | 拡張バージョン確認 | `claude --version` の確認 |
| 2 | リポジトリのクローン | `!git clone` プレフィックスの説明 |
| 3 | 技術スタック調査 | `composer.json` からの自動把握 |
| 4 | Laravel 環境構築 | PHP/Composer 導入 → `create-project` |
| 5 | 開発サーバー起動 | `php artisan serve` |
| 6 | Prism 導入と設定 | `composer require`・config publish・`.env` |
| 7 | チャットアプリ実装 | Controller / route / Blade の 3 ファイル |
| 8 | トラブルシュート | `APP_KEY` 欠落 / モデル名 404 の実例 |
| 9 | IME 不具合の修正 | `isComposing` による変換確定 Enter の除外 |
| ✓ | まとめ・学び | プロンプト一覧・発展課題 |

## 🛠 題材の技術スタック

| 分類 | 技術 |
|------|------|
| 言語 | PHP 8.5 |
| フレームワーク | Laravel 13 |
| LLM 統合 | Prism |
| LLM プロバイダー | Anthropic Claude |
| エディタ | VSCode + Claude Code 拡張 |

## 🚀 発展課題

- 会話履歴の保持（マルチターン対応）
- ストリーミング応答（`asStream()` でタイプライター表示）
- モデル選択 UI の追加（Haiku / Sonnet / Opus 切替）
- Prism の Testing 機能でモック化し、API キーなしのテストを書く

---

本資料は実際の Claude Code セッションを基に作成されました。
