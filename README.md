# 手順書

## 依存ソフトウェア
事前に以下のソフトウェアを導入しておいてください
* git
* Docker
* Docker Compose

## 構築手順
### 1.ソースコード設置
GitHub上に公開されているリポジトリをCloneします。
```
$ git clone https://github.com/sakakota/sysDev-late
$ cd sysDev-late
```

### 2.コンテナの起動
Docker Composeでコンテナを起動します。
```
$ docker-compose build
$ docker-compose up
```

### 3.データベースの初期化
コンテナ上のデータベースへ接続してSQLを実行します。
```
$ docker exec -it mysql mysql techc
[mysql] source /home/USER_NAME/sysDev-late/init.sql
```
### 4.動作の確認
ブラウザ上で動作確認をします。
http://YOUR_IP/login.php に接続します。
構築手順は以上になります。
