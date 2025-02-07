---
id: settings
title: Settings
sidebar_label: Settings
---

import useBaseUrl from '@docusaurus/useBaseUrl';

:::warning CloudPanel v1 is obsolete
CloudPanel v1 is **obsolete**; check out the [CloudPanel v2 Docs](https://www.cloudpanel.io/docs/v2/introduction/).
:::

## Settings

### Proftpd Settings

For connecting via **FTP** you need to enter the **Server IP** in the field **MasqueradeAddress**.

The **MasqueradeAddress** causes the server to display the network information for the specified IP address or DNS hostname to the client, 
on the assumption that the IP address or DNS host is acting as a NAT gateway or port forwarder for the server.

<img class="border" src={useBaseUrl('img/v1/admin/settings/proftpd_settings.png')} />