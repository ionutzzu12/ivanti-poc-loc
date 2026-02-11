---
title: Appleデバイスの導入
createdAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDMは、ご使用のすべてのAppleデバイスの管理を支援します。 フリートのプロビジョニング、管理、更新、保護を行うための包括的なソリューションであり、最高のユーザー体験をエンドユーザーに提供します。

このセクションは以下のトピックを含みます。

- [**Apple MDM証明書のインストール**](./Appleデバイスの導入.md)
- [**Appleデバイスの登録**](./Appleデバイスの導入.md)
- [**Ivanti Go for iOSクライアント**](./Appleデバイスの導入.md)
- [**Appleデバイス用のアプリケーションの管理**](./Appleデバイスの導入.md)
- [**構成の管理**](./Appleデバイスの導入.md)
- [**ソフトウェア更新の管理**](./Appleデバイスの導入.md)
- [**iOS/iPadOSデバイスの設定**](./Appleデバイスの導入.md)
- [**watchOSデバイスの設定**](./Appleデバイスの導入.md)
- [**watchOSデバイス向けにサポートされているデバイスアクション**](./Appleデバイスの導入.md)
- [**visionOSデバイスの設定**](./Appleデバイスの導入.md)
- [**visionOSデバイス向けにサポートされているデバイスアクション**](./Appleデバイスの導入.md)
- [**macOSデバイスの設定**](./Appleデバイスの導入.md)
- [**TvOSデバイスの設定**](./Appleデバイスの導入.md)
- [**宣言型デバイス管理（DDM）のサポート**](./Appleデバイスの導入.md)

## Apple MDM証明書のインストール

Appleデバイスを管理するには、まず、iOSデバイスを管理するためのApple MDM証明書を要求し、インストールします。 このApple MDM証明書は年1回更新します。 (有効期限が近づくと、Apple サイトからの通知が証明書を作成する際に使用された Apple アカウントに送信されます。)\[MDM 証明書] ページを使用して、この証明書を追加または更新してください。

[**MDM証明書のインストール**](./MDM証明書のインストール.md)に記載されている手順に従います。

## Appleデバイスの登録

次のどの方法でもデバイスを登録できます。

- [**自動デバイス登録**](./デバイス登録.md)
- [**Apple School Manager**](./Apple_Configurator.md)
- [**Apple Configurator**](./Apple_Configurator.md)

## Ivanti Go for iOSクライアント

次の手順として、会社が許可するデバイスの登録タイプを選択します。 Ivanti Neurons for MDMは現在、次のタイプをサポートしています。

- [**デバイス登録(iOS、macOS、Android)**](./デバイス登録_iOS、macOS、Android_.md)
- [**Apple Business Managerでのユーザー登録**](./Apple_Business_Managerでのユーザー登録.md)
- [**アカウント主導のUser Enrollment**](<Account driven User Enrollment.htm>)
- [**設定（Apple）**](./設定（Apple）.md)

## Appleデバイス用のアプリケーションの管理

Ivanti Neurons for MDMの \[アプリカタログ] ページは、管理者がアプリカタログを効率的に管理するためのインターフェイスとして機能します。 この機能は、エンドユーザーが公開アプリストアを通じて入手可能なモバイルアプリケーションと、Ivanti Neurons for MDMを通じて配布されることが決まっているモバイルアプリケーションの両方について、全体のオーケストレーションを担います。

サポートされているアプリ：

\[アプリカタログ] ページには、公開AppStoreアプリ、カスタムアプリ、自社開発アプリ、AppConnect対応アプリ、iOS向けGoクライアント、macOS向けM\@Wなど、さまざまなタイプのアプリが集約されるため、後続の構成や配布のためのインポートプロセスが合理化されます。

モバイルアプリケーション管理（MAM）のみの構成で稼働しているデバイス上のiOSユーザーには、アプリカタログへのアクセス時に、認証証明書を選択するよう求めるメッセージが表示されます。 この認証手順は、リストされたアプリへのアクセスを保護し、堅牢なセキュリティ慣行を維持する上で、不可欠です。

