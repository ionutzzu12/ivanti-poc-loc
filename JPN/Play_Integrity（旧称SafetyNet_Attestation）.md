---
title: Play Integrity（旧称SafetyNet Attestation）
createdAt: Wed Feb 11 2026 17:32:26 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:26 GMT+0200 (Eastern European Standard Time)
---

Play Integrity（旧称SafetyNet）は、GoogleのPlay Integrity APIを使用したAndroidデバイスのセキュリティと互換性の評価に役立ちます。 構成した場合、一定期間後にデバイスを分析することで、デバイスが改ざんされているかどうかを判断できます。

Play Integrityは、すべてのAndroidバージョンでサポートされるようになりました。

**手順**

::::WorkflowBlock
:::WorkflowBlockItem
**\[構成]** タブで **\[+追加]** をクリックします。
:::

:::WorkflowBlockItem
**\[Play Integrity]**&#x69CB;成を選択します。 **\[Play Integrity構成]** ページが表示されます。
:::

:::WorkflowBlockItem
**\[名前]** フィールドに、Play Integrity構成の適切な名前を入力します。
:::

:::WorkflowBlockItem
+\[**説明を追加**] リンクをクリックし、構成の説明を追加します。 このフィールドはオプションです。
:::

:::WorkflowBlockItem
**\[構成設定]** セクションで、デバイスでセキュリティおよび互換性チェックを評価するために適用される最小間隔 (時間) を入力します。値は 1 ～ 24 の範囲です。
:::

:::WorkflowBlockItem
**\[次へ]** をクリックして以下の配布オプションから1つ選択します。
:::

:::WorkflowBlockItem
- すべてのデバイス
- デバイスなし（デフォルト）
- カスタム
  **\[完了]** をクリックします。
:::
::::

Play Integrity nonceとSafetyNet nonceがデバイスに送信される場合は、SafetyNet nonceよりもPlay Integrity nonceが優先されます。
