---
localization_priority: Normal
description: You can specify the number of sequential unsuccessful sign-in attempts that are allowed before a caller is disconnected. The value of this setting can be from 1 through 20. Setting this value too low can frustrate users. For most organizations, this value should be set to the default of three attempts.
ms.topic: article
author: chrisda
ms.author: chrisda
ms.assetid: 02f93888-168c-44bb-8cf6-17f5fcc3d733
ms.date: 11/17/2014
ms.reviewer: 
title: Configure the number of sign-in failures before Outlook Voice Access users are disconnected in Exchange Online
ms.collection: exchange-online
audience: ITPro
ms.service: exchange-online
manager: dansimp

---

# Configure the number of sign-in failures before Outlook Voice Access users are disconnected in Exchange Online

You can specify the number of sequential unsuccessful sign-in attempts that are allowed before a caller is disconnected. The value of this setting can be from 1 through 20. Setting this value too low can frustrate users. For most organizations, this value should be set to the default of three attempts.

For additional management tasks related to UM dial plans, see [UM Dial Plan Procedures](https://technet.microsoft.com/library/1bda77c8-c4e2-4ae0-a001-76ae029bf843.aspx).

## What do you need to know before you begin?

- Estimated time to complete: Less than 1 minute.

- You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "UM dial plans" entry in the [Unified Messaging Permissions](https://technet.microsoft.com/library/d326c3bc-8f33-434a-bf02-a83cc26a5498.aspx) topic.

- Before you perform these procedures, confirm that a UM dial plan has been created. For detailed steps, see [Create a UM dial plan](../../voice-mail-unified-messaging/connect-voice-mail-system/create-um-dial-plan.md).

- For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center](../../accessibility/keyboard-shortcuts-in-admin-center.md).

> [!TIP]
> Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351)..

## Use the EAC to configure the number of sign-in failures before users are disconnected

1. In the EAC, navigate to **Unified Messaging** \> **UM dial plans**.

2. In the list view, select the UM dial plan you want to modify, and then click **Edit** ![Edit icon](../../media/ITPro_EAC_EditIcon.gif).

3. On the **UM dial plan** page, click **Configure**.

4. In **Settings**, under **Number of sign-in failures before disconnecting**, enter the number of sign-in failures.

5. Click **Save**.

## Use Exchange Online PowerShell to configure the number of sign-in failures before users are disconnected

This example sets the number of sign-in failures before users are disconnected to 5 for a UM dial plan named `MyUMDialPlan`.

```
Set-UMDialPlan -identity MyUMDialPlan -LogonFailuresBeforeDisconnect 5
```
