# お問い合わせフォーム - インターン生課題

## 概要

管理者がお問い合わせ内容を管理できる、フルスタック Web アプリケーションの開発課題です。

---

## 技術スタック

| カテゴリ | 技術 |
|----------|------|
| バックエンド | Laravel 12.x |
| フロントエンド | React / TypeScript / Chakra UI |
| フォーム管理 | React Hook Form / Zod |
| データベース | MySQL または PostgreSQL |
| インフラ | Docker / Laravel Sail |
| 開発ツール | Git, GitHub, Visual Studio Code, OpenAPI |

---

## 必須要件

### お問い合わせフォーム

- 以下の入力フィールドを持つフォームを実装する
  - 氏名（必須）
  - 会社名（任意）
  - メールアドレス（必須）
  - 問い合わせ内容（必須）
- バリデーションを実装する（メールアドレス形式チェック、必須項目チェックなど）
- フォーム送信後は送信完了画面を表示する

### 管理者ログイン画面

- ユーザー名またはメールアドレスとパスワードの入力フィールドを設ける
- ログインエラー時には適切なエラーメッセージを表示する
- ログイン成功後はお問い合わせ一覧ページに遷移する

### お問い合わせ一覧画面

- 管理者のみがアクセスできる（未ログイン状態でアクセスするとログインページにリダイレクト）
- 以下の項目をテーブル形式で表示する
  - 氏名
  - 会社名
  - メールアドレス
  - 問い合わせ内容
  - 問い合わせ日時

---

## 追加実装項目（余裕があれば）

| 機能 | 説明 |
|------|------|
| 検索・フィルタリング | 氏名・メールアドレスでの検索、日付・内容によるフィルタリング |
| ページネーション | 一覧データが増えた場合に備えたページング機能 |
| セキュリティ対策 | CSRF 対策、パスワードのハッシュ化などの基本的なセキュリティ実装 |

---

## セットアップ

### 必要な環境

**必須**
- Docker Desktop

**推奨**
- Homebrew
- PHP 8.5.x
- Composer 2.9.x

### インストール手順

```bash
# リポジトリのクローン
git clone <repository-url>
cd contact-form

# 依存パッケージのインストール
composer install

# 環境変数の設定
cp .env.example .env

# Sail の起動
./vendor/bin/sail up -d

# アプリケーションキーの生成
./vendor/bin/sail artisan key:generate

# マイグレーションの実行
./vendor/bin/sail artisan migrate

# フロントエンドのセットアップ
./vendor/bin/sail npm install
./vendor/bin/sail npm run dev
```

> **Tip:** `alias sail='./vendor/bin/sail'` を `~/.zshrc` に追加すると `sail up -d` のように短縮できます。

---

## ディレクトリ構成（予定）

```
contact-form/
├── app/                  # Laravel アプリケーション
│   ├── Http/Controllers/
│   └── Models/
├── database/
│   └── migrations/
├── resources/
│   └── js/              # React フロントエンド
│       ├── components/
│       └── pages/
├── routes/
│   └── api.php
└── README.md
```

---

## API 仕様

OpenAPI を使用して API 仕様を定義します。詳細は `openapi.yaml` を参照してください。
