<!-- omit in toc -->
# 目次
- [1. プロジェクト概要](#1-プロジェクト概要)
- [2. リポジトリ概要](#2-リポジトリ概要)
  - [2.1. 機能](#21-機能)
  - [2.2. アーキテクチャ](#22-アーキテクチャ)
  - [2.3. 使用技術](#23-使用技術)
  - [2.4. ディレクトリ構成](#24-ディレクトリ構成)
- [3. 環境構築](#3-環境構築)
  - [3.1. python](#31-python)
  - [3.2. GAS](#32-gas)
  - [3.3. インストール](#33-インストール)
  - [3.4. 環境変数](#34-環境変数)
    - [3.4.1. 一覧](#341-一覧)
    - [3.4.2. 設定](#342-設定)
  - [3.5. 使用方法](#35-使用方法)
    - [3.5.1. コマンド一覧](#351-コマンド一覧)
  - [3.6. トラブルシューティング](#36-トラブルシューティング)
- [4. 特記事項](#4-特記事項)
- [5. 参考資料](#5-参考資料)


# 1. プロジェクト概要
[コンフルエンス](aaa)を参照してください

# 2. リポジトリ概要
XXX用リポジトリ

## 2.1. 機能
1. XXX
2. XXX

## 2.2. アーキテクチャ
図    
  
## 2.3. 使用技術
TODO: パッケージ管理の検証が終わったら  
<table>
  <!-- ヘッダ -->
  <tr>
    <td>フロントエンド</td>
    <td>バックエンド</td>
    <td>バックエンド言語</td>
    <td>ミドルウェア</td>
    <td>インフラ</td>
  </tr>
  <!-- ボディ -->
  <tr>
    <td>
      <img src="https://img.shields.io/badge/-Node.js-000000.svg?logo=node.js&style=flat">
      <br>
      <img src="https://img.shields.io/badge/-Next.js-000000.svg?logo=next.js&style=flat">
      <br>
      <img src="https://img.shields.io/badge/-TailwindCSS-000000.svg?logo=tailwindcss&style=flat">
      <br>
      <img src="https://img.shields.io/badge/-React-20232A?style=flat&logo=react&logoColor=61DAFB">
    </td>
    <td>
      <img src="https://img.shields.io/badge/-Django-092E20.svg?logo=django&style=flat">
    </td>
    <td>
      <img src="https://img.shields.io/badge/-Python-F2C63C.svg?logo=python&style=flat">
    </td>
    <td>
      <img src="https://img.shields.io/badge/-Nginx-269539.svg?logo=nginx&style=flat">
      <br>
      <img src="https://img.shields.io/badge/-MySQL-4479A1.svg?logo=mysql&style=flat&logoColor=white">
      <br>
      <img src="https://img.shields.io/badge/-Gunicorn-199848.svg?logo=gunicorn&style=flat&logoColor=white">
    </td>
    <td>
      <img src="https://img.shields.io/badge/-Docker-1488C6.svg?logo=docker&style=flat">
      <br>
      <img src="https://img.shields.io/badge/-githubactions-FFFFFF.svg?logo=github-actions&style=flat">
      <br>
      <img src="https://img.shields.io/badge/-Amazon%20aws-232F3E.svg?logo=amazon-aws&style=flat">
      <br>
      <img src="https://img.shields.io/badge/-terraform-20232A?style=flat&logo=terraform&logoColor=844EBA">
    </td>
  </tr>
</table>  

その他のパッケージ、バージョンについては`pyproject.toml`を参照してください。
  
## 2.4. ディレクトリ構成

<!-- Treeコマンドを使ってディレクトリ構成を記載 -->
<details>
  <summary>ディレクトリ構成</summary>

  ```bash
  ❯ tree -a -I "node_modules|.next|.git|.pytest_cache|static" -L 2
  .
  ├── .devcontainer
  │   └── devcontainer.json
  ├── .env
  ├── .github
  │   ├── action
  │   ├── release-drafter.yml
  │   └── workflows
  ├── .gitignore
  ├── Makefile
  ├── README.md
  ├── backend
  │   ├── .vscode
  │   ├── application
  │   ├── docs
  │   ├── manage.py
  │   ├── output
  │   ├── poetry.lock
  │   ├── project
  │   └── pyproject.toml
  ├── containers
  │   ├── django
  │   ├── front
  │   ├── mysql
  │   └── nginx
  ├── docker-compose.yml
  ├── frontend
  │   ├── .gitignore
  │   ├── README.md
  │   ├── __test__
  │   ├── components
  │   ├── features
  │   ├── next-env.d.ts
  │   ├── package-lock.json
  │   ├── package.json
  │   ├── pages
  │   ├── postcss.config.js
  │   ├── public
  │   ├── styles
  │   ├── tailwind.config.js
  │   └── tsconfig.json
  └── infra
      ├── .gitignore
      ├── docker-compose.yml
      ├── main.tf
      ├── network.tf
      └── variables.tf

<p align="right">(<a href="#top">トップへ</a>)</p>

# 3. 環境構築
  
## 3.1. python

## 3.2. GAS

## 3.3. インストール

## 3.4. 環境変数
### 3.4.1. 一覧
  
| 変数名                 | 役割                                      | デフォルト値                       | DEV 環境での値                           |
| ---------------------- | ----------------------------------------- | ---------------------------------- | ---------------------------------------- |
| MYSQL_ROOT_PASSWORD    | MySQL のルートパスワード（Docker で使用） | root                               |                                          |
| MYSQL_DATABASE         | MySQL のデータベース名（Docker で使用）   | django-db                          |                                          |
| MYSQL_USER             | MySQL のユーザ名（Docker で使用）         | django                             |                                          |
| MYSQL_PASSWORD         | MySQL のパスワード（Docker で使用）       | django                             |                                          |
| MYSQL_HOST             | MySQL のホスト名（Docker で使用）         | db                                 |                                          |
| MYSQL_PORT             | MySQL のポート番号（Docker で使用）       | 3306                               |                                          |
| SECRET_KEY             | Django のシークレットキー                 | secretkey                          | 他者に推測されないランダムな値にすること |
| ALLOWED_HOSTS          | リクエストを許可するホスト名              | localhost 127.0.0.1 [::1] back web | フロントのホスト名                       |
| DEBUG                  | デバッグモードの切り替え                  | True                               | False                                    |
| TRUSTED_ORIGINS        | CORS で許可するオリジン                   | http://localhost                   |                                          |
| DJANGO_SETTINGS_MODULE | Django アプリケーションの設定モジュール   | project.settings.local             | project.settings.dev                     |

### 3.4.2. 設定

## 3.5. 使用方法
### 3.5.1. コマンド一覧
　　
| Make                | 実行する処理                                                            | 元のコマンド                                                                               |
| ------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| make prepare        | node_modules のインストール、イメージのビルド、コンテナの起動を順に行う | docker-compose run --rm front npm install<br>docker-compose up -d --build                  |
| make up             | コンテナの起動                                                          | docker-compose up -d                                                                       |
| make build          | イメージのビルド                                                        | docker-compose build                                                                       |
| make down           | コンテナの停止                                                          | docker-compose down                                                                        |
| make loaddata       | テストデータの投入                                                      | docker-compose exec app poetry run python manage.py loaddata crm.json                      |
| make makemigrations | マイグレーションファイルの作成                                          | docker-compose exec app poetry run python manage.py makemigrations                         |
| make migrate        | マイグレーションを行う                                                  | docker-compose exec app poetry run python manage.py migrate                                |
| make show_urls      | エンドポイントをターミナル上で一覧表示                                  | docker-compose exec app poetry run python manage.py show_urls                              |
| make shell          | テストデータの投入                                                      | docker-compose exec app poetry run python manage.py debugsqlshell                          |
| make superuser      | スーパーユーザの作成                                                    | docker-compose exec app poetry run python manage.py createsuperuser                        |
| make test           | テストを実行                                                            | docker-compose exec app poetry run pytest                                                  |
| make test-cov       | カバレッジを表示させた上でテストを実行                                  | docker-compose exec app poetry run pytest --cov                                            |
| make format         | black と isort を使ってコードを整形                                     | docker-compose exec app poetry run black . <br> docker-compose exec app poetry run isort . |
| make update         | Poetry 内のパッケージの更新                                             | docker-compose exec app poetry update                                                      |
| make app            | アプリケーション のコンテナへ入る                                       | docker exec -it app bash                                                                   |
| make db             | データベースのコンテナへ入る                                            | docker exec -it db bash                                                                    |
| make pdoc           | pdoc ドキュメントの作成                                                 | docker-compose exec app env CI_MAKING_DOCS=1 poetry run pdoc -o docs application           |
| make init           | Terraform の初期化                                                      | docker-compose -f infra/docker-compose.yml run --rm terraform init                         |
| make fmt            | Terraform の設定ファイルをフォーマット                                  | docker-compose -f infra/docker-compose.yml run --rm terraform fmt                          |
| make validate       | Terraform の構成ファイルが正常であることを確認                          | docker-compose -f infra/docker-compose.yml run --rm terraform validate                     |
| make show           | 現在のリソースの状態を参照                                              | docker-compose -f infra/docker-compose.yml run --rm terraform show                         |
| make apply          | Terraform の内容を適用                                                  | docker-compose -f infra/docker-compose.yml run --rm terraform apply                        |
| make destroy        | Terraform で構成されたリソースを削除                                    | docker-compose -f infra/docker-compose.yml run --rm terraform destroy                      |
  
リモートデバッグ を使用する際は以下の url を参考に設定してください<br>
[Django のコンテナへリモートデバッグしよう！](https://qiita.com/shun198/items/9e4fcb4479385217c323)

## 3.6. トラブルシューティング
  
<p align="right">(<a href="#top">トップへ</a>)</p>
  
# 4. 特記事項
Macでの動作確認なし
  
# 5. 参考資料
1. 