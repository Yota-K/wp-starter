## 起動
`$ git clone https://github.com/Yota-K/wp-starter.git`  
`$ docker-compose build`  
`$ docker-compose up -d`

## アクセス
`localhost:8080`

## コンテナを起動
`$ docker-compose start`

## コンテナを止める
`$ docker-compose stop`

## コンテナを消す
`$ docker-compose down`

## DBのデータを消す
`$ docker volume ls`   
`$ docker volume rm コンテナにマウントされたデータの名前`
