---
title: Branding Email Templates
createdAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:35 GMT+0200 (Eastern European Standard Time)
---

You can brand the end user email invitation to make its appearance more familiar to your end users. Click **Revert to Default Settings** to clear the customizations.

You can customize the following email templates in all of your supported languages:

- **End User Invitation**- Invite a user to connect their devices to get access to apps and configurations.
- **Password Reset Notification**- The system sends reminder emails 7-days and a 24-hours prior to the password expiration for local accounts. This does not apply to LDAP accounts.
- **Registration Confirmation**- Email sent after a user completes registration. You can use this to thank users for registering and to point them to more learning resources.
- **Policy Compliance Notification**- Email sent when devices go out of compliance.

This section contains the following topics:

- [**Previewing and testing an email template**](./Branding_Email_Templates.md)
- [**Customizing the message headers**](./Branding_Email_Templates.md)
- [**Customizing an email template**](./Branding_Email_Templates.md)
- [**Supported email variables**](./Branding_Email_Templates.md)

## Previewing and testing an email template

You can preview and test the email templates. The test allows you to send an email based on the template to an email address you specify.

To preview and test an email template:

1. Click **Admin**.
2. Under Email Templates, click **End User Invitation**, **Password Reset Notification**, **Registration Confirmation**, or **Policy Compliance Notification**.
3. Click the **Preview and Test** link associated with the email template you wish to preview and test.
4. View the rendered template in the rendered template pane.
5. Specify a test email address to which to send the test email.If the email address you specify belongs to a current user, the test email substitutes values for most of the email template variables, affording a very accurate idea of the user experience of the email. However, the test email does not substitute values for variables Ivanti Neurons for MDM generates at the time it generates an actual email invitation.
6. Click **Send Test Email**.

## Customizing the message headers

1. Click **Admin**.
2. Click **Email Templates**.
3. Click the **Edit** icon link (under Actions column) associated with the email template you wish to edit.
4. Provide new settings as desired for **Email Display Name**, **From Email Address**, **Reply-to Email Address**, and **Set up SMTP Email Configuration**.
5. If you customize the From and Reply-To email addresses, it is recommended that you Allowlist the Email Relay Service to ensure that your emails aren't blocked by email SPAM filtering services. See [**this document**](https://forums.ivanti.com/s/article/MobileIron-Cloud-Ports-Hosts-and-IP-Addresses) for more information.
   Click **Save**.
6. Review the preview of the email template and click **Save**.

## Using SMTP configuration

The **Set up SMTP Email Configuration** is added to enable the admin to configure their own email server integration for outbound notifications.

1. Go to **Admin > Branding > Email Settings**, enable the **Set up SMTP Email Configuration** option.
2. Update the following feilds:\* SMTP server
   - SMTP server port
   - Protocol
   - User Name
   - Password
3. Click **Test** to send a test mail, a **Test Email** pop-up screen is displayed.
4. Enter the **Recipient** name and **Body** of the message, click **Save**.If the credentials are not correct, and error message is displayed.
5. Click **Save**

The following table summarizes fields and descriptions in the SMTP Configuration window:

| Fields           | Description                                                                                                                                                    |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SMTP Server      | Specify the IP address or fully-qualified host name for the SMTP server the Ivanti Neurons for MDM Server will use.                                            |
| SMTP Server Port | Specify the port configured for the SMTP server.                                                                                                               |
| Protocol         | If the SMTP server you are configuring is a secured server, that is, it uses the SMTPS protocol, then select the SMTPS button. Otherwise, leave SMTP selected. |
| User Name        | Enter the user name required for SMTP authentication.                                                                                                          |
| Password         | Enter the password required for SMTP authentication.                                                                                                           |

## Customizing an email template

1. Select **Admin > Branding > Email Templates**.
2. Select the template to edit, **End User Invitation**, **Password Reset Notification**, **Registration Confirmation**, or **Policy Compliance Notification**.
3. Click the edit pen icon adjacent to the email template you wish to customize.

::Image[]{src="r45emailtemplates003.png" signedSrc="r45emailtemplates003.png" size="35" caption alt isUploading="false" sha initialPath="r45emailtemplates003.png" githubPath="r45emailtemplates003.png" position="flex-start" indent="2"}

4. Edit the subject line if desired.
5. Edit the email template containing HTML elements in the body pane to customize the message content.|                    |                                                                                                                    |
   \| ------------------ | ------------------------------------------------------------------------------------------------------------------ |
   \| :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/BbT7KQqqvz3LSYn2rwmao/e_ESs4BbLSU2XlMRzC9OR_infoicon.png" alt caption} | You can use the variables displayed on the right in the body of the email. See [**Supported email variables**](./Branding_Email_Templates.md). |
