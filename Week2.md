## 第2週: データ構造とモジュール

Pythonでのデータ構造とアルゴリズムの基礎を学びます。リスト、辞書、集合、タプルなどのデータ構造や、ソート、探索、再帰などのアルゴリズムを学びます。

### トピック１.  リスト

``` py
my_list = [1, 2, 3, 4, 5]

my_list.append(6)  # リストに要素を追加
print(my_list)  # 出力: [1, 2, 3, 4, 5, 6]

my_list.pop()  # リストから要素を削除
print(my_list)  # 出力: [1, 2, 3, 4, 5]

my_list[2] = 10  # リストの要素を変更
print(my_list)  # 出力: [1, 2, 10, 4, 5]

```

### トピック２.  タプル

``` py
my_tuple = (1, 2, 3, 4, 5)

print(my_tuple[1])  # タプルの要素にアクセス（出力: 2）

# タプルはイミュータブルなので、要素の変更や削除はできません。

```
### トピック３.  セット
``` py
my_set = {1, 2, 3, 4, 5}

my_set.add(6)  # セットに要素を追加
print(my_set)  # 出力: {1, 2, 3, 4, 5, 6}

my_set.remove(1)  # セットから要素を削除
print(my_set)  # 出力: {2, 3, 4, 5, 6}

```

### トピック４.  辞書
``` py
my_dict = {"apple": 3, "banana": 5, "orange": 2}

my_dict["grape"] = 4  # 辞書に要素を追加
print(my_dict)  # 出力: {'apple': 3, 'banana': 5, 'orange': 2, 'grape': 4}

del my_dict["apple"]  # 辞書から要素を削除
print(my_dict)  # 出力: {'banana': 5, 'orange': 2, 'grape': 4}

my_dict["banana"] = 6  # 辞書の要素を変更
print(my_dict)  # 出力: {'banana': 6, 'orange': 2, 'grape': 4}

```

### トピック５.  Python標準ライブラリ（datetime, random, math）
``` py
import datetime
import random
import math

# datetimeモジュール
current_date = datetime.datetime.now()
print(current_date)  # 現在日時を表示

# randomモジュール
rand_number = random.randint(1, 10)
print(rand_number)  # 1から10までのランダムな整数を表示

# mathモジュール
square_root = math.sqrt(16)
print(square_root)  # 16の平方根を表示（出力: 4.0）

```

### トピック６.  モジュールのインポートと使用法
``` py
# mathモジュールをインポートして使用する例
import math

print(math.pi)  # 円周率πを表示 (出力: 3.141592653589793)

# osモジュールをインポートして使用する例
import os

print(os.getcwd())  # 現在のディレクトリを表示

# 他のモジュールの関数やクラスをインポートする方法
from datetime import datetime

current_time = datetime.now()
print(current_time)  # 現在の日時を表示

```

### 週2の演習問題

    1.  リスト内の要素を逆順に並べ替えるプログラムを作成してください。
    2.  タプル内の要素をカウントし、辞書に格納して表示するプログラムを作成してください。
    3.  リスト内の重複する要素を削除し、新しいリストに格納するプログラムを作成してください。
    4.  辞書内のキーと値を入れ替えるプログラムを作成してください。