AppleのM1チップセットMacBookは、\[お使いのソフトウェア製品] 内でiPhoneアプリとiPad VPPアプリに対して特殊なサポートを提供しています。 特に、サポートされているiPhoneアプリやiPad VPPアプリをプッシュする権限を管理者だけが持っており、ユーザーがAppから直接それらのアプリをインストールすることは禁止されています。

詳細な実装手順と構成オプションについては、管理者ガイドおよび以下のリソースで入手可能な包括的なドキュメントを参照してください。

- [**アプリの管理**](./アプリ.md)
- [**アプリカタログ設定**](./カタログ設定.md)
- [**Apple Appとブックの設定**](./Appleの「Appとブック」.md)
- [**Apps@Work企業アプリストア**](./Apps@Work__iOS、Android、Windows、macOS_.md)
- [**macOS AppStoreの制約**](./macOS_AppStoreの制約.md)

## 構成の管理

構成とは、管理者がデバイスに送信する設定の集合体です。 たとえば、構成を使用すると、デバイス上のVPN設定やパスコード要件を自動的に設定することができます。 お使いのシステムの既存の構成は、\[構成] ページに一覧表示されます。 \[構成] ページから複数の構成を選択し、複数のデバイスにまとめてプッシュできます。 これらの構成は、スペース固有のデバイスにプッシュできます。他のスペースのデバイスは影響を受けません。 構成は、単一スペースまたは複数スペースにプッシュするか、または一度にすべてのスペースにプッシュすることができます。

Ivanti Neurons for MDMの構成の大半は、すべてのプラットフォームに共通です。 構成の操作方法の詳細については、「構成の操作」を参照してください。

特定のプラットフォームのみでサポートされている構成もあります。 サポートされているプラットフォーム別のリストは、「構成のタイプ」で確認できます。

## ソフトウェア更新の管理

手始めに、iOSデバイスとmacOSデバイス用のソフトウェア更新の構成を設定します。

ソフトウェア更新用にスケジュール済みの時間枠を設定する場合、OS更新コマンドは、更新のタイミングを逸することがないように1時間ごとにデバイスにプッシュされます。 Appleの挙動により、OS更新コマンドをデバイスが受け取るたびに、アップグレードするようユーザーに通知するポップアップが表示されます。 ユーザーは3回まで延期できます。 3回目には、Appleの挙動により、デバイスがアップグレードを強制的に実行します。

MacOSデバイスには、適用可能な特定のルールがいくつかあります。 「macOSソフトウェア更新ルール構成」を参照してください。

### iOS用のOS更新コマンド

デバイスリストから、またはデバイスページから、1台以上のデバイスに1回限りの更新コマンドを送信することもできます。 「OS更新のスケジュール設定」コマンドを参照してください。

## iOS/iPadOSデバイスの設定

iOS/iPadOSでは、以下の構成がサポートされています。

- [**iOS/iPadOSの制約**](./iOSの制約.md)
- [**eSIM構成**](./eSIM構成.md)\* [**データプランを保護**](./デバイスのワイプ.md)
- [**モバイルネットワーク構成**](./セルラーネットワーク構成.md)
- [**紛失モードを有効化**](./紛失モードにあるAppleデバイスの管理.md)
- [**iOS MDMプロファイルの構成**](./iOS_MDMプロファイルの構成.md)
- [**Single Appモード**](./iOSのSingle_Appモードの構成.md)\* [**自律型Single Appモード**](./自律_Single_Appモード構成の作成.md)
- [**ビジネス用の共有iPad**](./業務用共有_iPad_デバイス.md)
- [**教育用の構成**](./教育.md)
- [**iOSカスタム構成**](./iOSカスタム構成.md)
- [**ロック画面のメッセージ**](./ロック画面メッセージ構成.md)

## watchOSデバイスの設定

iOSデバイスとのペアリング中にApple watchOSデバイスをIvanti N-MDMに登録できるようになりました。

この機能は現在watchOS 10+をサポートしています。

Procedure手順

1. iOS 17+の監視対象デバイスを登録する必要があります。
2. Apple Watch登録構成をiOSデバイスに割り当てます。
3. これで、Apple WatchをiPhoneとペアリングできます。

