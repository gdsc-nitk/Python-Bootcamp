## 第4週: 応用編 (実践的なプロジェクト)

Pythonの応用的なトピックを学びます。Web開発、データ処理、機械学習など、実際に使えるトピックを学びます。

### トピック１.  ウェブスクレイピング（BeautifulSoup, requests）
``` py
import requests
from bs4 import BeautifulSoup

url = 'https://example.com'
response = requests.get(url)
soup = BeautifulSoup(response.text, 'html.parser')

titles = soup.find_all('h2')  # 例えば、ニュース記事のタイトルがh2タグで囲まれている場合

for title in titles:
    print(title.text)

```

### トピック２.  APIの利用（JSON, requests）
``` py
import requests
import json

api_url = 'https://api.example.com/data'
response = requests.get(api_url)

if response.status_code == 200:
    data = json.loads(response.text)
    for item in data:
        print(item)
else:
    print(f"API request failed with status code {response.status_code}")

```

### トピック３.  データ解析（pandas, numpy）
``` py
import pandas as pd
import numpy as np

data = pd.read_csv('example.csv')

# 平均値
mean_value = np.mean(data['column_name'])
print("平均値:", mean_value)

# 最大値
max_value = np.max(data['column_name'])
print("最大値:", max_value)

# 最小値
min_value = np.min(data['column_name'])
print("最小値:", min_value)

```

### トピック４.  データ可視化（matplotlib, seaborn）
``` py
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

data = pd.read_csv('example.csv')

# 散布図のプロット
sns.scatterplot(x='column_name1', y='column_name2', data=data)

# グラフのタイトルと軸のラベルを設定
plt.title('Column 1 対 Column 2の散布図')
plt.xlabel('Column 1')
plt.ylabel('Column 2')

# グラフを表示
plt.show()

```

### トピック５.  ウェブアプリケーション開発（Flask）

以下に、簡単なFlaskウェブアプリケーションの例を示します。

まず、Flaskアプリケーションを作成します。app.pyという名前の新しいファイルを作成し、以下のコードを入力して保存してください。

``` py
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello():
    return "Hello, World!"

if __name__ == '__main__':
    app.run()

```
このコードは、最も基本的なFlaskアプリケーションの構造を示しています。app = Flask(__name__) でFlaskインスタンスを作成し、デコレータ@app.route('/') を使用してルート（トップページ）にアクセスがあった際に実行される関数hello()を定義しています。ターミナルで、Flaskアプリケーションを実行するために以下のコマンドを入力します。

``` py
python app.py
```

ウェブブラウザで http://127.0.0.1:5000/ にアクセスすると、"Hello, World!" と表示されるはずです。これが、Flaskを使って作成したシンプルなウェブアプリケーションです。


### 週4の演習問題

    1.  BeautifulSoupを使用して、指定されたウェブサイトから特定の情報（例：ニュース記事のタイトル）を抽出するプログラムを作成してください。
    2.  requestsとJSONモジュールを使用して、指定されたAPIからデータを取得し、整形して表示するプログラムを作成してください。
    3.  pandasとnumpyを使用して、与えられたCSVファイルから特定のデータ（例：平均値、最大値、最小値）を抽出し、表示するプログラムを作成してください。
    4.  matplotlibとseabornを使用して、データ解析の結果をグラフで可視化するプログラムを作成してください。