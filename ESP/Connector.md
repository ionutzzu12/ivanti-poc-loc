---
title: Connector
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

**License:&#x20;**&#x53;ilver

Ivanti Neurons for MDM Connector provides access from your Ivanti Neurons for MDM service to corporate resources, such as an LDAP server or a Certificate Authority (CA). Set up one Connector per resource that you would like to access.

If you use Microsoft Active Directory or an LDAP server hosted in Amazon Web Services (AWS), you can host Ivanti Neurons for MDM Connector in AWS. No on-premise Connector is required.

The Connector automatically updates to the latest version of the software.

For the latest Ivanti Neurons for MDM Connector Installation Guide, visit [**https://help.ivanti.com/#106**](https://help.ivanti.com/#106) and search for "Connector".

## Connector hosting options

You can host the Ivanti Neurons for MDM Connector on-premise in your datacenter or in Amazon Web Services (AWS):

- Host the Connector in AWS if you are using AWS-hosted Microsoft Active Directory or self-managed Microsoft Active Directory in AWS. You do not need a Connector on-premise in this case.
- To access on-premise resources, such as an LDAP Server or a CA, set up the Connector on-premise.

### Hosting the connector on AWS

Customers can host Connector in AWS for use with the following AWS-hosted Microsoft Active Directory options:

- AWS Directory Service for Microsoft Active Directory
- Customer-managed Microsoft Active Directory in Amazon VPC

For more information on AWS Directory Service for Microsoft Active Directory, see [**https://aws.amazon.com/directoryservice**](https://aws.amazon.com/directoryservice). Refer to AWS documentation on hosting Microsoft Windows Server and Microsoft Active Directory in an Amazon VPC. Ivanti Neurons for MDM Connector supports Windows Server 2012, 2012 R2, 2015.

### Setting up the Ivanti Neurons for MDM Connector AMI in AWS

To set up the Ivanti Neurons for MDM Connector AMI:

1. Log in to AWS with administrator credentials.
2. On the AWS services page, select **EC2** under **Compute**.
3. Expand **Images** and select **AMIs** in the left pane.
4. Select **Public Images** from the drop-down list in the right pane.
5. Search for the Ivanti Neurons for MDM Connector using keywords such as "mobileiron-kocab."
6. Select the latest version of the connector from the list and click **Launch**.
7. Follow the instructions for installing the Connector in the section, "Deploying Ivanti Neurons for MDM Connector in AWS" in the *Ivanti Neurons for MDM Connector Installation Guide* available at [**https://help.ivanti.com/mi/help/en\_us/cld/**](https://help.ivanti.com/mi/help/en_us/cld/)*\<version>*/inst/default.htm, where *version* is the version of the Ivanti Neurons for MDM Connector you are installing. For example, for the version 74 Ivanti Neurons for MDM Connector, find the guide at [**https://help.ivanti.com/mi/help/en\_us/cld/**](https://help.ivanti.com/mi/help/en_us/cld/)**74**/inst/default.htm.

### Hosting the connector on-premise

To host Ivanti Neurons for MDM Connector on-premise in your datacenter, click **Download Connector** to download and set up the Ivanti Neurons for MDM Connector. Extract the contents of the downloaded package and follow the setup instructions in the Ivanti Neurons for MDM Connector Installation Guide included in the package.

## Accessing the Connector logs

You can access the Connector logs from the Connector service to help troubleshoot Connector related problems. You must have System Manager or System Read Only role.

1. Go to **Admin > Connector** to view the Connector page.The Connectors interface displays the Connector status (Enabled or Disabled), Connector Name, Connection (Connected or Not Connected), Version number, Logging Level, Actions (Disable or Remove the Connector).
2. Use the **Logging Level** pulldown menu to choose a level.The available logging levels are displayed in the pulldown menu in order from the lowest logging level to the highest logging level:\* Error
   - Warn
   - Info
   - Debug
   - TraceThe Info level is the default logging level setting. If you choose another logging level a rotating Sync icon

::Image[]{src="Sync_icon.png" signedSrc="Sync_icon.png" size="10" caption alt isUploading="false" sha initialPath="Sync_icon.png" githubPath="Sync_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
appears indicating that information is being collected at the level of logging that you selected. The logging level will reset to the Info level after an hour. The Trace level is the highest logging level setting. Use this level to collect all the messages at all the other levels. The sync icon is displayed for the duration of the request.
:::

3. If needed, hover over the Sync icon

::Image[]{src="Sync_icon.png" signedSrc="Sync_icon.png" size="10" caption alt isUploading="false" sha initialPath="Sync_icon.png" githubPath="Sync_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
to see the Cancel icon
:::

::Image[]{src="Cancel_icon.png" signedSrc="Cancel_icon.png" size="10" caption alt isUploading="false" sha initialPath="Cancel_icon.png" githubPath="Cancel_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
. Click the Cancel icon to cancel the logging level change.
:::

4. Hover over the Request icon to display the Request information. Click the Request icon

::Image[]{src="Fetch_icon.png" signedSrc="Fetch_icon.png" size="10" caption alt isUploading="false" sha initialPath="Fetch_icon.png" githubPath="Fetch_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
to request the files from the current log folder in a .zip file.The log files are added to a .zip file when a request is made.  When a new request is made the .zip file from the previous request is deleted.
:::

5. If needed, hover over the Request icon

::Image[]{src="Fetch_icon.png" signedSrc="Fetch_icon.png" size="10" caption alt isUploading="false" sha initialPath="Fetch_icon.png" githubPath="Fetch_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
and it becomes the Cancel icon
:::

::Image[]{src="Cancel_icon.png" signedSrc="Cancel_icon.png" size="10" caption alt isUploading="false" sha initialPath="Cancel_icon.png" githubPath="Cancel_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
. Click the Cancel icon to stop the request.When a request is canceled before completion, the Download icon
:::

::Image[]{src="Download_icon.png" signedSrc="Download_icon.png" size="10" caption alt isUploading="false" sha initialPath="Download_icon.png" githubPath="Download_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
 is not displayed because the previous log .zip file was deleted from the server. The original log files on the Connector are still available to request.
:::

6. Click the Download icon

::Image[]{src="Download_icon.png" signedSrc="Download_icon.png" size="10" caption alt isUploading="false" sha initialPath="Download_icon.png" githubPath="Download_icon.png" position="flex-start" indent="2"}

:::Paragraph{indent="1"}
when the request is completed to download the log .zip file containing log files collected during the latest request.The log file name  is in the format: kocab.log. The name of the zip file that is downloaded consists of the server name, connection version, and a time stamp including day, month, year, and the time of the day in the format: \<Connector\_Hostname>\_\<Connector\_Version>\_\<TimeStamp>.zip. The archived .zip file name is in the format: kocab.yyyy-mm-dd.0.log.gz.
:::

7. Optionally, use the **Actions** pulldown menu to Disable or Remove the Connector.

If you cannot see the **Connector** page, it might be that you do not have the required permissions. You need one of the following [**roles**](./User_Roles.md):

- System Management
- System Read Only
