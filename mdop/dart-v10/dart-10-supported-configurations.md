---
title: DaRT 10 Supported Configurations
description: DaRT 10 Supported Configurations
author: dansimp
ms.assetid: a07d6562-1fa9-499f-829c-9cc487ede0b7
ms.reviewer: 
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 04/20/2021
---

# DaRT 10 Supported Configurations

This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment. Both the operating system requirements and the system requirements that are required to run DaRT 10 are specified. For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 10 Recovery Image](planning-to-create-the-dart-10-recovery-image.md).

For supported configurations that apply to later releases, see the documentation for the applicable release.

You can install DaRT in one of two ways. You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT. Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.

## DaRT 10 prerequisite software

Make sure that the following prerequisites are met before you install DaRT.

### Administrator computer prerequisites

The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 10 and all of the DaRT tools.

<table>
<thead>
<tr class="header">
<th scope="col">Prerequisite</th>
<th scope="col">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<th scope="row">[Windows Assessment and Deployment Kit (ADK) 10.0](https://docs.microsoft.com/windows-hardware/get-started/adk-install)</th>
<td>Required for the DaRT Recovery Image wizard. Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE). The ADK is not required if you are installing only the Remote Connection Viewer or Crash Analyzer.</td>
</tr>
<tr class="even">
<th scope="row">Windows SDK or Windows Driver Kit (optional)</th>
<td>Crash Analyzer requires the Windows 10 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</td>
</tr>
<tr class="odd">
<th scope="row">Windows 10 x64 or x86 ISO image</th>
<td>DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 10 media. Download the x86 or x64 version of Windows 10, depending on the type of DaRT recovery image you want to create. If you support both system types in your environment, download both versions of Windows 10.</td>
</tr>
</tbody>
</table>

### Help desk computer prerequisites

The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 10 Remote Connection Viewer.

<table>
<thead>
<tr class="header">
<th scope="col">Prerequisite</th>
<th scope="col">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DaRT 10 Remote Connection Viewer</td>
<td>Must be installed on a Windows 10 operating system.</td>
</tr>
<tr class="even">
<td>Debugging Tools for Windows</td>
<td>Required only if you are installing the Crash Analyzer tool</td>
</tr>
</tbody>
</table>

### End-user computer prerequisites

There is no prerequisite software that must be installed on end-user computers, other than the Windows 10 operating system.

## DaRT 10 operating system requirements

### Administrator computer system requirements

The following table lists the operating systems that are supported for the DaRT 10 administrator computer installation.

> [!NOTE]
>
> - Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.
> - Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack. To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975). For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).

<table style="width:100%; table-layout:fixed;">
<thead>
<tr class="header">
<th scope="col">Operating System (OS)</th>
<th scope="col">Edition</th>
<th scope="col">Service Pack</th>
<th scope="col">System Architecture</th>
<th scope="col">OS RAM Requirements</th>
<th scope="col">DaRT RAM Requirements</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows 10</td>
<td>All editions</td>
<td>N/A</td>
<td>x64</td>
<td>2 GB</td>
<td>2.5 GB</td>
</tr>
<tr class="even">
<td>Windows 10</td>
<td>All editions</td>
<td>N/A</td>
<td>x86</td>
<td>1 GB</td>
<td>1.5 GB</td>
</tr>
</tbody>
</table>

### DaRT help desk computer system requirements

If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer. You can optionally install the Crash Analyzer tool on the help desk computer.

DaRT 10 enables a help desk worker to connect to a DaRT 10 computer by using either the DaRT 7.0, DaRT 8.0, DaRt 8.1, or DaRT 10 Remote Connection Viewer. The DaRT 7.0, DaRT 8.0 and DaRt 8.1, Remote Connection Viewers require Windows 7, Windows 8, or Windows 8.1 operating systems respectively, while the DaRT 10 Remote Connection Viewer requires Windows 10. The DaRT 10 Remote Connection Viewer and all other DaRT 10 tools can be installed only on a computer running Windows 10.

The following table lists the operating systems that are supported for the DaRT help desk computer installation.

<table style="width:100%; table-layout:fixed;">
<thead>
<tr class="header">
<th scope="col">Operating System (OS)</th>
<th scope="col">Edition</th>
<th scope="col">Service Pack</th>
<th scope="col">System Architecture</th>
<th scope="col">OS RAM Requirements</th>
<th scope="col">DaRT RAM Requirements</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows 10</td>
<td>All editions</td>
<td>N/A</td>
<td>x64</td>
<td>2 GB</td>
<td>2.5 GB</td>
</tr>
<tr class="even">
<td>Windows 10 (with Remote Connection Viewer 10.0 only)</td>
<td>All editions</td>
<td>N/A</td>
<td>x86</td>
<td>1 GB</td>
<td>1.5 GB</td>
</tr>
<tr class="odd">
<td>Windows 8</td>
<td>All editions</td>
<td>N/A</td>
<td>x64</td>
<td>2 GB</td>
<td>2.5 GB</td>
</tr>
<tr class="even">
<td>Windows 8 (with Remote Connection Viewer 8.0 only)</td>
<td>All editions</td>
<td>N/A</td>
<td>x86</td>
<td>1 GB</td>
<td>1.5 GB</td>
</tr>
<tr class="odd">
<td>Windows 7 (with Remote Connection Viewer 7.0 only)</td>
<td>All editions</td>
<td>SP1, SP2</td>
<td>x64 or x86</td>
<td>1 GB</td>
<td>N/A</td>
</tr>
<tr class="even">
<td>Windows Server 2012</td>
<td>Standard, Enterprise, Data Center</td>
<td>N/A</td>
<td>x64</td>
<td>2 GB</td>
<td>1.0 GB</td>
</tr>
<tr class="odd">
<td>Windows Server 2012 R2</td>
<td>Standard, Enterprise, Data Center</td>
<td>N/A</td>
<td>x64</td>
<td>2 GB</td>
<td>1.0 GB</td>
</tr>
</tbody>
</table>

DaRT also has the following minimum hardware requirements for the end-user computer:

- A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.
- BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.

### DaRT 10 end-user computer system requirements

The Diagnostics and Recovery Toolset window in DaRT 10 requires that the end-user computer use one of the following operating systems with the specified amount of system memory available for DaRT:

<table style="width:100%; table-layout:fixed;">
<thead>
<tr class="header">
<th scope="col">Operating System (OS)</th>
<th scope="col">Edition</th>
<th scope="col">Service Pack</th>
<th scope="col">System Architecture</th>
<th scope="col">OS RAM Requirements</th>
<th scope="col">DaRT RAM Requirements</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows 10</td>
<td>All editions</td>
<td>N/A</td>
<td>x64</td>
<td>2 GB</td>
<td>2.5 GB</td>
</tr>
<tr class="even">
<td>Windows 10</td>
<td>All editions</td>
<td>N/A</td>
<td>x86</td>
<td>1 GB</td>
<td>1.5 GB</td>
</tr>
</tbody>
</table>

## Related topics

- [Planning to Deploy DaRT 10](planning-to-deploy-dart-10.md)
