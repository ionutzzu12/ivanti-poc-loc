---
title: Preparing for Android Enterprise device support
createdAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:27 GMT+0200 (Eastern European Standard Time)
---

This section describes the minimum network requirements for Android Enterprise devices. Android devices generally do not require you to open inbound ports on the firewall in order to function correctly. However, there are a number of outbound connections that administrators need to be aware of when setting up their network environments for Android Enterprise devices.

The list of network changes provided in the following table is not exhaustive and may change. It covers known endpoints for current and past versions of enterprise management API and GMS apps.

In addition to the ports listed in the following table, Android Enterprise devices require access to Ivanti Neurons for MDM.

For information about the requirements for Android Enterprise devices, see [**Android Enterprise Network Requirements**](https://support.google.com/work/android/answer/10513641?hl=en) from the Android Enterprise Help.

Google does not provide specific IPs, so you should allow your firewall to accept outgoing connections to all IP addresses contained in the IP block listed in Google's ASN of 15169 listed here [**http://bgp.he.net/AS15169#\_prefixes**](http://bgp.he.net/AS15169#_prefixes).

IPs of Google peers and edge nodes are not listed in the AS15169 blocks. See [**https://peering.google.com/**](https://peering.google.com/) for more information about Google's Edge Network.
