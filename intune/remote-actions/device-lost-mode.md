---
# required metadata

title: Activate iOS lost mode with Microsoft Intune - Azure | Microsoft Docs
description: Turn on or start lost mode to customize a message that appears on the lock screen of a lost or stolen iOS device by using Microsoft Intune. And, get details on security and privacy information when you are using the lost mode action.
keywords:
author: ErikjeMS
ms.author: erikje
manager: dougeby
ms.date: 04/25/2018
ms.topic: conceptual
ms.service: microsoft-intune
ms.subservice: remote-actions
ms.localizationpriority: high
ms.technology:
ms.assetid: 126a7489-fe3e-43fd-a681-defb2fe0bb66

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
#ms.reviewer: coferro
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure
ms.collection: M365-identity-device-management
---

# Enable lost mode on iOS devices with Intune

[!INCLUDE [azure_portal](../includes/azure_portal.md)]

The **Lost mode** device action helps you enable lost mode on lost or stolen iOS devices. This mode lets you enter a message and a phone number that appears on the lock screen of the device. To use lost mode, the device must be a corporate-owned iOS device that is in supervised mode.

## Supported platforms

- iOS 9.3 and later

This feature is not supported for the following: 
- Windows
- Windows Phone
- macOS
- Android

## Enable lost mode

1. Sign in to [Intune](https://go.microsoft.com/fwlink/?linkid=2090973).
3. Select **Devices**, and then select **All devices**.
4. From the list of devices you manage, choose an iOS device, and then choose the **Lost mode (supervised only)**.
5. Under **Lost mode**, select **Enable**.
6. In the **Message to display on lock screen**, type a message to display on the device's lock screen.
7. Optionally, enter a phone number in the **Phone number to display** box.
6. Select **OK** to save your changes.

When you enable lost mode, all use of the device is blocked. The end user cannot access the device until you disable lost mode. While lost mode is enabled, use the [Locate device](device-locate.md) action to find the device.

## Security and privacy information for the lost mode and locate device actions
- No device location information is sent to Intune until you turn on this action.
- When you use the locate device action, the latitude and longitude coordinates of the device are sent to Intune, and shown in the Azure portal.
- The data is stored for 24 hours, then removed. You cannot manually remove the location data.
- Location data is encrypted, both while stored, and while being transmitted.
- In the message you enter to show on the lock screen, be sure to include specific details to return the lost device.

## Next steps

To see the status of enabling lost mode, open **Devices**, and select **Device actions**.