Watch 構成を iPhone にプッシュした後、Apple Watch をペアリングできます。 Apple WatchをiPhoneとペアリングした後でWatch構成をiPhoneにプッシュした場合は、Apple Watchのリモート管理を有効にすることはできません。

watchOSデバイスでは、以下の構成がサポートされています。

- [**セルラー（モバイル通信）構成**](./セルラー.md)
- [**証明書構成**](./証明書構成.md)
- [**証明書の透明性**](./証明書の透明性.md)
- [**ID証明書構成**](./ID証明書.md)
- [**iOSの制約**](./iOSの制約.md)
- [**パスコード設定**](./パスコード構成.md)
- [**アプリごとのVPN構成**](./Per-App_VPN構成.md)
- [**Wi-Fi構成**](./Wi-Fi構成.md)

## watchOSデバイス向けにサポートされているデバイスアクション

watchOSデバイスでは、以下のデバイスアクションがサポートされています。

- パスコードのクリア
- Apple Watchのロック
- Apple Watchのワイプ
- Ivanti Neurons for MDMからのApple Watchの登録解除ペアリングされているiOSデバイスの登録を解除すると、Watchがリセットされ、iOSデバイスとのペアリングが解除されます。

## macOSデバイスの設定

macOSでは、以下の構成がサポートされています。

- [**macOSの制約**](./macOSの制約.md)
- [**macOSデバイスの構成**](./macOSデバイスの構成.md)
- [**スクリプトとMobile@Workクライアントの操作**](./すべてのスクリプト.md)
- [**macOS MDM プロファイルの構成**](./macOS_MDM_プロファイルの構成.md)
- [**ファームウェアパスワードの設定**](./ファームウェアパスワードの設定.md)
- [**FileVaultの有効化**](./FileVault_2.md)\* [**FileVaultリカバリキー**](./FileVaultリカバリキー.md)
  - [**FileVaultオプション構成**](./FileVaultオプション構成.md)
- [**プラットフォームと拡張可能SSO**](./シングルサインオン構成.md)
- [**Active Directory macOS**](./Active_Directory（macOS）.md)
- [**Firewall (ファイアウォール)**](./macOSのファイアウォール.md)
- [**イーサネット**](./イーサネット構成（macOS）.md)
- [**Office 365アカウント作成**](./Office_365自動アカウント作成（macOS）.md)
- [**macOSシステム拡張**](./macOSシステム拡張の構成.md)
- [**メディアディスクへの書き込みの制約**](./macOSディスク焼き付けの制約.md)
- [**プライバシー設定**](./プライバシー設定（macOS）.md)

## TvOSデバイスの設定

tvOSでは、以下の構成がサポートされています。

- [**Apple TVの構成**](./Apple_TVの構成.md)
- [**Apple TVの制約**](./iOSの制約.md)
- [**会議室ディスプレイ**](./会議室ディスプレイ.md)
- [**AirPlayミラーリング**](./AirPlay構成.md)

## visionOSデバイスの設定

Ivanti Neurons for MDMにApple visionOSデバイスを登録できるようになりました。

この機能は現在visionOS 1.1+をサポートしています。

次のいずれかの方法でvisionOS デバイスを登録できます。

- [**アカウント主導のデバイス登録**](<Account driven Device Enrollment.htm>)
- [**アカウント主導のUser Enrollment**](<Account driven User Enrollment.htm>)
- [**デバイス登録**](./デバイス登録.md)

visionOSデバイスでは、以下の構成がサポートされています。

