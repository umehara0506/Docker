
まずはクローンでロカールに反映


```
git clone https://github.com/umehara0506/Docker.git
```

この記事自体は下記にあります。

```
cd Docker/JupyterLab環境
```

## DockerでJupyterLabを立ち上げる

ここからはDocker操作です。
下記のコマンドを順番に実行してください。

```
docker image build -t JupyterLab_env .
```

下記でイメージが作成されているか確認
```
docker image ls
```

JupyterLabの立ち上げ
```
docker run -v $PWD/src:/src -it --rm -p 8080:8080 jupyterlab_env jupyter-lab --ip 0.0.0.0 --port=8080 --allow-root
```

下記へアクセス
http://127.0.0.1:7777
http://127.0.0.1:8080

コマンド実行時にでるアクセストークンを入力するとJupyterLabを使えます。
