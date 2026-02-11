---
title: Android一括登録の使用
createdAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
---

一括登録機能では、Ivanti Neurons for MDM で複数のAndroidデバイスを迅速に登録できます。

ライセンス：Silver

一括登録を使用する前に次のタスクを実行してください。

1. Android Debug Bridge（adb）を含むAndroid SDKを、デバイス構成に使用するコンピュータ上にインストールします。Android Debug Bridgeの詳細については、[**http://developer.android.com/tools/help/adb.html**](http://developer.android.com/tools/help/adb.html)をご覧ください。
2. USBデバッグを有効化します。Androidデバイス上でUSBデバッグを有効化する手順は、Androidのリリースによって異なります。 USBデバッグの有効化に関する詳細については、[**http://developer.android.com/tools/device.html**](http://developer.android.com/tools/device.html)を参照してください。
3. 各デバイスにGoクライアントをインストールします。
4. USBケーブル経由でデバイスを登録に使用するプロビジョニングコンピュータに接続します。

Goを起動し、Android Debug Bridge（adb）シェルを使用してサーバーに登録することができます。 Android Debug Bridgeは、WindowsまたはiOSターミナルユーティリティのコマンドラインから使用できるツールです。 これを使用することで、接続されたAndroidデバイスと通信できるようになります。 adbシェルからのコマンドフォーマット：

\> adb shell

$ am start -a android.intent.action.MAIN -d "mirp\://na1.mobileiron.com?key=value\&key=value" -n com.mobileiron.anyware.android/com.mobileiron.polaris.manager.ui.StartActivity

 登録する関連データのエンコードには、登録プロトコル（**mirp**）が使用されます。

有効なキーと値：

| キー         | 利点                                                                                                                                                                                   |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| ユーザー       | iRegを使用する場合は、ユーザー名フィールドに入力されるユーザーのメールアドレス。必須.                                                                                                                                        |
| パスワード      | ユーザーのパスワード                                                                                                                                                                           |
| pin        | ユーザーの登録PIN                                                                                                                                                                           |
| quickStart | **\[TRUE] にセットすると、スプラッシュ画面が表示されますが、すぐに表示が消えます。** ようこそ画面でスピナーが \[続行] ボタンに変わると、\[続行] をタップしなくても自動的に画面が切り替わります。 また、この合理化されたプロビジョニングフローは全デバイスで生じます。\* プライバシーとショートカットに関するユーザープロンプトは省略されます。 |

- Zebraデバイスでは、ユーザープロンプトなしにクライアントが自身に管理者特権を与えます。 必要最小バージョンはZebra MX 4.3です。**\[FALSE] にセットすると、スプラッシュ画面が通常通りに表示され、ようこそ画面を表示するには \[続行] をタップしなければなりません。** オプション。デフォルトは \[FALSE] となっています。 |

一括登録には、パスワード、PINまたはトークンの使用が求められます。

このコマンド例では、サーバー、ユーザー、パスワード、PIN、quickStartが指定されています。

am start -a android.intent.action.MAIN -d "mirp\://ppp183.auto.mobileiron.com?user=[**miadmin@auto0001.mobileiron.com**](mailto\:miadmin@auto0001.mobileiron.com)\&password=P@$$W0R3\&pin=12345\&quickStart=true" -n com.mobileiron.anyware.android.qa/com.mobileiron.polaris.manager.ui.StartActivity

**一括登録スクリプトの例**

自分で一括登録スクリプトを作成する際、このスクリプト例を利用することができます。 このスクリプト例では、プロビジョニングマシンに接続されているすべてのデバイスを同じユーザーとパスワードで登録することになります。

for i in \`adb devices | grep -v devices |

do

 echo "Registering $i"

 adb -s $i shell "am start -a android.intent.action.MAIN -d \\"mirp\://\<servername?user=user email addresspassword=password

done

**考えられるエラーメッセージ**

一括登録の使用時に発生する可能性のあるエラーを次に紹介します。

| エラー                 | 解決策                                                                        |
| ------------------- | -------------------------------------------------------------------------- |
| mirpスキームが見つかりません    | mirpスキームを使用するコマンド例：am start -a android.intent.action.MAIN -d "xxxmirp\://? |
| URLが無効です            | データ文字列が送信されていない場合に発生します。 URLが正しいことを確認してください。                               |
| サーバー情報が見つかりません      | サーバー情報がないか、正しく入力されていません。                                                   |
| ユーザー情報が見つかりません      | ユーザーキーが入力されていることを確認してください。                                                 |
| パスワード/PIN情報が見つかりません | PINまたはパスワードキーが入力されていることを確認してください。                                          |

一括登録用の複数のプロファイルが作成されている場合：

- ネイティブに登録された完全に管理されているAndroid Enterpriseデバイスは、最初のプロファイルによって作成されたカスタム属性を受け取ります。
- デバイス移行時、いずれかの一括登録プロファイル内にデバイスが存在する場合は、その一括登録プロファイル内の、移行対象のデバイスに対して定義されているカスタム属性が、そのデバイスに移行時に適用されます。 この振る舞いは、移行対象の完全に管理されているAndroid Enterpriseデバイスの場合も同じです。なぜなら、最初のプロファイルのカスタム属性を受け取るためです。

また、その特定のデバイス用に作成されているすべてのプロファイルがアクティブと表示されます。
