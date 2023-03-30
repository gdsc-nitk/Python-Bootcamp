## 第3週: オブジェクト指向プログラミングとファイル操作

Pythonのオブジェクト指向プログラミングの基礎を学びます。クラス、オブジェクト、継承、多態性などの概念や、実際の例を使って学びます。

### トピック１.  クラスとオブジェクト
``` py
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def bark(self):
        print(f"わん！僕の名前は {self.name}です.")

dog1 = Dog("マロン", 3)
dog2 = Dog("ムギ", 5)

dog1.bark()  # 出力: わん！僕の名前はマロンです.
dog2.bark()  # 出力: わん！僕の名前はムギです.
```


### トピック２.  インスタンス変数とメソッド
``` py
class Circle:
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * (self.radius ** 2)

circle1 = Circle(5)
circle2 = Circle(10)

print(circle1.area())  # 出力: 78.5
print(circle2.area())  # 出力: 314.0

```


### トピック３.  継承と多態性
``` py
class Animal:
    def speak(self):
        raise NotImplementedError("サブクラスにこのメソッドを定義する必要がある")

class Dog(Animal):
    def speak(self):
        return "わん!"

class Cat(Animal):
    def speak(self):
        return "にゃん!"

animals = [Dog(), Cat()]

for animal in animals:
    print(animal.speak())  # 出力: わん!, にゃん!

```


### トピック４.  ファイル操作（読み込み、書き込み、追加）
``` py
# ファイルを書き込みモードで開く
with open("example.txt", "w") as f:
    f.write("Hello, World!")

# ファイルを読み込みモードで開く
with open("example.txt", "r") as f:
    content = f.read()
    print(content)  # 出力: Hello, World!

# ファイルを追記モードで開く
with open("example.txt", "a") as f:
    f.write("\nThis is a new line.")

```


### トピック５.  例外処理
``` py
try:
    number = int(input("整数を入力してください: "))
    print(f"入力された整数は {number}です")
except ValueError:
    print("不正入力. もう一度やり直してください.")

```


### トピック６.  コンテキストマネージャ
``` py
class Timer:
    def __init__(self):
        self.start_time = None

    def __enter__(self):
        self.start_time = datetime.now()
        return self

    def __exit__(self, exc_type, exc_val, exc_tb):
        end_time = datetime.now()
        elapsed_time = end_time - self.start_time
        print(f"時間経過: {elapsed_time}")

with Timer() as timer:
    total = 0
    for i in range(1000000):
        total += i

```

### 週2の演習問題

    1.  銀行口座のクラスを作成し、預金、引き出し、残高照会の機能を持たせてください。
    2.  人間クラスを作成し、そのサブクラスとして従業員クラスを作成してください。人間クラスには名前と年齢、従業員クラスには給与と職種を追加してください。
    3.  与えられたテキストファイルを読み込んで、行数、単語数、文字数をカウントするプログラムを作成してください。
    4.  ファイルのコンテンツを逆順に書き出すプログラムを作成してください。