# todo4(todoアプリ)

## 概要

やること(todo)を一覧表示、削除、更新できる基本機能を備えた練習用アプリです。

## 環境構築手順

リポジトリをclone
```
git clone git@github.com:aki5538/todo4.git
cd todo4
```

Dockerを起動
```
docker compose up -d --build
```

envファイルの準備
```
cp src/.env.example src/.env
```

envファイルの修正

作成ができたら、以下のように修正してください。
```
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=laravel_db
DB_USERNAME=laravel_user
DB_PASSWORD=laravel_pass
```

Laravelのセットアップ
```
docker-compose exec php bash
composer install
php artisan migrate
php artisan key:generate
```

初期データの投入
```
php artisan db:seed
```

## 使用技術(実行環境)
- PHP 8.1
- Laravel 8.75
- MySQL 8.0

## ER図
![alt](docs/erd.png)

## 動作URL

- 開発環境 : http://localhost/
- phpMyAdmin : http://localhost:8080/


