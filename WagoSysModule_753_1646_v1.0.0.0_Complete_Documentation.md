# WagoSysModule_753_1646 v1.0.0.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysModule_753_1646
- **Version:** 1.0.0.0
- **Categories:** WAGO LayerView|Sys
- **Author:** who / u090038
- **Placeholder:** WagoSysModule_753_1646

### Description ¶


This document is automatically generated.

Support for KNX module 753-1646

This document is automatically generated. Support for KNX module 753-1646

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks - Global Variable Lists - Other Components

### Indices and tables ¶


Based on WagoSysModule_753_1646.library, last modified 20.09.2024, 21:39:50. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysModule_753_1646.library, last modified 20.09.2024, 21:39:50. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysModule_753_1646 Library Documentation


| Company: | WAGO |
| Title: | WagoSysModule_753_1646 |
| Version: | 1.0.0.0 |
| Categories: | WAGO LayerView\|Sys |
| Author: | who / u090038 |
| Placeholder: | WagoSysModule_753_1646 |

### Description


This document is automatically generated.

Support for KNX module 753-1646

This document is automatically generated. Support for KNX module 753-1646

### Contents:


- 20 Program Organitzation Unit FbModule_753_1646 (FB) VersionHistory (GVL)

### Indices and tables


Based on WagoSysModule_753_1646.library, last modified 20.09.2024, 21:39:50. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysModule_753_1646.library, last modified 20.09.2024, 21:39:50. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysModule_753_1646.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 20.09.2024, 21:39:50 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 20.09.2024, 21:39:50 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | who / u090038 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysModule_753_1646 |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysModule_753_1646 |
| DefaultNamespace |  |
| Version | version | 1.0.0.0 |
| Title | string | WagoSysModule_753_1646 |
| Released | bool | False |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysModuleBase Library Identification : Placeholder: WagoSysModuleBase Default Resolution: WagoSysModuleBase, * (WAGO) Namespace: WagoSysModuleBase Library Properties : Library Parameter : Parameter: SYSLOG_MBX2_MAX_STRING_LEN = 0 Parameter: STARTUP_MODE = eStartUpMode.NONE Parameter: DYNAMIC_REGISTER_MODE = eDynamicRegisterMode.AUTO Parameter: TASK_PRIO_DAEMON_KBUS = 13 Parameter: SYSLOG_MBX2_LOGLEVEL = 2#10001 Parameter: SYSLOG_SERVER_IP = ‘127.0.0.1’ Parameter: TASK_PRIO_DAEMON_CYCLIC = 14 Parameter: SYSLOG_SERVER_PORT = 514 WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesModule_753_1646 Library Identification : Placeholder: WagoTypesModule_753_1646 Default Resolution: WagoTypesModule_753_1646, * (WAGO) Namespace: WagoTypesModule_753_1646 Library Properties :

### Function Blocks


## FbModule_753_1646 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 03.04.2024 | 1.0.0.0 | u090038 | Released |

WagoSysModule_753_1646

WagoSysModule_753_1646

### Other Components


## 20 Program Organitzation Unit


- FbModule_753_1646 (FB)