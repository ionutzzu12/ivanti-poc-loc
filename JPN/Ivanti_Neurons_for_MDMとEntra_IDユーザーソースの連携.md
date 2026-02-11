---
title: Ivanti Neurons for MDMとEntra IDユーザーソースの連携
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

Entra ID（Entra ID）と連携させるには、Microsoft Entra IDアカウントに関する詳細を使用してIvanti Neurons for MDMを構成する必要があります。 連携には既存の構成済みMicrosoft Entra IDアカウントが必要です。 このソリューションにオンプレのConnectorまたはLDAPは不要です。

このセクションは以下のトピックを含みます。

- [**ユースケース**](./Ivanti_Neurons_for_MDMとEntra_IDユーザーソースの連携.md)

## ユースケース

以下のいずれかの場合に、Ivanti Neurons for MDMとEntra IDを連携できます。

- Microsoft Office 365と連携させる
- ユーザー認証用に、Microsoft Entra ID、Microsoft ADFS、または別のSAML 2.0 IDプロバイダー（IdP）を設定する
- ユーザーソースとしてMicrosoft Entra IDを設定する
- Microsoft Entra IDからユーザーを同期して、使い始める。 Entra IDドメインのすべてのユーザーとグループがIvanti Neurons for MDMインスタンスに同期されますEntra ID同期に次の理由によるエラーが存在する場合、**\[通知]** ページに通知が表示されます。\* Entra IDサービスに到達できない
  - すべてのユーザー属性がEntra IDと同期されていない
  - 一部のユーザー属性がEntra IDと同期されていない
- 複数のIdPを持つ環境は現在サポートされていません。
- ユーザーソースとしてMicrosoft Entra IDを使用していない場合は、LDAPのローカルアカウントまたはソースユーザーを使用できます。 これには、オンプレのLDAPリソースにアクセスする Ivanti Neurons for MDM Connectorの設定が必要です。
- 現時点では、Microsoft Entra IDをユーザー認証用にのみ使用し、オンプレミスのLDAPをユーザーディレクトリ用に使用することはサポートされていません。

## Entra IDの使用

Entra IDを使用するには、以下のいずれかの方法でユーザー認証用のIDプロバイダーを設定します。

- ユーザーソース用とユーザー認証用の両方にMicrosoft Entra IDを使用する場合は、IdPとしてEntra IDを設定してください。 **\[管理] > \[ID] > \[Ivanti Neurons for MDM IdP設定]** を開き、メニューから **\[Entra ID]** を選択します。
- ユーザーソース用にMicrosoft Entra IDを使用し、ユーザー認証用にADFSを使用する場合は、IdPとしてADFSを設定してください。 **\[管理] >\[ ID] >\*\*\*\*\[オンプレミス IdP 設定]** を開き、メニューから \[ADFS] を選択します。
- Entra ID以外のSAML 2.0 IdPを使用し、ユーザー認証用にADFSを使用する場合は、**\[管理] > \[ID] >\*\*\*\*\[汎用IdP設定]** を開き、ページ上の指示に従います。

詳細については、[**IDプロバイダーの構成**](./IDプロバイダーの構成.md)をご参照ください。

## Entra ID設定

このトピックでは、Entra ID設定の構成について説明します。

**手順**

::::WorkflowBlock
:::WorkflowBlockItem
**\[管理] > \[Microsoft Azure] > \[Entra IDユーザーソース]** を開きます。
:::

:::WorkflowBlockItem
以下の詳細情報を指定します。
:::

:::WorkflowBlockItem
1. **Entra ID名**。
2. **同期間隔** - Ivanti Neurons for MDMがEntra IDからのユーザーデータを同期する頻度を変更します。
3. **このEntra IDを有効化** - このオプションを使用してEntra IDインスタンスを有効化または無効化します。
4. **Entra IDからインポートしたユーザーを自動的に招待**を選択 - Entra IDからIvanti Neurons for MDMにインポートしたユーザーに自動的に登録招待メールを送信するかどうかを管理します。
5. **管理対象Apple ID**を選択 - Entra IDユーザーの管理対象Apple IDを同期させる場合に選択します。\* **なし**
   - **パターン&#x20;**-\* **ユーザーのメールアドレス**
     - **userUPN**
     - (任意) \[「appleid」サブドメインを含める] オプションを選択し、既存のApple IDとの競合を避けます。
6. （任意）**カスタム属性の追加** - デバイス管理に適用したいカスタム ユーザ属性をディレクトリ サービスから指定します。 これにより、各属性は、変数をサポートする構成フィールドの$\{attributeName}によって参照されます。 このオプションを使用するには、すべてのEntra IDサーバーにカスタム属性を一貫して実装しておく必要があります。 実装に含まれるいずれかのEntra IDサーバーがこの属性を使用していない場合、この属性に依存する機能が意図どおりに機能しないことがあります。
   Entra ID設定を変更した後、**\[保存]** をクリックします。
:::
::::
