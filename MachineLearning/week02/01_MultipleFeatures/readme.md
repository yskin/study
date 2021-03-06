# Multiple Features
https://www.coursera.org/learn/machine-learning/lecture/6Nj1q/multiple-features  
Week1では変数が1つの線形回帰を扱った  
ここからは変数がnつの線形回帰を扱う

## Multivariate linear regression の変数
変数が複数あるLinearRegression(線形回帰)のことを  
MultivariateLinearRegression(多変量線形回帰?)と呼ぶ  

例えば 1週目で扱った 家の広さ(x) と 家の価格(y) の場合で考えると  
xとして階数や築年数が追加された以下のようなイメージ  
<img src="../../img/02_01_multiple_features.png" width=50%>  
これ以降は以下の通り変数定義を追加する
* n : 変数の数を表す  
* <img src="https://latex.codecogs.com/gif.latex?x^{(i)}" title="x^{(i)}" /> : i番目のトレーニングセットを指す  
  例えば <img src="https://latex.codecogs.com/gif.latex?x^{(2)}" title="x^{(2)}" /> は 2行目(1416 から始まるrow)のトレーニングセットを指す
* <img src="https://latex.codecogs.com/gif.latex?x^{(i)}_{j}" title="x^{(i)}_{j}" /> : i番目のトレーニングセット の j番目のパラメータ を指す  
  例えば <img src="https://latex.codecogs.com/gif.latex?x^{(2)}_{3}" title="x^{(2)}_{3}" /> は row=2, column=3 の2  
  つまり TrainingSet2行目のNumberOfFloorsを指す

## Multivariate linear regression の式
複数の変数を持つ仮説は以下の式で表すことができる  
<img src="../../img/02_01_multiple_features_algorithm.png" width=50%>  
パラメータθ0 は 変数x0(1固定) を持つと考えることで  
ベクトル(<img src="https://latex.codecogs.com/gif.latex?\theta^{T}x" title="\theta^{T}x" />)で表現することができる  
<img src="../../img/02_01_multiple_features_vectorization.png" width=50%>  
