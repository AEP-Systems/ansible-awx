# Introduction

[English](/README.md)

**AWX Automatic Installer**, is an automatic installation program of [AWX](https://github.com/ansible/awx) based on Ansible. It helps users install AWX and pre-configure required items automatically and users only need to run a command on Linux. It simplifies the complicated installation and initialization process.  

## System Requirement

System Requirement to install this repository are as following：

| Conditions       | Details                               | Notes                |
| -------------- | ----------------------------------- | -------------------- |
| Operating System   | CentOS7.x, Ubuntu18.04, Amazon Linux2 | Optional                 |
| Public Cloud     | AWS, Azure, Alibaba Cloud, HUAWEI ClOUD, Tencent Cloud    | Optional                 |
| Private Cloud     | KVM, VMware, VirtualBox, OpenStack    | Optional                 |
| Server Configuration | vCPU no less than 2 core, Memory no less than  4 GIB, Storage no less than 20 GB, Bandwidth no less than 100M ||

To learn more information, please view [System Requirement](https://github.com/ansible/awx/blob/devel/INSTALL.md#system-requirements).

## Ecosystem

Core components of this repository: AWX, PostgreSQL, Redis on Docker

Learn more about [Parameters](/docs/stack-components.md).

## Installation

You can install it by All-in-one Installer. In addition, you can deploy image published on major Cloud Platform by Websoft9.

#### All-in-one Installer

Run the automatic installation script with **root** authority to start the installation. If necessary, users need to make interactive choices, and then wait patiently until the installation is successful.

```
$ sudo su -
$ wget -N https://raw.githubusercontent.com/Websoft9/ansible-linux/main/scripts/install.sh; bash install.sh -r awx
```

If the network is broken or blocked, SSH will be interrupted and the installation will fail. Please reinstall.

#### Image on Cloud 

Follow our [AWX image](https://apps.websoft9.com/awx) for installation on major Cloud Platform.

## Documentation

To get information about initial installation, parameters, default username and password, Configuration, HTTPS, SMTP, Backup, Upgrade and more, please view AWX Administrator Guide. ([English](https://support.websoft9.com/docs/awx) | [简体中文](https://support.websoft9.com/docs/awx/zh))

## Changelog

Detailed changes are documented in the [CHANGELOG](/CHANGELOG.md).

## License

[LGPL-3.0](/License.md), Additional Terms: It is not allowed to publish free or paid image based on this repository in any Cloud platform's Marketplace.

Copyright (c) 2016-present, Websoft9

## FAQ

#### Can I run this repository on Ansible Tower? 

Yes.

#### How to install and view the latest release？

Get the AWX version from [awx releases](https://github.com/ansible/awx/releases), and modify the Ansible variable **[awx_version](/roles/ansible/defaults/main.yml)** to change the AWX version for this repository. 

#### Is the default password safe?

AWX Automatic Installer use the random password solution, every installation have different password, that mean your password is different from other users
