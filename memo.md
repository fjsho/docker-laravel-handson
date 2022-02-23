1. docker-compose.ymlの作成/記述
2. dockerfileの作成/記述
3. php.iniの作成/記述
4. srcディレクトリ作成
5. builed & up でアプリケーションサーバー動作確認
  `docker compose build`
  `docker dompose up -d`
Webサーバーコンテナを作る（nginx）
6. docker-compose.ymlの追記（web以下）
7. default.confの作成/記述
8. webサーバー動作確認
  デモファイル作成（src/public）
  http://localhost:8080/phpinfo.php
Laravelをインストール
9. appコンテナに入ってLaravelにインストール
  appコンテナ内に入る
  `docker compose exec app bash`
  コンテナ内でLaravelインストール
  `composer create-project --prefer-dist "laravel/laravel=9.*" .`
  権限設定（webからの書き込みに対して権限を付与する必要がある）
  `chmod -R 777 storage bootstrap/cache`
  バージョン確認
  `php artisan -V`
MySQLサーバのdbコンテナ作成
10. docker-compose.ymlの追記
11. Dockerfile作成/記述
12. infra/mysql/my.cnf作成/記述
13. build & up
14. 接続確認（エラー前提）
15. .envと.env.example環境ファイル修正
16. 接続確認
環境構築完了！！

