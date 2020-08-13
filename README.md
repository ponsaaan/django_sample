# django_sample

## 環境構築手順
* リポジトリをclone
* entrypoint.shに実行権限を付与
  * chmod +x app/entrypoint.sh
* アプリケーションを起動
  * docker-compose up -d --build
* localhost:8000にアクセス

* コマンド実行
  * docker-compose exec django <command you want to do>
  
## その他
* dockerコンテナ のなかに入る
  * sudo docker exec -i -t コンテナ名またはコンテナID bash
  or
  * sudo docker attach コンテナ名またはコンテナID
