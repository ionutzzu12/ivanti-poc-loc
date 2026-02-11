---
title: Connectorへのhttpproxyコマンド使用
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM でConnector構成を簡単に編集できる新しいklishシェルコマンドが作成されました。 このコマンドを使用すると、ログイン情報や、Connectorを構成するその他のパラメータを変更できます。

これらの要件により、今回のリリースではhttpproxyコマンドが利用できるようになりました。

- klishシェル

Connectorを構成するには

1. klishシェルにログインします。
2. 利用可能なklishシェルコマンドのリストを表示するには、\[?] を入力します。
3. **\[httpproxy]** と入力すると、次のパラメータの現在の値が表示されます。1) 有効
   2\) スキーム
   3\) サーバ
   4\) 認証タイプ
   5\) ユーザー名
   6\) パスワード
4. **\[httpproxy ?]** と入力すると、httpproxyで利用できるリストコマンドが表示されます。1) authtype - httpプロキシの認証タイプを \[なし]、\[基本]、\[NTLM] のいずれかに設定します
   2\) disable - httpプロキシを無効化します
   3\) enable - httpプロキシを有効化します
   4\) host - httpプロキシのホストを設定します（FQDNか、httpまたはhttpsのいずれかのIP）
   5\) password - httpプロキシの認証パスワードを設定します
   6\) port - httpプロキシのポートを設定します
   7\) scheme - httpプロキシのスキームを設定します（httpまたはhttps）
   8\) show - 現在のhttpプロキシ設定を表示します
   9\) username - httpプロキシの認証ユーザー名を設定します
5. 上のリストにあるコマンドを使用して、Connectorインスタンスを設定します。
