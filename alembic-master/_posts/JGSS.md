---
title: Description of an Alembic
categories:
- General
feature_image: "https://picsum.photos/2560/600?image=872"
---

###　JGSSデータを使って機械学習の勉強をしました。
(大学で課題として出したものを少し書き換えました。)
データ：[JGSS](http://jgss.daishodai.ac.jp/data/dat_top.html)
---
###　テーマ
大きなテーマとして結婚生活にフォーカスを当てました
[先行研究](https://nfrj.org/nfrjs01-2005_pdf/nfrjs01-2005kato1.pdf)として挙げられていた離婚の要因とされているものを変数としてロジスティック回帰を行いました。
以下がコードです

'''python:marry.py
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

y=data['domarry']
features=['ageb','sexa','szttlsta','incsp','incself','incpar','chiled','op5schpf','agegrd',]
X=data[features]
X_train, X_test, Y_train, Y_test = train_test_split(X, y, test_size = 0.２, random_state = 0) 

lr = LogisticRegression() 
lr.fit(X_train, Y_train)
'''

いくつかの変数は連続値であったためワンホットエンコーディングや離散値に直しています。
上記のコードでは精度が80％であり、そこそこの精度でした。
普段はKaggleできれいで要素も少ないデータで勉強していましたが、今回JGSSのデータはとても要素が多く、要素選びが大変でした。。。

以上今後追記していきたいと思います。