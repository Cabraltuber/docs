---
id: other
title: Other
sidebar_label: Other
---

import useBaseUrl from '@docusaurus/useBaseUrl';
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

On this page, we explain step by step how to install **CloudPanel** on a dedicated server or any other cloud. <br />

For the installation, you need an empty server with [Ubuntu 22.04](../../requirements) or [Debian 11](../../requirements) with root access.

## Install CloudPanel

Login via **SSH** to the **Server**.

If you are using a **private key** to login, the SSH command would be:

```bash
ssh -i path_to_your_private_key root@yourIpAddress
```

If you are using a **password** to login, the **SSH command** would be:

```bash
ssh root@yourIpAddress
```

Before running the installer, we need to update the system and install the required packages.

```bash
apt update && apt -y upgrade && apt -y install curl wget sudo
```

<Tabs
defaultValue="ubuntu-22.04"
values={[
{ label: 'Ubuntu 22.04 LTS', value: 'ubuntu-22.04', },
{ label: 'Debian 11 LTS', value: 'debian-11', },
]}>
<TabItem value="ubuntu-22.04">

Run the installer with your preferred **Database Engine**.

<Tabs
defaultValue="ubuntu-mysql-8.0"
values={[
{ label: 'MySQL 8.0', value: 'ubuntu-mysql-8.0', },
{ label: 'MariaDB 10.9', value: 'ubuntu-mariadb-10.9', },
{ label: 'MariaDB 10.8', value: 'ubuntu-mariadb-10.8', },
{ label: 'MariaDB 10.6', value: 'ubuntu-mariadb-10.6', },
]}>
<TabItem value="ubuntu-mysql-8.0">

```bash
curl -sSL https://installer.cloudpanel.io/ce/v2/install.sh | sudo bash
```

</TabItem>
<TabItem value="ubuntu-mariadb-10.9">

```bash
curl -sSL https://installer.cloudpanel.io/ce/v2/install.sh | sudo DB_ENGINE=MARIADB_10.9 bash
```

</TabItem>
<TabItem value="ubuntu-mariadb-10.8">

```bash
curl -sSL https://installer.cloudpanel.io/ce/v2/install.sh | sudo DB_ENGINE=MARIADB_10.8 bash
```

</TabItem>
<TabItem value="ubuntu-mariadb-10.6">

```bash
curl -sSL https://installer.cloudpanel.io/ce/v2/install.sh | sudo DB_ENGINE=MARIADB_10.6 bash
```

</TabItem>
</Tabs>

</TabItem>
<TabItem value="debian-11">

Run the installer with your preferred **Database Engine**.

<Tabs
defaultValue="debian-mysql-8.0"
values={[
{ label: 'MySQL 8.0', value: 'debian-mysql-8.0', },
{ label: 'MySQL 5.7', value: 'debian-mysql-5.7', },
{ label: 'MariaDB 10.9', value: 'debian-mariadb-10.9', },
{ label: 'MariaDB 10.8', value: 'debian-mariadb-10.8', },
{ label: 'MariaDB 10.7', value: 'debian-mariadb-10.7', },
]}>
<TabItem value="debian-mysql-8.0">

```bash
curl -sSL https://installer.cloudpanel.io/ce/v2/install.sh | sudo bash
```

</TabItem>
<TabItem value="debian-mysql-5.7">

```bash
curl -sSL https://installer.cloudpanel.io/ce/v2/install.sh | sudo DB_ENGINE=MYSQL_5.7 bash
```

</TabItem>
<TabItem value="debian-mariadb-10.9">

```bash
curl -sSL https://installer.cloudpanel.io/ce/v2/install.sh | sudo DB_ENGINE=MARIADB_10.9 bash
```

</TabItem>
<TabItem value="debian-mariadb-10.8">

```bash
curl -sSL https://installer.cloudpanel.io/ce/v2/install.sh | sudo DB_ENGINE=MARIADB_10.8 bash
```

</TabItem>
<TabItem value="debian-mariadb-10.7">

```bash
curl -sSL https://installer.cloudpanel.io/ce/v2/install.sh | sudo DB_ENGINE=MARIADB_10.7 bash
```

</TabItem>
</Tabs>

</TabItem>
</Tabs>

## Access CloudPanel

You can now access **CloudPanel** via Browser: **https://yourIpAddress:8443**

Ignore the self-signed certificate warning and click on **Advanced** and **Proceed** to continue to **CloudPanel**.

<img alt="Ignore Self-Signed Certificate" class="border" src={useBaseUrl('img/getting-started/ignore-self-signed-certificate.png')} />
