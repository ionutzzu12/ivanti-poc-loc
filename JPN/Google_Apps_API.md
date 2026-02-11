---
title: Google Apps API
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

シングルサインオン（SSO）を利用してGoogle Appsサービスへのユーザーアクセスを認証しているGoogleのお客様は、デバイスがSSOにトリガーされる外部認証サービスへのリダイレクトを行わないよう定めるプロトコルの制約により、Exchangeを使用してメール、連絡先、カレンダーにアクセスできない場合があります。 このサービスは、ActiveSync接続用のアカウントパスワードを作成し、管理することにより、この状態に対処します。

**前提条件**

Google Apps API機能を構成するには、以下の項目が必要です。

- [**https://console.developers.google.com/上のアカウントへの管理者アクセス**](https://console.developers.google.com/上のアカウントへの管理者アクセス)
- [**https://admin.google.com上のアカウントへの管理者アクセス**](https://admin.google.com上のアカウントへの管理者アクセス)

## Google Apps API機能の有効化

手順

1. **\[管理] > \[Google] > \[Google Apps API]** を選択します。
2. 左側に1と書かれた長方形の一番下にある **\[ステップ1：Google Dev]** をクリックします。
3. \[ステップ1：Google Dev] ページが表示されます。
   \[ステップ1：Google Dev] ページに表示される指示に従ったあとで、**\[完了]** をクリックします。
4. 2と書かれた中央の長方形の一番下にある **\[ステップ2：Google管理]** をクリックします。
5. \[ステップ2：Google管理] ページが表示されます。
   \[ステップ2：Google管理] ページに表示される指示に従ったあとで、**\[完了]** をクリックします。
6. 右側に3と書かれた長方形にある **\[Google管理ユーザー名を入力]** にGoogle管理ユーザー名を入力します。
7. 同じ長方形の中で、**\[ファイルを選択]** をクリックし、ステップ1でダウンロードしたJSONファイルをアップロードします。
8. **\[保存]** をクリックします。
9. \[Google Apps API] ページが表示されない場合、必要な権限を持っていない可能性があります。 以下のいずれかの[**役割**](./ユーザーの役割.md)が必要です。
   - システム管理
   - システム読み取り専用
