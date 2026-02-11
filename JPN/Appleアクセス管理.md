---
title: Appleアクセス管理
createdAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:25 GMT+0200 (Eastern European Standard Time)
---

**前提条件**：

- Apple Business ManagerまたはApple School Managerでドメインを確認し、ロックします。
- Ivanti Neurons for MDM内に管理対象Apple IDが存在するApple Business Manager組織またはApple School Manager組織から、MDMサーバーを少なくとも1つ構成します。

管理対象Apple IDにサインインすることで、組織では、ユーザがAppleのどのサービスと機能にアクセスできるかを制御できます。

Apple Business ManagerまたはApple School Managerの **\[次の場所では管理対象Appleアカウントを許可する]** 設定により、ユーザが各自の管理対象Apple IDでサインインできる場所を制御します。 管理者はこの設定を構成して、管理対象または監視対象のデバイスへのサインインを制限する、またはどのデバイス上でもサインインを許可することができます。

- **すべてのデバイス**（デフォルト）：ユーザはどのデバイス上でも、そのデバイスがMDMソリューションによって管理されているかどうかに関係なく、各自の管理対象Apple IDでサインインできます。
- **管理対象デバイスのみ**：ユーザは、Get TokenエンドポイントをサポートしているMDMソリューションによって管理されているデバイス上でのみサインインできます。
- **監視対象デバイスのみ**：ユーザは、Get TokenエンドポイントをサポートしているMDMソリューションによって監視（および管理）されているデバイス上でのみサインインできます。

これらの設定は、Apple Business ManagerおよびApple School Manager内のAppleサービスを対象とする、より広範な「アクセス管理」の一部です。

強化されたセキュリティにより、管理対象または監視対象のデバイスへのサインインを制限し、制御されたデバイス上でのみ仕事関連のデータにアクセスできるようにすることで、データセキュリティを向上させることができます。

**\[デバイス登録]** タブにゼロ個または複数個の「デバイス登録MDM」サーバー組織が存在しており、管理者がApple Business ManagerまたはApple School Mangerで **\[アクセス管理]** > **\[Appleサービス]** にある **\[次の場所では管理対象Appleアカウントを許可する]** を \[監視対象デバイスのみ] または \[管理対象デバイスのみ] に設定している場合、管理対象Appleアカウントログインは失敗します。

Ivanti Neurons for MDMデバイス登録MDMサーバーに**管理対象Apple**アカウントが存在しない場合、デバイスはログインに失敗します。
