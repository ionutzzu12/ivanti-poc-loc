---
title: Windowsハードウェアのポリシー
createdAt: Wed Feb 11 2026 17:32:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:27 GMT+0200 (Eastern European Standard Time)
---

通常のハードウェアインベントリチェックを継続することにより、ハードウェアアイテムがWindows 10デバイスに追加、コピー、削除、置換、または移動されたかを判断します。 Windowsハードウェアポリシーでは、監視するハードウェアの種類を指定し、デバイス上のハードウェアに変更が検出されたときに実行するアクションを選択できます。

1. **\[ポリシー]** に進みます。
2. **\[+追加]** をクリックします。
3. **\[Windowsハードウェア]** を選択します。
4. ハードウェアポリシーに名前を付けます。
5. 必要であれば **\[+説明を追加]** をクリックして詳細を追加します。
6. **\[ハードウェアルールを定義]** セクションで、以下のオプションを構成します。

| オプション            | 説明                                    |
| ---------------- | ------------------------------------- |
| **ハードウェアオブジェクト** | 以下のオプションからハードウェアの種類を選択します。\* **BIOS** |

:::Paragraph{listStyleType="disc" indent="2"}
**ハードウェアドライブ**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**CD-ROMドライブ**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**プロセッサ**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**物理メモリ**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
\| **変更イベント**       | チェックするハードウェアイベントの種類を選択します。\* **追加**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**コピー**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**削除**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**置換**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**移動**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
\| **アクションを選択**     | 実行されるアクションの種類を選択します。\* **何もしない**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**通知を送信**：以下のオプションのいずれかを選択します。\* **メール通知を送信** - **\[メールメッセージ]** セクションに件名と本文を入力し、通知を送信します。
:::

:::Paragraph{listStyleType="disc" indent="3"}
**プッシュ通知を送信** - プッシュ通知メッセージを入力します。
:::

:::Paragraph{listStyleType="disc" indent="3"}
**両方を送信** - メールメッセージとプッシュ通知メッセージを入力します。
:::

:::Paragraph{listStyleType="disc" indent="2"}
**待機**：ドロップダウンリストから待機する日数/時間を選択します。\* **日数は\*\*\*\*1**～**31**の範囲。
:::

:::Paragraph{listStyleType="disc" indent="3"}
**時間は\*\*\*\*1**～**24**の範囲。
:::

:::Paragraph{listStyleType="disc" indent="2"}
**検疫** - 以下の検疫オプションのいずれかを選択します。**任意の追加検疫アクション**\* **マネージドアプリを隔離** - **\[すべてのアプリケーション]** または **\[指定したアプリケーション]** を選択します（\[検索] フィールドでアプリ名を検索して選択）。
:::

:::Paragraph{listStyleType="disc" indent="3"}
**新規アプリダウンロードをブロック** - デバイスへのアプリのダウンロードをブロックします。 **\[すべてのアプリケーション]** または **\[指定したアプリケーション]** を選択します（\[検索] フィールドでアプリ名を検索して選択）。
:::

:::Paragraph{listStyleType="disc" indent="3"}
**構成を削除** - デバイスから構成を削除します。 **\[すべての構成]** または **\[指定した構成]** を選択します（\[検索] フィールドで構成を検索して選択）。
:::

:::Paragraph{listStyleType="disc" indent="3"}
**コンテンツを削除** - 配布されたアプリに関連するすべてのコンテンツをデバイスから削除します。**デフォルトの検疫アクション**\* **アプリストアへのアクセスをブロック**
:::

:::Paragraph{listStyleType="disc" indent="3"}
**コンテンツストアへのアクセスをブロック**
:::

:::Paragraph{listStyleType="disc" indent="3"}
**AppConnectをブロック**
:::

:::Paragraph{listStyleType="disc" indent="3"}
**AppTunnelをブロック**
:::

:::Paragraph{listStyleType="disc" indent="3"}
**ActiveSyncをブロック**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**ブロック**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**撤去**このアクションは元に戻せません。コンプライアンスアクションを追加または削除するには、「プラス」または「マイナス」のアイコンをクリックします。 |
**\[次へ]** をクリックします。
:::

8. 以下の配布オプションから1つ選択します。\* **すべてのデバイス**
   - **デバイスなし（デフォルト）**
   - **カスタム**
9. **\[完了]** をクリックします。
