---
title: Provisioning Package Enrollment with PIN
createdAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:28 GMT+0200 (Eastern European Standard Time)
---

The admin can enroll the devices managed by SCCM or Ivanti Endpoint Manager to the Ivanti Neurons for MDM. The Deployment Package Tool allows organizations to streamline the transition of Windows devices to Ivanti Neurons for MDM Modern Management, without downtime or end user interruption. The seamless transition is achieved by downloading a unique deployment package from the Ivanti Neurons for MDM Console, then deploying it through the existing management tool or domain. Once the package is executed, it will silently enroll the endpoint into Ivanti Neurons for MDM for the ongoing management. The approach allows administrators to first easily migrate the devices, then have the flexibility to configure devices later over-the-air. When a device completes the silent enrollment into Ivanti Neurons for MDM, it is joined with MDM and is co-managed by the two management authorities. Once an administrator has configured the desired Windows experience within Ivanti Neurons for MDM, the legacy management platform can be decommissioned, leaving Ivanti Neurons for MDM as the single management authority of the device.

There is an exception to this rule if a device is being transitioned from Microsoft Endpoint Manager (MEM) or formerly SCCM. The existing MEM Client continues to function in Coexistence Mode (opposed to Co-Management mode), until the MEM platform is decommissioned. When Coexistence Mode is enabled, the MEM Client automatically disables certain functionality in favor of Ivanti Neurons for MDM providing those workloads. For more information, see [**Microsoft's Coexistence documentation**](https://docs.microsoft.com/en-us/mem/configmgr/comanage/coexistence/).

For more exact behaviours when using MEM and other 3rd Party Management platforms, Ivanti suggests to first test the Ivanti Neurons for MDM Deployment Package Tool in your environment.

**Prerequisites**

- User accounts must be imported on Ivanti Neurons for MDM using LDAP, Entra ID (Entra ID), Local User Upload, or other identity integrations
- All devices should have [**Windows Configuration Designer**](https://docs.microsoft.com/en-us/windows/configuration/provisioning-packages/provisioning-install-icd) installed.
- Enable PIN based registration on Ivanti Neurons for MDM
- Users should not have spaces in their username, this may cause a user device transition to fail.
- This tool can be deployed in environments that do not leverage the Entra ID.
- The main elements of Ivanti Neurons for MDM Modern Windows Management Suite does not require Entra ID. Co-management or coexistence may require certain workloads / configurations to be deployed upon silent enrollment, to avoid any impact during transition.
- Deployment Package is currently supported for SCCM and Ivanti Endpoint Manager only.

**Procedure**

1. Go to **Admin>Windows>Deployment Package**.
2. Select **User** or **User Groups** to generate PINs and click **Download Deployment Package** (.zip file).
3. The Deployment Package is given to the SCCM / Ivanti Endpoint Manager administrators to unzip and transfer the files to the respective devices managed by these admins. For information on how to perform this step, see [**Packages and programs in Configuration Manager**](https://docs.microsoft.com/en-us/mem/configmgr/apps/deploy-use/packages-and-programs).
4. After the transfer, administrators remotely trigger the setup.ps1 script on the devices. For information of triggering the script, see [**Create and deploy scripts from the Configuration Manager**](https://docs.microsoft.com/en-us/mem/configmgr/apps/deploy-use/create-deploy-scripts).
5. The devices are enrolled on Ivanti Neurons for MDM.

- The PIN generated for the users are valid for 24 hours only. Once the PIN is expired, new PIN has to be generated.
- The file containing the PINs is deleted from the device post enrollment attempt is complete.

### Enrolling SCCM devices to Ivanti Neurons for MDM

**Procedure**

1. Download all the deployment related files from the Ivanti Neurons for MDM for selected users.
2. Select accounts or groups that should be enrolled.
3. Deploy the Package files to client devices using SCCM:1) Verify if the required clients are present in SCCM. If the Windows-configuration-designer is not present on the client, the admin should push the designer and deploy it on the client.
   2\) On the SCCM server, create a folder and copy the deployment zip file and extract the contents of the file.
   3\) Create a .bat file that will copy the contents of the folder where the files are extracted to the client device.
   4\) In SCCM, go to **Software Library > Application Management > Packages** and create a package to copy the contents of the folder to the client. Enter the destination folder to which you want to copy the contents.
   5\) Deploy the package to the device or device location.
   6\) Under the Monitoring section, you can monitor the deployment status and confirm that the files are copied to the client destination folder.
