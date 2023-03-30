## 第1週: Pythonの基本的な概念と構文

Pythonの基本的な構文、データ型、演算子、制御構造、関数などを学びます。また、Pythonの開発環境や実行方法、デバッグ方法なども学びます。


### トピック１：Pythonのインストールと環境設定

Pythonのインストールと環境設定はプログラムではなく、Pythonを使用するための準備です。公式サイト（https://www.python.org/) からPythonをダウンロードしてインストールし、環境変数にPythonのパスを追加します。


### トピック２：変数とデータ型

``` py
name = "にゃん太郎"
age = 30
height = 180.5
is_student = True

print(name, type(name))  # 出力: にゃん太郎 <class 'str'>
print(age, type(age))  # 出力: 30 <class 'int'>
print(height, type(height))  # 出力: 180.5 <class 'float'>
print(is_student, type(is_student))  # 出力: True <class 'bool'>

```

### トピック３：演算子と式

``` py
a = 10
b = 3

print(a + b)  # 出力: 13
print(a - b)  # 出力: 7
print(a * b)  # 出力: 30
print(a / b)  # 出力: 3.3333333333333335
print(a % b)  # 出力: 1
print(a ** b)  # 出力: 1000

```

### トピック４：条件文（if, elif, else）

``` py
score = 75

if score >= 90:
    print("秀")
elif score >= 80:
    print("優")
elif score >= 70:
    print("良")
else:
    print("不")

```

### トピック５：ループ（for, while）

``` py
# forループ
for i in range(5):
    print(i)  # 出力: 0, 1, 2, 3, 4

# whileループ
counter = 0
while counter < 5:
    print(counter)
    counter += 1  # 出力: 0, 1, 2, 3, 4

```


### トピック６：関数の定義と呼び出し

``` py
def greet(name):
    return f"やぁ, {name}!"

print(greet("John"))  # 出力: やぁ, John!

```

これらの例は、週1のトピックに関連する基本的なPythonプログラムです。これらを理解し、さらに練習することで、Pythonの基本概念を学ぶことができます。

### 週1の演習問題

    1.  自分の名前を表示するプログラムを作成してください。
    2.  二つの数値を入力し、それらの和、差、積、商を表示するプログラムを作成してください。
    3.  身長と体重を入力し、BMIを計算して表示するプログラムを作成してください。
    4.  1から100までの数字を出力するプログラムを作成してください。ただし、3の倍数のときは "Fizz"、5の倍数のときは "Buzz"、3と5の公倍数のときは "FizzBuzz" と表示してください。

