# WagoSysProcess_Internal_PFC v1.0.0.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysProcess_Internal_PFC
- **Version:** 1.0.0.0
- **Namespace:** WagoSysProcess_Internal
- **Author:** WAGO / u0100179
- **Placeholder:** WagoSysProcess_Internal

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Library to execute system commands [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Library to execute system commands [1]

### Contents: ¶


Contents: - Project Information - Library Information - Functions - Program Organization - Function Groups - Internal Components - Global Variable Lists

### Indices and tables ¶


| [1] | Based on WagoSysProcess_Internal_PFC.library, last modified 25.11.2020, 17:21:12. LibDoc 3.5.15.30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysProcess_Internal_PFC.library |
| contentFile | WagoSysProcess_Internal_PFC_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 25.11.2020, 17:21:13 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 25.11.2020, 17:21:12 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2020 – All rights reserved. |
| Author | WAGO / u0100179 |
| AutoResolveUnbound | bool | False |
| LanguageModelAttribute | string | qualified-access-only |
| Company | WAGO |
| DocFormat | reStructuredText |
| SourceLibrary | bool | False |
| Project | string | WagoSysProcess_Internal_PFC |
| DefaultNamespace | WagoSysProcess_Internal |
| Version | version | 1.0.0.0 |
| Title | string | WagoSysProcess_Internal_PFC |
| Released | bool | False |
| Placeholder | string | WagoSysProcess_Internal |
| LibraryCategories | library-category-list |  |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP15 Patch 4 |
| IsEndUserLibrary | bool | False |

### Library Information


## Library Reference


This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces.

### SysTypes2 Interfaces


#### Library Identification


Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes

#### Library Properties


| LinkAllContent: False QualifiedOnly: False | Key: SysTypes2 Interfaces, * (System) SystemLibrary: False | Optional: False |

### WagoSysVersion


#### Library Identification


Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion

#### Library Properties


| LinkAllContent: False QualifiedOnly: False | Key: WagoSysVersion, 1.0.0.0 (WAGO) SystemLibrary: False | Optional: False |

### Functions


## FuExecuteCommand (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuExecuteCommand | DINT |  |
| Input | sCommand | STRING(1024) |  |
| R_sStdOut | REFERENCE TO STRING |  |
| uiStdOutSize | UINT | The maximal supported length is STRING(255) |
| R_sStdError | REFERENCE TO STRING |  |
| uiStdErrorSize | UINT | The maximal supported length is STRING(255) |
| udiTimeoutMs | UDINT | Timeout for command execution |
| pResult | POINTER TO SysTypes.RTS_IEC_RESULT |  |

### Program Organization


## 20 Program Organization Units


- Functions FuExecuteCommand (FUN)

### Function Groups


## Functions ¶


- FuExecuteCommand (FUN)

### Internal Components


## WagoSysProcess_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysProcess_Internal_PFC |
| Version: | 1.0.0.0 |
| Namespace: | WagoSysProcess_Internal |
| Author: | WAGO / u0100179 |
| Placeholder: | WagoSysProcess_Internal |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Library to execute system commands [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Library to execute system commands [1]

### Contents:


- 20 Program Organization Units Functions VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysProcess_Internal_PFC.library, last modified 25.11.2020, 17:21:12. LibDoc 3.5.15.30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## VersionHistory (GVL)


| Date | Version | Author | Change |
| 26.08.2020 | 1.0.0.0 | WAGO / u0100179 | Release Version |

WagoSysProcess_Internal_PFC

WagoSysProcess_Internal_PFC