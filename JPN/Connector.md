---
title: Connector
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

**ライセンス：&#x20;**&#x53;ilver

Cloud Connectorは、Ivanti Neurons for MDM サービスからLDAPサービスや認証機関（CA）などの企業リソースへのアクセスを提供します。 アクセスしたいリソース1つに対して1つのConnectorを設定します。

Amazon Web Services（AWS）でホストされているMicrosoft Active DirectoryまたはLDAPサーバーを使用する場合は、AWSで Ivanti Neurons for MDM Connectorをホストできます。 オンプレでないConnectorが必要です。

Connectorは、ソフトウェアの最新バージョンに自動的に更新されます。

最新の Ivanti Neurons for MDM Connector インストール ガイドについては、[**https://help.ivanti.com/#106**](https://help.ivanti.com/#106) を開き、「Connector」を検索してください。

## Connector ホスティングオプション

Ivanti Neurons for MDM Connector は、オンプレのデータセンターでもAmazon Web Services（AWS）でもホスト可能です。

- AWSでホストされているMicrosoft Active Directory、またはAWSの自己管理型のMicrosoft ADを使用している場合は、Connector をAWSでホストしてください。 この場合、オンプレのConnectorは不要です。
- LDAPサーバーやCAなど、オンプレのリソースにアクセスする場合は、オンプレのConnectorを設定してください。

### AWSでConnector をホスト

AWSでConnector をホストすれば、AWSにホストされる以下のMicrosoft Active Directoryオプションをご利用いただけます。

- Microsoft Active Directory対応AWSディレクトリサービス
- Amazon VPCの顧客管理型Microsoft Active Directory

Microsoft Active Directory対応AWSディレクトリサービスの詳細は、以下をご覧ください：[**https://aws.amazon.com/directoryservice**](https://aws.amazon.com/directoryservice)。 Amazon VPCにおけるMicrosoft Windows ServerとMicrosoft Active Directoryのホストについては、AWSのドキュメンテーションをご覧ください。 Ivanti Neurons for MDM Connectorは、Windows Server 2012、2012 R2、2015をサポートしています。

### AWS で Ivanti Neurons for MDM Connector AMI を設定する

Ivanti Neurons for MDM Connector AMI を設定するには、次の手順を実行します。

1. 管理者認証情報でAWSにログインします。
2. AWSサービスページで **\[コンピューティング]** から **\[EC2]** を選択します。
3. **\[イメージ]** を展開し、左ペインから \[**AMI]** を選択します。
4. 右ペインのドロップダウンリストから **\[パブリックイメージ]** を選択します。
5. 「mobileiron-kocab」などのキーワードを使用してIvanti Neurons for MDMコネクタを検索します。
6. リストからConnectorの最新バージョンを選択し、**\[起動]** をクリックします。
7. 『*Ivanti Neurons for MDMコネクタインストールガイド*』の「AWSへのIvanti Neurons for MDMコネクタの配布」セクションに記載されているConnector のインストール手順に従います。このドキュメントは、[**https://help.ivanti.com/mi/help/en\_us/cld/**](https://help.ivanti.com/mi/help/en_us/cld/)*\<version>*/inst/default.htmから入手できます。*バージョン* は、インストールするIvanti Neurons for MDM Connectorバージョンです。 たとえば、バージョン74の Ivanti Neurons for MDM Connectorのガイドは、[**https://help.ivanti.com/mi/help/en\_us/cld/**](https://help.ivanti.com/mi/help/en_us/cld/)**74**/inst/default.htmにあります。

### オンプレでConnector をホスト

データセンターでオンプレミスで Ivanti Neurons for MDM Connector をホスティングするには、**\[Connector のダウンロード]** をクリックして、Ivanti Neurons for MDM Connector をダウンロードして設定します。 ダウンロードしたパッケージを展開し、パッケージに含まれる Ivanti Neurons for MDM Connectorインストールガイドの指示に従って設定してください。

## Connectorログへのアクセス

Connector ログには Connector サービスからアクセスし、Connector 関連の問題解決に役立てることができます。 これにはシステムマネージャーまたはシステム読み取り専用の役割が必要です。

1. **\[管理] > \[Connector]** を選択し、\[Connector] ページを開きます。Connectorのインターフェイスは、Connectorの状態（有効または無効）、Connector名、接続（接続あり、または接続なし）、バージョン番号、ログレベル、アクション（Connectorを無効化または削除）を表示します。
2. **\[ログレベル]** プルダウンメニューを使用してレベルを選択します。使用可能なログレベルが低い順にプルダウンメニューに表示されます。\* エラー
   - 警告
   - 情報
   - デバッグ
   - トレース情報レベルはデフォルトのログレベル設定です。 別のログレベルを選択すると、同期アイコン

::Image[]{src="Sync_icon.png" signedSrc="Sync_icon.png" size="10" caption alt isUploading="false" sha initialPath="Sync_icon.png" githubPath="Sync_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
が回転し、選択されたログレベルで情報が収集されていることを示します。 ログレベルは1時間後に情報レベルにリセットされます。 トレースレベルは最高のログレベル設定です。 このレベルでは、他の全レベルの全メッセージが収集されます。 同期アイコンは、要求の間、表示されます。
:::

3. 必要であれば、同期アイコン

::Image[]{src="Sync_icon.png" signedSrc="Sync_icon.png" size="10" caption alt isUploading="false" sha initialPath="Sync_icon.png" githubPath="Sync_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
にカーソルを置くと取り消しアイコン
:::

::Image[]{src="Cancel_icon.png" signedSrc="Cancel_icon.png" size="10" caption alt isUploading="false" sha initialPath="Cancel_icon.png" githubPath="Cancel_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
が表示されます。 取り消しアイコンをクリックすると、ログレベル変更が取り消されます。
:::

4. 要求アイコンにカーソルを置くと要求情報が表示されます。 要求アイコン

::Image[]{src="Fetch_icon.png" signedSrc="Fetch_icon.png" size="10" caption alt isUploading="false" sha initialPath="Fetch_icon.png" githubPath="Fetch_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
をクリックすると、現在のログフォルダーにあるファイルを.zipファイルで要求できます。要求が実行されるとログファイルが.zipファイルに追加されます。  新しい要求が実行されると前の要求の.zipファイルは削除されます。
:::

5. 必要であれば、同期アイコン

::Image[]{src="Fetch_icon.png" signedSrc="Fetch_icon.png" size="10" caption alt isUploading="false" sha initialPath="Fetch_icon.png" githubPath="Fetch_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
にカーソルを置くと取り消しアイコン
:::

::Image[]{src="Cancel_icon.png" signedSrc="Cancel_icon.png" size="10" caption alt isUploading="false" sha initialPath="Cancel_icon.png" githubPath="Cancel_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
になります。 取り消しアイコンをクリックすると要求が中止されます。要求を完了前に取り消した場合、前のログ.zipファイルがサーバーから削除されているため、ダウンロードアイコン
:::

::Image[]{src="Download_icon.png" signedSrc="Download_icon.png" size="10" caption alt isUploading="false" sha initialPath="Download_icon.png" githubPath="Download_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
が表示されません。 Connector上の元のログファイルは要求すればまだ取得できます。
:::

6. 要求が完了した後にダウンロードアイコン

::Image[]{src="Download_icon.png" signedSrc="Download_icon.png" size="10" caption alt isUploading="false" sha initialPath="Download_icon.png" githubPath="Download_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
をクリックすると、最新の要求で収集したログファイルを含むログ.zipファイルがダウンロードされます。ログファイル名の形式はkocab.logです。 ダウンロードした.zipファイル名は、サーバー名、接続バージョン、タイムスタンプ（日、月、年、時刻）で構成され、形式は\<Connector\_Hostname>\_\<Connector\_Version>\_\<TimeStamp>.zipとなります。 アーカイブに保存された.zipファイル名の形式はkocab.yyyy-mm-dd.0.log.gzです。
:::

7. 任意で **\[アクション]** プルダウンメニューをクリックし、Connectorを無効化または削除できます。

**\[Connector]** ページが見えない場合、必要な権限を持っていない可能性があります。 以下のいずれかの[**役割**](./ユーザーの役割.md)が必要です。

- システム管理
- 読み取り専用システム