4. Execute the script to enroll a device:1) Go to **Software Library > Scripts** and create script.
   2\) Enter a name to the script and import the PowerShell script **setup.ps1** from the unzipped folder.
   3\) Approve the script and execute the script on target device.
   4\) Select **Start now** and click **Save**. The Scheduled tasks starts executing the script. On successful execution, the status will become Green.
5. To verify the device enrollment, **Settings** > **Add or remove a provisioning package** > **Details**.

### Enrolling Ivanti Endpoint Manager devices to Ivanti Neurons for MDM

**Procedure**

::::WorkflowBlock
:::WorkflowBlockItem
Download all the deployment related files from the Ivanti Neurons for MDM for selected users.
:::

:::WorkflowBlockItem
Select accounts or groups that should be enrolled.
:::

:::WorkflowBlockItem
**Case 1**: A device name is considered for enrolling the device with the same username - In this case, the email address is not a valid user email address. An email with device name concatenated with the AD domain is considered as the enrollment email address. The admin must set Account as LocalSystemAccount and use setup.ps1 as primary file to initiate the PowerShell execution.

**Case 2**: A valid user email address is considered for enrolling the device and no restrictions on modifying files in the device location - Use the logged in user's email address for enrollment. To enable this enrollment, the admin must set Account as Current user account and use setup.ps1 as primary file to initiate the PowerShell execution.

**Case 3**: A valid email address is considered for enrolling the device with restrictions on modifying files in the device location - Use the logged in user's email address for enrollment. This case has two sub-cases: 

- Using two scripts for enrollment - Create a distribution package with **setupEPMCopyContentsToTempFolderStep1.ps1** and run as Current User Account. The files are copied to a temporary location. Create another distribution package with **setupEPMCopyContentsToTempFolderStep2.ps1** and run as Local System Account.
- In case the device user has restrictions on modifying the folder containing package files - Copy the files to a temporary folder, check the user id and create a PowerShell package. The PowerShell package is executed by the **setupEPMCopyContentsToTempFolderStep2.ps1** script. After the installation, the temporary folder will be deleted.
  Disable/Enable UAC
  1. Update the registry entry to disable UAC control and reboot the machine
  2. Execute the PowerShell package as Current user's account and using setup.ps1
  3. Update the registry entry to enable UAC control and reboot the machine

Create PowerShell package:1) Verify if the required clients are present in the Endpoint Manager.
2\) Copy the files to C:\Program Files\LANDesk\ManagementSuite\LANDesk\files\\. Create a sub-folder within this folder and extract files.
3\) Create Package: **Distribution > Distribution packages > New > Windows > PowerShell**.The admin can distribute the packages to different devices based on the level of restrictions set on devices.
4\) In the Primary file section, enter the package name and upload setup.ps1 from the folder that has the copied files
5\) Under the Additional files section, copy the remaining files (other than setup.ps1 script) using **Add**.
6\) Select Current user's account under the Accounts section.
7\) Click **Save**.
:::

:::WorkflowBlockItem
Create Scheduled task:1) Select the created package, right-click and select **Create Scheduled task(s)**. A Scheduled task is created.
2\) Drag the device and add it to the scheduled package section.
3\) On the Scheduled Package, right-click and select **Properties**.
4\) Verify the Package.
5\) Under Task type, select **Push**.
6\) Select **Start now** and click **Save**. The Scheduled tasks starts executing the script. On successful execution, the status will become Green.
:::

:::WorkflowBlockItem
To verify the device enrollment, **Settings** > **Add or remove a provisioning package** > **Details**. Alternatively, the admin can verify a device enrollment under the Diagnostic Logs of the device.
:::
::::
