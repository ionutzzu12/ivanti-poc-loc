---
title: Managing Content
createdAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:29 GMT+0200 (Eastern European Standard Time)
---

This section contains the following topics:

- [**Distributing Hosted Content**](./Managing_Content.md)
- [**Deleting content**](./Managing_Content.md)

Hosted Content supports the distribution of downloadable content with external URLs. External URL should lead to a downloadable PDF or EPUB or IBOOK files only and external URL must have these extensions.

Distribution of VPP Book licenses are not supported, hence the distribution of Apple Books based on iTunes Store ID are not supported.

Use Books or Pages app on device to access the pushed content from Ivanti Neurons for MDM. You can access them in Library section.

**iBook and EPUB** content can be distributed to iOS 8+ iPad devices (Gold license). These formats are restricted to iPad because Apple supports in-house distribution of these formats only to iPad. This restriction does not apply to iOS 9 devices.

Content previews are not available for these formats.

For **PDF** content, you have the option of pushing the document to the iBook app on iOS 8+ devices.

## Distributing Hosted Content

Though you cannot upload new documents to Ivanti Neurons for MDM, you can provide a path (URL) where the content is hosted and distribute it to the device groups.

**Procedure**

1. Go to **Content > Hosted Content**.
2. Click **+ Add**.
3. Enter the following information:\* Title
   - Author
   - Category
   - (Optional) Description
4. In the **Hosted Content Path** field, enter a URL for the file you would like to upload.
5. Click **Next**.
6. Make any necessary changes to the distribution.
7. Click **Done**.

To modify Hosted Content, the previous content has to be deleted, new Hosted Content has to be added and distributed.

To modify the settings other than the URL:

1. Go to **Content > Hosted Content**.
2. Click the link to the document in the **Name** column.
3. Click the Edit icon.
4. Make the required changes.
5. Click **Next**.
6. Make any necessary changes to the distribution.
7. Click **Done**.

## Deleting content

1. Click the link to the document in the **Name** column.
2. Select **Actions > Delete This Document**.
3. Click the check box to confirm.
4. Click **Delete Document**.

When you delete a document:

- It is removed from the system.
- It is no longer available in the content catalog.
- It is removed from devices that have downloaded it.

If you cannot perform tasks on the **Content** page, it might be that you do not have the required permissions. You need the following [**role**](./User_Roles.md):

- App & Content Management
