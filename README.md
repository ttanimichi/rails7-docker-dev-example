# 使い方

## Docker コンテナを起動

```sh
docker compose -f docker-compose.dev.yml up --build --remove-orphans
```

## データベースの作成

```sh
docker compose -f docker-compose.dev.yml exec app bin/rails db:create db:migrate
```

## rails server

Docker コンテナに入って手動で起動することを推奨しています（debugger 等を使用する際の問題を避けるため）

```sh
docker compose -f docker-compose.dev.yml exec app bin/rails s
```

## rails console

`rails server` と同様、Docker コンテナに入って起動することを推奨しています。

```sh
docker compose -f docker-compose.dev.yml exec app bin/rails c
```

## 停止

```sh
docker compose -f docker-compose.dev.yml stop
```
