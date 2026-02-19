---
title: All Scripts
createdAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** macOS devices

In the **Admin > All Scripts** page, Ivanti Neurons for MDM allows users with System Management role to create or upload, and manage scripts that can be used in configurations and distributed to devices. You can associate custom attributes with the scripts and assign the resultant values to the configured devices. Use Audit Trails to view logs of the script changes and execution results.

You can write a script that configures any settings on devices. For example, you can run scripts that:

- force device users to change their passwords monthly,
- lock the screen after 5 minutes of idle time, or
- configure a secured Wi-Fi network.

This section contains the following topics:

- [**Adding a script**](./All_Scripts.md)
- [**Modifying a script**](./All_Scripts.md)
- [**Using script variables**](./All_Scripts.md)
- [**Testing a script**](./All_Scripts.md)
- [**Verifying the script execution results**](./All_Scripts.md)

## Adding a script

You can create or upload a repository of bash scripts. This repository can be used in a configuration, such as [**Mobile@Work for macOS Script**](./Mobile@Work_for_macOS.md), to select a script and distribute it to execute on the devices as per the specified schedule in the configuration.

For example, you can create a shell script for execution on devices. You can use wrappers if necessary. The execution of binary files from within a shell script is not supported.

Ivanti highly recommends you test your shell scripts before running them on the devices to ensure their robustness and quality. Run your script locally, and correct any errors that result.

Procedure

1. Go to **Admin > Scripts > All Scripts**.
2. Click **+ Add**.
3. Name and describe the script.
4. Select one of the following **Script Type**:\* **bash**
   - **zsh**
   - **python**
   - **swift**
5. Select the **Run as root** check box to run the script as root on devices. By default, this option is cleared.
6. In the **Script Editor**, you can type, drag and drop, or copy and paste a script in the text box.
7. Alternatively, click **Import code from a Script** to drag and drop an existing script file or click Choose File to browse and select the script file to be uploaded to Ivanti Neurons for MDM. This will replace any existing script in the script editor. This action cannot be undone. Click **Import**. The code from the uploaded script will be displayed in the script editor.
8. (Optional) In the **Custom attributes available** section, select one or more displayed device custom attributes to associate them with the script. They can be used to assign the resultant script execution values to the device custom attributes of the configured devices. Click **Sample Code for Custom Attributes** to view a sample code using custom attributes in a script.
9. Click **Save**.

The custom attribute names in the script should be in lower case. If the custom attributes are referred to in any scripts, then the attributes cannot be removed. When you modify a custom attribute (for example, its name) and if it is associated with a script, then you should make the corresponding changes in the associated scripts.

## Modifying a script

To edit or remove a script:

1. Go to **Admin > Scripts > All Scripts**.
2. Under the **Actions** column for the script, click the corresponding icon for edit or delete action.
3. Follow the instructions on the screen to complete the action.

When a script (content, name, description) is changed, all the configurations that are associated with the script are redistributed to the devices.

## Using script variables

Define and store script inputs such as environment and substitution variables in the script repository. In the Mobile\@Work for macOS script configuration, depending on which script is linked, the related script variables will be available for use as required. This feature requires [**Mobile@Work for macOS**](./Mobile@Work_for_macOS.md) 1.71.0 through the most recently released version as supported by Ivanti Neurons for MDM.

Use the variables to run a script with different values every time it runs. For example, an administrator can create a script to use the $\{userEmailAddress} environment variable as the script variable and associate it with a Mobile\@Work for macOS script configuration. When the configuration is distributed and installed on each user device, Ivanti Neurons for MDM sends a different registered user email address for each device to take certain actions. The Ivanti Neurons for MDM administrative portal supports custom variables.

To add a script variable:

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Admin > Scripts > All Scripts**.
:::

:::WorkflowBlockItem
In the Script Input section, click **+ Add**.
:::

:::WorkflowBlockItem
In the Add Script Input - Environment Variable pop-up page, enter the following details:
:::

