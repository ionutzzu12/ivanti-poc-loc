---
title: Apps@Work (iOS、Android、Windows、macOS)
createdAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
---

Apps\@Work はソフトウェアおよびアプリケーションの安全な配布を支援するエンタープライズ アプリケーション ストアフロントです。 Apps\@work は iOS、Android、macOS、Windows デバイス版が提供されています。 Apps\@Workの企業用AppStoreが、iOS、Android、およびmacOS版のIvanti Go appクライアントおよびMobile\@Workクライアントと統合されます。 Windows デバイスでは、ネイティブ スタンドアロン アプリケーションです。 このセクションは以下のトピックを含みます。

- [**iOS Apps@Work**](./Apps@Work__iOS、Android、Windows、macOS_.md)
- [**Android Apps@Work**](./Apps@Work__iOS、Android、Windows、macOS_.md)
- [**macOS Apps@Work**](./Apps@Work__iOS、Android、Windows、macOS_.md)
- [**Windows Apps@Work**](./Apps@Work__iOS、Android、Windows、macOS_.md)

## iOS Apps\@Work

Apps\@work ネイティブ アプリストアは自動的に Go クライアントとともに配布されます。 管理者によるアクションは必要ありません。 Apps\@work タブは Go クライアントのタスクバーに表示されます。 各ユーザのこのタブには、会社で承認されたアプリケーションが表示され、インストールできます。 詳細については、[**iOS Apps@Work AppStore Features**](./iOS_Apps@Work_AppStore_Features.md)をご参照ください。

アプリケーション更新に関する iOS Apps\@Work エンドユーザ通知は、既定で有効です。 この設定を変更する場合は、[**カタログ設定**](./カタログ設定.md)の「**通知**」トピックをご参照ください。

## 既に iOS Apps\@Work Webclip を使用している場合

レガシー iOS Apps\@Work webclip が導入されている場合は、既定ではネイティブ統合されたアプリケーション カタログがありません。 iOS Apps\@Work ネイティブ カタログに移行し、Apps\@work webclip をデバイスから削除する場合は、次の手順を実行します。

### 構成のプッシュ

Go クライアント アプリケーションからネイティブ アプリストア エクスペリエンスで Apps\@Work を提供するには、管理者がネイティブ クライアントのアプリケーション カタログ構成をデバイスにプッシュする必要があります。 詳細については、[**構成の操作**](./構成の操作.md)をご参照ください。

**手順**

1. Ivanti Neurons for MDM 管理ポータルにログインします。
2. **\[構成]** > \[フィルタ] に移動し、**\[クライアント サービス]** を選択します。 すべてのクライアント構成が一覧表示されます。
3. **\[ネイティブ クライアントのアプリケーション カタログ]** を選択します。 \[ネイティブ クライアント構成のアプリケーション カタログ] ページが開きます。
4. **配布の編集**アイコンをクリックします。 \[配布の編集] ページが開きます。
5. 以下のオプションから1つ選択してください：\* **すべてのデバイス**
   - **デバイスなし** - どのデバイスにも配布しない場合
   - **カスタム** - デバイス、デバイス グループ、ユーザ、ユーザ グループを選択できます
6. 構成が配布された後、ユーザは Go クライアント バージョン83以降にアップグレードする必要があります。 Apps\@Work タブは Go app クライアントに表示されます。デバイスで Go クライアントが使用できないため、iReg を使用して登録されたデバイスでは構成をプッシュできません。 ネイティブ アプリケーション カタログを取得するには、Go app クライアントをインストールする必要があります。 詳細については、[**デバイス登録(iOS、macOS、Android)**](./デバイス登録_iOS、macOS、Android_.md) をご参照ください。

## iOS Apps\@Work Webclip の削除

Apps\@Work Webclip をデバイスに配布し、既に Apps\@Work ネイティブ エクスペリエンスに移行した場合は、iOS Apps\@Work webclip を削除できます。

**手順**

1. **\[構成]** を開きます。
2. 構成のフィルタ – **Apple App Catalog**。
3. **\[編集]&#x20;**&#x3092;クリックします。
4. **\[配布]** で **\[デバイスに配布しない]** を選択します。
5. **\[保存]** をクリックします。

## Android Apps\@Work

