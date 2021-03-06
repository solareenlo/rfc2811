# 5.2.5 サーバ再稼働の仕組み

チャネルが "再開遅延" 期間よりも長く無人となり、チャネルフラグ `r` が設定されている場合（[4.2.7 サーバ再開フラグ](../channel-modes/server-reop-flag.md) 参照）、IRC サーバはチャネルオペレータ状態を一部のメンバにランダムに与える責任を負います。

現在の実装でこのメカニズムに使用されている正確なロジックを以下に説明します。サーバは異なるロジックを使用することができますが、一貫性と公平性を維持するために、特定の IRC ネットワーク上ですべてのサーバが同じロジックを使用することが強く推奨されています。同じ理由で、"reop delay" は特定の IRC ネットワークのすべてのサーバで均一であるべきです。"チャネル遅延" については、IRC ネットワークの規模（ユーザ数）、ネットワークの分割の頻度など、様々な要素を考慮して "再開遅延" の値を設定する必要があります。

a) 再稼働メカニズムは、"再稼働遅延" の満了後、ランダムな時間の後にトリガーされます。これは、メカニズムが2つの別々のサーバで同時に（同じチャネルで）トリガーされる可能性を制限するはずです。

b) チャネルが小規模（5ユーザ以下）で、このチャネルの "チャネル遅延" が終了した場合、少なくとも1つのメンバがサーバにローカルであれば、すべてのチャネルメンバを再オープンします。

c) チャネルが小規模（5ユーザ以下）で、このチャネルの "チャネル遅延" が期限切れで、"再開遅延" の値より長い時間が経過した場合、すべてのチャネルメンバを再開させます。

d) その他の場合は、サーバに組み込まれた何らかの方法に基づいて、チャネル上の最大1人のメンバを再開させます。もし、メンバを再開しないのであれば、その方法は、他のサーバがおそらく誰かを再開するようなものでなければなりません。この方法は、ネットワーク全体で同じであるべきです。良いヒューリスティックは、単なるランダムな再開かもしれません。
  （現在の実装では、実際にサーバのローカルであまり長くアイドル状態になっていないメンバを選ぼうとし、最終的には行動を先延ばしにして、他のサーバに "あまりアイドル状態になっていない" メンバを見つける機会を与えています。これは、サーバがローカルユーザの "アイドル" 時間しか知らないため、複雑になりすぎています。）
