# Study-AI 実装演習レポート
## 機械学習（ロジスティック回帰モデル）
### 1. 要点まとめ

ロジスティック回帰モデルは、教師あり学習であり、分類問題を解くために使用される。
- 入力とm次元パラメータの線形結合をシグモイド関数に入力
- 出力は y=0～1 となる確率の値となる
- シグモイド関数
  <img src="https://latex.codecogs.com/svg.latex?\sigma(x)=\frac{1}{1+\rm{exp}(\it{-ax})}" />
シグモイド関数の微分はシグモイド関数自身で表現することができる。
尤度関数の微分を行う際にこの性質を利用する。
- ベルヌーイ分布
- 勾配下降法
- 確率的勾配下降法(SGD)



<u>分類の評価方法</u>
- 再現率(Recall) ... 誤りが多くても抜け漏れ減らしたい場合に利用
  <img src="https://latex.codecogs.com/svg.latex?\rm{Recall=}\frac{TP}{TP+FN}" />
- 適合率(Precision) ... 見逃しが多くてもより正確に予測したい場合に利用
  <img src="https://latex.codecogs.com/svg.latex?\rm{Precision}=\frac{TP}{TP+FP}" />
- F値
  <img src="https://latex.codecogs.com/svg.latex?\rm{\frac{2Recall\cdot Precision}{Recall+Precision}}" />

### 2. 実装演習

タイタニックの常客データを利用しロジスティック回帰モデルを作成し、特徴量を抽出する。
- 課題
年齢が30歳で男の客は生き残れるか？
- 実装
[実行結果（Jupyter）](Exercises-1.ipynb)
⇒XXXと言える。

### 3. 考察


### 4. 関連記事

