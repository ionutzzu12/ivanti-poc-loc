---
title: School Manager
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

## License: Gold

**Applicable to:** Supervised iOS 9.3+

Apple School Manager is an Apple cloud service dedicated to education institutions to provide services including purchasing applications in Apple Apps and Books, enrolling iPads through Apple Device Enrollment, and creating managed Apple IDs. With full integration with Apple School Manager, Ivanti Neurons for MDM UEM solution provides a seamless way to fully manage the iPads designated for teachers and students in order to leverage the School Manager ecosystem and apps such as Classroom.

Apple Books are not supported.

## Configuring School Manager

:::::WorkflowBlock
:::WorkflowBlockItem
Go to **Admin > School Manager**.
:::

:::WorkflowBlockItem
Click the **Setup Education** option if it is turned off.
:::

:::WorkflowBlockItem
Select one of the following options:
:::

::::WorkflowBlockItem
- **Sync with the Apple School Manager account to import school information**:1) Go to **Admin > Apple > Device Enrollment** to download your organization's key files.
  2\) Upload the key files to your Apple School Manager account to generate encryption keys.
  3\) Download the encryption keys from Apple School Manager and upload the keys into Ivanti Neurons for MDM (**Admin > Apple > Device Enrollment**).
  Existing Apple Device Enrollment accounts can be reused for Apple Education. Apple will give you the option to upgrade your Device Enrollment account to include Education capabilities when you access the Apple School Manager. For the upgrade instructions, visit [**https://support.apple.com/en-in/HT206960**](https://support.apple.com/en-in/HT206960).
  When the encryption keys are accepted, the **Sync Now** button appears.
  4\) Click **Sync Now** to start data sync with Apple School Manager.
- **Import data from CSV files**:::::WorkflowBlock

:::WorkflowBlockItem
(Optional) Click **Download CSV templates ZIP file** to download a zip file that contains templates of all the data types.
:::

:::WorkflowBlockItem
Click **Select files**...
:::

:::WorkflowBlockItem
Add the following six CSV files:
:::

:::WorkflowBlockItem
- Students data file (students.csv)
- Roster data file (roster.csv)
- Staff data file (staff.csv)
- Classes data file (classes.csv)
- Courses data file (courses.csv)
- Locations data file (locations.csv)You must select all the six CSV files together, every time, before uploading them.
  Click **Upload**.
:::

:::WorkflowBlockItem
(Optional) If the CSV files need to be modified, please retain all necessary data in all six files that had been previously uploaded. Make the required edits and upload them together once again.
:::

:::Paragraph{indent="1"}
\::::
Search for data from the **Classes** and **Individuals** tab.The individuals (students and staff) also appear in the **Users** page of Ivanti Neurons for MDM.
:::
::::

:::WorkflowBlockItem
Create two device groups for devices that will be used for education by students and staff as follows:1) Go to **Admin > Custom Attributes**.
2\) Create custom attributes for students and staff that will be used to create dynamically managed device groups.
3\) Go to **Devices > Device Groups**.
4\) Click **Add+**.
5\) Create one each dynamically managed device group for students and staff using the custom attributes created previously as filters.
:::

:::WorkflowBlockItem
Assign registered devices to students and staff from the **Devices** page using the **Actions > Assign to user** option.
:::

:::WorkflowBlockItem
Create a Leader (staff) configuration and a Member (students) configuration by adding the **Configurations >&#x20;**[**Education**](./Education.md) payloads.
:::

:::WorkflowBlockItem
Distribute the Leader (staff) and Member (students) configurations to the staff and student device groups.This distribution will push these configurations and install certificates on the respective devices.
:::
:::::

On the **Admin > School Manager** page, if there is no value present for the Class Name, the value is derived from the class system source identifier and the course identifier fields. These fields are optional in the Apple School Manager or the CSV file. However, it is recommended to enter a value at all times as their combination is used as the default identifier in the absence of a Class Name.

## Pushing the Classroom app to the teachers

Using the Classroom app, the teachers (Leader) can manage the following scenarios:

::::WorkflowBlock
:::WorkflowBlockItem
- Classroom management ability to control iPads and apps remotely.
- Ability to create a class group.
- Ability for a teacher to view the student members of that group.
- Ability for a teacher to send content to the students in that group.
- Restrict what apps and content the students can view.
:::
::::

You can push the Classroom app from the Apple App Store.

**Procedure**

1. Go to the **Apps > App Catalog** page.
2. Click the **+Add** button.
3. Search for and select the Classroom app by Apple.
4. Click **Next**.
5. Enter the category and description.
6. Click **Next**.
7. Distribute the app to the teachers device group created previously.
8. Configure the app settings in the App Configurations page.
9. Click **Done**.

## Disabling School Manager

Disabling School Manager will wipe all the current data. Please exercise caution while doing so.

1. Go to **Admin > School Manager**.
2. Click the **Setup Education** option if it is turned on.
3. Click **Yes**.
