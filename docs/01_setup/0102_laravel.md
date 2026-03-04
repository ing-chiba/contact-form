# 0102 Laravel プロジェクト作成 & Git セットアップ

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

## 4. Git リポジトリの作成

### ローカルリポジトリの初期化

Laravel プロジェクトには最初から `.gitignore` が用意されています。
そのまま Git の初期化と最初のコミットを行ってください。

```bash
git init
git add .
git commit -m "first commit"
```

### GitHub にリポジトリを作成してプッシュ

[GitHub](https://github.com) にログインし、新しいリポジトリを作成してください。
作成後に表示されるコマンドをターミナルで実行します。

```bash
git remote add origin https://github.com/<ユーザー名>/<リポジトリ名>.git
git branch -M main
git push -u origin main
```

---

### よく使う Git コマンド

開発中は以下のコマンドを繰り返し使います。

| コマンド | 説明 |
|----------|------|
| `git status` | 変更されたファイルの一覧を確認する |
| `git diff` | 変更内容の差分を確認する |
| `git add .` | すべての変更をステージング（コミット準備）する |
| `git add <ファイル名>` | 特定のファイルだけをステージングする |
| `git commit -m "メッセージ"` | ステージした変更をコミットする |
| `git push` | ローカルのコミットを GitHub に反映する |
| `git pull` | GitHub の最新状態をローカルに取り込む |
| `git log --oneline` | コミット履歴を一覧表示する |

---

## チェックリスト

- [ ] `contact-form` ディレクトリが作成されている
- [ ] `vendor/bin/sail` ファイルが存在している
- [ ] `.env` の `DB_CONNECTION` が `pgsql` になっている
- [ ] `docker-compose.yml` に `mailpit` が含まれている
- [ ] `git log --oneline` でコミットが確認できる
- [ ] GitHub にリポジトリが作成されプッシュされている

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
| `git init` | ローカルに Git リポジトリを新規作成するコマンド |
| `git add` | コミットするファイルをステージングエリアに追加するコマンド |
| `git commit` | ステージングした変更を履歴として記録するコマンド |
| `git push` | ローカルのコミットをリモートリポジトリ（GitHub）に送るコマンド |
| `.gitignore` | Git の管理対象から除外するファイル・ディレクトリを指定するファイル |

### 参考資料

- [Laravel 公式ドキュメント（日本語）](https://readouble.com/laravel/12.x/ja/installation.html)
- [Laravel Sail 公式ドキュメント](https://readouble.com/laravel/12.x/ja/sail.html)
- [Git 入門（サル先生のGit入門）](https://backlog.com/ja/git-tutorial/)
- [GitHub でリポジトリを作成する](https://docs.github.com/ja/repositories/creating-and-managing-repositories/quickstart-for-repositories)
