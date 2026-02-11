---
title: Certificate Transparency
createdAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:30 GMT+0200 (Eastern European Standard Time)
---

**Applicable to:** iOS 12.1.1, macOS 10.14.2, tvOS 12.1.1, watchOS 10.0+, visionOS 1.1+, and supported newer version.

Controls Certificate Transparency enforcement which can only appear in a device profile. You can include multiple certificates and disable domains as needed.

## Creating a Certificate Transparency configuration

**Procedure**

1. Select **Configurations**.
2. Click **+ Add**.
3. Type **certificate** in the search field, and then click the **Certificate Transparency** configuration.
4. Enter a name and describe the configuration.
5. Specify the **Domains that will be disabled**. Click **+ Add Domain** to add more than one domain. A leading period can be used to match subdomains, however a domain matching rule must not match all the domains within a top level domain. For example, ".example.com" and ".example.co.uk" are allowed while ".com" and ".co.uk" are not allowed. Wildcard domains are not supported.
6. Specify **Certificate Hash** after selecting an algorithm (SHA 256). Click **+ Add** to add more than one certificate hash.
7. Click **Next** to configure the distribution settings.
8. Click **Done**.

To generate the data specified by the Hash key in the subjectPublicKeyInfo dictionary, use the following command for a PEM-encoded certificate:

`openssl x509 -pubkey -in example_certificate.pem -inform pem | openssl pkey -pubin -outform der | openssl dgst -sha256 -binary | base64`

If your certificate is DER-encoded, use the following command:

`openssl x509 -pubkey -in example_certificate.der -inform der | openssl pkey -pubin -outform der | openssl dgst -sha256 -binary | base64`
