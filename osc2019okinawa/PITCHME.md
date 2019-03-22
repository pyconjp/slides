## Python言語最新情報

### 〜モダンな文法を知ってPythonを使いこなそう〜

2019年4月20日 / OSC沖縄 / 鈴木たかのり

---

## アジェンダ

* Pythonは30年近くの歴史
* 徐々に文法が改良されている
* 最新の書き方を把握して使いこなそう

---?include=assets/takanory.md

---?include=assets/pyconjp.md

## 最初に質問

+++

### プログラミングしたことある人🙋‍♂️

+++

### Python書いたことある人️🙋‍♀️‍

+++

### Python 2を書いたことある人🙋‍♂️

### Python 3を書いたことある人️🙋‍♀️

---

## Python開発の歴史

* TODO: ここに図を入れる

+++

## PEP: Python Enhancement Proposal

* https://www.python.org/dev/peps/pep-0001/
* PEPとはって説明をする

---

## 各バージョンでの重要な変更

### Python 2.4からPython 3.8まで

+++

### Python 2.4(2004年):

* [PEP 218](https://www.python.org/dev/peps/pep-0218/): Adding a Built-In Set Object Type
* [PEP 289](https://www.python.org/dev/peps/pep-0289/): Generator Expressions
* [PEP 318](https://www.python.org/dev/peps/pep-0318/): Decorators for Functions and Methods
* [PEP 322](https://www.python.org/dev/peps/pep-0322/): Reverse Iteration
* [PEP 328](https://www.python.org/dev/peps/pep-0328/): Multi-line Imports

+++

### Python 2.5(2006年):

* [PEP 308](https://www.python.org/dev/peps/pep-0308/): Conditional Expressions
* [PEP 328](https://www.python.org/dev/peps/pep-0328/): Absolute and Relative Imports
* [PEP 341](https://www.python.org/dev/peps/pep-0341/): Unified try/except/finally
* New Modules / ElementTree, sqlite3 and more package 

+++

### Python 2.6(2008年):

* [PEP 343](https://www.python.org/dev/peps/pep-0343/): The 'with' statement
* [PEP 3101](https://www.python.org/dev/peps/pep-3101/): Advanced String Formatting / str.format
* [PEP 3110](https://www.python.org/dev/peps/pep-3110/): Exception-Handling Changes / except Exception as e
* [PEP 3119](https://www.python.org/dev/peps/pep-3119/): Abstract Base Classes
* [PEP 3129](https://www.python.org/dev/peps/pep-3129/): Class Decorators

+++

### Python 2.7(2010年):

* [PEP 372](https://www.python.org/dev/peps/pep-0372/): Adding an Ordered Dictionary to collections
* [PEP 378](https://www.python.org/dev/peps/pep-0378/): Format Specifier for Thousands Separator
* [PEP 389](https://www.python.org/dev/peps/pep-0389/): The argparse Module for Parsing Command Lines

+++

### Python 3.0-3.2(2008年):

* [PEP 3105](https://www.python.org/dev/peps/pep-3105/): print As a Function
* [PEP 3106](https://www.python.org/dev/peps/pep-3106/): Revamping dict.keys():, .values(): and .items():
* [PEP 238](https://www.python.org/dev/peps/pep-0238/): Changing the Division Operator/ //
* [PEP 274](https://www.python.org/dev/peps/pep-0274/): Dict Comprehensions / {k](https://www.python.org/dev/peps/pep-0218/): v for k, v in stuff}
* Set literals and comprehensions

+++

### Python 3.3(2012年):

* [What's New In Python 3.3](https://docs.python.org/ja/3/whatsnew/3.3.html)
* [PEP 397](https://www.python.org/dev/peps/pep-0397/): `py` コマンド -- Windows の Python ランチャ
* [PEP 405](https://www.python.org/dev/peps/pep-0405/): `venv` モジュール -- 仮想環境
* [PEP 420](https://www.python.org/dev/peps/pep-0420/): 暗黙的な名前空間パッケージ
* [PEP 380](https://www.python.org/dev/peps/pep-0380/): サブジェネレータへの委譲構文 `yield from`
* [PEP 414](https://www.python.org/dev/peps/pep-0414/): 明示的なユニコードリテラル -- `u'あ'`

+++

### Python 3.4(2014年):

* [What's New In Python 3.4](https://docs.python.org/ja/3/whatsnew/3.4.html)
* [PEP 453](https://www.python.org/dev/peps/pep-0453/): Python インストール時の PIP の明示的なブートストラッピング
* [PEP 435](https://www.python.org/dev/peps/pep-0435/): `enum` モジュール -- 列挙型のサポート
* [PEP 428](https://www.python.org/dev/peps/pep-0428/): `pathlib` モジュール -- オブジェクト指向のファイルシステムパス
* [PEP 450](https://www.python.org/dev/peps/pep-0450/): `statistics` モジュール -- 基礎的な統計ライブラリ

+++

### Python 3.5(2015年):

* [What's New In Python 3.5](https://docs.python.org/ja/3/whatsnew/3.5.html)
* [PEP 492](https://www.python.org/dev/peps/pep-0492/): コルーチン、async 構文と await 構文
* [PEP 465](https://www.python.org/dev/peps/pep-0465/): 新たな行列乗算演算子 `a @ b`
* [PEP 484](https://www.python.org/dev/peps/pep-0484/): `typing` モジュール -- 型ヒント
* [PEP 441](https://www.python.org/dev/peps/pep-0441/): `zipapp` モジュール -- Python ZIP アプリケーションのサポートの改善
* [PEP 471](https://www.python.org/dev/peps/pep-0471/): `os.scandir()` 関数 -- より良く、速いディレクトリイテレータ

+++

### Python 3.6(2016年):

* [What's New In Python 3.6](https://docs.python.org/ja/3/whatsnew/3.6.html)
* [PEP 498](https://www.python.org/dev/peps/pep-0498/): フォーマット済み文字列リテラル
* [PEP 515](https://www.python.org/dev/peps/pep-0515/): 数値リテラル内のアンダースコア
* [PEP 526](https://www.python.org/dev/peps/pep-0526/): 変数アノテーションの文法
* [PEP 525](https://www.python.org/dev/peps/pep-0525/): 非同期ジェネレータ
* [PEP 530](https://www.python.org/dev/peps/pep-0530/): 非同期内包表記
* [PEP 506](https://www.python.org/dev/peps/pep-0506/): 標準ライブラリーに Secrets モジュールを追加

+++

### Python 3.7(2018年):

* [What's New In Python 3.7](https://docs.python.org/ja/3/whatsnew/3.7.html)
* [PEP 553](https://www.python.org/dev/peps/pep-0553/): `breakpoint()` 関数
* [PEP 557](https://www.python.org/dev/peps/pep-0557/): データクラス
* Modify to impliment ssl package

+++

### Python 3.8(2019年10月予定):

* [PEP 572](https://www.python.org/dev/peps/pep-0572/): Assignment Expressions
