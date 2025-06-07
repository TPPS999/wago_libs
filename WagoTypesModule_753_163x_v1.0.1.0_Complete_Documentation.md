# WagoTypesModule_753_163x v1.0.1.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesModule_753_163x
- **Version:** 1.0.1.0
- **Categories:** WAGO Internal|Common|Types and Interfaces
- **Namespace:** WagoTypesModule_753_163x
- **Author:** WAG0 / u090996
- **Placeholder:** WagoTypesModule_753_163x

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Interfaces for modules 753-163x [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Interfaces for modules 753-163x [1]

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Methods - Interfaces I_Module_753_1630 (ITF) - I_Module_753_1631 (ITF) - I_Module_753_163x (ITF) Global Variable Lists Other Components - 20 Program Organitzation Unit - I_Module_753_163x.EnableEnergySaverMode (PROP) - I_Module_753_163x.EnableMbx (PROP) - I_Module_753_163x.Firmware (PROP) - I_Module_753_163x.IsDigtialInputActive (PROP) - I_Module_753_163x.IsMbxIdle (PROP) - I_Module_753_163x.ModulePosition (PROP)

### Indices and tables ¶


| [1] | Based on WagoTypesModule_753_163x.library, last modified 14.01.2019, 18:36:00. The content of this file was automatically generated with None on 14.01.2019, 18:36:02 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesModule_753_163x Library Documentation


| Company: | WAGO |
| Title: | WagoTypesModule_753_163x |
| Version: | 1.0.1.0 |
| Categories: | WAGO Internal\|Common\|Types and Interfaces |
| Namespace: | WagoTypesModule_753_163x |
| Author: | WAG0 / u090996 |
| Placeholder: | WagoTypesModule_753_163x |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Interfaces for modules 753-163x [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Interfaces for modules 753-163x [1]

### Contents:


- 20 Program Organitzation Unit I_Module_753_1630 (ITF) - I_Module_753_1631 (ITF) - I_Module_753_163x (ITF) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoTypesModule_753_163x.library, last modified 14.01.2019, 18:36:00. The content of this file was automatically generated with None on 14.01.2019, 18:36:02 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesModule_753_163x.library |
| contentFile | WagoTypesModule_753_163x_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 18:36:02 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 18:36:00 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAG0 / u090996 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesModule_753_163x |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesModule_753_163x |
| DefaultNamespace | WagoTypesModule_753_163x |
| Version | version | 1.0.1.0 |
| Title | string | WagoTypesModule_753_163x |
| LibraryCategories | library-category-list | WAGO Internal\|Common\|Types and Interfaces |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : Library Parameter : Parameter: MAX_MODULE_OUTPUT_SIZE = 48 Parameter: MAX_MODULE_INPUT_SIZE = 48 Parameter: MBX_PIPE_SIZE = 1024 Parameter: MAX_MBX_SIZE = 18 Parameter: MAX_MBX1_SIZE = 18 Parameter: MAX_MBX_OUTPUT_SIZE = 47 Parameter: MAX_MBX_INPUT_SIZE = 47

### Methods


## I_Module_753_163x.ToggleCsBit (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | xToggleState | BOOL |

### Interfaces


## I_Module_753_1630 (ITF) ¶


## I_Module_753_1631 (ITF) ¶


## I_Module_753_163x (ITF)


- I_Module_753_163x.EnableEnergySaverMode (PROP) - I_Module_753_163x.EnableMbx (PROP) - I_Module_753_163x.Firmware (PROP) - I_Module_753_163x.IsDigtialInputActive (PROP) - I_Module_753_163x.IsMbxIdle (PROP) - I_Module_753_163x.ModulePosition (PROP) - I_Module_753_163x.ToggleCsBit (METH)

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 08.01.2019 | 1.0.1.0 | u015842 | Properties: free placeholder added |
| 27.04.2017 | 1.0.0.0 | u090996 | Release |
| 07.04.2017 | 0.0.0.4 | u090996 | Add interfaces for 1631 and 1630 |
| 25.01.2017 | 0.0.0.3 | u090996 | Add property “ModulePosition” |
| 24.01.2017 | 0.0.0.2 | u090996 | Add property “IsMbxIdle” |
| 23.01.2017 | 0.0.0.1 | u090996 | Merged interfaces to “I_Module_753_163x” |
| 02.08.2016 | 0.0.0.0 | u010545 | created |

WagoTypesModule_753_163x

WagoTypesModule_753_163x

### Other Components


## 20 Program Organitzation Unit


- I_Module_753_1630 (ITF) - I_Module_753_1631 (ITF) - I_Module_753_163x (ITF) I_Module_753_163x.EnableEnergySaverMode (PROP) - I_Module_753_163x.EnableMbx (PROP) - I_Module_753_163x.Firmware (PROP) - I_Module_753_163x.IsDigtialInputActive (PROP) - I_Module_753_163x.IsMbxIdle (PROP) - I_Module_753_163x.ModulePosition (PROP) - I_Module_753_163x.ToggleCsBit (METH)

## I_Module_753_163x.EnableEnergySaverMode (PROP) ¶


## I_Module_753_163x.EnableMbx (PROP) ¶


## I_Module_753_163x.Firmware (PROP) ¶


## I_Module_753_163x.IsDigtialInputActive (PROP) ¶


## I_Module_753_163x.IsMbxIdle (PROP) ¶


## I_Module_753_163x.ModulePosition (PROP) ¶