- [**CalDAV構成**](./CalDAV構成.md)
- [**CardDAV構成**](./CardDAV構成.md)
- [**証明書構成**](./証明書構成.md)
- [**証明書失効チェック構成**](./証明書失効チェック構成.md)
- [**証明書の透明性**](./証明書の透明性.md)
- [**DNSプロキシ構成の作成**](./DNSプロキシ構成の作成.md)
- [**暗号化DNS**](./暗号化DNS.md)
- [**Eメール構成**](./Eメール構成.md)
- [**Exchange構成**](./Exchange構成.md)
- [**Google構成**](./Google構成.md)
- [**ID証明書**](./ID証明書.md)
- [**iOSの制約**](./iOSの制約.md)
- [**LDAP構成**](./LDAP構成.md)
- [**マネージドドメイン**](./マネージドドメイン.md)
- [**ネットワークリレー構成**](./ネットワークリレー構成.md)
- [**Per-App VPN構成**](./Per-App_VPN構成.md)
- [**シングルサインオン構成**](./シングルサインオン構成.md)
- [**署名済みカレンダー構成**](./署名済みカレンダー構成.md)
- [**VPN構成**](./VPN構成.md)
- [**Webコンテンツフィルター**](./Webコンテンツフィルター.md)
- [**Wi-Fi構成**](./Wi-Fi構成.md)

## visionOSデバイス向けにサポートされているデバイスアクション

visionOSデバイスでは、以下のデバイスアクションがサポートされています。

- Apple Vision Proのワイプ
- Apple Vision Proの撤去
- Apple Vision Proのロック解除

## 宣言型デバイス管理（DDM）のサポート

Appleの宣言型デバイス管理は、管理対象デバイスがそれぞれの独自の管理設定を積極的かつ自律的に、より少ない通信で利用できるようにする、最新の管理プロトコルです。 宣言型デバイス管理は、新たに登録されたデバイスの場合は登録中に、すでに登録済みのデバイスの場合はチェックイン中に有効化されます。

宣言型デバイス管理は、次のような資格のあるデバイス上では、自動的に有効化されます。

- macOS 13以降を搭載したコンピューター
- iOS 15またはiPadOS 15以降を搭載したデバイス
- iOSまたはiPadOS 16以降でユーザー登録をサポートする宣言型デバイス管理を介して登録されたデバイス。
- tvOS 16以降を搭載したApple TVデバイス
- watchOS 10以降を搭載したApple Watchデバイス
- visionOS 1.1以降を搭載したApple Vision Proデバイス

現在サポートされている宣言型管理機能：

- **ステータスチャネル**：\* OSバージョンに対する変更
  - パスコードコンプライアンス
  - パスコードあり
- **構成**：- 宣言型管理構成

### DDM構成における述部

述部は、デバイス構成のアクティベーショに対して柔軟性と精度を提供できる、Cocoa言語の式です。 この式は、デバイス上に配置され、この述部の条件が満たされたときに適用されます。 述部を作成、保存し、任意のDDM構成に適用できる、新しい機能が追加されています。

\[配布] ページのDDM構成に、述部を適用するための新しいオプションが表示されます。 すでに作成済みの述部は、このセクションのドロップダウンリストで確認できます。

述部の作成

1. **\[管理]** > **\[Apple]** > **\[述部]** を開きます。
2. **\[Add]** をクリックします。 **\[述部を作成]** ウィンドウが画面に表示されます。
3. 次の情報を入力します。\* **名前** - 述語の名前
   - **説明** – 適切な説明を追加します
   - **述語式** - 述語式。 例：@status(device.model.family) ==’iPad’

::Image[]{src="Resources/Images/add_predicate1.png" signedSrc="Resources/Images/add_predicate1.png" size="68" caption alt isUploading="false" sha initialPath="Resources/Images/add_predicate1.png" githubPath="Resources/Images/add_predicate1.png" position="flex-start" indent="3"}

4. **\[保存]** をクリックします。 述部の作成を確認するダイアログが画面に表示されます。
5. ページを再読み込みし、\[ステータス] フィールドの値を見ることで（値：**不明**、**実行中**、**有効**、**無効**）、述部の構文の有効性を確認します。1) **\[テスト]** をクリックします。 **\[Predicateのテスト]** ウィンドウが画面に表示されます。

::Image[]{src="Resources/Images/test_predicate1.png" signedSrc="Resources/Images/test_predicate1.png" size="36" caption alt isUploading="false" sha initialPath="Resources/Images/test_predicate1.png" githubPath="Resources/Images/test_predicate1.png" position="flex-start" indent="2"}

