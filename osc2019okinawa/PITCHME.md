## Python言語最新情報

### 〜モダンな文法を知ってPythonを使いこなそう〜

2019年4月20日 / OSC沖縄 / 鈴木たかのり

---

## アジェンダ

* TODO
* Pythonは30年近くの歴史
* 徐々に文法が改良されている
* 最新の書き方を把握して使いこなそう

---?include=assets/takanory.md

---?include=assets/pyconjp.md

---

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

## PEP

* Python Enhancement Proposal
  * Pythonの拡張提案
* [PEP 1](https://www.python.org/dev/peps/pep-0001/): PEPの目的とガイドライン
* TODO: PEPとはって説明をする

---

## 各バージョンでの重要な変更

### Python 2.4からPython 3.8まで

+++

### Python 2.4(2004年)

* [What's New In Python 2.4](https://docs.python.org/ja/3/whatsnew/2.4.html)
* [PEP 218](https://www.python.org/dev/peps/pep-0218/): ビルトインの集合(`set`)オブジェクト
* [PEP 289](https://www.python.org/dev/peps/pep-0289/): ジェネレータ式
* [PEP 318](https://www.python.org/dev/peps/pep-0318/): 関数とメソッドのためのデコレータ
* [PEP 322](https://www.python.org/dev/peps/pep-0322/): 逆順のイテレーション - `reversed()` 関数
* [PEP 328](https://www.python.org/dev/peps/pep-0328/): マルチラインインポート

+++

### Python 2.5(2006年)

* [What's New In Python 2.5](https://docs.python.org/ja/3/whatsnew/2.5.html)
* [PEP 308](https://www.python.org/dev/peps/pep-0308/): 条件式 - `x = true if condition else false`
* [PEP 328](https://www.python.org/dev/peps/pep-0328/): 絶対インポート、相対インポート
* [PEP 341](https://www.python.org/dev/peps/pep-0341/): try/except/finally の一体化
* 新モジュール - `ElementTree`、`sqlite3`、`ctypes`など

+++

### Python 2.6(2008年)

* [What's New In Python 2.6](https://docs.python.org/ja/3/whatsnew/2.6.html)
* [PEP 343](https://www.python.org/dev/peps/pep-0343/): `with`文
* [PEP 3101](https://www.python.org/dev/peps/pep-3101/): 進化版文字列フォーマッティング
* [PEP 3110](https://www.python.org/dev/peps/pep-3110/): 例外処理の変更 - `as`キーワード
* [PEP 3119](https://www.python.org/dev/peps/pep-3119/): 抽象基底クラス
* [PEP 3129](https://www.python.org/dev/peps/pep-3129/): クラスデコレータ

+++

### Python 2.7(2010年)

* [What's New In Python 2.7](https://docs.python.org/ja/3/whatsnew/2.7.html)
* [PEP 372](https://www.python.org/dev/peps/pep-0372/): `collections`に順序付き辞書を追加
* [PEP 378](https://www.python.org/dev/peps/pep-0378/): 1000区切りのための書式指定子
* [PEP 389](https://www.python.org/dev/peps/pep-0389/): コマンドライン解析のための`argparse`モジュール

+++

### Python 3.0-3.2(2008年)

* [What's New In Python 3.0](https://docs.python.org/ja/3/whatsnew/3.0.html)
* [PEP 3105](https://www.python.org/dev/peps/pep-3105/): `print()` 関数
* [PEP 3106](https://www.python.org/dev/peps/pep-3106/): `dict.keys()`、`.values()`、`.items()`の改良
* [PEP 238](https://www.python.org/dev/peps/pep-0238/): 除算演算子(`/`)の変更
* [PEP 274](https://www.python.org/dev/peps/pep-0274/): 辞書内包表記 - `{k: v for k, v in stuff}`
* セットリテラルとセット内包表記

+++

### Python 3.3(2012年)

* [What's New In Python 3.3](https://docs.python.org/ja/3/whatsnew/3.3.html)
* [PEP 397](https://www.python.org/dev/peps/pep-0397/): `py`コマンド - Windows の Python ランチャ
* [PEP 405](https://www.python.org/dev/peps/pep-0405/): `venv`モジュール - 仮想環境
* [PEP 420](https://www.python.org/dev/peps/pep-0420/): 暗黙的な名前空間パッケージ
* [PEP 380](https://www.python.org/dev/peps/pep-0380/): サブジェネレータへの委譲構文 - `yield from`
* [PEP 414](https://www.python.org/dev/peps/pep-0414/): 明示的なユニコードリテラル - `u'あ'`

+++

### Python 3.4(2014年)

* [What's New In Python 3.4](https://docs.python.org/ja/3/whatsnew/3.4.html)
* [PEP 453](https://www.python.org/dev/peps/pep-0453/): Pythonインストール時のPIPの明示的なブートストラッピング
* [PEP 435](https://www.python.org/dev/peps/pep-0435/): `enum`モジュール - 列挙型のサポート
* [PEP 428](https://www.python.org/dev/peps/pep-0428/): `pathlib`モジュール - オブジェクト指向のファイルシステムパス
* [PEP 450](https://www.python.org/dev/peps/pep-0450/): `statistics`モジュール - 基礎的な統計ライブラリ

+++

### Python 3.5(2015年)

* [What's New In Python 3.5](https://docs.python.org/ja/3/whatsnew/3.5.html)
* [PEP 492](https://www.python.org/dev/peps/pep-0492/): コルーチン、`async`構文と`await`構文
* [PEP 465](https://www.python.org/dev/peps/pep-0465/): 新たな行列乗算演算子 - `a @ b`
* [PEP 484](https://www.python.org/dev/peps/pep-0484/): `typing`モジュール - 型ヒント
* [PEP 441](https://www.python.org/dev/peps/pep-0441/): `zipapp`モジュール - Python ZIPアプリケーションのサポート改善
* [PEP 471](https://www.python.org/dev/peps/pep-0471/): `os.scandir()`関数 - より良く、速いディレクトリイテレータ

+++

### Python 3.6(2016年)

* [What's New In Python 3.6](https://docs.python.org/ja/3/whatsnew/3.6.html)
* [PEP 498](https://www.python.org/dev/peps/pep-0498/): フォーマット済み文字列リテラル - `f''`
* [PEP 515](https://www.python.org/dev/peps/pep-0515/): 数値リテラル内のアンダースコア
* [PEP 526](https://www.python.org/dev/peps/pep-0526/): 変数アノテーションの文法
* [PEP 525](https://www.python.org/dev/peps/pep-0525/): 非同期(async)ジェネレータ
* [PEP 530](https://www.python.org/dev/peps/pep-0530/): 非同期(async)内包表記
* [PEP 506](https://www.python.org/dev/peps/pep-0506/): 標準ライブラリに`Secrets`モジュール追加

+++

### Python 3.7(2018年)

* [What's New In Python 3.7](https://docs.python.org/ja/3/whatsnew/3.7.html)
* [PEP 553](https://www.python.org/dev/peps/pep-0553/): `breakpoint()` 関数
* [PEP 557](https://www.python.org/dev/peps/pep-0557/): データクラス
* Modify to impliment ssl package

+++

### Python 3.8(2019年10月予定):

* [PEP 572](https://www.python.org/dev/peps/pep-0572/): Assignment Expressions
