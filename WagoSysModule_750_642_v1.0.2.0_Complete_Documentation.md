# WagoSysModule_750_642 v1.0.2.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysModule_750_642
- **Version:** 1.0.2.0
- **Categories:** WAGO LayerView|Sys
- **Author:** WAG0 / u010545
- **Placeholder:** WagoSysModule_750_642

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Support for ENOCEAN module 750-642 [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Support for ENOCEAN module 750-642 [1]

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks - Methods FbModule_750_642.BuiltRegisters (METH) - FbModule_750_642.GetComPortNo (METH) - FbModule_750_642.ModuleToPipe (METH) - FbModule_750_642.PipeToModule (METH) Global Variable Lists Other Components - 20 Program Organitzation Unit - KbusContext

### Indices and tables ¶


| [1] | Based on WagoSysModule_750_642.library, last modified 14.01.2019, 18:26:11. The content of this file was automatically generated with None on 14.01.2019, 18:26:13 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysModule_750_642 Library Documentation


| Company: | WAGO |
| Title: | WagoSysModule_750_642 |
| Version: | 1.0.2.0 |
| Categories: | WAGO LayerView\|Sys |
| Author: | WAG0 / u010545 |
| Placeholder: | WagoSysModule_750_642 |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Support for ENOCEAN module 750-642 [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Support for ENOCEAN module 750-642 [1]

### Contents:


- 20 Program Organitzation Unit FbModule_750_642 (FB) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysModule_750_642.library, last modified 14.01.2019, 18:26:11. The content of this file was automatically generated with None on 14.01.2019, 18:26:13 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysModule_750_642.library |
| contentFile | WagoSysModule_750_642_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 18:26:13 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 18:26:11 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAG0 / u010545 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysModule_750_642 |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysModule_750_642 |
| DefaultNamespace |  |
| Version | version | 1.0.2.0 |
| Title | string | WagoSysModule_750_642 |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False PublishSymbolsInContainer: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoSysModule_75x_65x Library Identification : Placeholder: WagoSysModule_75x_65x Default Resolution: WagoSysModule_75x_65x, * (WAGO) Namespace: WagoSysModule_75x_65x Library Properties : Library Parameter : Parameter: MAX_PIPE_SIZE = 1024 WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCom Library Identification : Placeholder: WagoTypesCom Default Resolution: WagoTypesCom, * (WAGO) Namespace: WagoTypesCom Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties : WagoTypesModule_750_642 Library Identification : Placeholder: WagoTypesModule_750_642 Default Resolution: WagoTypesModule_750_642, * (WAGO) Namespace: WagoTypesModule_750_642 Library Properties :

### Function Blocks


## FbModule_750_642 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

Interface variables - FbModule_750_642.BuiltRegisters (METH) - FbModule_750_642.GetComPortNo (METH) - KbusContext FbModule_750_642.ModuleToPipe (METH) - FbModule_750_642.PipeToModule (METH)

### Methods


## FbModule_750_642.BuiltRegisters (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | BuiltRegisters | WagoTypes.eResultCode |

Method overwrite =============== ==================================================================================== Result Codes —————————————————————————————————– 0 Success EBUSY The FB is busy with another instance EALREADY The com-port is already open ENOPROTOOPT The requested option or physical layer (RS-xyz) is not available =============== ====================================================================================

Interface variables Method overwrite =============== ==================================================================================== Result Codes —————————————————————————————————– 0 Success EBUSY The FB is busy with another instance EALREADY The com-port is already open ENOPROTOOPT The requested option or physical layer (RS-xyz) is not available =============== ====================================================================================

## FbModule_750_642.GetComPortNo (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetComPortNo | USINT |

Calculates the comport number from the amount of serial modules like 750-650, 750-652, ... The first found and registered module becomes the number one.

Modules with number ‘0’ are not mounted as ttyDevice (see 642 Enocean). Such Modules have to overwrite this Method and to return always 0.

Interface variables Calculates the comport number from the amount of serial modules like 750-650, 750-652, ... The first found and registered module becomes the number one. Modules with number ‘0’ are not mounted as ttyDevice (see 642 Enocean). Such Modules have to overwrite this Method and to return always 0.

## FbModule_750_642.ModuleToPipe (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ModuleToPipe | WagoTypes.eResultCode |

Read data from physical module and put it to pipe for application

Interface variables Read data from physical module and put it to pipe for application

## FbModule_750_642.PipeToModule (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | PipeToModule | WagoTypes.eResultCode |

Read data from application pipe and put it to physical module

Interface variables Read data from application pipe and put it to physical module

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 08.01.2019 | 1.0.2.0 | u015842 | Properties: free placeholder added |
| 05.05.2017 | 1.0.1.0 | U10545 | Compilerversion updated to 3.5.9.0 |
| 30.03.2017 | 1.0.0.1 | U015842 | e!Cockpit 1.3 Patch 1 |
| 26.10.2016 | 1.0.0.0 | U014521 | e!Cockpit 1.3 |

WagoSysModule_750_642

WagoSysModule_750_642

### Other Components


## 20 Program Organitzation Unit


- FbModule_750_642 (FB) FbModule_750_642.BuiltRegisters (METH) - FbModule_750_642.GetComPortNo (METH) - KbusContext FbModule_750_642.ModuleToPipe (METH) - FbModule_750_642.PipeToModule (METH)

## KbusContext


- FbModule_750_642.ModuleToPipe (METH) - FbModule_750_642.PipeToModule (METH)