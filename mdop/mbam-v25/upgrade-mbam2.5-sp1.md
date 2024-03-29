---
title: MBAM servicing release update
description: Upgrade Microsoft BitLocker Administration & Monitoring (MBAM) 2.5 to MBAM 2.5 SP1 with Microsoft Desktop Optimization Pack (MDOP) May 2019 update.
author: aczechowski
ms.author: aaroncz
ms.collection: must-keep
manager: aaroncz
ms.topic: article
ms.localizationpriority: medium
ms.date: 05/27/2020
---

# Upgrade MBAM to the latest servicing release update

This article provides step-by-step instructions to upgrade Microsoft BitLocker Administration and Monitoring (MBAM) to the latest [October 2020 servicing release for Microsoft Desktop Optimization Pack](https://support.microsoft.com/topic/october-2020-servicing-release-for-microsoft-desktop-optimization-pack-9c509089-51d3-0877-15c5-04b83313b7c9) in a standalone configuration. As of March 2021 the latest version is 2.5.1152.0.

In this guide, we will use a two-server configuration. One server will be a database server that's running Microsoft SQL Server 2016. This server will host the MBAM databases and reports. The other server will be a Windows Server 2012 R2 web server. This server will host "Administration and Monitoring" and "Self-Service Portal."

## Prepare to upgrade MBAM infratructure

### Know the MBAM servers in your environment

1. SQL Server Database Engine: Server that hosts the MBAM databases.
2. SQL Server Reporting Services: Server that hosts the MBAM reports.
3. Internet Information Services (IIS) web servers: Server that hosts MBAM Web Applications and MBAM services.

### Identify service accounts, groups, server name, and reports URL

1. Identify the MBAM application pool service account that's used by IIS web servers to read and write data to MBAM databases.
2. Identify the groups that are used during the MBAM web features configuration and the reports web service URL.
3. Identify the SQL Server name and instance name. Watch this video to learn more.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. Identify the SQL Server Reporting Services Account that's used for reading compliance data from the Compliance and Audit database. Watch this video to learn more.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## Upgrade the MBAM infrastructure to the latest version available.

MBAM Server infrastructure installation or upgrade is always performed in the order listed below:

- SQL Server Database Engine: Databases
- SQL Server Reporting Services: Reports
- Web Server: Web Applications
- Clients: MBAM Agent or Client Update
- Group Policy Templates: Update the existing Group Policy with new templates and enable new settings on existing MBAM Group Policy

> [!NOTE]
> We recommend that you create a full database backup of the MBAM databases before you run the upgrades.

### Upgrade the MBAM SQL Server

Watch this video to learn how to upgrade the MBAM SQL Server:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### Upgrade the MBAM Web Server

Watch this video to learn how to upgrade the MBAM Web Server:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## More information

For more information about known issues in MBAM 2.5 SP1, see [Release Notes for MBAM 2.5 SP1](/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).
