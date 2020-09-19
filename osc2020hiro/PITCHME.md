## Python開発環境の整え方

2020年9月19日 / OSC Online/Hiroshima

清水川貴之

<!-- https://docs.google.com/document/d/1sfhGtTWzKcSUvPucC851jxF9c1DkW9GWb1MDCeDxWjU/edit -->

---

## アジェンダ

* Pythonの環境について
* 開発環境を整える方法
* デバッグ方法

---

## Tweets 🐦 👍

`#osc20hi` / `@shimizukawa`

+++

## スライドはこちら

* @fab[github] [`github.com/pyconjp/slides`](https://github.com/pyconjp/slides)

+++

## どんどん質問してください ‍🙇‍♂️

* Zoomのチャット
* YouTubeのコメント

---?include=assets/shimizukawa.md

+++?image=osc2020hiro/images/hiroshima.png&position=bottom&size=auto 58%

@snap[north span-100]
## 私と広島

* OCS 2020 Hiroshima に初参加
* 初広島！（論理）
@snapend

---?include=assets/pyconjp2020.md

+++

### コミュニケーション用Slack

* PyCon JP Fellow Slack
* [`pyconjp-fellow.herokuapp.com`](https://pyconjp-fellow.herokuapp.com/)

+++

## Python Charity Talks

* [`pyconjp.connpass.com/event/177586`](https://pyconjp.connpass.com/event/177586/)
* 2020年7月4日(土) 13:00-18:00
* オンラインイベント
* 全額Python Software Foundation(PSF)に寄付

+++?image=osc2020hiro/images/pycharity.png&size=auto 100%

+++

## ミーティングにも来てね

* C会場で14:00〜14:45
* セミナーの質疑応答など

---

## Python開発環境の整え方

* Pythonの環境について
* 開発環境を整える方法
* デバッグ方法

---

## Pythonインストール

+++

## Pythonインストール

* [`www.python.org/downloads`](https://www.python.org/downloads/)から公式版をインストール
  * WindowsはPATH設定のチェックを忘れずに
* 最新バージョンは3.8.5
* 2020年10月に3.9がリリース予定

+++?image=osc2020hiro/images/python-downloads.png&size=auto 100%

+++

## 環境構築ガイド

* [`www.python.jp/install/install`](https://www.python.jp/install/install.html)

![python.jpの環境構築ガイド](osc2020hiro/images/pythonjp-install.png)

+++

## 他の手段

* Anaconda: [`www.anaconda.com`](https://www.anaconda.com/)
* pyenv: [`github.com/pyenv/pyenv`](https://github.com/pyenv/pyenv)
* Homebrew: [`brew.sh`](https://brew.sh/)
* Linux:
  * Ubuntu 20.04LTS: Python 3.8.2
  
+++

## Pythonインストール

* 特に理由がなければ公式版を使おう

---

## 仮想環境(venv)

+++

## 仮想環境(venv)

* [`docs.python.org/ja/3/library/venv`](https://docs.python.org/ja/3/library/venv.html)
* Pythonに標準でついてくる
* 常に使いましょう
* プロジェクト単位で使用パッケージを変えられる

+++?image=osc2020hiro/images/venv.png&size=auto 100%

+++

## venvの概念

* システムのPython
  * venv1
    * Django 3.0.7
  * venv2
    * Django 2.2.13

+++

## venv作成、有効化

* macOS、Linux
  * `python3.8 -m venv 環境名`
  * `source 環境名/bin/activate`

```sh
$ python3.8 -m venv env
$ source env/bin/activate
(env) $
```

+++

## venv作成、有効化

* Windows
  * `py -3.8 -m venv 環境名`
  * `環境名\Scripts\activate.ps1`
  * `環境名\Scripts\activate.bat`

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

* `deactivate`

```sh
(env) $ deactivate
$

(env) > deactivate
>
```

+++

## 仮想環境(venv)

* パッケージをインストールするときは常に使おう

---

## パッケージ管理(pip)

+++

## パッケージ管理(pip)

* [`pip.pypa.io`](https://pip.pypa.io/en/stable/)
* サードパーティ製パッケージの管理ツール
* venvの中で使用するのが一般的

+++?image=osc2020hiro/images/pip.png&size=auto 100%

+++

## PyPI

* [`pypi.org`](https://pypi.org/)
* サードパーティー製パッケージの配布サイト
* 「パイピーアイ」と読むらしい

+++?image=osc2020hiro/images/pypi.png&size=auto 100%

+++

## pipでインストール

* `pip install パッケージ名`
* 依存パッケージもまとめてインストール

```bash
(env) $ pip install beautifulsoup4
Collecting beautifulsoup4
  Downloading beautifulsoup4-4.9.1-py3-none-any.whl (115 kB)
     |████████████████████████████████| 115 kB 2.1 MB/s 
Collecting soupsieve>1.2
  Downloading soupsieve-2.0.1-py3-none-any.whl (32 kB)
Installing collected packages: soupsieve, beautifulsoup4
Successfully installed beautifulsoup4-4.9.1 soupsieve-2.0.1
```

+++

## pipでインストール

* バージョン指定
  * `pip install パッケージ名==バージョン`
* 最新にアップグレード
  * `pip install -U パッケージ名`

```bash
(env) $ pip install beautifulsoup4==4.8.0
: (省略)
      Successfully uninstalled beautifulsoup4-4.9.1
Successfully installed beautifulsoup4-4.8.0
(env) $ pip install -U beautifulsoup4
: (省略)
Successfully installed beautifulsoup4-4.9.1
```

+++?code=osc2020hiro/piplist.txt&lang=bash

@snap[north span-100]
## パッケージ一覧を表示

* `pip list`
@snapend

+++?code=osc2020hiro/piplist-o.txt&lang=bash

@snap[north span-100]
## 古いパッケージを確認

* `pip list -o`
@snapend

+++

## パッケージ一覧を再利用

* `pip freeze > requirements.txt`
* requirements.txtファイルをバージョン管理

```bash
(env) $ pip freeze > requirements.txt
(env) $ cat requirements.txt
beautifulsoup4==4.8.0
soupsieve==2.0.1
```

* 別の仮想環境でインストール
  * `pip install -r requirements.txt`

```bash
$ python3.8 -m venv newenv
$ source newenv/bin/activate
(newenv) $ pip install -r requirements.txt
(newenv) $ pip freeze
beautifulsoup4==4.8.0
soupsieve==2.0.1
```

+++

## アンインストール

* `pip uninstall -y パッケージ名`
* 依存パッケージは削除されない

```bash
(env) $ pip uninstall -y beautifulsoup4
Found existing installation: beautifulsoup4 4.8.0
Uninstalling beautifulsoup4-4.8.0:
  Successfully uninstalled beautifulsoup4-4.8.0
```

+++

## パッケージの探し方

* Awesome Python: [`awesome-python.com`](https://awesome-python.com/)

![Awesome Python](osc2020hiro/images/awesome-python.png)

+++

## パッケージ管理(pip)

* pipコマンドを使いこなそう

---

## テキストエディター

+++

## テキストエディター

* 好きな物を使いましょう
  * シンタックスハイライト
  * TABでスペース4つ
* とくになければ以下がおすすめ
  * VSCode: [`code.visualstudio.com`](https://code.visualstudio.com/)
  * PyCharm: [`www.jetbrains.com/pycharm`](https://www.jetbrains.com/pycharm/)

+++?image=osc2020hiro/images/vscode.png&size=auto 100%

+++?image=osc2020hiro/images/pycharm.png&size=auto 100%

---

## 静的チェック(Flake8)

+++

## 静的チェック(Flake8)

* [`flake8.pycqa.org`](https://flake8.pycqa.org/)
* コードを静的にチェックするコマンド
  * [pycodestyle](https://pycodestyle.pycqa.org/): PEP8のチェック
  * [pyflakes](https://pypi.org/project/pyflakes/): エラーが発生しそうなコードをチェック
  * [mccabe](https://pypi.org/project/mccabe/): 循環的複雑度のチェック

+++?image=osc2020hiro/images/flake8.png&size=auto 100%

+++

## PEP8

* PEP 8 -- Style Guide for Python Code
  * [`www.python.org/dev/peps/pep-0008/`](https://www.python.org/dev/peps/pep-0008/)
  * [`pep8-ja.readthedocs.io`](https://pep8-ja.readthedocs.io/): 日本語訳
* Python標準のスタイルガイド
* 主なルール
  * インデントはスペース4つ
  * 1行の最大文字数は79文字
  * 空行の入れ方
  * スペースの入れ方

+++?image=osc2020hiro/images/pep8.png&size=auto 100%

+++?image=osc2020hiro/images/pep8-ja.png&size=auto 100%

+++

## Flake8をインストール

* `pip install flake8`

+++

## だめなコード

```python
from random import *

def add(a,b):
    c = choice([a, b]) # 意味のない処理
    return a + b
```

+++

## Flake8を実行

* `flake8 ファイル名`

```sh
$ cat sample.py
from random import *

def add(a,b):
    c = choice([a, b]) # 意味のない処理
    return a + b
$ flake8 sample.py
sample.py:1:1: F403 'from random import *' used; unable to detect undefined names
sample.py:3:1: E302 expected 2 blank lines, found 1
sample.py:3:10: E231 missing whitespace after ','
sample.py:4:5: F841 local variable 'c' is assigned to but never used
sample.py:4:9: F405 'choice' may be undefined, or defined from star imports: random
sample.py:4:23: E261 at least two spaces before inline comment
```

+++

## コードをきれいにする

```python
from random import choice


def add(a, b):
    c = choice([a, b])  # 意味のない処理
    return a + b, c
```

+++

## Flake8を再実行

* エラーメッセージが出なくなった!!

```sh
$ flake8 sample.py
$
```

+++

## Flake8とエディター

* 多くのエディターから直接チェックできる
* PyCharm: External Toolsで設定
* VSCode: Python Extension→設定変更
  * デフォルトのPylintは制限が強い
* Emacs: flycheck, flymake
* Vim: vim-flake8

+++

## 静的チェック(Flake8)

* Flake8を通るコードにしよう

---

## コード整形(Black)

+++

## コード整形(Black)

![Black logo](/osc2020hiro/images/black.png)

+++

## コード整形(Black)

* [`black.readthedocs.io`](https://black.readthedocs.io/)
* 頑固なコードフォーマッター
* PEP8準拠のコードにしてくれる
* 設定はほぼなし
  * Blackの流儀に合わせる

+++?image=osc2020hiro/images/black-web.png&size=auto 100%

+++

## Blackをインストール

* `pip install black`

+++

## だめなコード

```python
from random import *

def add(a,b):
    c = choice([a, b]) # 意味のない処理
    return a + b
```

+++?code=osc2020hiro/diff.txt&lang=bash

@snap[north span-100]
## Blackで差分を確認
@snapend

+++

## Blackでファイルを更新

* `black ファイル名`

```sh
$ black sample.py
$ cat sample.py
from random import *


def add(a, b):
    c = choice([a, b])  # 意味のない処理
    return a + b
```

+++

## コード整形(Black)

* Blackでコードを整形しよう

---

## デバッグ(pdb)

+++

## デバッグ(pdb)

* [`docs.python.org/ja/3/library/pdb`](https://docs.python.org/ja/3/library/pdb.html)
* Pythonの標準ライブラリ
* 対話型のデバッガ

+++?image=osc2020hiro/images/pdb.png&size=auto 100%

+++

## pdbを起動

* `python3 -m pdb プログラム.py`
* `breakpoint()` 関数

```bash
$ python3 -m pdb sample.py
/path/to/sample.py(1)<module>()
-> from random import choice
(Pdb) n
/path/to/sample.py(4)<module>()
-> def add(a, b):
```

+++

## pdbの主なコマンド

* `h(elp)`: ヘルプを表示
* `b(reak) 行番号`: ブレイクポイントを設定
* `n(ext)`: 次の行に移動
* `c(ont(inue))`: ブレイクポイントまで実行
* `l(ist)`: コードを表示
* `p 式`: 式を評価した結果を出力
* `q(uit)`: デバッガを終了

+++

## デバッグ(pdb)

* `print()` デバッグより効率的

---

## その他

+++

## その他

* テストコード: [unittest](https://docs.python.org/ja/3/library/unittest.html), [pytest](https://docs.pytest.org/)
* テスト環境: [tox](https://tox.readthedocs.io/en/latest/)
* 型ヒント: [typing](https://docs.python.org/ja/3/library/typing.html)
* 型ヒントチェック: [mypy](http://www.mypy-lang.org/)

---

## まとめ

+++

## まとめ

* Python公式版
* venvで仮想環境
* pipでパッケージ管理
* テキストエディター
* Flake8で静的チェック
* Blackでコード整形
* pdbでデバッグ

---

## ありがとうございました 🙇‍♂️

* @fab[twitter] [@shimizukawa](https://twitter.com/shimizukawa)
* @fab[github] [`github.com/pyconjp/slides`](https://github.com/pyconjp/slides)

+++

## ミーティングにも来てね

* C会場で14:00〜14:45
* セミナーの質疑応答など

+++

## Question?

+++

## ありがとうございました 🙇‍♂️

* @fab[twitter] [@shimizukawa](https://twitter.com/shimizukawa)
* @fab[github] [`github.com/pyconjp/slides`](https://github.com/pyconjp/slides)

