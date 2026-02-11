---
title: AirPlayミラーリング
createdAt: Wed Feb 11 2026 17:32:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:27 GMT+0200 (Eastern European Standard Time)
---

**ライセンス：**&#x47;old

AirPlayミラーリングとは、Apple TVを使用しているモニター上にiOSデバイスの画面を表示できる機能です。 Apple TVとiOSデバイスは、同じWi-Fiネットワークに接続する必要があります。 この機能には以下のデバイスが必要です。

- iOS 7以降のデバイス - 監視対象
- macOS 10.10以降のデバイス - 監視対象
- Apple TVのバージョン - 監視対象
- AirPlay

非iOSデバイスの管理を可能にする変更は元に戻せません。

このセクションは以下のトピックを含みます。

- [**Apple AirPlayの構成**](./AirPlayミラーリング.md)
- [**モバイルデバイスでのAirPlayの設定**](./AirPlayミラーリング.md)
- [**Apple TVと連動するモニターの設定**](./AirPlayミラーリング.md)
- [**iOSデバイスとApple TVの接続**](./AirPlayミラーリング.md)

## Apple AirPlayの構成

AirPlay構成設定の詳細については、[**AirPlay構成**](./AirPlay構成.md)をご覧ください。

手順

1. **\[構成]** に進みます。
2. **\[+追加]** をクリックします。
3. **\[AirPlay]** をクリックします。
4. 該当するフィールドに構成の名前と説明を入力します。
5. 対応するすべてiOSバージョンについて、デバイス名とパスワードを入力します。
6. 必要に応じて **\[+追加]** をクリックし、別のデバイスを追加します。
7. 任意で、監視対象iOS 7以降のデバイスまたはmacOS 10.10以降に関してはデバイスIDを許可リストに追加します。
8. **\[次へ]** をクリックします。
9. 配布レベルを選択します。
10. **\[完了]** をクリックします。

## モバイルデバイスでのAirPlayの設定

手順

1. [**Apple Configurator**](./Apple_Configurator.md)を設定します。
2. **\[デバイス] > \[デバイス]** を開きます。
3. そのデバイスの \[詳細] ページに表示するiOSデバイスの名前をクリックします。

::Image[]{src="More_icon.png" signedSrc="More_icon.png" size="10" caption alt isUploading="false" sha initialPath="More_icon.png" githubPath="More_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
 アイコンをクリックします。
:::

5. **\[AirPlayミラーリング]** を選択し、AirPlayミラーリングダイアログを表示します。
6. プルダウンメニューからApple TVデバイスを選択します。
7. スキャン時間を秒数で入力し、選択したデバイスを検索する制限時間を指定します。
8. Apple TVデバイスのパスワードを入力します。
9. **\[リクエストを送信]** をクリックします。

## Apple TVと連動するモニターの設定

手順

1. Apple TVに接続されたモニター上で、**\[設定] > \[プロファイル]** を開きます。
2. **\[Ivanti Neurons for MDM Apple Configurator]** を選択します。
3. **\[プロファイルを追加]** をクリックします。

::Image[]{src="More_icon.png" signedSrc="More_icon.png" size="10" caption alt isUploading="false" sha initialPath="More_icon.png" githubPath="More_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
アイコンをクリックします。
:::

5. **\[AirPlayミラーリング]** を選択し、AirPlayミラーリングダイアログを表示します。
6. プルダウンメニューからApple TVデバイスを選択します。
7. スキャン時間を秒数で入力し、選択したデバイスを検索する制限時間を指定します。
8. Apple TVデバイスのパスワードを入力します。
9. **\[リクエストを送信]** をクリックします。

## iOSデバイスとApple TVの接続

手順

1. Apple TVデバイスをモニターに接続します。
2. Apple TVリモートを使用して、**\[設定] > \[アカウント] > \[ホームシェアリング]** を開き、ホームシェアリングをオンにします。
3. **iOSデバイス**を、**AppleTVデバイス**と同じWi-Fiネットワークに接続します。
4. **iOS**デバイス上でリモートアプリを開きます。
5. **\[リモート設定]** 画面から **\[ホームシェアリング]** を有効化します。
