# WagoSysModule_753_163x v1.0.1.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysModule_753_163x
- **Version:** 1.0.1.0
- **Categories:** WAGO LayerView|Sys; Application
- **Namespace:** WagoSysModule_753_163x
- **Author:** WAG0 / u090996
- **Placeholder:** WagoSysModule_753_163x

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Support for SMI module 753-163x [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Support for SMI module 753-163x [1]

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Global Variable Lists

### Indices and tables ¶


| [1] | Based on WagoSysModule_753_163x.library, last modified 14.01.2019, 18:36:48. The content of this file was automatically generated with None on 14.01.2019, 18:36:50 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysModule_753_163x Library Documentation


| Company: | WAGO |
| Title: | WagoSysModule_753_163x |
| Version: | 1.0.1.0 |
| Categories: | WAGO LayerView\|Sys; Application |
| Namespace: | WagoSysModule_753_163x |
| Author: | WAG0 / u090996 |
| Placeholder: | WagoSysModule_753_163x |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Support for SMI module 753-163x [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Support for SMI module 753-163x [1]

### Contents:


- VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysModule_753_163x.library, last modified 14.01.2019, 18:36:48. The content of this file was automatically generated with None on 14.01.2019, 18:36:50 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysModule_753_163x.library |
| contentFile | WagoSysModule_753_163x_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 18:36:50 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 18:36:48 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAG0 / u090996 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysModule_753_163x |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysModule_753_163x |
| DefaultNamespace | WagoSysModule_753_163x |
| Version | version | 1.0.1.0 |
| Title | string | WagoSysModule_753_163x |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys; Application |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysModuleBase Library Identification : Placeholder: WagoSysModuleBase Default Resolution: WagoSysModuleBase, * (WAGO) Namespace: WagoSysModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX_OUTPUT_SIZE = 47 Parameter: MAX_MODULE_QUANTITY = 250 Parameter: MAX_MODULE_INPUT_SIZE = 48 Parameter: MBX_PIPE_SIZE = 1024 Parameter: MAX_MODULE_OUTPUT_SIZE = 48 Parameter: MAX_MBX_INPUT_SIZE = 47 WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesModule_753_163x Library Identification : Placeholder: WagoTypesModule_753_163x Default Resolution: WagoTypesModule_753_163x, * (WAGO) Namespace: WagoTypesModule_753_163x Library Properties :

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 08.01.2019 | 1.0.1.0 | u015842 | Properties: free placeholder added |
| 23.05.2017 | 1.0.0.1 | u090996 | Deregistration of Mbx before an application runs |
| 16.02.2017 | 1.0.0.0 | u090996 | Release |
| 16.02.2017 | 0.0.0.4 | u090996 | Fixed issue of mailbox initialization |
| 25.01.2017 | 0.0.0.3 | u090996 | Add property “ModulePosition” |
| 24.01.2017 | 0.0.0.2 | u090996 | Add “IsMbxIdle” property |
| 23.01.2017 | 0.0.0.1 | u090996 | Merged FBs to FbModule_753_163x |
| 02.08.2016 | 0.0.0.0 | u010545 | created |

WagoSysModule_753_163x

WagoSysModule_753_163x