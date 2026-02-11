---
title: Azure Tenant Requirements
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

本セクションではMicrosoft Azureテナントにおける Ivanti Neurons for MDM の設定方法を説明します。

## 要件

### Microsoft

Ivanti Neurons for MDM のお客様は、Microsoft Intuneの有効なサブスクリプションを持ち、デバイスユーザーにMicrosoft Intuneライセンスを割り当てる必要があります。

### MobileIron

- Ivanti Neurons for MDM - MobileIron でサポートされる Ivanti Neurons for MDM バージョン 75 から最新のバージョン。
- 追加ライセンス - デバイスコンプライアンスはPremiumサービスとして[**Secure UEM Premium**](https://www.mobileiron.com/en/pricing#)およびPlatinumのユーザーに提供されています。 既存のお客様はPlatinumライセンスで十分です。
- Go for iOS（クライアント）またはGo for Android（クライアント）バージョン75.0からMobileIronがサポートする最新版まで。

### 複数の Ivanti Neurons for MDM サポート

複数の Ivanti Neurons for MDMを同じAzureテナントに連携している場合は、すべてのIvanti Neurons for MDMと連携を解除するか、特定の（1つの）Ivanti Neurons for MDMからEntra IDコンプライアンス統合のコンプライアンスポリシーを無効化することで、デバイスデータがAzureにアップロードされないようにします。

Ivanti Neurons for MDM の連携を解除する前に必ずコンプライアンスポリシーを無効化してください。

## Ivanti Neurons for MDM 管理者プロセス

Ivanti Neurons for MDM 管理者の視点から見た手順：

1. 管理者がデバイスユーザーにIntuneライセンスを適用します。 [**デバイスユーザーへのIntuneライセンス適用**](./デバイスユーザーへのIntuneライセンス適用.md)を参照してください。
2. 管理者がAzureポータルにログインします。
3. 管理者がAzureコンプライアンスパートナーとしてMobileIronを追加します。 [**コンプライアンスパートナーとしてのMobileIronの追加**](./コンプライアンスパートナーとしてのMobileIronの追加.md)を参照してください。
4. 管理者がアプリの条件付きアクセスポリシーを作成します。 [**Microsoft Endpoint Managerにおける条件付きアクセスポリシーの作成**](./Microsoft_Endpoint_Managerにおける条件付きアクセスポリシーの作成.md)を参照してください。
5. 管理者がMobileIronとAzureの連携を設定します。 [**Microsoft Azure の接続 Ivanti Neurons for MDM**](./Microsoft_Azure_の接続_Ivanti_Neurons_for_MDM.md)をご参照ください。
6. 管理者が Ivanti Neurons for MDM でデバイスコンプライアンスポリシーを作成します。 [**パートナーデバイスコンプライアンスポリシーの作成**](./パートナーデバイスコンプライアンスポリシーの作成.md)を参照してください。
7. 条件付きアクセスポリシーが有効になります。 デバイスのコンプライアンス状況により、アプリへのアクセスが許可または却下されます。Ivantiは管理者が各Microsoftアプリでテストを実行することを推奨します。
