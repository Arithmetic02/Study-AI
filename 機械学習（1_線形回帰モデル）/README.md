<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML"></script>

# Study-AI 実装演習レポート

## 機械学習（線形回帰モデル）

### 1. 要点まとめ

線形回帰モデルは、教師あり学習にて、ある入力から出力を予測するモデルである。
入力の各要素を説明変数、特徴量と呼ぶ。
$ x=(x_1, x_2, ..., x_m)^T \in \mathbb{R}^m $

出力は目的変数と呼び、スカラー値で表現される。
$ y \in \mathbb{R}^1 $

慣例として予測値にはハットを付ける。
$ w=(w_1, w_2, ..., w_m)^T $
$ \hat{y}=w^Tx+w_0 $

### 2. 実装演習

ボストンの住宅データセットを使用。
- 課題
部屋数が 4で犯罪率が 0.3の物件はいくらになるか？
- 手順
$ y=Xw+ε $ の重回帰にて推測する。
- 予測結果
約 $4,240
- [(sklearnでの実行結果)](Exercises-1.ipynb)

### 3. 考察

- ボストンの住宅セットには外れ値と思われるデータが含まれているため、二乗損失の演算に影響を受けている。
- 部屋数と価格の相関より、部屋数が少なくなると住宅価格がマイナスとなってしまうため、汎用性のあるモデルとは言えない。
- 犯罪発生率と価格の相関より、犯罪率が高くなると住宅価格がマイナスとなってしまうため、汎用のあるモデルとは言えない。
- [(seabornでの可視化結果)](Exercises-2.ipynb)

### 4. 関連記事

- Latex関連
https://qiita.com/tomtsutom0122/items/e0ab6b6ccbd369db1aa2
https://konoyonohana.blog.fc2.com/blog-entry-326.html
https://mathlandscape.com/latex-set/
- matplotlib関連
https://qiita.com/skotaro/items/08dc0b8c5704c94eafb9
https://ai-inter1.com/matplotlib-japanize/
