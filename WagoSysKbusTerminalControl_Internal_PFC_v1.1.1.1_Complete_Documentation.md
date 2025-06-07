# WagoSysKbusTerminalControl_Internal_PFC v1.1.1.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysKbusTerminalControl_Internal_PFC
- **Version:** 1.1.1.1
- **Categories:** WAGO Internal|Feature|LocalBus|K-Bus
- **Namespace:** WagoSysKbusTerminalControlInternal
- **Author:** WAGO / u015479

### Description ¶


This document is automatically generated.

target specific library for PFC

This document is automatically generated. target specific library for PFC

### Contents: ¶


Contents: - Project Information - Library Information - Function Blocks - Functions FuGetKbusDriverInstance (FUN) - FuGetTerminalSlotNumber (FUN) - FuStoreKbusDrvInstance (FUN) Methods - FbIoDrvWrapper.IoDrvCalculateSlotNumber (METH) - FbIoDrvWrapper.IoDrvGetConfMapState (METH) - FbIoDrvWrapper.IoDrvUpdateConfiguration_dynamic (METH) - FbIoDrvWrapper.IoDrvUpdateMapping_dynamic (METH) Program Organization Function Groups Internal Components Global Variable Lists Other Components

### Indices and tables ¶


Based on WagoSysKbusTerminalControl_Internal_PFC.library, last modified 29.05.2024, 19:55:51. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysKbusTerminalControl_Internal_PFC.library, last modified 29.05.2024, 19:55:51. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysKbusTerminalControl_Internal_PFC.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:55:51 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:55:51 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u015479 |
| DefaultNamespace | WagoSysKbusTerminalControlInternal |
| Released | bool | False |
| Company | string | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysKbusTerminalControl_Internal_PFC |
| NoPlaceholder |  |
| Version | version | 1.1.1.1 |
| Title | string | WagoSysKbusTerminalControl_Internal_PFC |
| LibraryCategories | library-category-list | WAGO Internal\|Feature\|LocalBus\|K-Bus |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False HideWhenReferencedAsDependency: True | QualifiedOnly: False SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CmpErrors2 Interfaces Library Identification : Name: CmpErrors2 Interfaces Version: newest Company: System Namespace: CmpErrors Library Properties : CmpIoDrvC Library Identification : Placeholder: CmpIoDrvC Default Resolution: CmpIoDrvC, 3.5.2.0 (System) Namespace: CmpIoDrvCLibrary Library Properties : IoStandard Library Identification : Placeholder: IoStandard Default Resolution: IoStandard, * (System) Namespace: IoStandard Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysKbusTerminalControl_Internal_Common Library Identification : Placeholder: WagoSysKbusTerminalControl_Internal_Common Default Resolution: WagoSysKbusTerminalControl_Internal_Common, * (WAGO) Namespace: WagoSysKbusTerminalControlInternal_Common Library Properties : WagoSysTypedefs_Internal_32Bit Library Identification : Placeholder: WagoSysTypedefsInternal Default Resolution: WagoSysTypedefs_Internal_32Bit, * (WAGO) Namespace: WagoTypesInternal Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties :

### Function Blocks


## FbIoDrvWrapper (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Input | _pIBase | IBase | CmpIoDrvWrapper |
| _bIecDriver | BOOL | CmpIoDrvWrapper |
| Output | _pIBaseIEC | IBase | CmpIoDrvWrapper |

Interface variables - FbIoDrvWrapper.IoDrvCalculateSlotNumber (METH) - FbIoDrvWrapper.IoDrvGetConfMapState (METH) - FbIoDrvWrapper.IoDrvUpdateConfiguration_dynamic (METH) - FbIoDrvWrapper.IoDrvUpdateMapping_dynamic (METH)

### Functions


## FuGetKbusDriverInstance (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuGetKbusDriverInstance | IoStandard.IBase |  |
| Input | usiSlotNo | USINT | in: terminal slot number |
| Output | xIecDriver | BOOL | out: C or IEC - driver |
| ResultCode | WagoTypes.eResultCode | out: wago result code |
| pConnector | POINTER TO IoStandard.IoConfigConnector | out: pointer to Kbus parent connector |

## FuGetTerminalSlotNumber (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuGetTerminalSlotNumber | RTS_IEC_RESULT |  |
| Input | pConnector | POINTER TO IoStandard.IoConfigConnector | input: pointer to static configured connector of traget KBUS terminal |
| Inout | usiSlotNo | USINT | output: slot number of traget KBUS terminal |

Function reads terminal slot number

Function reads terminal slot number for asynchronous module access. Function uses given configured connector to read slot number.

Interface variables Function reads terminal slot number Function reads terminal slot number for asynchronous module access. Function uses given configured connector to read slot number. Result codes: ERR_OK Slot number written ERR_FAILED Internal error ERR_PARAMETER pConnector or pudiSlotNo was NULL ERR_NOT_SUPPORTED Driver does not support function ERR_TYPE_MISMATCH Connector type not supported ERR_NOTINITIALIZED No static configuration found ERR_DEVICE No slot number for current terminal available

