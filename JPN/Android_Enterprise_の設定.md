---
title: Android Enterprise の設定
createdAt: Wed Feb 11 2026 17:32:26 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:26 GMT+0200 (Eastern European Standard Time)
---

このセクションは以下のトピックを含みます。

- [**サポートされるデバイス**](./Android_Enterprise_の設定.md)
- [**Ivanti Neurons for MDMをAndroid Enterpriseに接続する**](./Android_Enterprise_の設定.md)
- [**Android Enterpriseの認証情報の入手**](./Android_Enterprise_の設定.md)
- [**Android Enterprise MDMトークンをIvanti Neurons for MDMに追加する**](./Android_Enterprise_の設定.md)
- [**Ivanti Neurons for MDMとGoogleとの間でユーザーを同期させる**](./Android_Enterprise_の設定.md)
- [**Active Directory/LDAPユーザー**](./Android_Enterprise_の設定.md)
- [**ローカルユーザー**](./Android_Enterprise_の設定.md)
- [**Android Enterprise をサポートされているデバイスに配布する**](./Android_Enterprise_の設定.md)
- [**登録したデバイスの撤去**](./Android_Enterprise_の設定.md)
- [**デバイスの導入**](./Android_Enterprise_の設定.md)
- [**導入の確認**](./Android_Enterprise_の設定.md)
- [**Android Enterpriseアプリの導入**](./Android_Enterprise_の設定.md)
- [**ビジネスアプリの構成**](./Android_Enterprise_の設定.md)

**ライセンス：**&#x53;ilver

Android Enterprise は Google が提供するプログラムであり、モビリティ管理者は次のことができるようになります。

- 仕事用データと個人用データの分離
- 企業アプリのセキュリティ確保と管理
- システムアプリの制御（Camera、Galleryなど）
- Android Enterprise コンテナで一元的にアプリケーションをプロビジョニング、構成します。
- 情報漏洩（スクリーンキャプチャ）の防止

Android Enterpriseを管理する UEMサーバーとしてIvanti Neurons for MDMを構成できます。 Android Enterprise には Android 3.0以上が必要です。 Android Enterprise、デバイス所有者および管理対象プロファイル – 従業員所有の2つの構成がサポートされています。

## サポートされるデバイス

Ivanti Neurons for MDM 現在サポートされているのは、Android 5.0を実行し、メーカーによってAndroid Enterpriseが有効化されているデバイス上のAndroid Enterpriseのみです。 Android 5.0を実行しているデバイスでキオスク モードを使用するには、Android Enterprise が必要です。

**前提条件**

Googleにまだドメインを登録していない場合は、まずGoogleの以下のウェブサイト上でプログラムに登録する必要があります。

