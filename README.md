# Simple-Docker-MariaDB
Dockerを使用して、最小構成のMariaDBを構築します。


# 構築インフォ
## mariadbのimage情報
https://hub.docker.com/_/mariadb

## ポート
ローカルからアクセスする時は3333を使用する
既に、3333が使用済みでしたら重複しないポート番号に変更してください。
```
    ports:
      - "3333:3306"
```


# Dockerコンテナを作成・起動
現在のディレクトリにある docker-compose.yml ファイルを読み込み、
その設定に基づいてDockerコンテナを作成・起動します。
```
$ docker-compose up -d

// DBへのアクセス
$ mysql -h 127.0.0.1 -P 3333 -u root -pPasswordPassword
```

# 関連するものを含めて削除
$ docker-compose down --rmi all --volumes --remove-orphans

