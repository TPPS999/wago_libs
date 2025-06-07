# WagoTypesModule_75x_49x v1.5.1.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesModule_75x_49x
- **Version:** 1.5.1.0
- **Categories:** WAGO Internal|Common|Types and Interfaces
- **Author:** WAGO
- **Placeholder:** WagoTypesModule_75x_49x

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling module 750-493,740-494, 750-495,3PPM [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling module 750-493,740-494, 750-495,3PPM [1]

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Functions - Methods I_Module_3PPM.AccessByID (METH) - I_Module_3PPM.GetData_3PPM (METH) - I_Module_75x_493.GetData_493 (METH) - I_Module_75x_494.GetData_494 (METH) - I_Module_75x_495.GetData_495 (METH) Interfaces - I_Module_3PPM (ITF) - I_Module_75x_493 (ITF) - I_Module_75x_494 (ITF) - I_Module_75x_495 (ITF) - I_Module_75x_49x_PM (ITF)

### Indices and tables ¶


| [1] | Based on WagoTypesModule_75x_49x.library, last modified 14.01.2019, 17:59:02. The content of this file was automatically generated with None on 14.01.2019, 17:59:04 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesModule_75x_49x Library Documentation


| Company: | WAGO |
| Title: | WagoTypesModule_75x_49x |
| Version: | 1.5.1.0 |
| Categories: | WAGO Internal\|Common\|Types and Interfaces |
| Author: | WAGO |
| Placeholder: | WagoTypesModule_75x_49x |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling module 750-493,740-494, 750-495,3PPM [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling module 750-493,740-494, 750-495,3PPM [1]

### Contents:


- FuGetVersionHistory (FUN) - I_Module_3PPM (ITF) I_Module_3PPM.AccessByID (METH) - I_Module_3PPM.GetData_3PPM (METH) I_Module_75x_493 (ITF) - I_Module_75x_493.GetData_493 (METH) I_Module_75x_494 (ITF) - I_Module_75x_494.GetData_494 (METH) I_Module_75x_495 (ITF) - I_Module_75x_495.GetData_495 (METH) I_Module_75x_49x_PM (ITF)

### Indices and tables


| [1] | Based on WagoTypesModule_75x_49x.library, last modified 14.01.2019, 17:59:02. The content of this file was automatically generated with None on 14.01.2019, 17:59:04 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesModule_75x_49x.library |
| contentFile | WagoTypesModule_75x_49x_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 17:59:04 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 17:59:02 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesModule_75x_49x |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesModule_75x_49x |
| DefaultNamespace |  |
| Version | version | 1.5.1.0 |
| Version string | string |  |
| Title | WagoTypesModule_75x_49x |
| LibraryCategories | library-category-list | WAGO Internal\|Common\|Types and Interfaces |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoTypesCom Library Identification : Placeholder: WagoTypesCom Default Resolution: WagoTypesCom, * (WAGO) Namespace: WagoTypesCom Library Properties : WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX_SIZE = 18

### Functions


## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 08.01.2019 | 1.5.1.0 | u015842 | Properties: free placeholder added |
| 19.01.2018 | 1.5.0.5 | u010663 | new Interface I_Module_PM2 |
| 23.09.2016 | 1.5.0.4 | u010663 | new Interface I_Module_PM |
| 26.02.2016 | 1.5.0.3 | u010663 | WagoSysVersion eliminated |
| 29.09.2015 | 1.5.0.2 | u010663 | Libraries inserted by placeholder |
| 24.08.2015 | 1.5.0.1 | u010663 | Placeholder added |
| 16.06.2015 | 1.5.0.0 | u010663 | Released |

WagoTypesModule_75x_49x.library

Interface variables WagoTypesModule_75x_49x.library

### Methods


## I_Module_3PPM.AccessByID (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | AccessByID | BOOL |
| Input | dwID | DWORD |

## I_Module_3PPM.GetData_3PPM (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetData_3PPM | POINTER TO typData_3PPM |

## I_Module_75x_493.GetData_493 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetData_493 | POINTER TO typData_493 |

## I_Module_75x_494.GetData_494 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetData_494 | POINTER TO typData_494 |

## I_Module_75x_495.GetData_495 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetData_495 | POINTER TO typData_495 |

### Interfaces


## I_Module_3PPM (ITF)


- I_Module_3PPM.AccessByID (METH) - I_Module_3PPM.GetData_3PPM (METH)

## I_Module_75x_493 (ITF)


- I_Module_75x_493.GetData_493 (METH)

## I_Module_75x_494 (ITF)


- I_Module_75x_494.GetData_494 (METH)

## I_Module_75x_495 (ITF)


- I_Module_75x_495.GetData_495 (METH)

## I_Module_75x_49x_PM (ITF) ¶
