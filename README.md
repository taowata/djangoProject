# djangoProject
# 前提事項
- Macでの開発を前提としています。
- Docker Desktop for Macをインストールしておいてください。

# 環境構築手順
- このリポジトリをforkする。
- forkしたリポジトリをローカルにcloneする。
### Djangoプロジェクト用Dockerイメージの作成

clone したディレクトリに移動して、その直下にある Dockerfile から Docker イメージを作成します。
```command
$ cd django-project/
$ docker build -t django-project .
```
### Dockerコンテナの実行
作成したイメージを使ってDockerコンテナを作成、実行し、bashを起動します。
```command
$ docker run --rm -it 8000:8000 -v $(pwd):/root/django-project django-project
```


