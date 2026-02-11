---
title: [管理] - [Android Enterprise]
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

ライセンス：Silver

- Android Enterprise 対応の Ivanti, Inc 生産性アプリ (Email+、Docs\@Work、Web\@Work など) は Gold ライセンスが必要です。
- Tunnel for Android Enterprise には Platinum ライセンスが必要です。

Android Enterprise では、Android Enterprise アプリの使用と構成が可能です。 Android Enterprise ユーザは、アプリ カタログと Google Play からアプリを表示してインストールできます。

新しいお客様の場合は、アプリ配布がデフォルトで「デバイス単位」に設定されています。 この設定は変更できません。 アップグレードのお客様の場合は、アプリ配布を「ユーザー単位」と「デバイス単位」からお選びいただけます。 デフォルトの選択は「ユーザー単位」です。 多くのユーザーは複数のデバイスを持っています。 ユーザーが複数のデバイスを持っている場合、アプリ配布を「デバイス単位」にすると、各デバイスに異なるアプリ群を配布できます。

このセクションは以下のトピックを含みます。

- [**Android Enterpriseの構成**](./\[管理]_-_\[Android_Enterprise].md)
- [**Android Enterprise仕事用プロファイルの構成**](./\[管理]_-_\[Android_Enterprise].md)

## Android Enterpriseの構成

::::WorkflowBlock
:::WorkflowBlockItem
Ivanti Neurons for MDM ポータルで、**\[管理] > \[Google] > \[Android Enterprise]** をクリックします。
:::

:::WorkflowBlockItem
以下のオプションから1つ選択してください。
:::

:::WorkflowBlockItem
- **マネージド Google Play アカウント:** G Suite を利用していない企業の場合、ユーザは個人情報 (Google の電子メールアドレス) を送信せずに、Android Enterprise に登録できます。 Ivanti Neurons for MDM はGoogleで自動的にユーザーをプロビジョニングし、管理します。 管理者は、管理者用GoogleアカウントでAndroidエンタープライズを許可するよう求められます。
- **マネージド Google アカウント:** G Suite を利用している企業の場合、ユーザは Android Enterprise に登録できます。 各ユーザは、Android Enterprise を登録するために Google アカウントが必要です。
  画面上の指示に従い、構成プロセスを完了します。
:::

:::WorkflowBlockItem
自動方式では以下のようになります。

- UEM APIを有効化し、企業認証情報を作成します。
- 統合の所有者を許可することでGoogleに登録します。 これは個人アカウントではなくIT部門のアカウントにしてください。
- サービスアカウント（JSONクライアントID）をドラッグ＆ドロップし、認証情報を設定します。
  オルタネート方式では以下のようになります。
- 以下のセクションのクライアント ID を参照し、Google 管理に追加します。
- Google 管理の MDM トークンと、Google Cloud コンソールのサービス アカウントを検索します。
- Ivanti Neurons for MDM で、MDM トークン、エンタープライズ Google ドメイン、企業管理者の電子メールアドレスを入力し、Google サービスに接続します。
- Ivanti Neurons for MDM で、サービス アカウント JSON クライアント ID をドラッグアンドドロップします。
- Ivanti Neurons for MDM で **\[認可]** をクリックし、Ivanti Neurons for MDM で Google ユーザを表示、管理することを許可します。
:::
::::

Ivanti Neurons for MDM ユーザーインターフェイスガイドに従って以下の手順を実行します。

### Ivanti Neurons for MDM を管理された Google アカウントとバインドするためのクライアント ID

管理コンソールで、クライアント ID 「**140561810807-tiiglke17laibbrt5darupmvo4ae7cbj.apps.googleusercontent.com**」を追加し、Ivanti Neurons for MDM テナントと管理された Google アカウントをバインドします。

## Android Enterprise仕事用プロファイルの構成

1. Ivanti Neurons for MDM ポータルで **\[構成]** に移動します。
2. **\[+追加]** をクリックします。
3. **\[ロックダウン＆キオスク：Android Enterprise]** 構成を選択します。
4. 構成名と説明を入力します。
