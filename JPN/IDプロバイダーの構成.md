---
title: IDプロバイダーの構成
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

ライセンス：Silver

IDプロバイダー（IdP）を構成し、Ivanti Neurons for MDM へのデバイス登録、管理ポータルへのアクセス、セルフサービスポータルへのアクセスを希望するユーザーを認証します。 オンプレミス LDAP 対応ユーザ ディレクトリが必要です。 Ivanti Neurons for MDM は、すべての SAML 2.0 対応 IdP と連携できます。 Microsoft Entra ID認証（Entra ID）、Microsoft ADFS（Active Directory Federation Services）、Okta、OneLogin、PingOne、Ping IdentityのPingFederateは、Ivanti Neurons for MDMに対応することが検証されています。

これまでSAML auth/IdPを設定すると、SAML認証がデバイス登録とポータル認証の両方に使用されていました。 トグルボタンが提供され、管理ポータルのアクセスとデバイス登録で異なる認証方法を選択できます。 バイパストグルはデバイス登録にのみ使用します。

デバイス登録中に、管理者は ID プロバイダ オプションを回避できます。このようにすると、ユーザは ID プロバイダ ページでの認証ではなく、PIN を使用した認証を選ぶことができます。

## 概要

- Microsoft AD または他のオンプレLDAPディレクトリを使用している場合は、Ivanti Neurons for MDM に接続し、ユーザーをインポートするようConnectorを設定する必要があります。 Connector または[**LDAP**](./LDAPサーバーの構成.md)の設定が完了していない場合は完了させてください。
- IdPが追加されると、ユーザー認証は自動的にLDAPからIdPに切り替わります。
- IdPプロバイダーは1つにしてください。
- IdPにアクセスできなくなった場合は、Ivanti Neurons for MDM テナント管理者（TA）アカウントを使用してこの管理ポータルにアクセスし、トラブルシューティングを行います。 TAはローカルアカウントであり、外部認証を必要としません。 Ivanti Neurons for MDM がプロビジョニングされ、組織の技術担当者または同等の担当者に情報が提供されるとTAアカウントが作成されます。 TAアカウント情報をお持ちでない場合は、サポート担当者にお問い合わせください。
- Ivanti Neurons for MDMは、Windows 10デバイス登録中のユーザー認証用にMicrosoft Entra ID（Entra ID）をサポートしています。IdPベンダーが提供したツールを使用し、LDAPユーザーの認証タイプを設定します。 IdPの認証方式は Ivanti Neurons for MDM の設定より優先されます。Ivanti Neurons for MDM 認証設定は、**\[ユーザー] > \[ユーザー設定] > \[デバイス登録設定] > \[デバイス登録認証タイプ]** にあります。
- Apple Device EnrollmentおよびConfiguratorデバイス登録は、ユーザー認証にIdPを使用しません。
- Apple Business ManagerのiOSデバイス登録とmacOSデバイス登録で機能するようにIDプロバイダを構成するには、**\[管理] > \[Apple] > \[デバイス登録] >&#x20;***\[デバイス登録プロファイルを編集]* にある**カスタム登録を有効化**と、関連する**IvantiがホストしているWebページ**設定を有効にする必要があります。詳細はこちらの「[**デバイス登録**](./デバイス登録.md)」をご覧ください。

::Image[]{src="Resources/Images/idp001.png" signedSrc="Resources/Images/idp001.png" size="32" caption alt isUploading="false" sha initialPath="Resources/Images/idp001.png" githubPath="Resources/Images/idp001.png" position="flex-start" indent="2"}

## IdPの設定タイプ

Ivanti Neurons for MDM の \[ID] ページが、以下の種類のIdPプロバイダーの設定を導いてくれます。

- **Ivanti Neurons for MDM IdPの設定**- サポートされているIvanti Neurons for MDM IdPプロバイダーは、Entra ID、OneLogin、Okta、PingOneです。
- **オンプレIdP設定** - サポートされるオンプレIdPプロバイダーはADFS 3.0、PingFederate 8.2.1、PingFederate 8.1.3です。
- **汎用IdP設定** - これは、Microsoft ADFS、Okta、OneLogin、PingFederateを使用していない場合の汎用設定パスです。

## IDプロバイダー（IdP）の構成

**手順**

1. **\[管理]&#x20;**> **\[ID]** > **\[SAML 認証]** を開きます。
2. IDプロバイダの設定の種類をクリックします。\* **Ivanti Neurons for MDM IdP設定**
   - **オンプレIdP設定**
   - **汎用IdP設定**
