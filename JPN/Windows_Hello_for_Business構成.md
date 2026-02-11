---
title: Windows Hello for Business構成
createdAt: Wed Feb 11 2026 17:32:26 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:26 GMT+0200 (Eastern European Standard Time)
---

この構成により管理者はデバイスでWindows Helloのセットアップを実行します。 Windows HelloのセットアップにはデバイスにサインインするPINを設定する必要があります。

対象：Windows 10

Procedure**手順**

1. \[構成] > \[+追加] を開きます。
2. 検索フィールドに \[Windows] と入力し、\[Windows Hello for Business] 構成をクリックします。
3. 構成の \[名前] と \[説明] を入力します。
4. \[Windows 10デバイスでWindows Hello for Businessを有効化/無効化] をトグルして、\[オン] を選択します。トグルスイッチはデフォルトでオンに設定されています。 Windows Hello for Businessを無効化しても、デバイスからPINは削除されません。
5. \[PINの複雑さ] を設定します。
6. 必要な構成を選択します。\* Windows Hello for Business用のTPM（Trusted Platform Module）が必要
   - スマートカード証明書としてWindows Hello for Business証明書を使用
   - Windows Hello for BusinessのPINジェスチャーの代わりに顔や指紋などの生体ジェスチャーを使用
   - Windows Hello顔認証機能に顔の特徴の認識に対応する高度ななりすまし防止機能が必要
   - 動的ロック
   - ユーザーによるFIDO2セキュリティキーでのサインインを許可
7. \[次へ] をクリックします。
8. \[この構成を有効化] オプションを選択します。
9. 以下の配布オプションから1つ選択します。\* すべてのデバイス
   - デバイスなし（デフォルト）
   - カスタム
10. \[完了] をクリックします。
