---
title: SCIM によるユーザー プロビジョニング
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

このセクションは以下のトピックを含みます。

- [**ユーザー プロビジョニング**](./SCIM_によるユーザー_プロビジョニング.md)
- [**Ivanti Neurons for MDMからのトークンの生成**](./SCIM_によるユーザー_プロビジョニング.md)
- [**トークンステータスの変更**](./SCIM_によるユーザー_プロビジョニング.md)
- [**監査トライアルからのトークンステータスの表示**](./SCIM_によるユーザー_プロビジョニング.md)
- [**SCIMプロビジョニングにおける属性の構成**](./SCIM_によるユーザー_プロビジョニング.md)

## ユーザー プロビジョニング

ユーザープロビジョニングでは、SCIMプロトコルを使用して IdP をIvanti Neurons for MDMと同期させ、部分的なユーザーとグループの同期を可能にします。 ユーザープロビジョニングでは、SCIM プロトコルを使用して、IdP から Ivanti Neurons for MDM に供給されるユーザーオブジェクトとグループオブジェクトを自動的に作成および更新します。 現在のEntra IDおよびOktaとの統合のように、ユーザーおよびグループのプロビジョニング プロセスは自動化されます。IdPでユーザーまたはグループに対して変更が行われると、同じ変更がIvanti Neurons for MDMにも反映されます。

ユーザー名の値はIvanti Neurons for MDM内で一意であるため、既にプロビジョンされているユーザーの \[ユーザープリンシパル名] 属性をIdPで更新することはできません。

## Ivanti Neurons for MDMからのトークンの生成

IdPのユーザープロビジョニングを開始するには、Ivanti Neurons for MDMでトークンとターゲットURLを生成します。

必ずトークンとターゲット URL を保存してください。

一度に生成できるトークンの数は最大2個です。

**手順**

1. Ivanti Neurons for MDM 管理ポータルにログインします。
2. **\[管理]&#x20;**>**&#x20;\[ID]&#x20;**>**&#x20;\[ユーザ プロビジョニング]** を開きます。
3. ドロップダウンリストからIDプロバイダー（IdP）を選択します。
4. 新しいトークンを生成するには、**\[生成]** をクリックします。 通知メッセージが表示されます。**\[生成]** をクリックします。 新しいページが開き、トークンの詳細とターゲットのSCIM URLが表示されます。
5. **\[コピー]** をクリックすると、トークンまたはSCIM URLのいずれかがコピーされます。
6. ページを更新します。 **\[ユーザー プロビジョニング]** ページにトークンステータス表が表示されます。

## トークンステータスの変更

既存のトークンの状態を変更できます。

**手順**

1. **\[Entra IDユーザープロビジョニング]** ページで **\[選択]** ドロップダウンメニューをクリックします。
2. **\[選択]** をクリックし、トークンに対して次の変更を行います。\* **アクティブに設定**
   - **非アクティブに設定**
   - **更新**
   - **削除**

## 監査トライアルからのトークンステータスの表示

SCIM トークンに対して行われたアクション/イベントのログを、\[監査トライアル] セクションから表示できます。 SCIMトークンの取りうるステータスは次のいずれかです。

- SCIMトークンが作成されました - SCIMトークンが作成されました。
- SCIMトークンが有効化されました - そのSCIMトークンは有効化されています。
- SCIMトークンが無効化されました - そのSCIMトークンは無効化されています。
- SCIMトークンが更新されました - そのSCIMトークンは更新されています。
- SCIMトークンが削除されました - そのSCIMトークンは削除されています。

\[詳細] カラムには、Azure、Oktaなど、SCIMベンダー名（IDP）も表示されるため、 Ivanti Neurons for MDMとの通信が容易になります。

## SCIMプロビジョニングにおける属性の構成

このセクションでは、ユーザープロビジョニング中における、IdP用のカスタム属性とエンタープライズ属性の作成方法を説明します。

## 属性のマッピング

接続が確立された後、IdPとIvanti Neurons for MDMとの間で属性をマッピングできます。 Ivanti Neurons for MDM では、以下のユーザー属性をサポートしています。

### コア属性

- id
- userName
- displayname
- active
- givenName
- familyName
- emails
  Entra ID IdPの場合は、外部IdPがサポートされています。

### 更新操作が許可される属性の一覧

- displayName
- emails
- givenName
- familyName
- active
- urn\:ietf\:params\:scim\:schemas\:extension\:ivanti:2.0\:User
- urn\:ietf\:params\:scim\:schemas\:extension\:enterprise:2.0\:User

### カスタム属性

**スキーマ** - urn\:ietf\:params\:scim\:schemas\:extension\:ivanti:2.0\:User:\<CustomAttribute123Name>

### エンタープライズ属性

現在、部署属性のみがサポートされています。

**スキーマ** - urn\:ietf\:params\:scim\:schemas\:extension\:enterprise:2.0\:User\:department
