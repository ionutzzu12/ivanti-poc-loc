---
title: Android APN設定の構成
createdAt: Wed Feb 11 2026 17:32:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:27 GMT+0200 (Eastern European Standard Time)
---

Android APN設定の構成では、パブリックネットワーク上のデバイスに必要なアクセスポイント名（APN）を設定できます。 この構成は、Android Enterprise仕事用マネージドデバイス、および会社所有デバイス上の仕事用プロファイルを持つマネージドデバイス（Androidバージョン9.0またはサポートされる以降のバージョン）に適用されます。

**手順**

::::WorkflowBlock
:::WorkflowBlockItem
**\[構成]\*\*\*\* > \[+追加]** を開きます。
:::

:::WorkflowBlockItem
**\[Android APN設定]** 構成を選択します。
:::

:::WorkflowBlockItem
構成の名前を入力します。
:::

:::WorkflowBlockItem
説明を入力します。
:::

:::WorkflowBlockItem
\[構成設定] セクションで、以下のオプションを構成します。
:::

:::WorkflowBlockItem
| 設定              | 説明                              |
| --------------- | ------------------------------- |
| **エントリー名**      | アクセスポイント設定の名前を入力。               |
| **アクセスポイント名**   | アクセスポイントの名前を入力。                 |
| **アクセスポイントタイプ** | アクセスポイントの種類を以下から選択：\* **デフォルト** |

- **DUN**
- **IMS**
- **緊急**
- MMS
- **HIPRI**
- **CBS**
- **MCX**
- **SUPL**
- **FOTA**
- **IA**                                                                                                                         |
  \| **MVNOの種類**             | 仮想移動体通信事業者（MVNO）の種類を以下から選択：\* **なし**
- **SPN**
- **IMSI**
- **GID**
- **ICCID**                                                                                                                                                                           |
  \| **Bearer**              | データ送信に使用されるベアラサービスの種類を以下から選択：\* **1xRTT**
- **CDMA**
- **EDGE**
- **EHRPO**
- **EVDO**
- **EVDO A**
- **EVDO B**
- **GPRS**
- **GSM**
- **HSDPA**
- **HASP**
- **HSPAP**
- **HSUPA**
- **IDEN**
- **IWLAN**
- **LTE**
- **NR**
- **TD\_SCDMA**
- **UMTS** |
  \| **APNプロトコル**            | APNに必要なAPNプロトコルを 以下から選択：\* **なし**
- **IPV4**
- **IPV6**
- **IPV4/IPV6**
- **NON\_IP**
- **PPP**（ポイントツーポイントプロトコル）
- **非構造化**                                                                                                                               |
  \| **APNローミングプロトコル**       | APNに必要なAPNローミングプロトコルを 以下から選択：\* **なし**
- **IPV4**
- **IPV6**
- **IPV4/IPV6**
- **NON\_IP**
- **PPP**（ポイントツーポイントプロトコル）
- **非構造化**                                                                                                                          |
  \| **APNを有効化/無効化**         | APN構成をオンにする。                                                                                                                                                                                                                                             |
  \| **通信事業者ID**             | 通信事業者IDの数値を入力。                                                                                                                                                                                                                                           |
  \| **認証タイプ**               | 認証プロトコルの種類を以下から選択：\* **なし**
- **PAP**（Password Authentication Protocol）
- **CHAP**（Challenge-Handshake Authentication Protocol）
- **PAPまたはCHAP**                                                                                                          |
  \| **ユーザー名**               | ログインユーザー名を入力。                                                                                                                                                                                                                                            |
  \| **パスワード**               | ログインパスワードを入力。                                                                                                                                                                                                                                            |
  \| **パスワードの確認**            | 確認のためパスワードを再入力。                                                                                                                                                                                                                                          |
  \| **ポート番号**               | ポート番号を入力（1～65535の数値）。                                                                                                                                                                                                                                    |
  \| **プロキシアドレス**            | プロキシアドレスの種類。                                                                                                                                                                                                                                             |
  \| **Mobile Country Code** | Mobile Country Codeを入力。                                                                                                                                                                                                                                  |
  \| **Mobile Network Code** | Mobile Network Codeを入力。                                                                                                                                                                                                                                  |
  \| **MMSプロキシアドレス**         | MMSプロキシアドレスを入力。                                                                                                                                                                                                                                          |
  \| **MMSポート番号**            | MMSポート番号を入力（1～65535の数値）。                                                                                                                                                                                                                                 |
  \| **MMSサーバーアドレス（mmsc）**   | MMSサーバーアドレスを入力。                                                                                                                                                                                                                                          |
  **\[次へ]** をクリックします。
:::

:::WorkflowBlockItem
以下の配布オプションから1つ選択します。
:::

:::WorkflowBlockItem
- **すべてのデバイス**
- デバイスなし（デフォルト）
- **カスタム**
  **\[完了]** をクリックします。
:::
::::

デバイスが以下の値を持つ既存のAPN構成がある場合、以下のフィールドに同じ値を持つAPN構成を追加することはできません。

- Mobile Country Code
- Mobile Network Code
- アクセスポイント名
- プロキシアドレス
- ポート番号
- MMSプロキシアドレス
- MMSポート番号
- MMSサービスアドレス
- APNを有効化/無効化
- MVNOの種類
- APNプロトコル
- APNローミングプロトコル

Android APN設定の構成は、手動で、または通信事業者によってデバイス内ですでに構成されている他のAPN設定より優先されます。