## FuStoreKbusDrvInstance (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuStoreKbusDrvInstance | WagoTypes.eResultCode |
| Input | wModuleType | UINT |
| dwInstance | UDINT |
| pConnector | POINTER TO IoStandard.IoConfigConnector |

### Methods


## FbIoDrvWrapper.IoDrvCalculateSlotNumber (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | IoDrvCalculateSlotNumber | RTS_IEC_RESULT |  |
| Input | pConnector | POINTER TO IoStandard.IoConfigConnector | input: pointer to static configured connector of traget KBUS modul |
| Inout | udiSlotNo | UDINT | output: slot number of traget KBUS modul |

## FbIoDrvWrapper.IoDrvGetConfMapState (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | IoDrvGetConfMapState | RTS_IEC_RESULT |  |
| Input | pConnector | POINTER TO IoStandard.IoConfigConnector | input: pointer to static configured connector of traget KBUS modul |
| Inout | eCnfSts | eCONFIG_STS | output: modul configuration state |
| eMapSts | eMAPPING_STS | output: modul data mapping state |

## FbIoDrvWrapper.IoDrvUpdateConfiguration_dynamic (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | IoDrvUpdateConfiguration_dynamic | RTS_IEC_RESULT |  |
| Input | pConnectorList | POINTER TO IoStandard.IoConfigConnector | input: pointer to list of connectors |
| nCount | DINT | input: number of connectors in list |
| eCtrl | eCONFIG_CTRL | input: control update configuration |

## FbIoDrvWrapper.IoDrvUpdateMapping_dynamic (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | IoDrvUpdateMapping_dynamic | RTS_IEC_RESULT |  |
| Input | pTaskMapList | POINTER TO IoStandard.IoConfigTaskMap | input: pointer to list of task mappings |
| nCount | DINT | input: number of task mappings in list |
| eCtrl | eMAPPING_CTRL | input: control update mapping |

### Program Organization


## 20 Program Organization Units


- 10 Function Blocks FbIoDrvWrapper (FB) FbIoDrvWrapper.IoDrvCalculateSlotNumber (METH) - FbIoDrvWrapper.IoDrvGetConfMapState (METH) - FbIoDrvWrapper.IoDrvUpdateConfiguration_dynamic (METH) - FbIoDrvWrapper.IoDrvUpdateMapping_dynamic (METH) 20 Functions - FuGetKbusDriverInstance (FUN) - FuGetTerminalSlotNumber (FUN) - FuStoreKbusDrvInstance (FUN)

### Function Groups


## 20 Functions


- FuGetKbusDriverInstance (FUN) - FuGetTerminalSlotNumber (FUN) - FuStoreKbusDrvInstance (FUN)

### Internal Components


## WagoSysKbusTerminalControl_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysKbusTerminalControl_Internal_PFC |
| Version: | 1.1.1.1 |
| Categories: | WAGO Internal\|Feature\|LocalBus\|K-Bus |
| Namespace: | WagoSysKbusTerminalControlInternal |
| Author: | WAGO / u015479 |

### Description


This document is automatically generated.

target specific library for PFC

This document is automatically generated. target specific library for PFC

### Contents:


- 20 Program Organization Units 10 Function Blocks - 20 Functions VersionHistory (GVL)

### Indices and tables


Based on WagoSysKbusTerminalControl_Internal_PFC.library, last modified 29.05.2024, 19:55:51. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysKbusTerminalControl_Internal_PFC.library, last modified 29.05.2024, 19:55:51. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 24.10.2023 | 1.1.1.1 | u010663 | 64-Bit adjustment ->SysTypes2Interfaces |
| 18.08.2022 | 1.1.1.0 | u015479 | local handle used in methods ‘FbIoDrvWrapper.IoDrvCalculateSlotNumber()’ and ‘FbIoDrvWrapper.IoDrvGetConfMapState()’ |
| 12.07.2022 | 1.1.0.0 | u015479 | kbus parent redefined from 32778 to 32779; localbus child redefined from 32779 to 32778 |
| 01.06.2022 | 1.0.0.0 | u015479 | based on V0.0.0.4; funktion block, iec-function and C-functions added; GVL renamed to GVL_WSKTCIP |

WagoSysKbusTerminalControl_Internal_PFC.library

WagoSysKbusTerminalControl_Internal_PFC.library

### Other Components


## 10 Function Blocks


- FbIoDrvWrapper (FB) FbIoDrvWrapper.IoDrvCalculateSlotNumber (METH) - FbIoDrvWrapper.IoDrvGetConfMapState (METH) - FbIoDrvWrapper.IoDrvUpdateConfiguration_dynamic (METH) - FbIoDrvWrapper.IoDrvUpdateMapping_dynamic (METH)