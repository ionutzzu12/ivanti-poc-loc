---
title: コンプライアンスパートナーとしてのMobileIronの追加
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

**前提条件**

- Microsoft Intuneライセンスをインストールしている。 [**デバイスユーザーへのIntuneライセンス適用**](./デバイスユーザーへのIntuneライセンス適用.md)を参照してください。
- Microsoft Azureでユーザーを作成している。
- Microsoft Azureでグループを作成している。

手順

1. ログインします：[**https://endpoint.microsoft.com**](https://endpoint.microsoft.com/)
2. Microsoft Endpoint Manager管理センターの左側のメニューから \[テナント管理] をクリックします。 \[コネクタとトークン] > \[パートナーコンプライアンス管理] をクリックします。

::Image[]{src="Resources/Images/AAD_Add MI as comp partner_01.png" signedSrc="Resources/Images/AAD_Add MI as comp partner_01.png" size="54" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_Add MI as comp partner_01.png" githubPath="Resources/Images/AAD_Add MI as comp partner_01.png" position="flex-start" indent="2"}

1. 検索フィールドの右側にある \[+コンプライアンスパートナーを追加] をクリックします。

::Image[]{src="Resources/Images/AAD_Add MI as comp partner_02.png" signedSrc="Resources/Images/AAD_Add MI as comp partner_02.png" size="65" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_Add MI as comp partner_02.png" githubPath="Resources/Images/AAD_Add MI as comp partner_02.png" position="flex-start" indent="2"}

1. \[基本] タブで \[コンプライアンスパートナー] フィールドのドロップダウンから \[MobileIron Device Compliance Cloud] を選択します。

::Image[]{src="Resources/Images/AAD_compliance partner.png" signedSrc="Resources/Images/AAD_compliance partner.png" size="70" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_compliance partner.png" githubPath="Resources/Images/AAD_compliance partner.png" position="flex-start" indent="2"}

1. \[プラットフォーム] フィールドでiOSまたはAndroidを選択し、\[次へ] をクリックします。
2. \[割り当て] タブをクリックします。 \[割り当て先] ドロップダウンでコンプライアンスステータスを指定するユーザーまたはデバイスユーザーグループを選択します。 ライセンスを持つユーザー/グループを選択します。

::Image[]{src="Resources/Images/AAD_Add MI as comp partner_04.png" signedSrc="Resources/Images/AAD_Add MI as comp partner_04.png" size="19" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_Add MI as comp partner_04.png" githubPath="Resources/Images/AAD_Add MI as comp partner_04.png" position="flex-start" indent="2"}

1. \[次へ] を選択します。
2. \[作成] をクリックします。 新しいコンプライアンスパートナーが \[パートナーコンプライアンス管理] ページに表示されます。

::Image[]{src="Resources/Images/AAD_completed Conn with Azure.png" signedSrc="Resources/Images/AAD_completed Conn with Azure.png" size="63" caption alt isUploading="false" sha initialPath="Resources/Images/AAD_completed Conn with Azure.png" githubPath="Resources/Images/AAD_completed Conn with Azure.png" position="flex-start" indent="2"}
