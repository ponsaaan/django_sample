# django_sample

## 環境構築手順
* リポジトリをclone
* entrypoint.shに実行権限を付与
  * chmod +x app/entrypoint.sh
* .envファイルを配置受け取る
* アプリケーションをビルド&起動
  * docker-compose up -d --build
* DB生成
  * docker-compose exec django python3 manage.py migrate
* adminユーザー生成
  * docker-compose exec django python3 manage.py createsuperuser
  * username: root
  * pass: password
* 初期データを読み込む
  * docker-compose exec django python3 manage.py loaddata app/polls/fixtures/polls.json
* localhost:8000にアクセス

* コマンド実行
  * docker-compose exec django <command you want to do>
  
## その他
* dockerコンテナ のなかに入る
  * docker exec -it django bash
  * docker exec -it postgres bash
  * など
