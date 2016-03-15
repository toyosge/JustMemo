まっさんチャレンジ 2/24 2016

おさらいこぼりさん本そして、next stageへ

# PRGパターン
Post, Redirect, Getの略。
入力、確認、完了がある画面で、完了画面でリロードした時に起こるごたごたを亡き者にする。
さいきょうの2重submits対策でググる。

# HttpOnly
YFCのCookieの中身を除くと
MSESSIONやuuuidなどなどがいるが、 HttpOnlyというのも隠れている。
cookieはJavascriptからもいじれるので、いじれないようにするための設定

# Servlet,Filter
あとでぐぐる

# About nginx
SSL, HTTPSの暗号化を高速にやれる
SSLアクセレラレーターとかとして、有名

# スコープ
requestスコープが基本
入力、確認、完了などステップがあるときは、session使うと良い？
マスターデータのキャッシュなどはapplicaitonスコープ

# memo
SpringSecurityがsessionを削除したりinvalidateしてくれちゃってる。
メソッド？が用意されてる?
