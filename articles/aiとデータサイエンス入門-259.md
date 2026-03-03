---
title: "AIとデータサイエンスの基礎"
emoji: "📈"
type: "idea"
topics: ["投資", "株式投資", "canslim", "成長株", "日本株"]
published: true
---

# AIとデータサイエンスの基礎
## まずは、基本概念を理解する
** Supervised Learning **
*   教師付き学習では、モデルが教師付けるデータに基づいて学習します。
    ```python
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.svm import SVC
# Iris datasetを読み込む
iris = load_iris()
X_train, X_test, y_train, y_test = train_test_split(iris.data, iris.target, test_size=0.2)
# サポートベクターマシン(SVM)で学習する
svm = SVC(kernel='rbf', C=1)
svm.fit(X_train, y_train)
```
** Unsupervised Learning **
*   教師付かない学習では、モデルが教師付かずにデータから学習します。
    ```python
from sklearn.datasets import load_iris
from sklearn.cluster import KMeans
# Iris datasetを読み込む
iris = load_iris()
# k-means法でクラスタリングする
kmeans = KMeans(n_clusters=3)
kmeans.fit(iris.data)
```
## 次に、実践例を紹介する
** AIとデータサイエンスの応用例 **
*   ** 自動販売機の故障予測 **
    ```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
# 自動販売機データを読み込む
data = pd.read_csv('data.csv')
X_train, X_test, y_train, y_test = train_test_split(data.drop('故障', axis=1), data['故障'], test_size=0.2)
# 回帰分析で予測する
model = LinearRegression()
model.fit(X_train, y_train)
```
## まとめ
*   AIとデータサイエンスは、実践的な技術であることがわかりました。
    ```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
# 自動販売機データを読み込む
data = pd.read_csv('data.csv')
X_train, X_test, y_train, y_test = train_test_split(data.drop('故障', axis=1), data['故障'], test_size=0.2)
# 回帰分析で予測する
model = LinearRegression()
model.fit(X_train, y_train)
```
