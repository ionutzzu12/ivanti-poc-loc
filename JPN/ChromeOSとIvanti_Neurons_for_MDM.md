---
title: ChromeOSとIvanti Neurons for MDM
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

ChromeOSは、Googleが作成して提供している、Linuxベースのオペレーティングシステムです。 Ivanti Neurons for MDM は、Android、Windows、iOS、macOSで動作しているデバイスをサポートしています。 このサポートがChromeOSデバイスにも拡張されました。 Ivanti Neurons for MDM により、ChromeOSデバイスを構成、管理するための、統一されたシンプルなモビリティ管理ソリューションが提供されます。 Ivantiでは、Ivanti Neurons for MDMでiOS、Android、Windows、Mac向けに提供されている管理ワークフローに類似した、ChromeOSデバイス向けの統一された、シンプルな、豊富な機能を備えたソリューションを提供しています。 管理者は、**\[管理] > \[Google] > \[ChromeOS管理]** にある簡易統合を使用することで、簡単にIvanti Neurons for MDMをGoogle Cloud（Google管理コンソールとも呼ばれます）と接続できます。

### 前提条件

1. 管理対象のGoogle管理者アカウントがあることが必要です。
2. LDAPユーザーとOUを、Google管理コンソールでインポートする必要があります。 Ivanti Neurons for MDM は、LDAPソースからインポートされたOUのみをサポートしています。 ローカルのOUはサポートされていません。
3. 管理者は、組織ユニット（ユーザーグループ）をIvanti Neurons for MDMと同期させておく必要があります。 これは、LDAPサーバーを構成し、組織ユニットを追加することによって行えます。

### Googleの許可

Google管理コンソールで選択可能なChromeOSデバイスを、Ivanti Neurons for MDMで直接登録することはできません。 代わりに、これらのデバイスを、Googleに登録し、これらのデバイスに関する情報をGoogleとIvanti Neurons for MDMの間で同期させます。 Googleがデバイスをインポートし、その他のアクション（アプリや構成の割り当てなど）を実行することを、管理者が許可しなければなりません。

**手順**

1. **\[管理] > \[Google] > \[ChromeOS管理]** に進みます。
2. **\[Googleを許可]** をクリックします。
3. 許可するGoogle管理アカウントを選択します。
4. **\[続行]** をクリックして、必要なサービスを提供する権限を承諾します。
   **\[ChromeOSの設定に成功しました]** という確認のメッセージが、画面に表示されます。 確認メッセージの下には、ドメイン情報も記載されています。

### GoogleからのChromeOSデバイスの同期

管理者は、Google管理コンソールからChromeOSデバイスを同期させる必要があります。 Google管理コンソールを使用してChromeOSデバイスに初めてアクセスする際、管理者は、\[ChromeOS管理] ページにある \[今すぐ同期] オプションを使用して手動でデバイスを同期させる必要があります。

初めてデバイスを手動で同期させた後、それ以降の同期は、1時間ごとに自動的に行われます。

### Google管理コンソールとの統合の削除 Ivanti Neurons for MDM

統合を削除すると、Googleから受け取った、GoogleリソースにアクセスするためのOAuthトークンが失効します。 失効すると、ChromeOSデバイス、ブループリント構成およびアプリ構成に関連付けられたインベントリ、ならびに登録のメタデータが削除されます。 ブループリント構成およびアップロード済みのアプリは削除されません。

テナント登録が削除されない場合は、チケットを発行して問題を調べることができます。

**手順**

1. **\[管理] > \[Google] > \[ChromeOS管理]** に進みます。
2. ChromeOS Ivanti Neurons for MDM登録セクションで、**\[削除]** をクリックします。
   削除操作を続行するかどうか、またこの統合に関連付けられたすべてのデバイスが削除されることを示すポップアップが画面に表示されます。 **\[Ok]** を選択します。
