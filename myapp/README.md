## DockerでNext.jsの環境構築を行う手順

1. 作業ディレクトリを作成

```
$ mkdir 作業ディレクトリ
```

2. Dockerfile, docker-compose.ymlを作成

3. Dcokerイメージの作成

```
$ docker-compose build
```

4. イメージの確認

```
$ docker images
```

5. next.jsアプリの作成

```
$ docker-compose run --rm node npx create-next-app <docker-compose.ymlのcommandで指定したディレクトリ名>
```

6. コンテナの起動

```
$ docker-compose up -d
```

7. コンテナの確認(stateがupだと起動中..)

```
$ docker-compose ps -a
```

8. コンテナの停止、削除、ネットワーク削除を全て実行する場合

```
$ docker-compose down
```

9. さらにイメージも削除する場合

```
$ docker-compose down --rmi all
```
