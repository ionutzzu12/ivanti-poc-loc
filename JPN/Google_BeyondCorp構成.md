---
title: Google BeyondCorp構成
createdAt: Wed Feb 11 2026 17:32:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:27 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM をGoogleのBeyondCorpと統合して、条件付きアクセスを実現できます。 Ivanti Neurons for MDMは、GoogleのBeyondCorpにデバイス コンプライアンス ステータス信号を送信します。 これにより、N-MDM下の準拠デバイスのみがGoogleワークスペースのアプリケーションにアクセスできることが保証されます。

前提条件

- Ivanti Neurons for MDMに関しては、Ivanti Professional Plus / Premiumライセンスが必要です。
- Googleに関しては、BeyondCorp Enterpriseライセンス、Google Workspace Enterpriseライセンス、またはCloud Identity Premiumライセンスが必要です。

手順（Google）

1. 管理者の認証情報で**Google管理コンソール**にログインします。
2. **\[デバイス]** > **\[モバイルとエンドポイント]** > **\[設定]** > **\[サードパーティ統合]** を開きます。

::Image[]{src="Resources/Images/googlebc1.png" signedSrc="Resources/Images/googlebc1.png" size="27" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc1.png" githubPath="Resources/Images/googlebc1.png" position="flex-start" indent="2"}

3. **\[セキュリティ パートナーとMDMパートナー]** > **\[管理]** をクリックします。

::Image[]{src="Resources/Images/googlebc2.png" signedSrc="Resources/Images/googlebc2.png" size="26" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc2.png" githubPath="Resources/Images/googlebc2.png" position="flex-start" indent="2"}

4. **\[パートナー接続を管理]** ウィンドウで **\[Ivanti]** を選択します。

::Image[]{src="Resources/Images/googlebc3.png" signedSrc="Resources/Images/googlebc3.png" size="23" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc3.png" githubPath="Resources/Images/googlebc3.png" position="flex-start" indent="2"}

5. **\[接続を開始]** をクリックします。Ivanti Neurons for MDM のログインページにリダイレクトされますので、テナント管理者の認証情報を入力します。 テナントにログインすると、**Google BeyondCorp**が有効になっており、お使いのGoogleアカウントに自動的にリンクされていることがわかります。
6. Google管理コンソールで、**\[セキュリティ]** > **\[コンテキストアウェア アクセス]** > **\[アクセスレベル]** を開きます。

::Image[]{src="Resources/Images/googlebc5.png" signedSrc="Resources/Images/googlebc5.png" size="28" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc5.png" githubPath="Resources/Images/googlebc5.png" position="flex-start" indent="2"}

7. **\[アクセスレベルを作成]** をクリックします。\[アクセスレベルを作成] ウィンドウのコンテキスト条件セクションで、**\[詳細]** をクリックし、必要な情報を入力します。

::Image[]{src="Resources/Images/googlebc7.png" signedSrc="Resources/Images/googlebc7.png" size="28" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc7.png" githubPath="Resources/Images/googlebc7.png" position="flex-start" indent="2"}

8. **\[セキュリティ]** > **\[コンテキストアウェア アクセス]** > **\[アクセスレベル]** を開き、ポリシーを割り当てるアプリケーションを選択します。

::Image[]{src="Resources/Images/googlebc9.png" signedSrc="Resources/Images/googlebc9.png" size="28" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc9.png" githubPath="Resources/Images/googlebc9.png" position="flex-start" indent="2"}

9. **\[割り当てる]** をクリックします。
10. **\[アクセスレベルの選択]** ウィンドウで、割り当てるポリシーを選択し、**\[保存]** をクリックします。

::Image[]{src="Resources/Images/googlebc11.png" signedSrc="Resources/Images/googlebc11.png" size="28" caption alt isUploading="false" sha initialPath="Resources/Images/googlebc11.png" githubPath="Resources/Images/googlebc11.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
上記の設定が完了すると、**Google BeyondCorp**を使用してパートナーデバイスコンプライアンス構成を作成できます。
:::

**手順（**&#x49;vanti Neurons for MD&#x4D;**）**：

1. **\[構成]** > **\[構成を追加]** を開きます。
2. **\[パートナーデバイスコンプライアンス]** 構成を選択します。
3. 画面に \[パートナーデバイスコンプライアンス構成の作成] ページが表示されます。
   構成の名前を入力します。
4. \[パートナーの選択] リストで **\[Google BeyondCorp]** を選択します。
5. \[構成設定] セクションが画面に表示されます。 \[iOSおよびAndroidデバイスについてコンプライアンスステータスをレポートします] オプションがオンに設定されていることを確認します。
   **\[次へ]** をクリックします。
6. **\[この構成を有効化]** を選択します。
7. 配布オプションとして **\[カスタム]** を選択します。
8. **\[カスタム配布]** オプションで **\[ユーザー/ユーザーグループ]** を選択します。
9. **\[下記を選択してこの構成を配布]** セクションのリストからユーザー/ユーザーグループを選択します。
10. **\[完了]** をクリックします。
