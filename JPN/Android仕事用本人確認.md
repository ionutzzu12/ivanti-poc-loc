---
title: Android仕事用本人確認
createdAt: Wed Feb 11 2026 17:32:26 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:26 GMT+0200 (Eastern European Standard Time)
---

このセクションは以下のトピックを含みます。

- [**Android仕事用本人確認（Work Challenge）構成の作成：**](./Android仕事用本人確認.md)
- [**構成設定**](./Android仕事用本人確認.md)

**ライセンス：**&#x53;ilver

Android仕事用本人確認（Work Challenge）構成は、ユーザーが仕事用プロファイルのデータとアプリにアクセスするためのセキュアパスワードを設定します。 Android Enterprise仕事用プロファイルが必要です。

実装上の注意：

- 管理者は、デバイスパスワードポリシーと仕事用プロファイルパスワードポリシーを独立して適用できます。
- Android 7.0より古いデバイスはこの機能をサポートしないため、それらには Ivanti Neurons for MDM はこの構成を送信しません。
  Ivanti Neurons for MDMは、Android Enterprise仕事用プロファイルがあるデバイスにのみ、この構成を送信します。

## Android仕事用本人確認（Work Challenge）構成の作成：

**手順**

1. **\[構成]** をクリックします。
2. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/B4zFZnij1DD7DD9nr9eWt_r43workchallenge001.png" alt caption}
   **\[+追加]** をクリックします。
3. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/S7T6WdkQ25ttsHS5MUqkb_r43workchallenge002.jpg" alt caption}
   検索フィールドに「仕事用（work）」と入力します。
4. **\[Android仕事用本人確認（Work Challenge）]** 構成を選択します。
5. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/5O4wD3WMMxuScLjBFB0H2_r44workchallenge003.png" alt caption}
   構成名を入力し、必要に応じて説明も入力します。
6. 構成設定フィールドを使用して構成を作成します。 設定の詳細は[**構成設定**](./Android仕事用本人確認.md)をご覧ください。
7. **\[次へ ->]** をクリックします。
8. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/K05Iu-g3HjcIMDwR5JECM_r43workchallenge004.png" alt caption}
   必要であれば構成を有効化します。
9. すべてのデバイスに配布、カスタマイズしたデバイス群に配布、どのデバイスにも配布しない、のいずれかに配布設定を行います。
10. **\[完了]** をクリックします。

## 構成設定

| **設定**        | **操作内容**                                                    |
| ------------- | ----------------------------------------------------------- |
| 名前            | この構成を識別する名前に入力します。                                          |
| 説明            | この構成の目的を明示する説明を入力します。                                       |
| あらゆるロック方式を有効化 | パターンロック解除を含め、あらゆるロック方式の選択をユーザーに許可します。 他のすべてのパスコード設定をオーバーライド |
| パスコードの最小文字数   | パスコードの最小文字数を4～16から選択します。                                    |
| シンプルな値を許可     | 繰り返し、昇順または降順の文字列を含むパスコードを許可する場合に有効化します。                     |
| 英数字の値が必要      | パスコードに、アルファベット1つ以上と数字1つ以上を含める必要がある場合に有効化します。                |
| 複雑な文字と要素タイプ特性 | 以下のいずれかの複雑な文字と要素タイプの要件を設定します。\* なし                          |

- 英数字以外の文字が1文字以上
- 英数字以外の文字が2文字以上
- 英数字以外の文字が3文字以上
- 英数字以外の文字が4文字以上 |
  \| 指紋によるロック解除    | ユーザーが指紋でデバイスのロックを解除できるようにする場合に有効化します。                                                                 |
  \| パスコードの最大有効期間  | パスコードの有効期間を0～730日から選択します。                                                                             |
  \| オートロック        | デバイスにオートロックがかかるまでの時間を選択します。 0～15分から選択してください。                                                          |
  \| パスコードの履歴      | パスコードをいくつ使用すれば再び同じパスコードを使用できるかを0～50から指定します。                                                           |
  \| 入力失敗の最大回数     | 何回まで入力を失敗できるかを選択します。 **警告：ユーザーによるパスワードの入力失敗回数がこの最大回数を超えた場合、Ivanti Neurons for MDMはそのデバイスをワイプします。**    |
