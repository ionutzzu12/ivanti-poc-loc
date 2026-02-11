---
title: Appleアプリカタログ
createdAt: Wed Feb 11 2026 17:32:26 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:26 GMT+0200 (Eastern European Standard Time)
---

**対象：**&#x69;OSとmacOS

Appleアプリカタログ構成は、Webクリップ経由でのAppleアプリカタログへのアクセスを管理します。 Ivanti Neurons for MDM リリース83以降では、Go アプリケーションから Apps\@Work ネイティブ エクスペリエンスに移行できます。 新しく作成されたテナントでは、既定では、Apps\@work Webclip 構成は iReg またはクライアントからインストールされた iOS デバイスに配布されません。 管理者は、iReg またはクライアントから登録されたデバイスに手動で webclip 構成を配布する必要があります。

iOSデバイスとiPadデバイスでは、検索要求の行パラメータが10を超えていても、Apps\@Work Webクリップの検索結果には、10個のアプリケーションのみが表示されます。

**手順**

管理者は、このシステム定義の構成を以下の手順で編集できます。

::::WorkflowBlock
:::WorkflowBlockItem
**\[構成]** に進みます。
:::

:::WorkflowBlockItem
**\[Appleアプリカタログ]** をクリックします。
:::

:::WorkflowBlockItem
**\[配布を編集]** をクリックします。
:::

:::WorkflowBlockItem
以下の配布オプションから1つ選択します。
:::

:::WorkflowBlockItem
- 全デバイス - 互換性のあるすべてのデバイスが、この構成の送信を受けます。
- デバイスなし - Appleアプリカタログへのアクセスを無効化するか、この構成を今後の配布用にします。
- カスタム - この構成の送信を受ける特定のデバイスグループを定義します。
  **\[保存]** をクリックします。
:::
::::
