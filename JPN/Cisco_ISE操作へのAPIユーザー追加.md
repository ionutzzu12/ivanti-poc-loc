---
title: Cisco ISE操作へのAPIユーザー追加
createdAt: Wed Feb 11 2026 17:32:24 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:24 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDMでCisco ISEがCisco ISE APIと対話できるようにする「Cisco ISE操作」役割を持つAPIユーザーを追加できます。 このユーザーを作成した後、このユーザーのCisco ISE内での認証情報を使用して、Ivanti Neurons for MDMに対するAPI呼び出しを認証します。 これらのAPI呼び出しにより、Cisco ISEは、デバイス情報の取得、デバイスに対するフル/コーポレートワイプやPINロックなどの操作実行、デバイスへのメッセージ送信を実行できます。

APIユーザーは管理ポータルにログインできません。 APIの使用を許可するだけです。

デフォルトでは、テナントのスーパー管理者のみが 「Cisco ISE操作」の役割を持ちます。 スーパー管理者は、この役割を持つべき他のユーザーをシステム内で明示的に選択し、役割を割り当てる必要があります。 その後、\[Cisco ISE操作] の役割に割り当てられたユーザーが、システム内でその他の適切なユーザーにこの役割を割り当てます。

**手順**

::::WorkflowBlock
:::WorkflowBlockItem
**\[ユーザー]** タブをクリックします。
:::

:::WorkflowBlockItem
:inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/02ZqyRvJVRvheYEa9MJE5_r36addapiuser001.png" alt caption}
**\[追加]** をクリックします。
:::

:::WorkflowBlockItem
**\[APIユーザー]** を選択します。
:::

:::WorkflowBlockItem
表示されるフォームにユーザーの情報を入力します：
:::

:::WorkflowBlockItem
- Eメールアドレス
- 名
- 性
  \[ユーザー名] フィールドには入力したEメールアドレスが表示されます。 ほとんどの場合、このデフォルトは変更しないでください。 [**\[ユーザー名編集のタイミング\]**](./ユーザー名の編集.md) を参照してください。

このユーザーの表示名を変更したい場合は、**\[表示名]** フィールド内のデフォルトテキストを編集します。
:::

:::WorkflowBlockItem
**\[パスワード]** と **\[パスワードを確認]** フィールドに入力してパスワードを指定します。
:::

:::WorkflowBlockItem
**\[役割を割り当てる]** セクションで選択されてい&#x308B;**&#x20;\[API管理Cisco ISE操作]** の役割をそのままにします。
:::

:::WorkflowBlockItem
**\[完了]** をクリックするとユーザーが追加されます。
:::
::::

**\[ユーザー]** ページでタスクを実行できない場合、必要な権限を持っていない可能性があります。 以下のいずれかの[**役割**](./ユーザーの役割.md)が必要です。

- システム管理
- ユーザー管理
