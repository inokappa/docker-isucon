# 追加したこと

## 起動

```sh
# isucon7-qualify の取得
git clone https://github.com/isucon/isucon7-qualify.git

# コンテナの起動
docker-compose up -d db
docker-compose up -d app
docker-compose up -d web

# app にログインしてアプリケーションサーバーを起動
docker exec -t -i isucon7qualifier_app_1 /bin/bash
bundle exec puma -p 5000 -t 10 &
```

## app ソースコード

Sinatra Reloader が動いているので, カレントディレクトリの app.rb をいじれば, それがそのまま反映される.
