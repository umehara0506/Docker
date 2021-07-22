
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
JupyterLab環境
docker run -v $PWD/src:/src -it --rm -p 7777:8888 jupyterlab_env jupyter-lab --ip 0.0.0.0 --allow-root
```

下記へアクセス
http://127.0.0.1:7777

コマンド実行時にでるアクセストークンを入力するとJupyterLabを使えます。