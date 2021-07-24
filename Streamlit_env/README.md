
まずはクローンでロカールに反映


```
git clone https://github.com/umehara0506/Docker.git
```


## DockerでJupyterLabを立ち上げる


ここからはDocker操作です。
下記のコマンドを順番に実行してください。


### フォルダの移動
```
cd Docker/Streamlit環境
```

### イメージの作成
```
docker image build -t streamlit .
```

### イメージの確認
```
docker image ls
```

### app.pyの実行
```
docker run -v $PWD/src:/src -dit --rm -p 8501:8501 streamlit
```

http://localhost:8501/
で反映されていることを確認してください。

このままでも反映されますが、


JupyterLabの立ち上げ
```
docker run -v $PWD/src:/src -dit --rm -p 7777:8888 streamlit jupyter-lab --ip 0.0.0.0 --allow-root
```
docker run -v $PWD/src:/src -dit --rm -p 7777:8888 app jupyter-lab --ip 0.0.0.0 --allow-root

下記へアクセス
http://127.0.0.1:7777

コマンド実行時にでるアクセストークンを入力するとJupyterLabを使えます。