[**https://admin.google.com.**](https://admin.google.com/)

このプロセスでは以下を実行します。

- ドメインを取得する（ユーザーのEメールアドレスに一致するドメイン）
- トークンを受け取る
- JSONクライアントIDをダウンロードする

Ivanti Neurons for MDMでAndroid Enterpriseをセットアップする場合、両方の項目が必須です。

処理後、取得したドメインを所有することを証明する方法を記載したEメールをお送りします。

**会社がすでに自社ドメイン名を使用して**Google Apps for Workに登録している場合は、Android Enterpriseを有効化する方法について[**https://support.google.com/work/android/answer/6174062**](https://support.google.com/work/android/answer/6174062)をご覧ください。

## Ivanti Neurons for MDMをAndroid Enterpriseに接続する

Android Enterpriseにサインアップした後、Ivanti Neurons for MDMをUEMサーバーとしてセットアップします。

## Android Enterpriseの認証情報の入手

**手順**

1. **\[管理] > \[Android Enterprise]** に移動します。
2. **\[Googleデベロッパーコンソール]** をクリックします。
3. 最初に表示されたリンクをクリックし、Googleデベロッパーコンソールに進みます。
4. ドロップダウンメニューから **\[プロジェクトを作成]** を選択します。
5. プロジェクトの名前を入力します。
6. サービス利用規約に同意します。
7. **\[作成]** をクリックします。
8. **API** をクリックします。
9. **\[API]** を選択します。
10. 検索フィールド&#x306B;**「emm」**&#x3068;入力し、Google Play EMMを検索します。
11. **Google Play EMM API**リンクをクリックします。
12. **\[APIを有効化]** をクリックします。
13. **\[認証資格情報]** をクリックします。
14. **\[サービスアカウント]** を選択します。
15. **\[作成]** をクリックするとJSONファイルが保存されます。

## Android Enterprise MDMトークンをIvanti Neurons for MDMに追加する

**手順**

1. [**https://admin.google.com**](https://admin.google.com/)にログインします。
2. **\[セキュリティ]** をクリックします。
3. Android Enterprise 設定が表示されない場合、**\[詳細を表示]** をクリックします。
4. **\[Android Enterprise 設定]** を選択します。
5. **\[エンタープライズモビリティ管理プロバイダーの管理]** にMDMトークンをコピーします。
6. Ivanti Neurons for MDMポータルに戻ります。
7. **\[完了]** をクリックします。
8. ボックス2で、コピーしたMDMトークンを貼り付けます。
9. **\[ドメイン]** フィールドに、Googleで取得したドメインを入力します。
10. **\[ファイルを選択]** をクリックし、ダウンロードしたJSONファイルをアップロードします。
11. **\[接続]** をクリックします。接続に成功すると、**\[Googleに接続]** というメッセージが表示されます。
12. ボックス3で、**\[認証]** をクリックして、Ivanti Neurons for MDMにGoogleユーザーデータへのアクセスを付与することを示します。
13. **\[承諾]** をクリックします。メッセージ「**ユーザーに接続**」がIvanti Neurons for MDMポータルに表示されます。

## Ivanti Neurons for MDMとGoogleとの間でユーザーを同期させる

Android Enterprise を Ivanti Neurons for MDMIvanti Neurons for MDM で管理された Android ユーザに配布する前に、各ユーザには Google Admin Portal で対応するレコードが必要です。 Ivanti Neurons for MDMとGoogle Admin Portalとの間でユーザー情報を同期させるために必要なステップは、組織のディレクトリサービス（ AD/LDAP）との統合をセットアップ済みであるかどうかによって異なります。

## Active Directory/LDAPユーザー

Ivanti Neurons for MDMとのAD/LDAP統合をセットアップ済みである場合は、Google Apps Directory Syncを使用して、Google Admin PortalとのAD/LDAP統合をセットアップする必要があります。 詳細は、[**https://support.google.com/a/answer/106368?hl=en**](https://support.google.com/a/answer/106368?hl=en)を参照してください。

## ローカルユーザー

Ivanti Neurons for MDMでローカルユーザーのみを作成し、ディレクトリサービスと統合するつもりがない場合、それらのユーザーをGoogle Admin Portalと同期させるには、以下のステップを完了します。

**手順**

1. [**https://admin.google.com**](https://admin.google.com/)からGoogle管理ポータルにログインします。
2. **\[ユーザー]** をクリックします。
3. 右下隅の **\[ユーザーの追加]** または **\[複数ユーザーの追加]** のアイコンをクリックします。
4. Android Enterpriseを使用するIvanti Neurons for MDMユーザーごとに、Ivanti Neurons for MDMユーザーと同じユーザー名およびEメールアドレスを使用して、Googleユーザーを追加します。
5. Google Admin Portalに追加したIvanti Neurons for MDMユーザーごとに、Ivanti Neurons for MDMポータルで以下のステップを行います。a. \[ユーザ] タブでユーザ名リンクをクリックすると、ユーザの詳細情報が表示されます。b. **\[Googleユーザーディレクトリとユーザーを同期]** を選択します。c. **\[Googleユーザーディレクトリと同期]** をクリックします。d. Google ステータスが \[有効] であることを確認します。

## Android Enterprise をサポートされているデバイスに配布する

Android Enterprise を配布するには、次の2つの構成が必要です。

- Android Enterprise：会社所有のデバイス構成の仕事用プロファイルは、Android Enterpriseを有効化します。
- ロックダウン & キオスク構成は、適用する Android Enterprise 制限を定義します。

## 登録したデバイスの撤去

BYOD シナリオでは、会社所有デバイスでデバイス管理者から Android Enterprise 仕事用プロファイルに移行する際に、デバイスを除却して再登録する必要はありません。 デバイスのワイプや撤去は、デバイス管理者からデバイス所有者モードに移行する場合のみ必要です。

撤去アクションのデバイス所有者/拡張プロファイル所有者/会社所有の個人が有効化モードで登録されたデバイスを選択すると、「撤去コマンドは組織が所有するデバイスではサポートされていない」ことを示すポップアップが画面に表示されます。

## デバイスの導入

**手順**

1. Ivanti Neurons for MDMポータルで **\[構成]** を開きます。
2. **\[Android Enterprise: 仕事用プロファイル]** をクリックします。
3. **\[編集]&#x20;**&#x3092;クリックします。
4. **\[次へ]** をクリックします。
5. **\[すべてのデバイス]** または **\[カスタム]** を選択します。
6. **\[カスタム]** を選択した場合は、Android for Work設定を受信すべきデバイスグループを検索し、選択します。
7. **\[完了]** をクリックします。
8. **\[リストに戻る]**（左上）をクリックします。
9. **\[+追加]** をクリックします。
10. **\[ロックダウン & キオスク: Android Enterprise]** をクリックします。
11. **\[名前]** フィールドに構成を識別するテキストを入力します。
12. **\[ロックダウンの種類を選択]**&#x3067;、**\[仕事用プロファイル]** をクリックします。
13. 対象デバイスに適用したいロックダウン設定を選択します。
14. **\[次へ]** をクリックします。
15. **\[すべてのデバイス]** または **\[カスタム]** を選択します。
16. \[カスタム] を選択した場合は、Android Enterprise設定を受け取る必要があるデバイスグループを検索して選択します。
17. **\[完了]** をクリックします。

導入後は、作成したプロファイルを変更できません。 代わりに、新しいAndroid Enterprise構成を作成し、これを導入する必要があります。

## 導入の確認

Android Enterpriseが導入されたことを、以下の方法で確認できます。

- **\[ユーザー] > \[ユーザー]** からユーザーのエントリを探し、その**Googleステータス**が **\[有効]** であることを確認します。
- **\[デバイス] > \[デバイス]** の下でデバイスのリンクをクリックしてから、**Android Enterprise** のステータスが **\[有効]** であることを確認します。

ユーザーの**Googleステータス**は **\[有効]** である必要があります。 これが有効でなければ、ユーザーはデバイスを登録できません。

GSuiteを利用していない企業の場合、マネージドGoogle Playアカウントの方法を使用することで、ユーザーをAndroid Enterpriseに登録できます。 Android EnterpriseがマネージドGoogle Playアカウントとしてセットアップされた場合は、Android Enterpriseデバイスが登録されるまで、ユーザーは **\[Googleステータス：有効化済み]** として表示されません。 マネージドGoogle Playアカウントの詳細は[**マネージドGoogle Playアカウント**](./マネージドGoogle_Playアカウント（Android_Enterpriseアカウント）.md)をご覧ください。

## Android Enterpriseアプリの導入

Android Enterprise用に開発されたアプリには、Ivanti Neurons for MDMを通じて構成できるオプションが含まれている場合があります。

**手順**

1. Ivanti Neurons for MDMポータルで、**\[アプリ] > \[アプリカタログ]**&#x3092;開きます。
2. Google Playストアでアプリを検索します。
3. アプリのエントリをクリックします。
4. Android Enterpriseユーザーに代わって承認事項を承諾します。
5. **\[次へ]** をクリックします。
6. 配信オプションを選択します。
7. **\[詳細オプションとアプリ構成]** を展開します。
8. 次のガイドラインに従って、オプションに情報を入力します。

| 設定                               | 説明                                                                                                                                    |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **デバイスにインストール**                  | 登録後すぐにインストールを開始するには、このオプションを選択します。 デバイスがSamsung Knoxデバイスで、以下のサイレントインストールオプションが選択されている場合を除き、ユーザーにアプリのインストールを確認するメッセージが表示されます。          |
| **エンドユーザーのアプリカタログでアプリを表示しない**    | ユーザーにデバイス上でアプリカタログを見せたくない場合に選択します。                                                                                                    |
| **Samsung Knoxデバイスにサイレントインストール** | ユーザーにSamsung Knoxデバイスへのインストールを指示したくない場合に選択します。                                                                                        |
| **アプリインストール優先度を設定**              | Android Enterpriseアプリの場合は、特定のアプリのダウンロードを他のアプリより優先させることができます。 たとえばTunnelとメールアプリを、他の重要でないアプリの前にダウンロードするなどです。 選択可能な優先度は以下のとおりです。\* **高** |

:::Paragraph{listStyleType="disc" indent="2"}
中（デフォルト）
:::

:::Paragraph{listStyleType="disc" indent="2"}
**低**この設定は、自社開発アプリ、公開アプリ、非公開アプリ、およびWebアプリに適用されます。 自社開発アプリはクライアント経由、市販アプリと非公開アプリはGoogle経由でインストールされます。 アプリの優先度は同じチャネルでインストールされたアプリにのみ適用されます。 |
\| **Wi-Fiに接続したときのみインストール**         | これを選択すると、デバイスがWi-Fiに接続している場合のみアプリをインストールします。                                                                                                                                                                                                                                                 |
\| **充電中にのみインストール**                 | これを選択すると、デバイスが充電中の場合のみアプリをインストールします。                                                                                                                                                                                                                                                         |
\| **アイドル状態のときのみインストール**            | これを選択すると、デバイスがアイドル状態のとき（ユーザーが特に何かに使用していないとき）のみアプリをインストールします。                                                                                                                                                                                                                                 |
\| **インストール時に自動起動**                 | インストール後、自動的にアプリを起動する場合に選択します。 この機能はアプリがデバイス上に新しくインストールされた場合（バージョン更新ではなく）のみ使用可能です。                                                                                                                                                                                                            |
**\[次へ]** をクリックします。
:::

10. プロモーションオプションを選択します。
11. **\[完了]** をクリックします。

## ビジネスアプリの構成

アプリカタログの\[ビジネスアプリ] セクションで、次のようなAndroid Enterpriseアプリを入手できます。

- [**生産性の分割**](./Android_enterpriseによるDivide_Productivityの導入.md)
- 電子メール+
- トンネル
- Gmail
