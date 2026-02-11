---
title: Microsoft Azureの使用
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

Microsoft Azureを使用してIvanti Neurons for MDMを設定すると、Windows 10を実行するWindowsデスクトップとタブレットを使用するユーザーをシームレスに登録できます。 以下の手順に従い、インスタンスの構成と接続を行ってください。

このセクションは以下のトピックを含みます。

- [**Entra IDアカウントの設定**](./Microsoft_Azureの使用.md)
- [**Windows 10デバイスのためのEntra IDとUEMの連携**](./Microsoft_Azureの使用.md)
- [**Windowsデバイスにおけるマルチユーザーサポート**](./Microsoft_Azureの使用.md)

## Entra IDアカウントの設定

Entra IDを設定するには：

1. [**https://azure.microsoft.com/en-in/pricing/purchase-options/**](https://azure.microsoft.com/en-in/pricing/purchase-options/) を開き、Azureアカウントを購入します。
2. 既存のHotmailまたはOutlook.comアカウントを使用するか、新規アカウントを作成し、新規ユーザーとして登録します。
3. いずれかの支払オプションを使用し、検証手順に従って、Azureアカウントを購入します。
4. Ivanti Neurons for MDM テナントを許可リストに追加するように Microsoft に依頼します。
5. 手順2で使用したのと同じHotmailアカウントまたはOutlook.comアカウントを使用してEntra ID（[**https://manage.windowsazure.com/**](https://manage.windowsazure.com/)[**https://manage.windowsazure.com/**](https://manage.windowsazure.com/)）に管理者としてログインします。
6. **\[ドメイン]** タブに進みます。お使いのアカウントに対し、デフォルトのドメイン、TestMiBGLRoutlook.onmicrosoft.comが作成され、作成したユーザーはこのドメインに属することになります。 必要に応じて、カスタムドメインを作成し直すこともできます。

## Entra IDでのユーザーの作成

Entra IDでユーザーを作成するには:

1. \[Active Directory] > **\[デフォルトディレクトリ] > \[ユーザー]** を開きます。
2. \[ユーザーオプションを追加] を選択し、組織内の \[新規ユーザー] を選択します。
3. ユーザー名を入力します。 \[次へ]**（->）**&#x3092;クリックします。**\[ユーザープロフィール]** ページが表示されます。
4. 姓名や表示名などのユーザー情報を追加します。
5. ドロップダウンメニューを使用し、ユーザーに適切な役割を割り当てます。
6. 仮パスワードを生成します。最初のログイン時にユーザーはこのパスワードの変更を求められます。

## Windows 10デバイスのためのEntra IDとUEMの連携

Entra IDをUEMに接続するには:

1. **\[管理]** > **\[Microsoft Azure] > \[Entra IDを使用したWindows登録およびコンプライアンス]** を開きます。
2. [**Entra ID Windows 10 統合エンドポイント管理の設定**](./Entra_ID_Windows_10_統合エンドポイント管理の設定.md)セクションの手順に従って、UEMをセットアップします。
3. [**Entra ID UEMアプリの割り当て**](./Entra_ID_UEMアプリの割り当て.md) 設定をAzureポータルで実行します。
4. Ivanti Neurons for MDM管理ポータルでEntra IDアカウントのドメイン名を入力した後、\[Azureポータルを連携] をクリックし、チェックボックスを選択します。
5. サインインした後、MobileIron AD Tenant Validationアプリが Ivanti Neurons for MDM UEMアプリのセットアップを確認することを許可する文章に同意します。 連携の完了を示すメッセージが表示されます。

### Windows 10デバイス対応Microsoft Passport for Work

Microsoft Passport for WorkはWindows Hello for Businessに変更されました。 詳細は[**Windows Hello for Business構成**](./Windows_Hello_for_Business構成.md)を参照してください。

### WindowsデバイスのEntra ID登録

**前提条件**

ユーザを Ivanti Neurons for MDM で登録する必要があります。

ドメインに接続して、Windows 10+デバイス上のユーザーを登録します。

1. **\[Entra IDに参加]** をクリックします。
2. ユーザー名とパスワードを入力します。
3. **\[サインイン]** をクリックします。
4. EULAを承諾します。
5. **\[PINを作成]** をクリックします。\* Microsoft Passport for WorkのPIN複雑性を有効化している場合は、構成されたポリシーに従って複雑なPINを設定するようプロンプトが表示されます。
   - Entra IDがユーザーを認証し、JWT（JSON Webトークン）をデバイスにダウンロードします。
   - これで、デバイスが登録されました。
   - 確認のためにデバイス経由でユーザーに連絡が届きます。
6. PINを入力し、確認します。
7. **\[OK]** をクリックします。

## Windowsデバイスにおけるマルチユーザーサポート

Ivanti Neurons for MDM は、Windows 10 Entra IDに登録されたデバイスに対してマルチユーザー機能をサポートしています。 これには、VPN、Wi-Fi、デフォルトのメールクライアントプロファイルなどのプロファイルや証明書を、デバイスではなく各ユーザーにプッシュする機能が含まれます。 ログインしたユーザーに対する自社開発アプリや市販アプリの配布もサポートします。 新規Entra IDユーザーがデバイスにログオンするたびに、Ivanti Neurons for MDMは、デバイスだけでなくユーザーも評価します。 新規ユーザーの場合、Ivanti Neurons for MDMはそのユーザー用にデバイスを更新します。 ユーザーがそのデバイス上の既存ユーザーである場合、前回のログイン以降にデバイスやユーザー設定の変更があり、更新する必要があるかどうかを判断します。

デバイスにログインしているEntra IDユーザーの詳細が、Ivanti Neurons for MDM管理ポータルに報告されます。 ユーザーがデバイスからログアウトし、次のユーザーがログインすると、デバイス詳細ページに2番目のユーザーが表示されます。

## UEMでのビジネス向けMicrosoft Storeの設定

ビジネス向けMicrosoft Storeは、Azureの一環としてMicrosoftが提供するポータルです。 管理者は、このポータルにログインし、アプリを購入したり、そのアプリをすべてのマネージドデバイスに配布したりできます。 以下の手順を行うことで、ビジネス向けMicrosoft Storeを使用してIvanti Neurons for MDMを設定し、Ivanti Neurons for MDM管理ポータルからアプリケーションを管理できます。    

### ステップ1：Microsoft AzureポータルでのEntra IDアプリケーション登録

1. 最初のブラウザを開き、Microsoft Azureポータル（[**https://portal.azure.com/**](https://portal.azure.com/)[**https://portal.azure.com/**](https://portal.azure.com/)）にログインします。
2. 左ペイン&#x306E;**&#x20;\[アプリ登録]&#x20;**&#x3092;クリックします。
3. **\[+新規アプリケーションの登録]** をクリックします。
4. 以下の情報を入力し、MobileIronをAzureアプリとして登録します。\* **名前**：MobileIronアプリの名前を入力します。 （このフィールドは4文字以上で必須です。）
   - **アプリケーションタイプ**：Webアプリ/APIを選択します。
   - **サインオンURL**：デバイスユーザーがMobileIronにサインインするためのURLを入力します（必須）。
5. **\[作成]** をクリックし、アプリを追加してAzureホームページに戻ります。
6. \[設定] を開き、新しいキーを作成します。

### ステップ2：管理ツールとしてのアプリケーション追加

1. ビジネス向けMicrosoft Storeの \[設定] から \[管理] をクリックします。
2. 配布設定
3. \[管理ツールを追加] で、作成したアプリケーションを有効化します。

### Admin Portalでのアカウント連携

1. **\[管理] > \[Microsoft Azure] > \[ビジネス向けMicrosoft Store]** を開きます。
2. ステップ1の **\[Entra IDアプリケーションを登録]** で、**\[はい、この手順を完了しました]** のチェックボックスを選択します。
3. ステップ2の **\[管理ツールを追加]**&#x3067;、**\[はい、この手順を完了しました]** のチェックボックスを選択します。
4. ステップ3の \[アカウントを連携] で以下のフィールドを更新します。\* Entra IDドメイン
   - アプリケーション識別子
   - アプリケーションキー
   - 同期間隔（時間）
5. **\[連携]** をクリックします。ビジネス向けMobileIronストアが正常に設定されたという確認メッセージが表示されます。
6. **\[アプリを同期]** をクリックします。正常に同期されると、**\[アプリケーションが正常に同期されました]** というステータスが表示されます。

アプリ用Microsoft Storeがデバイスにプッシュされると、デバイス詳細の **\[インストール済みアプリ]** タブにアプリの詳細が表示されます。 デバイスから報告されるビジネス向けMicrosoft Storeの各アプリは、**\[ソース]** カラムの **\[ビジネス向けMicrosoft Store]** で識別できます。
