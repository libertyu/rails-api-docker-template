# 環境構築手順

1. リポジトリをクローン

```
git cloen https://github.com/libertyu/rails-api-docker-template.git
```

2. ビルド

```
docker-compose build

```

3. docker 起動

```
<!-- ActiveRecordやサーバーログみたい時はこれを実行 -->
docker-compose up

<!-- バックグラウンド起動 -->
docker-compose up -d
```

# コマンド

コンテナ停止

```
docker-compose up -d
```

コンテナ停止

```
docker-compose down
```

コンテナに入る

```
docker container exec -it <コンテナ名> bash
```

DB 作成

```
docker-compose run web rails db:create
```

DB リセット

```
docker-compose run web rails db:reset
```

マイグレーション実行

```
docker-compose run web rails db:migrate
```

コンソール実行

```
docker-compose run web rails console
```

コントローラー作成

```
docker-compose run web rails g controller <コントローラー名>
```

モデル作成

```
docker-compose run web rails g model <モデル名>
```
