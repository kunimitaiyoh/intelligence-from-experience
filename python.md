# Python

## pdb を使用したデバッグ

| コマンド     | 説明                   |
| :----------- | :--------------------- |
| `s(tep)`     | ステップ イン          |
| `n(ext)`     | ステップ オーバー      |
| `r(eturn)`   | ステップ アウト        |
| `c(ontinue)` | 再開                   |
| `l(ist)`     | 前後のコードを表示     |
| `a(rgs)`     | 現在の関数の引数を表示 |
| `p foo`      | プリント               |
| `where`      | コールスタック         |
| `quit`       | 終了                   |

## モック

```python
# Python 3.3 以上なら、特別なモジュールをインストールする必要はない。
import unittest
from unittest.mock import patch

class FooTestCase(unittest.TestCase):
    @patch('Foo.bar')
    def test_mock_foo(self, bar):
        # Foo.bar メソッドが返す値を指定する
        bar.return_value = 1

        # 例外を発生させるには、その例外を生成して side_effect に追加する
        bar.side_effect = ValueError('あ')
```
