# 0101 環境構築

ターミナルを開いて、以下の手順を進めてください。

---

## 1. Docker Desktop（必須）

[Docker Desktop 公式サイト](https://www.docker.com/products/docker-desktop/) からダウンロードしてインストールしてください。

インストール後、Docker Desktop を起動してください。

```bash
docker --version
# Docker version 29.2.1, build a5c7197
```

---

## 2. Homebrew（推奨）

[https://brew.sh/ja/](https://brew.sh/ja/) に記載のコマンドをターミナルに貼り付けて実行してください。

```bash
brew --version
# Homebrew 5.0.16
```

---

## 3. Git（推奨）

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

## 4. Node.js / npm（推奨）

[https://nodejs.org/ja/download](https://nodejs.org/ja/download) から **LTS 版**をダウンロードしてインストールしてください。

```bash
node --version
# v24.13.1

npm --version
# 11.11.0
```

---

## 5. PHP（推奨）

```bash
brew install php
```

```bash
php --version
# PHP 8.5.3 (cli) ...
```

---

## 6. Composer（推奨）

```bash
brew install composer
```

```bash
composer --version
# Composer version 2.9.5 ...
```

---

## 7. Visual Studio Code（推奨）

[https://code.visualstudio.com/](https://code.visualstudio.com/) から Mac 版をダウンロードしてインストールしてください。

インストール後、コマンドパレット（`Cmd + Shift + P`）から `Shell Command: Install 'code' command in PATH` を実行しておくと、ターミナルから `code .` でプロジェクトを開けます。

---

## チェックリスト

- [ ] `docker --version` が表示される
- [ ] Docker Desktop が起動している
- [ ] `brew --version` が表示される
- [ ] `git --version` が表示される
- [ ] `node --version` が表示される
- [ ] `npm --version` が表示される
- [ ] `php --version` が表示される
- [ ] `composer --version` が表示される
- [ ] VS Code が起動できる

---

## 学習

### 今何をしたか

開発環境のセットアップをしました。
それぞれのツールには役割があり、組み合わせて使うことで効率よく開発できます。

| ツール | 役割 |
|--------|------|
| Docker | アプリをどの環境でも同じように動かすための仮想コンテナ |
| Homebrew | Mac にツールを簡単にインストールできるパッケージマネージャー |
| Git | コードの変更履歴を管理するバージョン管理ツール |
| Node.js / npm | JavaScript をサーバーサイドで動かす実行環境とパッケージマネージャー |
| PHP | Laravel（バックエンド）を動かすプログラミング言語 |
| Composer | PHP のパッケージマネージャー |
| VS Code | コードを書くためのエディタ |

### 参考資料

- [Docker とは何か？（Docker 公式ドキュメント）](https://docs.docker.com/get-started/docker-overview/)
- [Git 入門（サル先生のGit入門）](https://backlog.com/ja/git-tutorial/)
- [Node.js とは（Node.js 公式）](https://nodejs.org/ja/about)
- [Composer 入門（公式ドキュメント）](https://getcomposer.org/doc/00-intro.md)