:::WorkflowBlockItem
- Label to Show - This text will be shown as a label in the Mobile\@Work for macOS script configuration page. For example, Enter OS Folder, Enter Apache Number, and so on.
- Environment Variable Name - For example, JAVA\_HOME, OS\_VERSION, and so on. Ivanti Neurons for MDM substitutes values for the script variables while sending the configuration details to a target device as the values are persisted in the database.
- Environment Variable Default Value - For example, 1024, bin/java, $\{PhoneNumber}, and so on. The input variables would be used in the script uploaded or edited by an administrator. See also the following notes.
  In the Preview region, review how the environment variable's value will be shown as script input in the configuration page.
:::

:::WorkflowBlockItem
Click **Save**.
:::
::::

This way, only the label and the default value are available to the configuration and not the environment variable name, which provides a layer of abstraction.

- Alphanumeric value (for example, 1024, bin/java, root\@localhost) or system attributes (for example, $\{userFirstName}) are acceptable as environment variable's value.
- The environment variable's value can be modified or deleted during deployment in the configuration page.
- If the environment variable's value is not provided, ensure a value is provided during script deployment. Otherwise, empty value will be passed to the script.
- After a script configuration is distributed and installed on the device, editing environment variables in the Admin > All Scripts page will not impact the existing configurations associated with the script. See also [**Mobile@Work for macOS script configuration**](./Mobile@Work_for_macOS.md).

### Editing a script variable

To modify a script variable, click the edit (pencil) icon against the variable and save the changes.

If a script configuration refers to a script having script variables, editing the label of an existing script variable will also reflect in the script configuration. However:

- A change in the default value of the script variable will not reflect in existing configurations.
- A change in the default value of the script variable will reflect in any new configurations created with the preceding script.

### Deleting a script variable

To delete a script variable, click the delete (minus) icon against the variable and confirm.

A newly created script variable, or deletion of an existing script variable will reflect even in an already existing configuration.

## Testing a script

Test run a script in the debug tool quickly before testing it on a device and without necessary saving the scripts. This feature requires [**Mobile@Work for macOS**](./Mobile@Work_for_macOS.md) 1.67 through the most recently released version as supported by Ivanti Neurons for MDM.

Procedure

1. Go to **Admin > Scripts > All Scripts**.
2. In the Script Editor, add or import a script.
3. If the tenant has multiple spaces, then select a space.
4. In the Test Script section, select **macOS** as the platform.
5. In the **Find devices** text field, find and select the device on which the script can be tested. The device can be searched by serial number, user name, device name, and OS version.
6. Click **Test Now**. This way, an environment variable can be added, edited, and deleted, and the script can be tested with that state (without even saving the changes made).
7. Wait for the script to be pushed and executed on the device.
8. Review the published test results in the Script Input (containing environment variable details), Script Output, and Custom Attributes sections. The default values of the environment variables are also displayed.

## Verifying the script execution results

To view the logs of the script execution results:

::::WorkflowBlock
:::WorkflowBlockItem
Go to **Devices**.
:::

:::WorkflowBlockItem
Click the name of the device.
:::

:::WorkflowBlockItem
Click the **Logs** tab.
:::

:::WorkflowBlockItem
In a row that displays the Script Execution action, you can verify the following information:
:::

:::WorkflowBlockItem
- Script name in the Details column.
- Script execution status in the Status column.
- Script execution date and time in the Date column.
- Script execution logs (device log plist) by clicking the eye icon under the Actions column.
  Use filters to display the **Script Execution** rows. Logs from these rows include the output (plist) of standard output and standard error for the scripts.
:::

:::WorkflowBlockItem
Use filters to display the **Script Execution Result Processing** rows. Logs from these rows include details (plist) of how the results were processed.

- If a script did not have any custom attributes associated with it, there will not be any results to process. Such scripts will not be displayed in the list of the filtered rows.
- If a script had custom attributes associated with it and if they were in the expected format, then the custom attributes from the results are mapped and the status is displayed as Success. You can verify the mapped custom attributes and their values in the **Attributes** tab.
- If a script had custom attributes associated with it and if they were not in the expected format, then the custom attributes from the results are not mapped and the status is displayed as Error.
- If the result format is correct but not all the associated custom attributes are sent in the result, the status is displayed as Error.
- If a script variable is sent with the script, Script Execution Result Processing logs will include details (plist) for the script variable.
:::
::::

Related topics:

- [**Mobile@Work for macOS Script configuration**](./Mobile@Work_for_macOS.md)
