# WagoSysModule_753_649 v1.0.2.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysModule_753_649
- **Version:** 1.0.2.0
- **Categories:** WAGO LayerView|Sys
- **Author:** WAG0 / u010545
- **Placeholder:** WagoSysModule_753_649

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Support for M-Bus module 753-649 [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Support for M-Bus module 753-649 [1]

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks - Methods - Global Variable Lists - Other Components

### Indices and tables ¶


| [1] | Based on WagoSysModule_753_649.library, last modified 14.01.2019, 18:34:28. The content of this file was automatically generated with None on 14.01.2019, 18:34:30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysModule_753_649 Library Documentation


| Company: | WAGO |
| Title: | WagoSysModule_753_649 |
| Version: | 1.0.2.0 |
| Categories: | WAGO LayerView\|Sys |
| Author: | WAG0 / u010545 |
| Placeholder: | WagoSysModule_753_649 |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Support for M-Bus module 753-649 [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Support for M-Bus module 753-649 [1]

### Contents:


- 20 Program Organitzation Unit FbModule_753_649 (FB) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysModule_753_649.library, last modified 14.01.2019, 18:34:28. The content of this file was automatically generated with None on 14.01.2019, 18:34:30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysModule_753_649.library |
| contentFile | WagoSysModule_753_649_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 18:34:30 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 18:34:28 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAG0 / u010545 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysModule_753_649 |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysModule_753_649 |
| DefaultNamespace |  |
| Version | version | 1.0.2.0 |
| Title | string | WagoSysModule_753_649 |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysModuleBase Library Identification : Placeholder: WagoSysModuleBase Default Resolution: WagoSysModuleBase, * (WAGO) Namespace: WagoSysModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX_OUTPUT_SIZE = 47 Parameter: MAX_MODULE_QUANTITY = 250 Parameter: MAX_MODULE_INPUT_SIZE = 48 Parameter: MBX_PIPE_SIZE = 1024 Parameter: MAX_MODULE_OUTPUT_SIZE = 48 Parameter: MAX_MBX_INPUT_SIZE = 47 WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesModule_753_649 Library Identification : Placeholder: WagoTypesModule_753_649 Default Resolution: WagoTypesModule_753_649, * (WAGO) Namespace: WagoTypesModule_753_649 Library Properties :

### Function Blocks


## FbModule_753_649 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

Interface variables - FbModule_753_649.FB_init (METH)

### Methods


## FbModule_753_649.FB_init (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FB_init | BOOL |  |
| Input | bInitRetains | BOOL | TRUE: the Retain-variables are initialized (reset warm / reset cold) |
| bInCopyCode | BOOL | TRUE the instance will be copied to the copy-code afterward (online change) |

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

WagoSysModule_753_649

WagoSysModule_753_649

### Other Components


## 20 Program Organitzation Unit


- FbModule_753_649 (FB) FbModule_753_649.FB_init (METH)