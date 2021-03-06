# 3.1 標準チャネル

これらのチャネルは、最初のユーザが参加したときに暗黙的に作成され、最後のユーザが退出したときに存在しなくなります。チャネルが存在する間は、どのクライアントもチャネル名を使用してチャネルを参照することができます。

チャネルを作成したユーザは自動的にチャネルオペレータになりますが、チャネル名の前に `+` が付くチャネルは例外です（[4. チャネルモード](../channel-modes/index.md) を参照）。このタイトルの詳細については、[2.4.1チャネルオペレータ](../channel-characteristics/channel-operators.md) を参照してください。

重複したチャネルが作成されるのを避けるため（典型的には2つのサーバ間で分割されたために IRC ネットワークが不連続になった場合）、チャネルオペレータ（[2.4.1 チャネルオペレータ](../channel-characteristics/channel-operators.md) を参照）がネットワークの分割によって最近チャネルから離れた場合は、チャネル名をユーザが再利用することを許可してはいけません。この場合，チャネル名は一時的に利用できなくなります。チャネルが利用できない状態にある期間は、IRC ネットワークごとに設定する必要があります。これはローカルユーザが同じ名前のチャネルを作成することを防ぎますが、リモートユーザがチャネルを再作成することは防げないことに注意することが重要です。後者は通常、IRC ネットワークが再接続されたときに起こります。明らかに、このメカニズムは名前が `#` で始まるチャネルにのみ意味がありますが、名前が `+` で始まるチャネルにも使用することができます。このメカニズムは一般的に "Channel Delay" として知られています。
