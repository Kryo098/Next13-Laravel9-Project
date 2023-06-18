# Next13-Laravel9-Project


1.docker-compose.ymlの内容をビルドする(ルートディレクトリで下記コマンドを入力)

docker compose build

2.ビルド終了後、Laravelの依存関係をインストール

docker compose run --rm backend composer install
backend/src/.env.exampleファイルの内容をコピーし同じディレクトリに.envファイルを作成し、コピーした内容を張り付け保存

docker compose run --rm backend composer fund

docker compose upコマンドを入力しDockerを立ち上げ
http://localhost:8080/ にアクセスし、Laravelのデフォルト画面でkeyをgenerateし、Laravelのデフォルト画面が遷移したら成功

3.続いてNext.jsの依存関係をインストール

docker compose run --rm frontend npm install

4.デフォルトのマイグレーションが通るか確認（DBサーバが立ち上がっていないとエラーとなるので立ち上げ確認）

docker compose run --rm backend php artisan migrate

http://localhost:3000/ にアクセスし、Next.jsデフォルト画面が表示されたら成功
