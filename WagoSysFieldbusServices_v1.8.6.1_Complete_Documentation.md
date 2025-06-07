# WagoSysFieldbusServices v1.8.6.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysFieldbusServices
- **Version:** 1.8.6.1
- **Categories:** WAGO Internal|Feature|LocalBus|K-Bus; WAGO LayerView|Sys; Application
- **Namespace:** WagoSysFieldbusServices
- **Author:** WAGO / u010545
- **Placeholder:** WagoSysFieldbusServices

### Description ¶


This document is automatically generated.

Base Services for Module Access via Fieldbus

This document is automatically generated. Base Services for Module Access via Fieldbus

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks - Methods FbFieldBusService.GetBusType (METH) - FbFieldBusService.GetNewPaOutputs (METH) - FbFieldBusService.SetNewPaInputs (METH) - Set Process Data Global Variable Lists Other Components - 15 FieldBus Services - I_ModuleAccess - Info - Parameter (PARAMS)

### Indices and tables ¶


Based on WagoSysFieldbusServices.library, last modified 29.05.2024, 20:28:53. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysFieldbusServices.library, last modified 29.05.2024, 20:28:53. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysFieldbusServices Library Documentation


| Company: | WAGO |
| Title: | WagoSysFieldbusServices |
| Version: | 1.8.6.1 |
| Categories: | WAGO Internal\|Feature\|LocalBus\|K-Bus; WAGO LayerView\|Sys; Application |
| Namespace: | WagoSysFieldbusServices |
| Author: | WAGO / u010545 |
| Placeholder: | WagoSysFieldbusServices |

### Description


This document is automatically generated.

Base Services for Module Access via Fieldbus

This document is automatically generated. Base Services for Module Access via Fieldbus

### Contents:


- 15 FieldBus Services FbFieldBusService (FB) Parameter (PARAMS) VersionHistory (GVL)

### Indices and tables


Based on WagoSysFieldbusServices.library, last modified 29.05.2024, 20:28:53. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysFieldbusServices.library, last modified 29.05.2024, 20:28:53. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysFieldbusServices.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:28:53 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:28:53 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u010545 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysFieldbusServices |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysFieldbusServices |
| DefaultNamespace | WagoSysFieldbusServices |
| Version | version | 1.8.6.1 |
| Title | string | WagoSysFieldbusServices |
| LibraryCategories | library-category-list | WAGO Internal\|Feature\|LocalBus\|K-Bus; WAGO LayerView\|Sys; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CmpErrors2 Interfaces Library Identification : Name: CmpErrors2 Interfaces Version: newest Company: System Namespace: CmpErrors Library Properties : CmpEventMgr Library Identification : Placeholder: CmpEventMgr Default Resolution: CmpEventMgr, * (System) Namespace: CmpEventMgr Library Properties : CmpIecTask Library Identification : Placeholder: CmpIecTask Default Resolution: CmpIecTask, * (System) Namespace: CmpIecTask Library Properties : IoStandard Library Identification : Placeholder: IoStandard Default Resolution: IoStandard, * (System) Namespace: IoStandard Library Properties : Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : SysCpuHandling Library Identification : Placeholder: SysCpuHandling Default Resolution: SysCpuHandling, * (System) Namespace: SysCpuHandling Library Properties : SysMem Library Identification : Placeholder: SysMem Default Resolution: SysMem, * (System) Namespace: SysMem Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesBusServices Library Identification : Placeholder: WagoTypesBusServices Default Resolution: WagoTypesBusServices, * (WAGO) Namespace: WagoTypesBusServices Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties : WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties :

### Function Blocks


## FbFieldBusService (FB)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | _usiInputSize | USINT | number of input bytes |
| _usiOutputSize | USINT | number of output bytes |
| _usiRegisterFillBytes | USINT (0..3) | current used fillbytes at fieldbus |
| _usiFillByteOffset | USINT (0..3) | Offset for Fillbytes expected by application |
| _usiExpectedFillBytes | USINT (0..3) | Quantity of Fillbytes expected by the application layer |

Interface variables - I_ModuleAccess Info FbFieldBusService.GetBusType (METH) Set Process Data - FbFieldBusService.GetNewPaOutputs (METH) - FbFieldBusService.SetNewPaInputs (METH)

### Methods


## FbFieldBusService.GetBusType (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetBusType | WagoTypesBusServices.eBusType |

## FbFieldBusService.GetNewPaOutputs (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | pOutputData | POINTER TO BYTE | pointer to output data structure |
| usiOutputSize | USINT (0..MAX_MODULE_OUTPUT_SIZE) | number of output bytes |

## FbFieldBusService.SetNewPaInputs (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | pInputData | POINTER TO BYTE | pointer to input data structure |
| usiInputSize | USINT (0..MAX_MODULE_INPUT_SIZE) | number of input bytes |

## Set Process Data


- FbFieldBusService.GetNewPaOutputs (METH) - FbFieldBusService.SetNewPaInputs (METH)

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 06.02.2024 | 1.8.6.1 | u010663 | compiled SP16.3 |
| 11.11.2022 | 1.8.6.0 | u0103719 | add ParameterServiceList |
| 23.09.2021 | 1.8.5.1 | u010545 | update for test projects |
| 26.08.2021 | 1.8.5.0 | u010545 | CmpErrors changed to “CmpErrors2Interfaces” |
| 23.06.2021 | 1.8.4.1 | u010545 | expected fillbytes added |
| 11.01.2021 | 1.8.4.0 | u010545 | I_RegisterService implemented |
| 07.01.2021 | 1.8.3.0 | u010545 | modification for ADV-GW -> fillbytes |
| 29.09.2020 | 1.8.2.4 | u010545 | bugfix |
| 24.09.2020 | 1.8.2.3 | u010545 | PA-Exchange optimized |
| 28.04.2020 | 1.8.2.2 | u010545 | TimeOut register communication modified |
| 04.07.2019 | 1.8.2.1 | u010545 | Strategy for set PW modified |
| 14.06.2019 | 1.8.2.0 | u010545 | WriteRegister(..) modified -> set PW before write |
| 08.01.2019 | 1.8.1.0 | u015842 | Properties: free placeholder added |
| 23.04.2018 | 1.8.0.3 | u010545 | update documentation |
| 10.10.2017 | 1.8.0.2 | u010545 | bugfix register communication |
| 25.07.2017 | 1.8.0.1 | u010545 | include error for not supported register service |
| 29.06.2017 | 1.8.0.0 | u010545 | splitt WagoSysModuleBase |
| 06.04.2017 | 1.7.0.0 | u010545 | created for new module access concept |

WagoSysFieldbusServices

WagoSysFieldbusServices

### Other Components


## 15 FieldBus Services


- FbFieldBusService (FB) I_ModuleAccess Info FbFieldBusService.GetBusType (METH) Set Process Data - FbFieldBusService.GetNewPaOutputs (METH) - FbFieldBusService.SetNewPaInputs (METH)

## I_ModuleAccess


- Info FbFieldBusService.GetBusType (METH)

## Info ¶


- FbFieldBusService.GetBusType (METH)

## Parameter (PARAMS)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | REGISTER_COM_TIMEOUT | TIME | TIME#5s0ms | Timeout for access to terminal configuration values which are located in registers |
| PARAMETER_COM_TIMEOUT | TIME | TIME#5s0ms | Timeout for access to terminal configuration values which are located as parameter |