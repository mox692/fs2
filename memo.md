## TODO
* `Stream.emit(1,2,3).compile.toList.unsafeRunSync` の間で何が起きているか 
* `Pull` のデータ構造について
  * writeAll の Stream[F, A] 版の実装の際に知っておきたい

あれから、fs2-io_uringやcats-effectのnativeの実装を読んで、fs2-io_uringのFiles APIの実装プロジェクトのproposalを書きました.

今回も、proposalに対してショートフィードバックをいただくことは可能でしょうか？ (そして、コメントでいくつか質問をしています)

--- 

fs2 is a Scala streaming library that provides a pure functional API.


fs2 is a Scala streaming library that provides a pure functional API. It offers APIs to handle I/O operations such as File I/O and Network I/O, and other libraries such as http4s and skunk depend on these APIs.

The Linux kernel has introduced a relatively new API called io_uring, as a technique to handle asynchronous IO efficiently. For Scala Native, it is possible to access these APIs by linking to a library that provides the io_uring API.


This project aims to improve the performance of file I/O operations in fs2-native by adding the io_uring backend to its Files API and implementing basic read and write APIs using it.

---
こんにちはarman, いつもサポートありがとう

これまでもらったproposalに対するreviewを一旦反映して、デットラインはApril 05なのでまだ時間はありますが、一旦先ほど現時点でのproposalをGSoCに提出しました。


念のため共有です。

---
