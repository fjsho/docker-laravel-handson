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
  権限設定
  `chmod -R 777 storage bootstrap/cache`
  バージョン確認
  `php artisan -V`
