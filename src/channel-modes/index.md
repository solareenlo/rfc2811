# 4. チャネルモード

チャネルに用意されている各種モードは以下の通りです。

    O - "チャネル作成者" のステータスを与える。
    o - チャネルオペレータの権限を与える/取る。
    v - 音声の特権を与える/取る。

    a - 匿名チャネルフラグを切り替える。
    i - 招待専用チャネルフラグを切り替える。
    m - モデレートされたチャネルを切り替える。
    n - 外部のクライアントからチャネルへのメッセージの受信禁止を切り替える。
    q - クワイエットチャネルフラグを切り替える。
    p - プライベートチャネルフラグを切り替える。
    s - シークレットチャネルフラグを切り替える。
    r - サーバ再開チャネルフラグを切り替える。
    t - チャネルオペレータだけが設定可能なトピックフラグを切り替える。

    k - チャネルキー（パスワード）を設定／解除する。
    l - チャネルに対するユーザ制限を設定/解除する。

    b - ユーザを締め出すための禁止マスクを設定/解除する。
    e - 禁止マスクを上書きするための例外マスクを設定/削除する。
    I - 招待専用フラグを自動的に上書きする招待マスクを設定/削除する。

以下に特に断りがない限り、これらのモードは ["IRC クライアントプロトコル" [IRC-CLIENT]](https://solareenlo.com/rfc2812/) で定義されている MODE コマンドを使用することで "チャネルオペレータ" が操作することができる。
