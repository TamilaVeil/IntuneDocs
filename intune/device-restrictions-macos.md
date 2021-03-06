---
# required metadata

title: Microsoft Intune device restriction settings for macOS
titlesuffix:
description: Learn the Intune settings you can use to control device settings and functionality on devices running macOS.
keywords:
author: MandiOhlinger
ms.author: mandia
manager: dougeby
ms.date: 3/6/2018
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure

---

# Microsoft Intune macOS device restriction settings

[!INCLUDE [azure_portal](./includes/azure_portal.md)]

This article shows you the Microsoft Intune device restrictions settings that you can configure for devices running macOS.

## Password
- 	**Password** - Require the end user to enter a password to access the device.
	- 	**Required password type** - Specify whether the password can be Numeric only, or whether it must be Alphanumeric (contain letters and numbers). This setting is supported only on Mac OS X version 10.10.3 and later.
	- 	**Number of non-alphanumeric characters in password** - Specify the number of complex characters required in the password (**0** to **4**).<br>A complex character is a symbol, for example "**?**".
	- 	**Minimum password length** - Enter the minimum length of password a user must configure (between **4** and **16** characters).
	- 	**Simple passwords** - Allow the use of simple passwords such as **0000** or **1234**.
	- 	**Maximum minutes after screen lock before password is required** - Specify how long the computer must be inactive before a password is required to unlock it.
	- 	**Maximum minutes of inactivity until screen locks** - Specify the length of time that the computer must be idle before the screen locks.
	- 	**Password expiration (days)** - Specify how many days elapse before the user must change the password (**1** to **255** days).
	- 	**Prevent reuse of previous passwords** - Specify the number of previously used passwords that cannot be reused (**1** to **24**).

## Restricted apps

In the restricted apps list, you can configure one of the following lists:

- A **Prohibited apps** list - List the apps (not managed by Intune) that users are not allowed to install and run. Users are not prevented from installing a prohibited app, but if they do so, this is reported to you.
- An **Approved apps** list - List the apps that users are allowed to install. Users must not install apps that are not listed. Apps that are managed by Intune are automatically allowed. Users are not prevented from installing an app that is not on the approved list, but if they do so, this is reported to you.

To configure the list, click **Add**, then specify a name of your choice, optionally the app publisher, and the bundle ID of the app (for example *com.apple.calculator*).

## Domains

### Unmarked email domains

In the **Email Domain URL** field, add one or more URLs to the list. When users receive an email from a domain other than one you configured, the email is marked as untrusted in the MacOS Mail app.

