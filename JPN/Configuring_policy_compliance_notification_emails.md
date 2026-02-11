---
title: Configuring policy compliance notification emails
createdAt: Wed Feb 11 2026 17:32:24 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:24 GMT+0200 (Eastern European Standard Time)
---

## ポリシーコンプライアンス通知メールの構成と使用

管理者は、ポリシーコンプライアンス通知メールテンプレートに、カスタム/許可されたアプリ ポリシーのメール送信アクションがコンプライアンス違反のデバイスを持つユーザーに送信するメールをラップすることができます。 以下のプロセスで構成を説明します：

- **機能の構成：**\* **メールテンプレートを構成します。**&#x82F1;語のメールテンプレートはデフォルトで以下のようになっていますが、[**メールテンプレートのブランディング**](./メールテンプレートのブランディング.md)の[**メールテンプレートのカスタマイズ**](./メールテンプレートのブランディング.md)に記載された指示に従い、目的に合わせて変更が可能です、

::Image[]{src="Resources/Images/68PolicyEmailTemplate.png" signedSrc="Resources/Images/68PolicyEmailTemplate.png" size="41" caption alt isUploading="false" sha initialPath="Resources/Images/68PolicyEmailTemplate.png" githubPath="Resources/Images/68PolicyEmailTemplate.png" position="flex-start" indent="2"}

:::Paragraph{listStyleType="disc" indent="2"}
**ポリシーコンプライアンス通知テンプレートをオンにします。** このテンプレートは、カスタム/許可されたアプリ ポリシーのメール送信アクションを使用して作成するメッセージとともに機能します。 Ivanti Neurons for MDM は、メールアクションに指定した情報をポリシーコンプライアンス通知テンプレートに挿入します。 ポリシーコンプライアンスメールテンプレートは、カスタム/許可されたアプリ ポリシーの作成または編集時にオンにすることができます。 カスタムポリシーまたは許可されたアプリのポリシーコンプライアンス通知テンプレートを有効化する方法については、[**カスタムポリシーの追加**](./カスタムポリシー.md)と[**許可されたアプリ ポリシーの作成**](./許可されたアプリの監視と制御.md)をそれぞれ参照してください。
:::

- **機能の使用：**\* ポリシー通知テンプレートを有効化した状態で、デバイスがカスタム/許可されたアプリ ポリシーのコンプライアンス違反になった場合、Ivanti Neurons for MDM は、ポリシー通知テンプレートにメールをラップした上で、デバイス所有者にメールを送信します。 この機能を使用するのは Ivanti Neurons for MDM ですが、ユーザーが上記のように機能を設定してください。