3. 対応のIIdPを選択します。 ステップ3で **\[汎用IdP設定]** を選択した場合は、このステップをスキップし、ステップ5に進んでください。
4. 選択したIdPに応じて表示される、画面上の指示に従います。
5. **\[完了]** をクリックします。

管理者は、IdPを使用した最初の認証から2時間までシングルサインオンが可能です。

### 必要になる可能性のある設定タスク

選択したIdPに応じて、関連する以下のページやステップに進みます。

| **IdP**    | **手順** |
| ---------- | ------ |
| - Entra ID |        |

- Okta
- OneLogin
- PingOne               | \* IdPにアップロードするキーを生成します。
- IdPにログインし、生成したキーをアップロードします。
- IdPからメタデータファイルをエクスポートし、Ivanti Neurons for MDM にインポートします。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
  \| - ADSF 3.0
- PingFederate 8.2.1
- PingFederate 8.1.3 | \* Ivanti Neurons for MDM からメタデータ ファイルをダウンロードします。
- ADFSの \[証明書利用者の信頼] を設定するか、PingFederateの \[SP接続] を設定し、Ivanti Neurons for MDM メタデータファイルをインポートします。
- IdPからメタデータファイルをエクスポートし、Ivanti Neurons for MDM にインポートします。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
  \| - 汎用IdP                                              | ::::WorkflowBlock

:::WorkflowBlockItem
Ivanti Neurons for MDM からメタデータ ファイルをダウンロードします。
:::

:::WorkflowBlockItem
IdP ベンダーから提供された手順に従い、「サービス プロバイダ」として Ivanti Neurons for MDM サービスに接続するための IdP サーバーまたはサービスを構成します。
:::

:::WorkflowBlockItem
1. 上記ステップ1のメタデータファイルをIdPにアップロードします。 この構成ファイルは、SAML 2.0 IDプロバイダーと通信するSAML 2.0サービスプロバイダーとして Ivanti Neurons for MDM を有効化するための必須情報を含みます。 標準的なSAML 2.0のURL、証明書、設定はメタデータファイルに含まれます。Ivanti Neurons for MDM は SAML 2.0対応 IdP がサービスプロバイダからエクスポートされた XML メタデータをインポートおよび処理できることを想定しています。
2. IdPがRSA-SHA1を使用してSAML認証要求に署名するよう構成します。 認証要求の検証に使用される署名証明書に関する情報は、ステップ1でダウンロードしたメタデータファイルに含まれます。
3. SAML 応答にユーザー名を含めるようにする IdP の構成が Ivanti Neurons for MDM に送信されました。 IdPからのSAML応答の \[Name Id] 要素でユーザー名を指定します。
   IdPからメタデータファイルをエクスポートし、Ivanti Neurons for MDM にインポートします。
:::

:::WorkflowBlockItem
(任意) - SAML 認証要求にユーザ名を含める: 認証要求にユーザーを認証するユーザー名を含め、IdP で認証するときに追加のユーザー入力を削除します。 このオプションを有効にすると、認証失敗が発生する場合があります。 IdP 検証についてわからない場合は、**\[この変更の影響を理解しています]** オプションを選択し、**\[SAML 認証要求にユーザー名を含める]** 設定を **\[オン]** に切り替えます。Ivanti Access は、この設定の検証された IdP です。
:::

\:::: |

## IdP認証をバイパスするローカルユーザの有効化

IdPまたは Ivanti Neurons for MDM の接続がダウンし、Ivanti Neurons for MDM 側からのトラブルシューティングが必要な場合、一部の管理者は、LDAPやIdPなどの外部システムによる認証に頼らず、Ivanti Neurons for MDM にログインできる必要があります。 システム管理者の役割を持つローカルユーザーのみIdP認証をバイパスできます。

IdP認証をバイパスするローカルユーザーのリストを作成します。

**手順**

1. **\[管理] > \[ID]** をクリックします。
2. \[IdP認証をバイパスするローカルユーザー] セクションで **\[+ユーザーを追加]** をクリックします。
3. システム管理者の役割を持つローカルユーザーだけを表示したリストから、少数のユーザーを選択してください。
4. **\[保存]** をクリックします。

IdP認証をバイパスするローカルユーザーのリストからユーザーを削除するには、削除したいエントリの横にある削除アイコンをクリックします。

\[ID] ページが表示されない場合、必要な権限を持っていない可能性があります。 以下のいずれかの[**役割**](./ユーザーの役割.md)が必要です。

- システム管理
- 読み取り専用システム
