# 使い方

1. cd コマンドで dockerファイルまで移動してください。
1. dockerのファイル内で以下コマンドを実行しましょう
```
sh run.sh
```

- run.shで何をしているか
> 以下コマンドと`npm install`が実行されている
```
docker-compose up -d --build
```

- 接続してみる http://localhost:8080/

# コンテナを消す

1. dockerファイルまで移動。
1. 以下コマンドを実行。
```
sh delete.sh
```

- 実行内容
```
docker-compose down --rmi all
```

# 使えると便利なコマンド集
---
- `docker-compose up`
> コンテナの構築、作成、起動を行ってくれます
>
> オプションを付けることでバックグラウンドで実行することもできます
##### 少し紹介
- `-d` バックグラウンドでコンテナを実行
- `-build` コンテナを開始前にイメージを構築する
---
- `docker-compose down`
> コンテナを停止し、 up で作成したコンテナ・ネットワーク・ボリューム・イメージを削除します
- `--rmi all` docker-compose upで作られた全イメージを削除
---
- `docker-compose exec`
> サービスに対する任意のコマンドを実行する
---
- `docker-compose ps`
> コンテナのプロセス(状態)を見ることができます
---
- `docker-compose start`
- `docker-compose stop`
- `docker-compose restart`
> `docker-compose stop`は、コンテナを停止しますが、削除しません。
>
> `docker-compose start`で、停止させたコンテナを起動できます。
>
> コンテナを再起動したい場合は`docker-compose restart`を使いましょう。
