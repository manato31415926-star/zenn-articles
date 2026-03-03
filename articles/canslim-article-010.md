---
title: "AIとPythonの基礎入門"
emoji: "📈"
type: "idea"
topics: ["投資", "株式投資", "canslim", "成長株", "日本株"]
published: true
---

# AIとPythonの基礎入門

## はじめに

この記事では、AIとPythonの基本概念を解説し、実践的な例も含んでいます。初心者から中級者まで、PythonでAIを学びたい方には役立ちます。

## Pythonでの基本的な機械学習実装

### 必要なライブラリのインストール

まず必要なライブラリをインストールします。

git add requirments.txt
pip install -r requirements.txt

### scikit-learnを使った回帰分析

scikit-learnはPythonで最も人気のある機械学習ライブラリです。ここでは、回帰分析を行ってみましょう。
```python
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
import numpy as np

# データ生成
X = np.random.rand(100, 1)
y = X * 2 + np.random.randn(100, 1) / 1.5

# データの分割
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# モデルの構築と学習
model = LinearRegression()
model.fit(X_train, y_train)

# モデルの評価
y_pred = model.predict(X_test)
print('予測値:', y_pred[:5])
```

### scikit-learnを使った分類

ここでは、scikit-learnで分類を行ってみましょう。
```python
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
import numpy as np

dataset = load_iris()
X = dataset.data
y = dataset.target

# データの分割
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# モデルの構築と学習
model = LogisticRegression()
model.fit(X_train, y_train)

# モデルの評価
y_pred = model.predict(X_test)
print('予測値:', y_pred[:5])
```

## まとめ

ここまでで、Pythonでの基本的な機械学習実装を解説しました。初心者でも扱いやすく作成したサンプルコードは、AIとPythonの基礎入門として役立ちます。
