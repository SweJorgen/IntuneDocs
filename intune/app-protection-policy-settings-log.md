---
# required metadata

title: App protection policy logs
titlesuffix: "Azure portal"
description: This topic describes the record of app protection policy settings stored in the app logs.
keywords:
author: erikre
ms.author: erikre
manager: angrobe
ms.date: 11/15/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 4CD5EE94-7BA6-4F59-8E28-1EBCA7CA6436

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: andcerat
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure

---

# Review app protection logs in the Managed Browser

You can access the logs by enabling Intune Diagnostics Mode for an application on a mobile client. The following table shows the name and an explanation of the settings recorded in the log.

## App protection policy settings

| Name                        | Possible Value(s)​                                                                                                                                                                                                                                                                                           | Setting in Azure Intune Mobile Application Management portal​                                                                                                                            |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AccessRecheckOfflineTimeout​ | x minutes                                                                                                                                                                                                                                                                                                   | [Access] Recheck access requirements - Offline Grace Period<br>Note: This is the time period before access requirements for the app are rechecked if the device is offline.             |
| AccessRecheckOnlineTimeout​  | _x_ minutes                                                                                                                                                                                                                                                                                                   | [Access] Recheck access requirements - Timeout.<br>Note: This is the time period before access requirements for the app are rechecked after the app is launched if the device is online. |
| AppPinDisabled​              | 0 = No​<br>1 = Yes                                                                                                                                                                                                                                                                                           | [Access] Disable app PIN when device PIN is managed​.                                                                                                                                     |
| AppSharingFromLevel​         | 0 = No apps​<br>1 = Managed apps<br>2 = Any app.                                                                                                                                                                                                                                                              | [Data Relocation] Allow this app to receive data from other apps.​                                                                                                                        |
| AppSharingToLevel​           | 0 = No apps​<br>1 = Managed apps<br>2 = Any app.                                                                                                                                                                                                                                                              | [Data Relocation] Allow this app to transfer data to other apps​..                                                                                                                         |
| AuthenticationEnabled​       | 0 = No​<br>1 = Yes                                                                                                                                                                                                                                                                                           | [Access] Require corporate credentials for access instead of a PIN​.                                                                                                                      |
| ClipboardSharingLevel​       | 0 = Blocked​<br>1 = Managed apps.<br>2 = Managed apps with paste in.<br>3 = Any app                                                                                                                                                                                                                            | [Data Relocation] Restrict cut, copy, and paste with other apps​.                                                                                                                         |
| ContactSyncDisabled​         | 0 = No​<br>1 = Yes                                                                                                                                                                                                                                                                                           | [Data Relocation] Disable contacts sync​.                                                                                                                                                 |
| DataBackupDisabled​          | 0 = No​<br>1 = Yes​                                                                                                                                                                                                                                                                                           | [Data Relocation] Prevent iTunes and iCloud backups.​                                                                                                                                     |
| DeviceComplianceEnabled​     | 0 = No​<br>1 = Yes​                                                                                                                                                                                                                                                                                           | [Access] Block managed apps from running on jailbroken or rooted devices.​                                                                                                                |
| DisableShareSense​           | ​N/A                                                                                                                                                                                                                                                                                                         | N/A: not actively used by Intune service.​                                                                                                                                                |
| FileEncryptionLevel​         | 0 = When device is locked​<br>1 = When device is locked and there are open files​<br>2 = After device restart​<br>3 = Use device settings​.                                                                                                                                                                      | [Data Relocation] Encrypt app data​.                                                                                                                                                      |
| FileSharingSaveAsDisabled​   | 0 = No​<br>1 = Yes​                                                                                                                                                                                                                                                                                           | [Data Relocation] Prevent “Save As” ​                                                                                                                                                    |
| IntuneIdentityUPN​           | UPN of the Intune MAM user.                                                                                                                                                                                                                                                                                  | N/A​                                                                                                                                                                                     |
| ManagedBrowserRequired​      | 0 = No​<br>1 = Yes​                                                                                                                                                                                                                                                                                           | [Data Relocation] Restrict web content to display in the Intune Managed Browser app​.                                                                                                     |
| ManagedLocations​            | A value that represents the number of managed storage locations to which the app can save data.​ <br>1 = OneDrive<br>2 = SharePoint<br>3 = OneDrive and SharePoint<br>32 = Local Storage<br>33 = Local Storage & OneDrive<br>34 = Local Storage & SharePoint<br>35 = Local Storage, OneDrive, and SharePoint | [Data Relocation] Select which storage services corporate data can be saved to​.                                                                                                          |
| MinAppVersion​               | ”0.0” = no minimum app version​<br>anything else = minimum app version                                                                                                                                                                                                                                       | [Access] Require minimum app version.                                                                                                                                                    |
| MinAppVersionWarning​        | ”0.0” = no minimum app version​.<br>anything else = minimum app version​.                                                                                                                                                                                                                                       | [Access] Require minimum app version (warning only)​                                                                                                                                     |
| MinOsVersion​                | ”0.0” = no minimum OS version​<br>anything else = minimum OS version​                                                                                                                                                                                                                                         | [Access] Require minimum iOS operating system​.                                                                                                                                           |
| MinOsVersionWarning​         | ”0.0” = no minimum OS version​<br>anything else = minimum OS version​                                                                                                                                                                                                                                         | [Access] Require minimum iOS operating system (warning only).​                                                                                                                            |
| MinSDKVersion​               | ”0.0” = no minimum SDK version​<br>anything else = minimum OS version.​                                                                                                                                                                                                                                        | [Access] Require minimum Intune app protection policy SDK version​.                                                                                                                       |
| PINCharacterType​            | ​N/A                                                                                                                                                                                                                                                                                                         | N/A                                                                                                                                                                                     |
| PINEnabled​                  | 0 = No​<br>1 = Yes​                                                                                                                                                                                                                                                                                           | [Access] Require PIN for access​                                                                                                                                                         |
| PINMinLength​                | x characters                                                                                                                                                                                                                                                                                                | [Access] PIN length​                                                                                                                                                                     |
| PINNumRetry​                 | x attempts                                                                                                                                                                                                                                                                                                  | [Access] Number of attempts before PIN reset​                                                                                                                                            |
| PrintingBlocked​             | 0 = No​<br>1 = Yes​                                                                                                                                                                                                                                                                                           | [Data Relocation] Disable printing​                                                                                                                                                      |
| SimplePINAllowed​            | 0 = No<br>1 = Yes​​                                                                                                                                                                                                                                                                                           | [Access] Allow Simple PIN​                                                                                                                                                               |
| TouchIDEnabled​              | 0 = No​<br>1 = Yes​                                                                                                                                                                                                                                                                                           | [Access] Allow fingerprint instead of PIN (iOS 8+)​.                                                                                                                                      |

## Next steps

 - To learn more about app protection policies, see [What are app protection policies?](app-protection-policy.md)
 - Intune offers a number of tools to help you troubleshoot issues in your environment. For more information, see [Use the troubleshooting portal to help users](help-desk-operators.md).