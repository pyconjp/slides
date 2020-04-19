# グラフ作成用のJupyter Notebook置き場

## 環境構築

* 以下の手順で環境を作成してJupyter Notebookを起動する

```sh
$ python3.8 -m venv env
$ . env/bin/activate
(env) $ pip install -r requirements.txt
(env) $ jupyter notebook
```

## グラフ描画

* `python history.ipynb`を開いて実行すると、Pythonのバージョンについてのグラフが描画されて `history.png` に保存される