:::Paragraph{listStyleType="decimal" listStart="2" indent="2"}
次の情報を入力します。\* **名前** - デフォルト
:::

:::Paragraph{listStyleType="disc" indent="3"}
**Predicate 式** – デフォルト
:::

:::Paragraph{listStyleType="disc" indent="3"}
**スペース** – デフォルトスペース
:::

:::Paragraph{listStyleType="disc" indent="3"}
**プラットフォーム** – iOS/macOS
:::

:::Paragraph{listStyleType="disc" indent="3"}
**デバイス名** – Predicate 式に関&#x9023;**\[デバイス名]** フィールドは、**\[スペース]** フィールドと **\[プラットフォーム]** フィールドの詳細がドロップダウンから選択されてはじめて、**\[プラットフォーム]** フィールドのすぐ下に表示されます。
:::

::Image[]{src="Resources/Images/test_predicate2.png" signedSrc="Resources/Images/test_predicate2.png" size="64" caption alt isUploading="false" sha initialPath="Resources/Images/test_predicate2.png" githubPath="Resources/Images/test_predicate2.png" position="flex-start" indent="4"}

:::Paragraph{listStyleType="decimal" listStart="3" indent="2"}
**\[Predicateのテスト]** をクリックします。
:::

:::Paragraph{listStyleType="decimal" listStart="4" indent="2"}
述部のテストの開始を確認するダイアログが画面に表示されます。
:::

:::Paragraph{listStyleType="decimal" listStart="5" indent="2"}
ページを再読み込みして述部の構文のステータスを見つけます。\* 正しい述部式の場合は、ステータスが **\[不明]** から **\[実行中]** > **\[有効]** に変わります。
:::

:::Paragraph{listStyleType="disc" indent="3"}
正しくない述部式の場合は、ステータスが **\[不明]** から **\[実行中]** > **\[無効]** に変わります。
:::

6. 異なる述語式を使用して複数の述部を作成する場合は、この手順を繰り返します。

### DDM構成の述部の配布

1. DDM対応の構成を作成します。
2. トグルスイッチ「述部を使用したアクティベーション」をオンに設定し、\[+] ボタンを使用して（必要に応じて）述部を含めます。

::Image[]{src="Resources/Images/predicates.png" signedSrc="Resources/Images/predicates.png" size="77" caption alt isUploading="false" sha initialPath="Resources/Images/predicates.png" githubPath="Resources/Images/predicates.png" position="flex-start"}

述部を編集または削除するには、**\[管理]** > **\[Apple]** > **\[述部]** を開きます。 このページで利用できる述部のリストを確認できます。 既存の述部に変更を加えて保存するには、**\[編集]** をクリックします。 同様に、既存の述部を削除するには、述部を選択して **\[削除]** をクリックします。

いずれかの構成に関連付けられている述部は削除できません。

### DDM構成の管理プロパティ

管理者は、以下のプロパティを使用して述部を作成できます。 

- ユーザー変数とデバイス変数
- ユーザ属性
- デバイス属性

述部での管理プロパティの使用例（カスタム属性）： 

ユーザーの名が 'test' かどうかをチェックするための述部 @property(userFirstName)=='test'

### その他の例

- デバイスのハードウェアファミリー：（Mac、iPhone、iPadなど）@status(device.model.family) =='iPad'trueの場合、デバイス上にパスコードが存在します。 falseの場合、デバイス上にパスコードは存在しません。@status(passcode.is-present)==true
- デバイスで使用中のオペレーティングシステムファミリー。macOS、iOSなど。@status(device.operating-system.family)=='iPadOS'
- デバイスで使用中のオペレーティングシステムバージョン。15.0など。@status(device.operating-system.version)=='18.2'@status(device.operating-system.version)\<'18.3'@status(device.operating-system.version)>='18.2'
- デバイス上のFile Vault有効化ステータスを指定するブール値@status(diskmanagement.filevault.enabled)==true
- 管理プロパティの例（カスタム属性）：ユーザーの名が 'test' かどうかをチェックするための述部@property(userFirstName)=='test'
