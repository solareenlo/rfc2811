```
Network Working Group                                            C. Kalt
Request for Comments: 2811                                    April 2000
Updates: 1459
Category: Informational
```

<h1 align="center">
Internet Relay Chat: チャネル管理
</h1>

## IRC

- [RFC 1459](https://solareenlo.com/rfc1459) (Internet Relay Chat Protocol)
- [RFC 2810](https://solareenlo.com/rfc2810) (Internet Relay Chat: Architecture)
- [RFC 2811](https://solareenlo.com/rfc2811) (Internet Relay Chat: Channel Management)
- [RFC 2812](https://solareenlo.com/rfc2812) (Internet Relay Chat: Client Protocol)
- [RFC 2813](https://solareenlo.com/rfc2813) (Internet Relay Chat: Server Protocol)
- [RFC 7194](https://solareenlo.com/rfc7194) (Default Port for Internet Relay Chat (IRC) via TLS/SSL)

## 本メモの位置づけ

このメモは、インターネットコミュニティーのための情報を提供するものです。このメモは、いかなる種類のインターネット標準も規定するものではありません。このメモの配布は無制限です。

## 著作権について

Copyright (C) The Internet Society (2000).  All Rights Reserved.

## 概要

IRC（Internet Relay Chat）プロトコルの最大の特徴は、チャンネルと呼ばれるフォーラムでユーザをグループ化し、複数のユーザが一緒にコミュニケーションする手段を提供することです。

もともとチャネルは一種類しかなかったが、時代とともにニーズに応え、あるいは実験的に新しいタイプのチャネルが登場してきました。

この文書では、チャネルとその特性およびプロパティが IRC サーバによってどのように管理されるかを規定します。
