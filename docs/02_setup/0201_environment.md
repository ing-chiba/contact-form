# 0201 環境構築（CLI ツール）

ターミナルを開いて、以下の手順を進めてください。

---

## 1. Homebrew（推奨）

[https://brew.sh/ja/](https://brew.sh/ja/) に記載のコマンドをターミナルに貼り付けて実行してください。

```bash
brew --version
# Homebrew 5.0.16
```

---

## 2. Git（推奨）

Mac にすでに入っている場合があります。まず確認してください。

```bash
git --version
# git version 2.53.0
```

表示されない場合はインストールしてください。

```bash
brew install git
```

---

## 3. Node.js / npm（推奨）

[https://nodejs.org/ja/download](https://nodejs.org/ja/download) から **LTS 版**をダウンロードしてインストールしてください。

```bash
node --version
# v24.13.1

npm --version
# 11.11.0
```

---

## 4. PHP（推奨）

```bash
brew install php
```

```bash
php --version
# PHP 8.5.3 (cli) ...
```

---

## 5. Composer（推奨）

```bash
brew install composer
```

```bash
composer --version
# Composer version 2.9.5 ...
```

---

## チェックリスト

- [ ] `brew --version` が表示される
- [ ] `git --version` が表示される
- [ ] `node --version` が表示される
- [ ] `npm --version` が表示される
- [ ] `php --version` が表示される
- [ ] `composer --version` が表示される

---

## 学習

### 今何をしたか

開発に必要な CLI ツールをセットアップしました。

| ツール | 役割 |
|--------|------|
| Homebrew | Mac にツールを簡単にインストールできるパッケージマネージャー |
| Git | コードの変更履歴を管理するバージョン管理ツール |
| Node.js / npm | JavaScript をサーバーサイドで動かす実行環境とパッケージマネージャー |
| PHP | Laravel（バックエンド）を動かすプログラミング言語 |
| Composer | PHP のパッケージマネージャー |

### 参考資料

- [Git 入門（サル先生のGit入門）](https://backlog.com/ja/git-tutorial/)
- [Node.js とは（Node.js 公式）](https://nodejs.org/ja/about)
- [Composer 入門（公式ドキュメント）](https://getcomposer.org/doc/00-intro.md)
