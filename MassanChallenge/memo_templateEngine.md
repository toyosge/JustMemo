まっさんチャレンジ 3/15 2016

# テンプレートエンジン
### 概念
テンプレートがあって、いれこむ、ような仕組み

### 参考資料
http://aoiso.hatenablog.com/entry/2015/10/14/173333

### htmlベース
#### 素
* FreeMarker
* Thymeleaf

#### 素じゃない
* mayaaa

### Javaベース
Java側でviewを組み立てる？
* Mixer2
* appach wicket
https://codezine.jp/article/detail/4459

### 覚えておこう
#### レイアウトという考え方

#### 値の突っ込む時に、思ったようにいれれるか
ヘッドにcssなどいれたり、タイトルをうまく生成できるか、jsは、
ビューヘルパー(J2EEのビューヘルパーパターン)はあるか

#### エスケープ
最近のフレームワークは、デフォルトで、エスケープする。utext の uはunescaped text の u。エスケープしない時だけ、utextを使うと、データを入力する、ユーザー由来（ユーザーが入力できる、触れる）のデーターはエスケープしないと危ない

#### コメント
コメントアウトをどう書けるか。

#### 部品化
テンプレートエンジンは大体部品化ができる

# クライアントサイドで他に知っておいてもいいかもしれない子たち
* MVVM
* isomorphic
    * サーバークライアントどちらも動くように
* browserify
    * ブラウザで、nodeが使えますように

## 丼とフォゲット
動いてから、いじるのがこつ。

## ハンズオンやっとけ
yoeman + coffee <br>
http://lxyuma.hatenablog.com/entry/2013/10/04/001331

backborn + something else<br>
http://albatrosary.hateblo.jp/entry/2014/02/05/172603
