## Python言語最新情報

#### 〜モダンな文法を知ってPythonを使いこなそう〜

2019年9月28日 / OSC島根 / 清水川貴之

---

## アジェンダ

* Pythonには30年近くの歴史がある
* 徐々に改良されている
* 最新の書き方を知って、使いこなそう

+++

## どんどん質問してください‍🙇‍♂️

---?include=assets/shimizukawa.md

---

## 島根に初めて来ました

+++

### TBD

（島根エピソード?）

---?include=assets/pyconjp2019.md

+++

## PyCon JPブースにも来てね

![PyCon JPブース](osc2019do/images/pyconjp-booth.jpg)

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

+++?image=assets/images/python-version-graph.png&size=90% auto

+++

## PEP

* Python Enhancement Proposal
  * Pythonの拡張提案
* [PEP 1](https://www.python.org/dev/peps/pep-0001/): PEPの目的とガイドライン
  * 新機能を提案(Draft)
  * →議論して受理(Accepted)/否認(Rejeted)
  * →実装→マージして終了(Final)

---

## 各バージョンでの重要な変更

#### Python 2.4からPython 3.8まで

+++

### Python 2.4(2004年)

* [What's New In Python 2.4](https://docs.python.org/ja/3/whatsnew/2.4.html)
* [PEP 218](https://www.python.org/dev/peps/pep-0218/): ビルトインの集合(`set`)オブジェクト
* [PEP 289](https://www.python.org/dev/peps/pep-0289/): ジェネレータ式
* [PEP 318](https://www.python.org/dev/peps/pep-0318/): 関数とメソッドのためのデコレータ
* [PEP 322](https://www.python.org/dev/peps/pep-0322/): 逆順のイテレーション
  * `reversed()` 関数
* [PEP 328](https://www.python.org/dev/peps/pep-0328/): マルチラインインポート

+++

### Python 2.5(2006年)

* [What's New In Python 2.5](https://docs.python.org/ja/3/whatsnew/2.5.html)
* [PEP 308](https://www.python.org/dev/peps/pep-0308/): 条件式
* [PEP 328](https://www.python.org/dev/peps/pep-0328/): 絶対インポート、相対インポート
* [PEP 341](https://www.python.org/dev/peps/pep-0341/): `try`/`except`/`finally` の一体化
* 新モジュール - `ElementTree`、`sqlite3`、`ctypes` など

+++

### Python 2.6(2008年)

* [What's New In Python 2.6](https://docs.python.org/ja/3/whatsnew/2.6.html)
* [PEP 343](https://www.python.org/dev/peps/pep-0343/): `with` 文
* [PEP 3101](https://www.python.org/dev/peps/pep-3101/): 進化版文字列フォーマッティング
* [PEP 3110](https://www.python.org/dev/peps/pep-3110/): 例外処理の変更
  * `as` キーワード
* [PEP 3119](https://www.python.org/dev/peps/pep-3119/): 抽象基底クラス
* [PEP 3129](https://www.python.org/dev/peps/pep-3129/): クラスデコレータ

+++

### Python 2.7(2010年)

* [What's New In Python 2.7](https://docs.python.org/ja/3/whatsnew/2.7.html)
* [PEP 372](https://www.python.org/dev/peps/pep-0372/): `collections` に順序付き辞書を追加
* [PEP 378](https://www.python.org/dev/peps/pep-0378/): 1000区切りのための書式指定子
* [PEP 389](https://www.python.org/dev/peps/pep-0389/): コマンドライン解析のための `argparse` モジュール

+++

### Python 3.0-3.2(2008年)

* [What's New In Python 3.0](https://docs.python.org/ja/3/whatsnew/3.0.html)
* [PEP 3105](https://www.python.org/dev/peps/pep-3105/): `print()` 関数
* [PEP 3106](https://www.python.org/dev/peps/pep-3106/): `dict.keys()` `.values()` `.items()` の改良
* [PEP 238](https://www.python.org/dev/peps/pep-0238/): 除算演算子(`/`)の変更
* [PEP 274](https://www.python.org/dev/peps/pep-0274/): 辞書内包表記
* セットリテラルとセット内包表記

+++

### Python 3.3(2012年)

* [What's New In Python 3.3](https://docs.python.org/ja/3/whatsnew/3.3.html)
* [PEP 397](https://www.python.org/dev/peps/pep-0397/): Windows の Python ランチャ
  * `py` コマンド
* [PEP 405](https://www.python.org/dev/peps/pep-0405/): `venv`モジュール -- 仮想環境
* [PEP 420](https://www.python.org/dev/peps/pep-0420/): 暗黙的な名前空間パッケージ
* [PEP 380](https://www.python.org/dev/peps/pep-0380/): サブジェネレータへの委譲構文
  * `yield from`
* [PEP 414](https://www.python.org/dev/peps/pep-0414/): 明示的なユニコードリテラル -- `u'あ'`

+++

### Python 3.4(2014年)

* [What's New In Python 3.4](https://docs.python.org/ja/3/whatsnew/3.4.html)
* [PEP 453](https://www.python.org/dev/peps/pep-0453/): Pythonインストール時のpipの明示的なブートストラッピング
* [PEP 435](https://www.python.org/dev/peps/pep-0435/): `enum` モジュール
  * 列挙型のサポート
* [PEP 428](https://www.python.org/dev/peps/pep-0428/): `pathlib` モジュール
  * オブジェクト指向のファイルシステムパス
* [PEP 450](https://www.python.org/dev/peps/pep-0450/): `statistics` モジュール
  * 基礎的な統計ライブラリ

+++

### Python 3.5(2015年)

* [What's New In Python 3.5](https://docs.python.org/ja/3/whatsnew/3.5.html)
* [PEP 492](https://www.python.org/dev/peps/pep-0492/): コルーチン、`async`構文と`await`構文
* [PEP 465](https://www.python.org/dev/peps/pep-0465/): 新たな行列乗算演算子 -- `a @ b`
* [PEP 484](https://www.python.org/dev/peps/pep-0484/): `typing` モジュール -- 型ヒント
* [PEP 441](https://www.python.org/dev/peps/pep-0441/): `zipapp` モジュール
  * Python ZIPアプリケーションのサポート改善
* [PEP 471](https://www.python.org/dev/peps/pep-0471/): `os.scandir()`関数
  * より良く、速いディレクトリイテレータ

+++

### Python 3.6(2016年)

* [What's New In Python 3.6](https://docs.python.org/ja/3/whatsnew/3.6.html)
* [PEP 498](https://www.python.org/dev/peps/pep-0498/): フォーマット済み文字列リテラル -- `f''`
* [PEP 515](https://www.python.org/dev/peps/pep-0515/): 数値リテラル内のアンダースコア
* [PEP 526](https://www.python.org/dev/peps/pep-0526/): 変数アノテーションの文法
* [PEP 525](https://www.python.org/dev/peps/pep-0525/): 非同期(async)ジェネレータ
* [PEP 530](https://www.python.org/dev/peps/pep-0530/): 非同期(async)内包表記
* [PEP 506](https://www.python.org/dev/peps/pep-0506/): 標準ライブラリに `secrets` モジュール追加

+++

### Python 3.7(2018年)

* [What's New In Python 3.7](https://docs.python.org/ja/3/whatsnew/3.7.html)
* [PEP 553](https://www.python.org/dev/peps/pep-0553/): `breakpoint()` 関数
* [PEP 557](https://www.python.org/dev/peps/pep-0557/): データクラス

+++

### Python 3.8(2019年10月予定)

* [What's New In Python 3.8](https://docs.python.org/ja/3.8/whatsnew/3.8.html)
* [PEP 572](https://www.python.org/dev/peps/pep-0572/): 代入式
* [PEP 570](https://www.python.org/dev/peps/pep-0570/):	位置指定のみ引数
* fリテラルでの `=` によるデバッグ

---

## 新旧のスタイルを比較

+++

### PEP 328: マルチラインインポート

* 全バージョン

```python
from module_name import func1, func2, \
                        func3, func4, \
                        func5, func6
```

* Python 2.4以上

```python
from module_name import (func1, 
                         func2, 
                         func3,
                         func4, 
                         func5, 
                         func6)
```

+++

### PEP 202: リスト内包表記(1/3)

* 内包表記なし

```python
li = []
for i in range(10):
    li.append(i * i)
```

* リスト内包表記

```python
li = [i * i for i in range(10)]
```

+++

### PEP 202: リスト内包表記(2/3)

* 内包表記なし

```python
li = []
for i in range(10):
    if i % 2 == 0:
        li.append(i * i)
```

* リスト内包表記

```python
li = [i * i for i in range(10) if i % 2 == 0]
```

+++

### PEP 202: リスト内包表記(3/3)

* 内包表記なし

```python
li = []
for i in range(10):
    for j in range(5):
        li.append(i * j)
```

* リスト内包表記

```python
li = [i * j for i in range(10) for j in range(5)]
```

+++

### リスト、辞書、セット内包表記

* リスト内包表記

```python
>>> [i * i for i in range(10)]
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

* Python 2.7以上
* PEP 274: 辞書内包表記

```python
>>> {str(i): i * i for i in range(10)}
{'0': 0, '1': 1, '2': 4, '3': 9, '4': 16, '5': 25, '6': 36, '7': 49, '8': 64, '9': 81}
```

* セット内包表記

```python
>>> {i * i % 10 for i in range(10)}
{0, 1, 4, 5, 6, 9}
```

+++

### PEP289: ジェネレータ式

* ジェネレータ関数

```python
def func():
    for i in range(10):
        if i % 2 == 0:
            yield i * 1
```

* ジェネレータ式

```python
(i * i for i in range(10) if i % 2 == 0)
```

+++

### `sort()` メソッドと `sorted()` 関数

* 全バージョン

```python
li = [1, 3, 10, 2, 5]
li.sort()
```

* Python 2.4以上(副作用なし)

```
li = [1, 3, 10, 2, 5]
new_li = sorted(li)
```

+++

### PEP 308: 条件式

* 全バージョン

```python
if condition:
    x = true_value
else:
    x = false_value
```

* Python 2.5以上

```python
x = true_value if condition else false_value
```

+++

### PEP 343: `with` 文

* 全バージョン

```python
f = open('filename.txt')
data = f.read()
f.close()
```

* Python 2.6以上

```python
with open('filename.txt') as f:
    data = f.read()
```

+++

### `%s` / `.format()` / `f` リテラル

* 全バージョン

```python
from datetime import date
s = "Today: %s" % date.today()
```

* Python 2.6以上

```python
from datetime import date
s = "Today: {}".format(date.today())
```

* Python 3.6以上
* PEP 498: フォーマット済み文字列リテラル

```python
from datetime import date
s = f"Today: {date.today()}"
```

+++

### PEP 3110: 例外処理の変更

* Python 2

```
try:
    1/0
except Exception, e:
    return e
```

* Python 2.6以上

```
try:
    1/0
except Exception as e:
    return e
```

+++

### PEP3105: `print` 文と `print()` 関数

* Python 2

```python
print "message"
```

* Python 3

```python
print("message")
```

+++

### PEP238: 除算演算子 `/` と `//`

* Python 2

```python
>>> 5 / 2
2
>>> 5 / 2.0
2.5
```

* Python 3

```python
>>> 5 / 2
2.5
>>> 5 // 2.0
2
```

+++

### PEP 435: `enum` モジュール

* Python 3.4以上

```
import enum

class Tast(enum.IntEnum):
    todo = 1
    in_progress = 2
    done = 3
    
    @classmethod
    def get_task_types(cls):
        return tuple((x.value, x.name) for x in cls)
```

+++

### PEP 465: `@` 演算子 -- `a @ b`

```python
>>> import numpy as np
>>> a = np.array([[1, 2]])
>>> b = np.array([[3], [4]])
```

* 全バージョン

```python
>>> np.dot(a, b)
array([[11]])
```

* Python3.5以上

```
>>> a @ b
array([[11]])
```

+++

### PEP 428: `pathlib` モジュール

* 全バージョン

```python
import os
current = os.getcwd()
filepath = os.path.join(current, "dir", "filename.txt")
with open(filepath) as f:
    data = f.read()
```

* Python 3.6以上

```python
from pathlib import Path
p = Path(".") / "dir" / "filename.txt"
with p.open() as f:
    data = f.read()
```

+++

### `os.listdir()` と `pathlib`

* 全バージョン

```python
import os
for name in os.listdir(PATH):
    if not name.startswith('.') and os.path.isfile(os.path.join(PATH, name)):
        print(name)
```

* Python 3.6以上

```python
from pathlib import Path
for entry in Path(PATH).iterdir():
    if not entry.name.startswith('.') and entry.is_file():
        print(entry.name)
```

+++

### PEP 557: データクラス

* Python 3.7以上

```python
@dataclass
class InventoryItem:
    name: str
    unit_price: float
    quantity_on_hand: int = 0

    def total_cost(self) -> float:
        return self.unit_price * self.quantity_on_hand
```

+++

### PEP 553: `breakpoint()` 関数

* 全バージョン

```python
import pdb; pdb.set_trace()
```

* Python 3.7以上

```python
breakpoint()
```

+++

### PEP 572: 代入式 -- `a := b`

* "walrus operator" (セイウチ演算子) `:=`

* 全バージョン

```python
m = re.match(pat, s)
if m:
    # mに対しての処理
```

* Python 3.8

```python
if m := re.match(pat, s):
    # mに対しての処理
```

+++

### PEP 570: 位置指定のみ引数

* Python 3.8
* `/` の前の引数は位置指定のみ

```python
def pow(x, y, z=None, /):
    r = x**y
    if z is not None:
        r %= z
    return r
```

```python
pow(2, 10)  # OK
pow(2, 10, 17)  # OK
pow(x=2, y=10)  # NG
pow(2, 10, z=17)   # NG
```

+++

### fリテラルでの `=` によるデバッグ

* Python 3.8

```python
x = 3
print(f'{x*9 + 15=}')
```

* 以下のように出力される

```
x*9 + 15=42
```

---

## まとめ

+++

### まとめ

* Pythonは徐々に改良されている
* 後方互換性を維持しながら、新しい機能を追加している
* 少しずつ新しい文法を使っていこう

---

## ありがとうございました🙇‍♂️

---

## Question?
