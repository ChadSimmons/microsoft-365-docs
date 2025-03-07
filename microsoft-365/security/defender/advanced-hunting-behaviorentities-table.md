---
title: BehaviorEntities table in the advanced hunting schema
description: Learn about behaviors in the BehaviorEntities table of the advanced hunting schema
keywords: advanced hunting, threat hunting, cyber threat hunting, Microsoft 365 Defender, microsoft 365, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, AlertInfo, alert, severity, category, MITRE, ATT&CK, Microsoft Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Defender for Cloud Apps, and Microsoft Defender for Identity
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.service: microsoft-365-security
ms.subservice: m365d
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords: 
  - NOCSH
ms.author: maccruz
author: schmurky
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: 
- m365-security
- tier3
ms.topic: conceptual
ms.date: 02/16/2021
---

# BehaviorEntities

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


**Applies to:**
- Microsoft 365 Defender


The `BehaviorEntities` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about behaviors in Microsoft Defender for Cloud Apps. Use this reference to construct queries that return information from this table.

> [!IMPORTANT]
> Some information relates to prereleased product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.

Behaviors are a type of data in Microsoft 365 Defender based on one or more raw events. Behaviors provide contextual insight into events and can, but not necessarily, indicate malicious activity. [Read more about behaviors](/defender-cloud-apps/behaviors)

For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).

| Column name | Data type | Description |
|-------------|-----------|-------------|
| `Timestamp` | `datetime` | Date and time when the event was recorded |
| `BehaviorId` | `string` | Unique identifier for the behavior|
| `ActionType` | `string` | Type of behavior |
| `Categories` | `list` | Type of threat indicator or  breach activity identified by the behavior|
| `ServiceSource` | `string` | Product or service that identified the behavior |
| `DetectionSource` | `string` | Detection technology or sensor that identified the notable component or activity |
| `DataSources` | `list` | Products or services that provided information for the behavior |
| `EntityType` | `string` | Type of object, such as a file, a process, a device, or a user |
| `EntityRole` | `string` | Indicates whether the entity is impacted or merely related |
| `DetailedEntityRole` | `string` | The roles of the entity in the behavior|
| `FileName` | `string` | Name of the file that the behavior applies to|
| `FolderPath` | `string` | Folder containing the file that the behavior applies to|
| `SHA1` | `string` | SHA-1 of the file that the behavior applies to|
| `SHA256` | `string` | SHA-256 of the file that the behavior applies to|
| `FileSize` | `long` | Size, in bytes, of the file that the behavior applies to |
|`ThreatFamily`|`string`| Malware family that the suspicious or malicious file or process has been classified under |
|`RemoteIP`|`string` |IP address that was being connected to |
|`RemoteUrl`|`string` |URL or fully qualified domain name (FQDN) that was being connected to |
|`AccountName`|`string` |User name of the account |
|`AccountDomain`|`string` |Domain of the account |
|`AccountSid`|`string` |Security Identifier (SID) of the account |
| `AccountObjectId` | `string` | Unique identifier for the account in Azure AD |
| `AccountUpn` | `string` | User principal name (UPN) of the account |
| `DeviceId` | `string` | Unique identifier for the machine in the service |
|`DeviceName`|`string` | Fully qualified domain name (FQDN) of the device |
|`LocalIP`|`string` | IP address assigned to the local device used during communication |
|`NetworkMessageId`|`string`| Unique identifier for the email, generated by Office 365 |
|`EmailSubject`|`string`| Subject of the email |
|`EmailClusterId`|`string`| Identifier for the group of similar emails clustered based on heuristic analysis of their contents |
|`Application`|`string`| Application that performed the recorded action |
|`ApplicationId	`|`int`| Unique identifier for the application |
|`OAuthApplicationId`|`string`| Unique identifier of the third-party OAuth application |
|`ProcessCommandLine`|`string`| Command line used to create the new process |
|`RegistryKey`|`string`| Registry key that the recorded action was applied to |
|`RegistryValueName`|`string`| Name of the registry value that the recorded action was applied to |
|`RegistryValueData	`|`string`| Data of the registry value that the recorded action was applied to |
| `AdditionalFields` | `string` | Additional information about the behavior|

## Related topics
- [Advanced hunting overview](advanced-hunting-overview.md)
- [Learn the query language](advanced-hunting-query-language.md)
- [Use shared queries](advanced-hunting-shared-queries.md)
- [Hunt across devices, emails, apps, and identities](advanced-hunting-query-emails-devices.md)
- [Understand the schema](advanced-hunting-schema-tables.md)
- [Apply query best practices](advanced-hunting-best-practices.md)
[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/defender-m3d-techcommunity.md)]