Apps\@work ネイティブ アプリストアは自動的に MI Go クライアントとともに配布されます。 管理者によるアクションは必要ありません。 Apps\@work タブは Mi Go クライアントのタスクバーに表示されます。 各ユーザのこのタブには、会社で承認されたアプリケーションが表示され、インストールできます。 詳細については、[**\[管理\] - \[Android Enterprise\]**](./\[管理]_-_\[Android_Enterprise].md) をご参照ください。

## macOS Apps\@Work

MacOs Apps\@work は macOS Mobile\@Work クライアントと統合されています。 デバイスがIvanti Neurons for MDMに登録されると、クライアントが切り替わり、Apps\@Workとして表示されます。 新しく作成されたテナントでは、Apple App Catalog Webclip 構成が macOS デバイスにプッシュされません。 必要に応じて、管理者は Apps\@work Webclip 構成を macOS デバイスに配布できます。 詳細については、[**macOSデバイスの構成**](./macOSデバイスの構成.md)をご参照ください。

### macOSアプリの配布

- Ivanti は Apple MDM プロトコルで Mobile\@Work を使用した macOS アプリケーションの配布をサポートします。 管理者は以下のいずれかまたは両方を選択可能です。
  - AppleのMDMプロトコル - 管理者は、所定のPKG形式（配布形式）のみ自社開発アプリとしてアップロードできます。また、Mac App Storeからアプリを配布することも可能です（Appleの「Appとブック」ライセンスサポートを含む）。 ただしこの方法で管理者がDMGおよび他のPKG形式を配布することはできません。
  - macOS対応Mobile\@Workアプリ - ユーザーにアプリを配布する方法として、管理者はMobileIron Packager（MIP）アプリを使用し、任意のPKG、DMG、.appファイルをMIPファイルに変換できます。 MIPファイルを自社開発アプリとしてIvanti Neurons for MDMにアップロードします。
    [**ソフトウェアダウンロードサイト**](https://support.mobileiron.com/mi/mobileatwork-macos/current/)からユーティリティをダウンロードできます。
- 管理者はMobile\@Workを使用し、DMG、PKG、.app形式の自社開発アプリを配布できます。 Mac App Storeでのみ提供されるアプリの場合、管理者は「Appとブック」ライセンス機能を含むAppleネイティブのMDMを引き続き使用できます。 詳細については、[**macOSデバイスの構成**](./macOSデバイスの構成.md)をご参照ください。

## Windows Apps\@Work

Apps\@Work はスタンドアロンのネイティブ アプリケーションで、Microsoft Store からダウンロードするか、Ivanti Neurons for MDM から直接プッシュできます。 Windows 10以上のデバイスでは、Ivanti Neurons for MDM で Windows 公開アプリケーションと社内アプリケーションを使用できます。 Apps\@Work はサポートされている Windows 10以降のデバイスでサイレント インストールされます。

詳細は[**アプリ構成**](./アプリ構成.md)をご参照ください。

### Windows Apps\@Work の使用

Apps\@Workにより、Windows 10デバイス上のWindows公開アプリや自社開発アプリをIvanti Neurons for MDMで利用できるようになります。 Apps\@Workは、サポートされているWindows 10デバイスにサイレント インストールされます。

**Apps\@Work 証明書認証**

Windows Apps\@Work で証明書認証を使用するには、次の手順を実行します。

1. **\[管理]****>****\[Windows]****>****\[Apps\@Work 証明書認証]** に移動します。
2. 設定を**オン**にします。
   設定を**オフ**にすると、ユーザ名とパスワードを使用する必要があります。

Windows対応のApps\@WorkではSAMLがサポートされません。

Apps\@Work用にアプリを構成するには：

1. Windowsアプリを選択します。
2. **\[アプリ構成]** タブをクリックします。
3. **\[デバイスにインストール]** をクリックします。Windows自社開発アプリの構成は、サイレントインストールフラグ、またはApps\@Workを使用したインストールのいずれかに設定できます。 パブリックアプリは、サイレントインストールに設定できません。
4. 任意で、Apps\@workカタログにアプリを表示するか非表示にするかを選択します。この選択は社内アプリのみ可能です。
5. **\[プロモーション]** タブをクリックします。現在、Apps\@Work ではバナー プロモーションがサポートされていないため、使用可能なオプションは **\[特集]** および **\[特集以外]** です。市販アプリでは **\[プロモーション]** オプションのみ表示されます。
