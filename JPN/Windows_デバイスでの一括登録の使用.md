---
title: Windows デバイスでの一括登録の使用
createdAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
---

一括登録機能では、Ivanti Neurons for MDM で複数のAndroidデバイスを迅速に登録できます。

**前提条件：**

- ユーザーアカウントを、Entra ID（Entra ID）Premiumアカウントを使用してIvanti Neurons for MDM上でインポートする必要があります。
- すべてのデバイスには [**Windows Configuration Designer**](https://docs.microsoft.com/en-us/windows/configuration/provisioning-packages/provisioning-install-icd) がインストールされている必要があります。

**手順：**

::::WorkflowBlock
:::WorkflowBlockItem
Ivanti Neurons for MDMとEntra IDテナントを関連付けます。[**Windows 10デバイスのためのEntra IDとUEMの連携**](./Microsoft_Azureの使用.md)を参照してください。
:::

:::WorkflowBlockItem
**\[Windows Configuration Designer]** アプリを使用して、**\[デスクトップデバイスのプロビジョニング]** を選択します。 画面で \[新しいプロジェクト] ウィンドウが表示されます。
:::

:::WorkflowBlockItem
以下の情報を入力します。
:::

:::WorkflowBlockItem
- 名前 - プロジェクトの一意の名前
- プロジェクト フォルダ - プロジェクトを保存するデバイスの場所
- 説明 - 任意のプロジェクトの説明
  **\[完了]** をクリックすると、\[新しいプロジェクト] ウィンドウが閉じ、一連のステップが実行されます。
:::

:::WorkflowBlockItem
**デバイスのセットアップ**

デバイスの一意の名前を入力します。 名前には、シリアル番号 (%SERIAL%) またはランダムな文字を含めることができます。
:::

:::WorkflowBlockItem
Windows をアップグレードしているか、共有するデバイスを構成しているか、プリインストール済みソフトウェアを削除している場合は、任意でプロダクトキーを入力できます。
:::

:::WorkflowBlockItem
**ネットワークの設定**

任意で、初回の起動時に、接続する Wi-Fi ネットワークデバイスを構成できます。 ネットワークデバイスが構成されていない場合は、デバイスの初回の起動時に、有線ネットワーク接続が必要です。
:::

:::WorkflowBlockItem
**アカウント管理**

**\[Entra IDで登録]** を選択し、**\[一括トークンの有効期限]** の日付を入力して、**\[一括トークンの取得]** をクリックします。
:::

:::WorkflowBlockItem
Entra ID認証資格情報を入力して、一括トークンを取得します。
:::

:::WorkflowBlockItem
**\[すべてのアプリのサインイン状態を維持]** ページで **\[いいえ。このアプリにのみサインイン]** をクリックします。
:::

:::WorkflowBlockItem
- 一括トークンが正常に取得されたら、\[次へ] をクリックして、パッケージを作成します。
- Azure ポータル - ユーザプリンシパル名 ([**package\_0ea893a5-1e93-4d21-a6b1-dc788946fd1d@miwinqe.onmicrosoft.com**](mailto\:package_0ea893a5-1e93-4d21-a6b1-dc788946fd1d@miwinqe.onmicrosoft.com) など) でユーザとプロビジョニング パッケージが作成されます。 ファイル (ランタイム ppkg ツール) をストレージデバイスにコピーします。
  一括トークンを作成するためのEntra IDユーザー。パッケージユーザーの多要素認証を有効にしないでください。 確認するには、そのユーザーについてOOBEとEntra ID Joinを実行する必要があります。

(Azure で作成された) パッケージ ユーザを作成し、Ivanti Neurons for MDM と同期します。
:::
::::

プロビジョニング パッケージに含まれるフラッシュドライブを使用して、デバイスを一括登録します。 既存のデバイスをダブルクリックすると、OOBE 後のエクスペリエンスを実行することもできます。 最初の試行でパッケージをインストールできなかった場合は、2 回目の試行も失敗します。 新しいデバイスがIvanti Neurons for MDMで作成されており、Entra IDがパッケージユーザーに属しているかどうかを確認してください。
