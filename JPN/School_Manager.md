---
title: School Manager
createdAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:32:28 GMT+0200 (Eastern European Standard Time)
---

## ライセンス： Gold

**対象：**&#x76E3;視対象のiOS 9.3+

Apple School Managerは、教育機関専用のAppleのクラウドサービスであり、Appleの「Apps and Books」を通じたアプリの購入、Apple Device EnrollmentによるiPadの登録、マネージドApple IDの作成などのサービスを提供します。 Apple School Managerとの完全な統合により、Ivanti Neurons for MDM UEMソリューションは、教師や生徒に割り当てられたiPadの完全な管理を容易にし、School ManagerのエコシステムとClassroomなどのアプリを活用します。

Apple Booksはサポートされません。

## School Managerの構成

:::::WorkflowBlock
:::WorkflowBlockItem
**\[管理] > \[School Manager]** を開きます。
:::

:::WorkflowBlockItem
**\[Educationの設定]** オプションがオフになっている場合はクリックします。
:::

:::WorkflowBlockItem
以下のオプションから1つ選択してください：
:::

::::WorkflowBlockItem
- **Apple School Managerアカウントと同期し、学校情報をインポートしてください。**&#x31;) **\[管理] > \[Apple] > \[Device Enrollment]** を開き、組織のキーファイルをダウンロードします。
  2\) キーファイルをApple School Managerアカウントにアップロードし、暗号化キーを生成します。
  3\) Apple School Managerから暗号化キーをダウンロードし、Ivanti Neurons for MDM にキーをアップロードします（**\[管理] > \[Apple] > \[Device Enrollment]**）。
  Apple Educationには既存のApple Device Enrollmentアカウントを再利用できます。 Apple School Managerにアクセスすると、Education機能を含むDevice EnrollmentアカウントにアップグレードするオプションをAppleが提示します。 アップグレード方法は、[**https://support.apple.com/en-in/HT206960**](https://support.apple.com/en-in/HT206960)をご覧ください。
  暗号キーの承認後、**\[今すぐ同期]** ボタンが表示されます。
  4\) Apple School Managerとデータ同期を開始するには **\[今すぐ同期]** をクリックします。
- **CSVファイルからデータをインポートしてください。**::::WorkflowBlock

:::WorkflowBlockItem
（任意）**\[CSVテンプレートのZIPファイルをダウンロード]** をクリックし、全データタイプのテンプレートを含むzipファイルをダウンロードします。
:::

:::WorkflowBlockItem
**\[ファイルを選択...]** をクリックします。
:::

:::WorkflowBlockItem
以下の6つのCSVファイルを追加します。
:::

:::WorkflowBlockItem
- 学生データファイル（students.csv）
- 登録者データファイル（roster.csv）
- スタッフデータファイル（staff.csv）
- クラスデータファイル（classes.csv）
- コースデータファイル（courses.csv）
- 場所データファイル（locations.csv）アップロードする前に、毎回6つすべてのCSVファイルを一緒に選択する必要があります。
  **\[アップロード]** をクリックします。
:::

:::WorkflowBlockItem
（任意）CSVファイルを変更する必要がある場合は、前にアップロードした6つのファイルの必要データすべてを保存してください。 必要な編集を行った後、再び全部一緒にアップロードします。
:::

:::Paragraph{indent="1"}
\::::
**\[クラス]** と **\[個人]** タブからデータを検索します。個人 (学生と職員) も Ivanti Neurons for MDM の **\[ユーザ]** ページに表示されます。
:::
::::

:::WorkflowBlockItem
次のように、学生と職員が教育目的で使用するデバイスで2つのデバイス グループを作成します。1) **\[管理] > \[カスタム属性]** を開きます。
2\) 学生とスタッフのカスタム属性を作成します。これらは動的に管理されるデバイスグループの作成に使用します。
3\) **\[デバイス] > \[デバイスグループ]** に進みます。
4\) **\[追加+]** をクリックします。
5\) 前にフィルターとして作成したカスタム属性を使用し、学生用とスタッフ用に1つずつ、動的に管理されるデバイスグループを作成します。
:::

:::WorkflowBlockItem
**\[デバイス]** ページから **\[アクション] > \[ユーザーに割り当てる]** オプションを使用し、登録済みデバイスを学生とスタッフに割り当てます。
:::

:::WorkflowBlockItem
**\[構成] >&#x20;**[**\[Education\]**](./教育.md) ペイロードを追加することにより、リーダー（スタッフ）構成とメンバー（学生）構成を作成します。
:::

:::WorkflowBlockItem
リーダー（スタッフ）構成とメンバー（学生）構成をスタッフと学生のデバイスグループに配布します。この配布によって構成がプッシュされ、各デバイスに証明書がインストールされます。
:::
:::::

**\[管理] > \[School Manager]** ページでクラス名として値が表示されない場合、クラスシステムソース識別子およびコース識別子フィールドから値が作成されます。これらのフィールドはApple School ManagerまたはCSVファイルでは任意です。 しかし、クラス名がない場合、これらの組み合わせがデフォルトの識別子として使用されるため、常に値を入力することをお勧めします。

## 教師へのClassroomアプリのプッシュ

Classroomアプリでは、教師（リーダー）が以下のシナリオを管理できます。

::::WorkflowBlock
:::WorkflowBlockItem
- iPadとアプリをリモートで制御するClassroom管理
- クラスグループの作成
- 教師による対象グループの学生メンバーの閲覧
- 教師による対象グループの学生へのコンテンツ送信
- 学生が閲覧できるアプリやコンテンツの制限
:::
::::

Apple App Store から Classroom アプリケーションをプッシュできます。

**手順**

1. **\[アプリ] > \[アプリカタログ]** ページを開きます。
2. **\[+追加]** ボタンをクリックします。
3. AppleのClassroomアプリを検索し、選択します。
4. **\[次へ]** をクリックします。
5. カテゴリと説明を入力します。
6. **\[次へ]** をクリックします。
7. 前に作成した教師デバイスグループにアプリを配布します。
8. \[アプリ構成] ページでアプリを設定します。
9. **\[完了]** をクリックします。

## School Managerの無効化

School Managerを無効化すると、現行のデータがすべてワイプされます。 無効化する際は注意してください。

1. **\[管理] > \[School Manager]** を開きます。
2. **\[Education設定]** オプションがオンになっている場合はクリックします。
3. **\[はい]** をクリックします。
