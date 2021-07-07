---
title: Planning How to Save and Deploy the DaRT 10 Recovery Image
description: Planning How to Save and Deploy the DaRT 10 Recovery Image
author: dansimp
ms.assetid: 9a3e5413-2621-49ce-8bd2-992616691703
ms.reviewer: 
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 04/20/2021
---

# Planning How to Save and Deploy the DaRT 10 Recovery Image

You can save and deploy the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image by using the following methods. When you are determining the method that you will use, consider the advantages and disadvantages of each. You should also consider your infrastructure and support staff. If you have a small infrastructure, you might want to deploy DaRT 10 by using removable media, since the recovery image will always be available if you install it to the local hard drive.

If your organization uses Active Directory Domain Services (AD DS), you may want to deploy recovery images as a network service by using Windows DS. Recovery images are always available to any connected computer. You can deploy multiple images from Windows DS and maintain them all in one place.

> [!NOTE]
> You may want to use more than one method in your organization. For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.

The following table shows some advantages and disadvantages of each method of using DaRT in your organization.

<table style="table-layout:fixed">
<thead>
<tr class="header">
<th>Method to Boot into DaRT</th>
<th>Advantages</th>
<th>Disadvantages</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>

**Removable Media:** The recovery image is written to a CD, DVD, or USB flash drive to enable the support staff to take the recovery tools with them to the unstable computer.

</td>
<td>

- Supports scenarios in which the master boot record (MBR) is corrupted (thus, you cannot access the hard disk) or cases in which there is no network connection.
- Enables you to create multiple recovery images with different tools to provide different levels of support.
- Provides a built-in tool for burning recovery images to removable media

</td>
<td>

- Requires the support staff to be physically at the end-user computer.
- Requires time and maintenance to create multiple media with different configurations for x86 and x64 computers.

</td>
</tr>
<tr class="even">
<td>

**A remote (network) partition:** The recovery image is hosted on a network boot server like Windows Deployment Services, which allows users or the support staff to stream it to computers on demand.

</td>
<td>

- Available to all computers that have access to the network boot server.
- Recovery images are hosted on a central server, which enables centralized updates.
- Centralized help desk staff can provide repairs remotely.
- No local storage requirement on client computers.
- Ability to create multiple recovery images with different tools for specific support levels.

</td>
<td>

- The need to secure the boot server to ensure that regular users can start only the DaRT recovery image and not the full operating system imaging process.
- Requires the end-user computer to be connected to the network at troubleshooting time.
- Requires enough network bandwidth to enable accessing the recovery image across the network.

</td>
</tr>
<tr class="odd">
<td>

**A recovery partition on the local hard drive:** The recovery image is installed on a local hard drive either manually or by using electronic software distribution systems, like System Center Configuration Manager.

</td>
<td>

- The recovery tools are readily available.
- Centralized help desk staff can provide support through Remote Connection.
- The recovery image is centrally managed and deployed.
- Additional recovery key requests on computers that are protected by Windows BitLocker drive encryption are eliminated.

</td>
<td>

- Local storage is required.
- A dedicated partition for recovery image placement is required to reduce the risk of a failed boot partition.
- When updating DaRT, you must update all computers in your enterprise instead of just one partition (on the network) or removable device.
- Additional consideration is required if you deploy the recovery image after enabling BitLocker.

</td>
</tr>
</tbody>
</table>

## Related topics

- [Planning to Deploy DaRT 10](planning-to-deploy-dart-10.md)
