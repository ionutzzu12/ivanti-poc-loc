---
title: Prioritizing Policies
createdAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 15:31:33 GMT+0200 (Eastern European Standard Time)
---

The Allowed Apps policy supports a priority, similar to Configurations. A priority is used to determine which policy of the same type is distributed to multiple device groups, and the case where the same device appears in those multiple device groups. For example, a policy priority is useful to determine policy distribution in the case where:

- "Required App A" needs to be distributed to Device Group 1,
- "Required App B" needs to be distributed to Device Group 2, and
- The user's device is a member of both device groups.

You can prioritize policies as follows:

1. Go to **Policies > Policy & Compliance**.
2. Select **Actions > Prioritize policies**. If **Actions** is not displayed, then you do not have multiple policies requiring priorities.
3. Use the arrows to list priorities from highest (top) to lowest (bottom). A lock icon means the policy's priority cannot be changed without editing the All Devices distribution setting within the policy.
4. Click **Save**.
