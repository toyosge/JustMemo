# クラウドが生まれて良かったこと
* スケールアウトが簡単になった。
* インスタンスの追加、削除などがプログラマブルにできるようになった

# 言葉まとめ
## スケールアップ
一個のサーバーのパワーをアップすること
## スケールアウト
サーバーをよこに広げるイメージ。数をふやすこと。


## lesson

スケールアウトさせるためにはサーバー一つ一つに状態を保たせたくない。
例えば、sessionなどを、サーバーのメモリにもっていると、いけてない。
YFCではsessionはredisで外だしして管理している。

ちなみにYFCでも一部キャッシュを使っていて
@Cachableというアノテーションをつけることで、Springくんが頑張ってくれる。
CacheConfiguration.java的なものに設定を書く。YFCではehcacheというのを使っていて、
どれくらいの時間キャッシュするかなどの情報をehcache.xmlに書く。

こんな感じの設定ファイル。

```
<?xml version="1.0" encoding="UTF-8"?>
<ehcache xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:noNamespaceSchemaLocation="http://ehcache.org/ehcache.xsd">

  <diskStore path="java.io.tmpdir"/>

  <defaultCache
      maxElementsInMemory="1000"
      eternal="true"
      overflowToDisk="false"/>

</ehcache>

```

# あとでこの辺を読んで理解を深める。
初めてのSpring著者の牧さんsのブログ
SpringのCache Abstractionについて
https://blog.ik.am/entries/339



# あとでググるワード
* スティッキーセッション
* ラウンドロビー

# 気になるセンテンス
* rubyはスネークケース
* Reilsは一番巨大なオープンソースコミュニティだ
* createdAtや、updateByなどの命名規則は、Reilsを参考にしている。
* ページキャッシュなどは完全静的ページではないと使えない。（ページキャッシュで有名なのはreils）
* reilsは現在、フラグメントキャッシュのみになった？

# 気になるコメント
* ダイナミックな言語はチームでやると死ぬ？
* ダイナミックな言語は動かしてみないとわからない。
* rubyで大きなプロジェクトで成功しているのはクックパッド。だが、彼らは優秀すぎるゆえ。
* tomcatはsessionを同期できた？できる？今はやる必要なし、というかやらない設計にするのがよい。


# メモ
マーチンファウラーは言葉を作る人。
例) マイクロサービス

# one more things
初めてのSpring著者の牧さん発信のドキュメント<br>
http://jsug-spring-boot-handson.readthedocs.org/en/latest/
