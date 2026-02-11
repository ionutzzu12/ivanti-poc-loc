---
title: Azureテナントのプロビジョニング解除
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

複数の Ivanti Neurons for MDM で同じ Azure テナントを使用できる場合は、すべての Ivanti Neurons for MDM からプロビジョニング解除します。 1つの Ivanti Neurons for MDM によるAzure使用を停止する場合は、その Ivanti Neurons for MDM 専用のパートナーコンプライアンスポリシーから無効化が可能です。

管理者が Ivanti Neurons for MDM で連携解除を実行すると、Ivanti Neurons for MDM はAzureへのデバイスインベントリおよびコンプライアンス状態の報告を停止します。

前提条件

- すべてのデバイスを非マネージドにする
- すべてのデバイスをコンプライアンス違反にする

手順

### Microsoft

1. Microsoft Azureにログインします。
2. \[Intune] > \[条件付きアクセス] を開きます。 条件付きアクセスが無効であることを確認します。

### Ivanti Neurons for MDM

1. Ivanti Neurons for MDM にログインし、\[管理] に移動します。
2. 左側のメニューで \[Microsoft Azure] > \[iOS/Androidのデバイスコンプライアンス] をクリックします。
3. \[アカウントの連携解除] をクリックします。

::Image[]{src="Resources/Images/AAD_Deprov_confirm.png" signedSrc="Resources/Images/AAD_Deprov_confirm.png" size="36" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_Deprov_confirm.png" githubPath="Resources/Images/AAD_Deprov_confirm.png" position="flex-start" indent="2"}

4. \[はい] をクリックします。

### Azureからのデバイス撤去

デバイスを撤去すると、Ivanti Neurons for MDM はAzureにデバイスがもはや管理下になく、コンプライアンスが確保されていないことを報告します。

Azureは撤去済みデバイスの情報を90日後に削除します。

### ログに記録されたAzureアカウントアクティビティ

すべてのアクティビティはログに記録されます。

![](Resources/Images/AAD_logs.png)
