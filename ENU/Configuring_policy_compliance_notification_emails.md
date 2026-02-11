---
title: Configuring policy compliance notification emails
createdAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
---

## Configuring and using policy compliance notification emails

Administrators can wrap in a policy compliance notification email template the emails sent by the Custom and Allowed Apps policies' send email actions to users whose devices have fallen out of compliance. The following process describes the configuration:

- **Configuring the feature:**\* **Configure the email template**.The English email template looks like this by default, but you can revise it to better suit your purposes by following the instructions at [**Customizing an email template**](./Branding_Email_Templates.md) in [**Branding Email Templates**](./Branding_Email_Templates.md):

::Image[]{src="Resources/Images/68PolicyEmailTemplate.png" signedSrc="Resources/Images/68PolicyEmailTemplate.png" size="40" caption alt isUploading="false" sha initialPath="Resources/Images/68PolicyEmailTemplate.png" githubPath="Resources/Images/68PolicyEmailTemplate.png" position="flex-start" indent="2"}

:::Paragraph{listStyleType="disc" indent="2"}
**Turn on the policy compliance notification template**. This template works in conjunction with the message you craft using the Custom and Allowed Apps policies' send email actions. Ivanti Neurons for MDM inserts the information you specify in those email actions into the policy compliance notification template. You can turn on the policy compliance email template when you create or edit a Custom or Allowed Apps policy. For more information about instructions on enabling the policy compliance notification template for a Custom policy or Allowed apps policy, see [**Adding a custom policy**](./Custom_Policy.md) and [**Creating an Allowed Apps policy**](./Monitoring_and_Controlling_Allowed_Apps.md) respectively.
:::

- **Using the feature:**\* When a device falls out of compliance with a Custom or Allowed apps policy with the policy notification template enabled, Ivanti Neurons for MDM sends the device owner an email, first wrapping the email in the policy notification template. Your interaction with the feature is to configure it as summarized above, whereas Ivanti Neurons for MDM itself uses the feature.
