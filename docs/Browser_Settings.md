---
title: Browser Settings
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

Using Browser Settings, you can configure settings and restrictions for Google Chrome, Mozilla Firefox, Microsoft Edge and Internet Explorer in Windows 10 Devices.

This feature requires Bridge. See [**Ivanti Bridge**](./Ivanti_Bridge.md) for details.

Ensure that the browsers are installed in the device before applying the browser settings.

To configure browser settings:

1. Go to **Configuration > +Add**.
2. Select **Browser Settings** configuration.
3. Enter a name for the configuration.
4. Enter a description.
5. In the Configuration Setup section, specify the remaining settings as described in the following table.|                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
   \| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| **Setting**            | **What To Do**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
   \| **Browsers**           | Select the browser type for which settings are required:\* **Chrome**
   - **Firefox**
   - **Microsoft Edge**
   - **Internet Explorer**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
     \| **Browser settings**   | Configure the following options:**Allow Browsers**:\* Allow saving of Passwords
   - Allow Safe Browsing mode
   - Allow outdated plugins to stay on the browser**Chrome and Firefox**:\* **Allow deleting browser history\*\*\*\*Chrome and Internet Explorer**:\* **Allow browser printing**
   - **New Tab Page URL\*\*\*\*Chrome Only**:\* **Show apps shortcuts in Bookmark Bar**
   - **Show Home button**
   - **Allow synchronization of data with Google**
   - **Continue running background apps when Chrome is closed\*\*\*\*Firefox only**:\* **Allow install extensions\*\*\*\*Internet Explorer Only**:\* **Allow downloading data from websites**                                                                                                                                                                                                                                                                                                                                                                   |
     \| **Browser favorites**  | Click **+Add**.The **Add Browser Favorite** window is displayed. Configure the following fields:\* **Display Name**: Type the display name for the favorite
   - **URL**: type the URL of the browser favorite.Click **Add**.The details of added browser favorite is displayed in the page. In the **Actions** column, click the Edit icon to edit the setting. To delete the browser favorite, click the Delete icon.**Browser Favorites Folder Name**: Type the name of the browser favorites folder name where the favorites should be listed.You can also add browser favorite in a CSV format. To upload in CSV format:1) Click Upload CSV file. Browse and choose the CSV file to be uploaded.

:::Paragraph{listStyleType="decimal" listStart="2" indent="2"}
Click **Upload**.The details in the CSV file should be added in the following format:\* First column (Display Name) should specify the display name of the favorite. Example: "shopping".
:::

:::Paragraph{listStyleType="disc" indent="2"}
Second column (URL) should specify the URL of the favorite. Example: "[**https://amazon.com**](https://amazon.com)". |
\| **Website Security**   | Configure the following website security settings:**All Websites (Chrome and Firefox)**\* **Block Cookies**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Block Javascript**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Block Plugins**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Block Popups**Specific Websites(Chrome Only)**Blockedlisted Websites (Chrome and Edge)**: Add the website that you wish to Blockedlist.Click **+Add**. The **Add Blockedlisted Website** window is displayed.In the **Website URL**, type the URL of the website that should be Blockedlisted.In the **Access** field, select **Block** to Blockedlist the website. The default option is **Allow**.Click **Add**.                                                                                                                                                                                                                                                                                                                                                                                                                |
\| **Browser Extensions** | **Allowed Extension Types (Chrome Only)**: Select any of the following options:\* **Extension**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**User Script**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Themes**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Packaged App**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Hosted App**
:::

:::Paragraph{listStyleType="disc" indent="2"}
**Platform App\*\*\*\*Browser extension sources (Chrome only)**:Click **+Add** to add browser extension sources. After the browser extension sources are added, you can edit or delete the sources by clicking the relevant options in the **Actions** column.**Force-Install Extensions (Chrome Only)**:Click **+Add** to add force-install extensions.After the force-install extensions are added, you can edit or delete the sources by clicking the relevant options in the **Actions** column.                                                                                                                                                                                                                                                                                                                        |
:::

6. Click **Next**.
7. Select one of the following distribution options:\* All Devices
   - No Devices(default)
   - Custom
8. Click **Done**.
