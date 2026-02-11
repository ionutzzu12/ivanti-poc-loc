---
title: デバイスユーザーへのIntuneライセンス適用
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

- 以下の場合は使用しないでください：\* ユーザーを変更する予定がある、またはユーザーが変わる可能性の高い状況を管理している
  - 1台のデバイスが複数のユーザーに所有されている
- Ivantiは、以下のようなマルチユーザーデバイスに \[ユーザーに割り当てる] を実行したり、デバイスコンプライアンス構成を配布したりしないことを推奨します。- セキュアサインインWebクリップのあるデバイス
  - 共有iPadデバイス
  - Androidキオスクモードのデバイス

## Ivanti Neurons for MDM ライセンス要件

デバイスコンプライアンスはPremiumサービスとしてSecure UEM PremiumおよびPlatinumのユーザーに提供されています。 既存のお客様はPlatinumライセンスで十分です。

## デバイスユーザーへのライセンス一括割り当て

既存のデバイスユーザーにライセンスを一括で割り当てるには：

### グループベースの割り当て

[**https://docs.microsoft.com/ja-jp/azure/active-directory/users-groups-roles/licensing-groups-assign**](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/licensing-groups-assign)

### PowerShell ベースの割り当て

[**https://docs.microsoft.com/ja-jp/microsoft-365/enterprise/assign-licenses-to-user-accounts-with-microsoft-365-powershell?view=o365-worldwide**](https://docs.microsoft.com/en-us/microsoft-365/enterprise/assign-licenses-to-user-accounts-with-microsoft-365-powershell?view=o365-worldwide)
