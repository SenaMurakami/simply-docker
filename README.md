# Simply Docker

こちらはDockerでローカル環境にシンプルな開発環境を作るためのリポジトリです。  

## 構築する開発環境

- PHP: 7.4.33
- Nginx: 1.25.0
- mysql: 5.7.44

## インストール/セットアップ方法

リポジトリをcloneしてください。

```ターミナル:ターミナル
git clone https://github.com/SenaMurakami/simply-docker.git project
cd project
touch .env
```

.envファイルを作成して、`MYSQL_ROOT_PASSWORD`,`MYSQL_DATABASE`,`MYSQL_USER`,`MYSQL_PASSWORD`を追加します。

.envファイル作成

```ターミナル:ターミナル
touch .env
```

`MYSQL_ROOT_PASSWORD`,`MYSQL_DATABASE`,`MYSQL_USER`,`MYSQL_PASSWORD`追加

```.env
MYSQL_ROOT_PASSWORD=mysql_root_password
MYSQL_DATABASE=database_name
MYSQL_USER=mysql_user
MYSQL_PASSWORD=mysql_password
```

> [!IMPORTANT]
> 上記をそのまま使わず、自分の環境に合わせてください。

コンテナを立ち上げてください。

```ターミナル:ターミナル
docker compose up -d
```

ブラウザで`http://localhost:8080/`を開いてください。  
phpinfoが表示されていればセットアップ完了です。

コンテナを停止するには

```ターミナル:ターミナル
docker compose down
```

## .envファイルについて

**絶対に.envファイルを共有しないでください**  
.envファイルには機密情報が含まれます。  
機密情報を含むファイルはGitで管理しないでください。