6. Click **Preview** to preview the email template as you create iterations to your satisfaction.
7. When you are ready to save the template, click **Preview**. This renders the preview and provides a save function.

::Image[]{src="r45emailtemplates004.png" signedSrc="r45emailtemplates004.png" size="19" caption alt isUploading="false" sha initialPath="r45emailtemplates004.png" githubPath="r45emailtemplates004.png" position="flex-start" indent="2"}

8. Click **Save** if you are satisfied with the preview.

### Allowlisted and Blockedlisted content in customized user invitation

While customizing the user invitation email template in **End user invitation**, there are a set of Allowlisted HTML tags and attributes that are allowed. There are also a list of Blockedlisted strings that are not allowed in the user invitation to prevent Cross Site Scripting (XSS) vulnerability.

You are allowed to use only the Allowlisted tags and attributes in the invitation email. The following table list the Allowlisted tags and the corresponding attributes that are allowed.

Some Allowlisted tags(Example: \<big>) should not have any Allowlisted attribute and therefore are displayed blank.

| Allowlisted Tags | Allowlisted Attributes                                                                                                                                             |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| \<big>           | \[]                                                                                                                                                                |
| \<img>           | \["id","label","editable","height","border","src","style","width", "align", "class","cellpadding","alt","title","data-max-width","data-default"]                   |
| \<strong>        | \[]                                                                                                                                                                |
| \<singleline>    | \["label"]                                                                                                                                                         |
| \<tbody>         | \[]                                                                                                                                                                |
| \<!DOCTYPE>      | \[]                                                                                                                                                                |
| \<h1>            | \["style"]                                                                                                                                                         |
| \<h2>            | \["style"]                                                                                                                                                         |
| \<hr>            | \["noshade","style"]                                                                                                                                               |
| \<h3>            | \[]                                                                                                                                                                |
| \<body>          | \["style", "class", "bgcolor", "paddingwidth", "paddingheight", "offset", "toppadding", "leftpadding", "lang","link","vlink","border","cellspacing","cellpadding"] |
| \<title>         | \["id"]                                                                                                                                                            |
| \<head>          | \[]                                                                                                                                                                |
| \<div>           | \["style","class","width","align","id"]                                                                                                                            |
| \<br>            | \[]                                                                                                                                                                |
| \<path>          | \["d"]                                                                                                                                                             |
| \<ul>            | \["style"]                                                                                                                                                         |
| \<html>          | \["xmlns","xmlns\:mso","xmlns\:msdt"]                                                                                                                              |
| \<ol>            | \["start"]                                                                                                                                                         |
| \<table>         | \["class","width","border","cellspacing","cellpadding","style","height","bgcolor","align","background"]                                                            |
| \<a>             | \["href","style","target","rel","class","title"]                                                                                                                   |
| \<b>             | \[]                                                                                                                                                                |
| \<o\:p>          | \[]                                                                                                                                                                |
| \<svg>           | \["xmlns","class","viewbox","width","height","role","aria-labelledby"]                                                                                             |
| \<center>        | \[]                                                                                                                                                                |
| \<em>            | \[]                                                                                                                                                                |
| \<i>             | \[]                                                                                                                                                                |
| \<label>         | \["style"]                                                                                                                                                         |
| \<td>            | \["valign","width","height","class", "cellpadding", "cellspacing","border","bgcolor","align", "style","colspan","id"]                                              |
| \<p>             | \["style","class","align"]                                                                                                                                         |
| \<u>             | \[]                                                                                                                                                                |
| \<meta>          | \["name","content","http-equiv","charset"]                                                                                                                         |
| \<multiline>     | \["label"]                                                                                                                                                         |
| \<style>         | \["type","id"]                                                                                                                                                     |
| \<li>            | \["style"]                                                                                                                                                         |
| \<tr>            | \["style"]                                                                                                                                                         |
| \<span>          | \["style","class","lang"]                                                                                                                                          |
| \<font>          | \["color"]                                                                                                                                                         |

The following are the list of Blockedlisted strings that are not allowed in the customized user invitation.

