## タイトル

#### サブタイトル

2020年6月27日 / OSC Online/Hokkaido

鈴木たかのり

<!-- https://docs.google.com/document/d/1sfhGtTWzKcSUvPucC851jxF9c1DkW9GWb1MDCeDxWjU/edit -->

---

## アジェンダ

* Pythonの環境について
* 開発環境を整える方法
* その他

---

## Tweets 🐦 👍

`#osc2020do` / `@takanory`

+++

## スライドはこちら

* @fab[github] [`github.com/pyconjp/slides`](https://github.com/pyconjp/slides)

+++

## どんどん質問してください ‍🙇‍♂️

---?include=assets/takanory.md

---?include=assets/pyconjp2020.md

## Python Charity Talks

* https://pyconjp.connpass.com/event/177586/
* 2020年7月4日(土) 13:00-18:00
* オンラインイベント
* 参加費は全額Python Software Foundation(PSF)に寄付

+++

## PyCon JP ブース??に来てね

![PyCon JPブース](Remoで雑談)

#### コミュニケーション用 Slack ワークスペース

- [PyCon JP Fellow Slack](https://pyconjp-fellow.herokuapp.com/)

---

## インストール

+++

## インストール

* [`www.python.org/downloads`](https://www.python.org/downloads/)から公式版をインストール
* 最新バージョンは3.8.3
* 2020年10月に3.9がリリース予定

+++

## 他の手段

* anaconda
* pyenv?
* Linuxの話する?

---

## 仮想環境(venv)

+++

## 仮想環境(venv)

* [`docs.python.org/ja/3/library/venv`](https://docs.python.org/ja/3/library/venv.html)
* Pythonに標準でついてくる
* 常に使いましょう
* プロジェクト単位で使用するパッケージを変える

+++

## venv作成、有効化

```sh
$ python3.8 -m venv env
$ . env/bin/activate
(env) $
```

```sh
> py -3.8 -m venv env
> env\Scripts\activate.ps1
(env) >
```

+++

## venvとは

* パスを書き換えているだけ
* 削除するときはフォルダーごと削除

+++

## venv無効化

```sh
(env) $ deactivate
$
```

```sh
(env) > deactivate
>
```

---

## 静的チェックツール(flake8)

+++

## 静的チェックツール(flake8)

* [`flake8.pycqa.org`](https://flake8.pycqa.org/)
* コードを静的にチェックするコマンド
  * [pycodestyle](https://pycodestyle.pycqa.org/): PEP8のチェック
  * [pyflakes](https://pypi.org/project/pyflakes/): エラーが発生しそうなコードをチェック
  * [mccabe](https://pypi.org/project/mccabe/): 循環的複雑度のチェック

+++

## PEP8

* PEP 8 -- Style Guide for Python Code
  * [`www.python.org/dev/peps/pep-0008/`](https://www.python.org/dev/peps/pep-0008/)
  * [`pep8-ja.readthedocs.io`](https://pep8-ja.readthedocs.io/): 日本語訳
* Python標準のスタイルガイド
* 主なルール
  * インデント4つ
  * 1行の最大文字数
  * 空行の入れ方
  * スペースの入れ方

+++

## flake8をインストール

```
$ pip install flake8
```

+++

## だめなコード

```python
TODO: ここにだめなコードを入れる
```

+++

## flake8を実行

```sh
$ flake8 sample.py
TODO: ここにエラーメッセージ
```

+++

## コードをきれいにする

```python
TODO: きれいになったコード
```

+++

## flake8を再実行

```sh
$ flake8 sample.py
$
```

* エラーメッセージが出なくなった!!

+++

## flake8とエディター

* 多くのエディターから直接チェックできる
* PyCharm: External Toolsで設定
* VSCode: Python Extension→設定変更
* Emacs: flycheck, flymake
* Vim: vim-flake8

---

## black

![black logo](/osc2020do/images/black.png)

+++

## black

* [`black.readthedocs.io`](https://black.readthedocs.io/)
* black自体の説明

---

## まとめ

+++

## まとめ

* Python公式版
* venvで仮想環境
* flake8で静的チェック

---

## ありがとうございました 🙇‍♂️

---

## Question?


