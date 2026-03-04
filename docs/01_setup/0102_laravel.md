# 0102 Laravel プロジェクト作成

## 1. プロジェクトの作成

```bash
composer create-project laravel/laravel contact-form
cd contact-form
```

> 📖 [Laravel インストール（公式ドキュメント）](https://readouble.com/laravel/12.x/ja/installation.html)

---

## 2. Laravel Sail のインストール

```bash
composer require laravel/sail --dev
php artisan sail:install
```

> 📖 [Laravel Sail（公式ドキュメント）](https://readouble.com/laravel/12.x/ja/sail.html)

サービスの選択肢が表示されるので `pgsql` と `mailpit` を選択してください。
複数選択はカンマ区切りで入力します。

```
Which services would you like to install? [mysql]:
  [0] mysql
  [1] pgsql
  ...
  [8] mailpit
  ...
> 1,8
```

> Mailpit はメール送信のテストに使うツールです。実際には送信されず、ブラウザで内容を確認できます。

---

## 3. .env の確認

`sail:install` 後、`.env` のデータベース設定が自動で書き換えられます。
以下のようになっていれば OK です。

```env
DB_CONNECTION=pgsql
DB_HOST=pgsql
DB_PORT=5432
DB_DATABASE=laravel
DB_USERNAME=sail
DB_PASSWORD=password
```

---

## チェックリスト

- [ ] `contact-form` ディレクトリが作成されている
- [ ] `vendor/bin/sail` ファイルが存在している
- [ ] `.env` の `DB_CONNECTION` が `pgsql` になっている
- [ ] `docker-compose.yml` に `mailpit` が含まれている

---

## 学習

### 今何をしたか

Laravel のプロジェクトを新規作成し、Docker で動かすための Laravel Sail を導入しました。

| 用語 | 説明 |
|------|------|
| Laravel | PHP の Web アプリケーションフレームワーク |
| Composer | PHP のパッケージ管理ツール。`composer create-project` でプロジェクトを雛形から作成できる |
| Laravel Sail | Docker を使って Laravel の開発環境を簡単に構築するツール |
| .env | アプリケーションの設定ファイル。DB 接続情報などを記載する |
| Mailpit | 開発環境でメール送信をテストするツール。実際には送信されず画面で確認できる |

### 参考資料

- [Laravel 公式ドキュメント（日本語）](https://readouble.com/laravel/12.x/ja/installation.html)
- [Laravel Sail 公式ドキュメント](https://readouble.com/laravel/12.x/ja/sail.html)