- Script, @import, ¼script¾, script>, \<script, \<script>, \</script>, javascript, alert(, moz-binding, expression(, +ADw-SCRIPT+AD4- ,+ADw-/SCRIPT+AD4-, xml\:base
- Special characters and search for javascript or script
- The meta content attribute containing "url=" case insensitive
- The img src not containing .svg.
- Attribute value containing "\00"

If any of the above Blockedlisted strings are used in the HTML content of the end user invitation, an error message is displayed when you click **Preview**. This error message lists the HTML content that is not allowed in the end user invitation. Edit and remove the HTML content that is not allowed and then click **Preview** to proceed further.

You will not be allowed to save the edited templates containing Blockedlisted HTML content.

## Supported email variables

Ivanti Neurons for MDM offers several variables you can use to customize your email templates.

### End user invitation variables

| Variable                                                 | Description                                                                                                                                           |
| -------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| $\{userActivationUrl}                                    | The user activation URL - this is the hyperlink around the $\{email.idp.invitation.get.started} text.                                                 |
| $\{clusterRegistrationUrl}                               | The cluster registration URL - it is NOT found in the default template, but is referenced indirectly (via the $\{email.idp.invitation.pg4} variable). |
| $\{productBrandName}                                     | The product brand name - this is defined as the \<title> tag in the header of the default template.                                                   |
| $\{companyLogoUrl}                                       | The company Logo URL - this is the one image in the default template - it points to an image in the Mobilelron CDN.                                   |
| $\{message:$\{email.idp.invitation.register.your.device} | The register the user device title.                                                                                                                   |
| $\{message:$\{email.idp.invitation.title}}               | Email invitation title.                                                                                                                               |
| $\{message:$\{email.idp.invitation.pg1}}                 | Verification that the user in on their device.                                                                                                        |
| $\{message:$\{email.idp.invitation.get.started}}         | The email invitation Get Started text.                                                                                                                |
| $\{message:$\{email.idp.invitation.pg2}}                 | Login and registration instructions.                                                                                                                  |
| $\{message:$\{email.idp.invitation.pg3}}                 | Email and apps pushed to the device information.                                                                                                      |
| $\{message:$\{email.idp.invitation.pg4}}                 | Registration information if the user is not on their device, which includes the cluster registration URL.                                             |
| $\{message:$\{email.footer}}                             | The email invitation footer that includes the company website label.                                                                                  |
| $\{companyWebsiteLabel}                                  | The company website label - it is NOT found in the default template, but is referenced indirectly (via the $\{email.footer} variable) .               |

### Password expiration notification variables

| Variable                                               | Description                                                                                                                             |
| ------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------- |
| $\{passwordResetUrl}                                   | The password reset URL.                                                                                                                 |
| $\{productBrandName}                                   | The product brand name - this is defined as the \<title> tag in the header of the default template.                                     |
| $\{companyLogoUrl}                                     | The company Logo URL - this is the one image in the default template - it points to an image in the Mobilelron CDN.                     |
| $\{message:$\{password.expiration.notification.title}} | The password expiration notification title.                                                                                             |
| $\{message:$\{password.expiration.notification.pg1}}   | The password expiration notification introductory paragraph.                                                                            |
| $\{message:$\{email.password.reset.url.name}}          | The password reset URL name.                                                                                                            |
| $\{message:$\{email.footer}}                           | The email invitation footer that includes the company website label.                                                                    |
| $\{companyWebsiteLabel}                                | The company website label - it is NOT found in the default template, but is referenced indirectly (via the $\{email.footer} variable) . |

### Registration confirmation variables

| **Variable**                             | **Description**                                                                                                     |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| $\{productBrandName}                     | The product brand name - this is defined as the \<title> tag in the header of the default template.                 |
| $\{companyLogoUrl}                       | The company Logo URL - this is the one image in the default template - it points to an image in the Mobilelron CDN. |
| $\{message:$\{email.confirmation.title}} | The registration confirmation title.                                                                                |
| $\{message:$\{email.confirmation.pg1}}   | The registration confirmation introductory paragraph.                                                               |

### Policy compliance variables

| Variable                     | Description                                                                                                                                   |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| $\{policyMessageTitle}       | This variable will be replaced by the content that is entered into the subject line in the send email compliance action within the policy.    |
| $\{policyMessageContent}     | This variable will be replaced by the content that is entered into the message portion in the send email compliance action within the policy. |
| $\{productBrandName}         | The product brand name - this is defined as the \<title> tag in the header of the default template.                                           |
| $\{companyLogoUrl}           | The company Logo URL - this is the one image in the default template - it points to an image in the Mobilelron CDN.                           |
| $\{message:$\{email.footer}} | The email invitation footer that includes the company website label.                                                                          |
| $\{companyWebsiteLabel}      | The company website label - it is NOT found in the default template, but is referenced indirectly (via the $\{email.footer} variable) .       |

### Custom user attribute variables

An admin can use [**custom user attributes**](./Attributes.md) as email variables in the customized email template under the following conditions:

- The custom user attributes exist on the **Admin > Attributes** page.
