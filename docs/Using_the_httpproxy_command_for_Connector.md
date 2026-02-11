---
title: Using the httpproxy command for Connector
createdAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:34 GMT+0200 (Eastern European Standard Time)
---

A new klish shell command has been created to help edit Connector configuration for your Ivanti Neurons for MDM installation. Use this command to change the login information and other parameters to configure the connector.

The httpproxy command is now available in this release with these requirements.

- klish shell

To configure your connector

1. Log in to klish shell.
2. Enter a ? for a list of available klish shell commands.
3. Enter **httpproxy** to show the current value of these parameters:1) enabled
   2\) scheme
   3\) server
   4\) authtype
   5\) username
   6\) password
4. Enter **httpproxy ?** to see a list commands available for use with httpproxy.1) authtype - Set the authentication type of the http proxy to NONE, BASIC, or NTLM
   2\) disable - Disable the http proxy
   3\) enable - Enable the http proxy
   4\) host - Set the host of the http proxy - must be an FQDN or an IP either http or https
   5\) password - Set the Authentication password of the http proxy
   6\) port - Set the port of the http proxy
   7\) scheme - Set the scheme of the http proxy - must be either http or https
   8\) show - Show the current http proxy settings
   9\) username - Set the authentication username of the http proxy
5. Use the commands listed above to setup your connector instance.
