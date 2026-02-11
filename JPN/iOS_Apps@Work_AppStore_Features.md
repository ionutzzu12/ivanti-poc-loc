---
title: iOS Apps@Work AppStore Features
createdAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
---

Apps\@Work タブには次の機能があります。

- [**Go アプリケーションから Apps@Work タブにアクセス**](./iOS_Apps@Work_AppStore_Features.md)から Apps\@Work タブにアクセス
- [**検索**](./iOS_Apps@Work_AppStore_Features.md)
- [**アプリのインストール - ボタン状態**](./iOS_Apps@Work_AppStore_Features.md)
- [**特集されたアプリケーションとバナー**](./iOS_Apps@Work_AppStore_Features.md)
- [**アプリケーション更新通知**](./iOS_Apps@Work_AppStore_Features.md)
- [**設定-デバイス**](./iOS_Apps@Work_AppStore_Features.md)

### Go アプリケーションから Apps\@Work タブにアクセス

**手順**

1. iOS デバイスから Go app にログインします。
2. **Apps\@Work** アイコンをタップします。\[すべてのアプリケーション] と \[カテゴリ] という2つの既定のタブを使用できます。

::Image[]{src="Resources/Images/All apps.png" signedSrc="Resources/Images/All apps.png" size="34" caption alt isUploading="false" sha initialPath="Resources/Images/All apps.png" githubPath="Resources/Images/All apps.png" position="flex-start" indent="2"}

3. **\[すべてのアプリ]** タブをタップします。 \[すべてのアプリケーション] リストにはすべてのアプリケーションがアルファベット順に表示されます。
4. **\[カテゴリ]** タブをタップします。 \[カテゴリ] タブには、アプリケーションが含まれるカテゴリのみが表示されます。\* 各カテゴリには存在するアプリケーションの数が表示されます。
   - \[カテゴリ] タブの下の \[アプリケーション] 行は、すべてのインストールされているアプリケーションが表示されたリスト項目です。 \[アプリケーション] 行は常に最初のカテゴリで、残りのカテゴリはアルファベット順に表示されます。
   - アプリケーションがインストールされていないと、MyApps リストに \[なし] と表示されます。
   - カテゴリをクリックすると、カテゴリに固有のすべてのアプリケーションが一覧表示され、\[インストール] オプションが表示されます。 **\[インストール]** をクリックして各アプリケーションを個別にインストールするか、**\[すべてインストール]** をクリックしてカテゴリのすべてのアプリケーションをインストールします。 各アプリケーションのインストールを許可するように指示されます。

### 検索

**手順**

::::WorkflowBlock
:::WorkflowBlockItem
iOS デバイスから Go app にログインします。
:::

:::WorkflowBlockItem
**Apps\@Work** アイコンをタップします。
:::

:::WorkflowBlockItem
検索 (レンズ) アイコンをタップすると、次を検索します。

- **新しいリリース**-検索バーにテキストを入力していないときに表示される新しくリリースされたアプリケーションの一覧

::Image[]{src="Resources/Images/Search.png" signedSrc="Resources/Images/Search.png" size="34" caption alt isUploading="false" sha initialPath="Resources/Images/Search.png" githubPath="Resources/Images/Search.png" position="flex-start" indent="2"}

- 文字を入力すると、検索フィールドで動的に予測され、一致するアプリケーションが表示されます。
- 検索結果件数は下位見出しとして表示されます。
- **\[インストール]** ボタンをタップすると、詳細ページに移動せずに、アプリケーションがインストールされます。

::Image[]{src="Resources/Images/Search results.png" signedSrc="Resources/Images/Search results.png" size="34" caption alt isUploading="false" sha initialPath="Resources/Images/Search results.png" githubPath="Resources/Images/Search results.png" position="flex-start" indent="2"}
:::
::::

### アプリのインストール - ボタン状態

アプリケーションのインストールでは、サーバが要求を処理し、アプリケーションをデバイスにプッシュする必要があるため、インストール ボタンにはリアルタイムの進行状況が表示されません インストール ボタンの状態は \[インストール] > \[要求済み] > \[インストール済み] に変わります。

**手順**

1. iOS デバイスから Go app にログインします。
2. **Apps\@Work** アイコンをタップします。
3. **\[インストール]** をタップすると、ステータス通知が次のように表示されます。\* 初めて、インストールが要求されたことを示すアラート メッセージが表示されます。
   - \[要求済み] ボタンをタップします。 アラート メッセージが表示されます。\[インストール済み] ステータスはボタンではありません。

::Image[]{src="Resources/Images/Search.png" signedSrc="Resources/Images/Search.png" size="34" caption alt isUploading="false" sha initialPath="Resources/Images/Search.png" githubPath="Resources/Images/Search.png" position="flex-start" indent="2"}

### 特集されたアプリケーションとバナー

\[特集] タブは管理者がプッシュした構成に基づいて表示されます。 \[特集] タブは、更新がないときの既定のランディング ページです。

![](<Resources/Images/Featured App.png>)

**手順**

1. iOS デバイスから Go app にログインします。
2. **Apps\@Work** アイコンをタップします。
3. **\[特集]** タブをタップします。\* 特集されたアプリケーション バナーにはバナーに1つのアプリケーションが表示されます。
   - 特集されたアプリケーションには、すべての特集されたアプリケーションが一覧表示されます。

::Image[]{src="Resources/Images/Featured Banner.png" signedSrc="Resources/Images/Featured Banner.png" size="37" caption alt isUploading="false" sha initialPath="Resources/Images/Featured Banner.png" githubPath="Resources/Images/Featured Banner.png" position="flex-start" indent="3"}

### アプリケーション更新通知

アプリケーション更新が利用可能になると、デバイスで通知が表示されます。 通知には利用可能な更新があるアプリケーションの数が表示されます。 通知をクリックすると、Apps\@Work が開きます。

**手順**

1. iOS デバイスから Go app にログインします。 Apps\@Work アイコンには、更新が保留中のアプリケーションの件数が表示されます。
2. アプリケーション更新通知をタップすると、Apps\@Workの \[すべてのアプリ] タブに移動します。 次の情報が表示されます。\* \[すべてのアプリケーション] タブの下の \[使用可能な更新] サブセクションには、更新可能なアプリケーションの件数が表示されます。
   - 更新が必要なすべてのアプリケーションに赤色のドット アイコンが表示されます。

::Image[]{src="Resources/Images/Updates.png" signedSrc="Resources/Images/Updates.png" size="100" caption alt isUploading="false" sha initialPath="Resources/Images/Updates.png" githubPath="Resources/Images/Updates.png" position="flex-start" indent="3"}

### 設定-デバイス

**手順**

1. iOS デバイスから Go app にログインします。
2. **\[設定]** アイコンをタップします。\* \[デバイス] タブは \[設定] の下にあります。
   - \[デバイス] は \[認証] の下の明細項目として表示されます。
