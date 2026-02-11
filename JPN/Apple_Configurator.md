---
title: Apple Configurator
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

このページを使用して、iOSデバイス上で Ivanti Neurons for MDM デバイス管理をセットアップするためのApple Configuratorを準備することができます。 Apple Configuratorは大規模のiOSデバイスの展開を非常に容易にします。 さらに、Configuratorでは管理者がiOSデバイスを監視対象にすることができ、これによりレベルの高い構成および管理機能を可能にします。 Apple Configuratorの詳細は、Mac App Storeをご覧ください。

基本的な手順は次のとおりです。

1. Ivanti Neurons for MDM テナントから MDM プロファイルをエクスポートします。
2. ConfiguratorにMDMプロファイルをインポートします。
3. Configuratorを使用し、テザードされたデバイスにMDMプロファイルを適用します。

## デバイスのデフォルトユーザーの定義

Apple Configuratorで構成されたデバイスは、別のユーザーを選択しない限り、Ivanti Neurons for MDM ではnobodyユーザーに割り当てられます。

1. **\[構成されたデバイスを以下に割り当てる]** フィールドをクリックします。
2. 選択したい Ivanti Neurons for MDM ユーザーのユーザー名を入力し始めます。
3. ユーザー名がドロップダウンリストに表示されたら選択します。
4. **\[保存]** をクリックします。

## Apple Configuratorを使用したアプリのインストール

Apple Configuratorを使用してアプリをインストールする前に：

- Apple App Storeへのアクセスは、デバイス構成によって制限されています。
- アプリのインストールは、デバイス構成によって許可されています。
- デバイス構成に使用するコンピュータ上に、Apple Configuratorがインストールされている必要があります。

Apple Configuratorを使用してアプリをインストールするには：

::::WorkflowBlock
:::WorkflowBlockItem
Ivanti Neurons for MDM で **\[管理] > \[Apple Configurator]** を選択します。
:::

:::WorkflowBlockItem
登録デバイス切換を \[オン] にします。
:::

:::WorkflowBlockItem
次のいずれかをクリックします。
:::

:::WorkflowBlockItem
- **デフォルトユーザーのplist**
- **特定ユーザーのplist** - 特定ユーザーのユーザー名またはメールIDを入力します。
  Apple Configuratorで、**\[準備] > \[アプリ]** を開きます。
:::

:::WorkflowBlockItem
**\[準備] > \[設定] を開き、\[監視] を無効化します**。
:::

:::WorkflowBlockItem
\[iOSのアップデート] で、**\[デバイスをアップデートしない]** を選択します。
:::

:::WorkflowBlockItem
**\[準備]**（Apple Configuratorの下）をクリックします。デバイスにチェックインすると、デバイス上のインストール済みアプリのリストにアプリが表示されるようになります。
:::
::::

## UEMサーバーを使用したアプリのインストール

UEMサーバーを使用してアプリをインストールするには：

1. \[アプリ] タブの社内ストアからアプリをアップロードします。
2. アプリを選択します。
3. **\[アプリ構成]** タブをクリックします。
4. **\[デバイスにインストール]** を選択します。構成設定を完了させます。
5. **\[アクション] > \[チェックインの強制]** を選択します。

## エンドユーザーが実行すべき内容

Appleの場合、エンドユーザーが一度Goを起動する必要があります。この操作を行わないと、Ivanti Neurons for MDM 位置情報機能が正しく動作しません。 これは、エンドユーザーに自分の位置が追跡されるということを認識してもらうための措置です。

**注：**&#x43;onfiguratorを使用してデバイスをSingle Appモードで展開している場合は、このアプローチは実行できません。

**\[Apple Configuratorのインストール]** ページが表示されない場合、必要な権限を持っていない可能性があります。 以下のいずれかの[**役割**](./ユーザーの役割.md)が必要です。

- システム管理
- 読み取り専用システム
