# 4.3 チャネルアクセス制御

最後のカテゴリのモードは，チャネルへのアクセスを制御するために使用され，引数としてマスクを取ります。

チャネルに設定される制御アクセスモードのグローバルデータベースのサイズを縮小するために、サーバは特定のチャネルに設定されるそのモードの数に最大限の制限を設けることができます。そのような制限が課される場合、それはユーザのリクエストにのみ影響するものでなければなりません。制限は IRC ネットワークごとに均質であるべきです。
