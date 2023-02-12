# 使い方

## 起動

```sh
docker compose -f docker-compose.dev.yml up --build --remove-orphans
```

## rails server

Docker コンテナに入って手動で起動することを推奨しています（debugger 等を使用する際の問題を避けるため）

```sh
$ docker compose -f docker-compose.dev.yml exec app bash
# bin/rails s -b '0.0.0.0'
```

## rails console

`rails server` と同様、Docker コンテナに入って手動で起動することを推奨しています。

```sh
$ docker compose -f docker-compose.dev.yml exec app bash
# bin/rails c
```

## 停止

```sh
docker compose -f docker-compose.dev.yml stop
```
