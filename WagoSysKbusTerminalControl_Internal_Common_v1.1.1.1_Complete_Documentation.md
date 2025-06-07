# WagoSysKbusTerminalControl_Internal_Common v1.1.1.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysKbusTerminalControl_Internal_Common
- **Version:** 1.1.1.1
- **Categories:** WAGO Internal|Feature|LocalBus|K-Bus
- **Namespace:** WagoSysKbusTerminalControlInternal_Common
- **Author:** WAGO / u015479
- **Placeholder:** WagoSysKbusTerminalControl_Internal_Common

### Description ¶


This document is automatically generated.

common data types

This document is automatically generated. common data types

### Contents: ¶


Contents: - Project Information - Library Information - Methods I_DynamicDriverAccess.IoDrvCalculateSlotNumber (METH) - I_DynamicDriverAccess.IoDrvGetConfMapState (METH) - I_DynamicDriverAccess.IoDrvUpdateConfiguration_dynamic (METH) - I_DynamicDriverAccess.IoDrvUpdateMapping_dynamic (METH) Interfaces Program Organization Internal Components Global Variable Lists Other Components - 10 Interfaces - 40 Data Types - eCONFIG_CTRL (ENUM) - eCONFIG_STS (ENUM) - eKBTC_LIB_STATUS_CODES (ENUM) - eMAPPING_CTRL (ENUM) - eMAPPING_STS (ENUM)

### Indices and tables ¶


Based on WagoSysKbusTerminalControl_Internal_Common.library, last modified 29.05.2024, 19:55:48. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysKbusTerminalControl_Internal_Common.library, last modified 29.05.2024, 19:55:48. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysKbusTerminalControl_Internal_Common.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:55:48 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:55:48 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u015479 |
| DefaultNamespace | WagoSysKbusTerminalControlInternal_Common |
| Placeholder | WagoSysKbusTerminalControl_Internal_Common |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysKbusTerminalControl_Internal_Common |
| Version | version | 1.1.1.1 |
| Title | string | WagoSysKbusTerminalControl_Internal_Common |
| LibraryCategories | library-category-list | WAGO Internal\|Feature\|LocalBus\|K-Bus |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False HideWhenReferencedAsDependency: True | QualifiedOnly: False SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. IoStandard Library Identification : Placeholder: IoStandard Default Resolution: IoStandard, 3.5.16.0 (System) Namespace: IoStandard Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties :

### Methods


## I_DynamicDriverAccess.IoDrvCalculateSlotNumber (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | IoDrvCalculateSlotNumber | RTS_IEC_RESULT |  |
| Input | pConnector | POINTER TO IoStandard.IoConfigConnector | input: pointer to static configured connector of traget KBUS modul |
| Inout | udiSlotNo | UDINT | output: slot number of traget KBUS modul |

## I_DynamicDriverAccess.IoDrvGetConfMapState (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | IoDrvGetConfMapState | RTS_IEC_RESULT |  |
| Input | pConnector | POINTER TO IoStandard.IoConfigConnector | input: pointer to static configured connector of traget KBUS modul |
| Inout | eCnfSts | eCONFIG_STS | output: modul configuration state |
| eMapSts | eMAPPING_STS | output: modul data mapping state |

## I_DynamicDriverAccess.IoDrvUpdateConfiguration_dynamic (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | IoDrvUpdateConfiguration_dynamic | RTS_IEC_RESULT |  |
| Input | pConnectorList | POINTER TO IoStandard.IoConfigConnector | input: pointer to list of connectors |
| nCount | DINT | input: number of connectors in list |
| eCtrl | eCONFIG_CTRL | input: control update configuration |

## I_DynamicDriverAccess.IoDrvUpdateMapping_dynamic (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | IoDrvUpdateMapping_dynamic | RTS_IEC_RESULT |  |
| Input | pTaskMapList | POINTER TO IoStandard.IoConfigTaskMap | input: pointer to list of task mappings |
| nCount | DINT | input: number of task mappings in list |
| eCtrl | eMAPPING_CTRL | input: control update mapping |

### Interfaces


## I_DynamicDriverAccess (ITF)


- I_DynamicDriverAccess.IoDrvCalculateSlotNumber (METH) - I_DynamicDriverAccess.IoDrvGetConfMapState (METH) - I_DynamicDriverAccess.IoDrvUpdateConfiguration_dynamic (METH) - I_DynamicDriverAccess.IoDrvUpdateMapping_dynamic (METH)

### Program Organization


## 20 Program Organization Units


- 10 Interfaces I_DynamicDriverAccess (ITF) I_DynamicDriverAccess.IoDrvCalculateSlotNumber (METH) - I_DynamicDriverAccess.IoDrvGetConfMapState (METH) - I_DynamicDriverAccess.IoDrvUpdateConfiguration_dynamic (METH) - I_DynamicDriverAccess.IoDrvUpdateMapping_dynamic (METH) 40 Data Types - eCONFIG_CTRL (ENUM) - eCONFIG_STS (ENUM) - eKBTC_LIB_STATUS_CODES (ENUM) - eMAPPING_CTRL (ENUM) - eMAPPING_STS (ENUM)

### Internal Components


## WagoSysKbusTerminalControl_Internal_Common Library Documentation


| Company: | WAGO |
| Title: | WagoSysKbusTerminalControl_Internal_Common |
| Version: | 1.1.1.1 |
| Categories: | WAGO Internal\|Feature\|LocalBus\|K-Bus |
| Namespace: | WagoSysKbusTerminalControlInternal_Common |
| Author: | WAGO / u015479 |
| Placeholder: | WagoSysKbusTerminalControl_Internal_Common |

### Description


This document is automatically generated.

common data types

This document is automatically generated. common data types

### Contents:


- 20 Program Organization Units 10 Interfaces - 40 Data Types VersionHistory (GVL)

### Indices and tables


Based on WagoSysKbusTerminalControl_Internal_Common.library, last modified 29.05.2024, 19:55:48. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysKbusTerminalControl_Internal_Common.library, last modified 29.05.2024, 19:55:48. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 24.10.2023 | 1.1.1.1 | u010663 | 64-Bit adjustment ->SysTypes2Interfaces |
| 18.08.2022 | 1.1.1.0 | u015479 | error code ‘KBTC_E_DEACTIVATED’ added |
| 12.07.2022 | 1.1.0.0 | u015479 | ‘gc_ParentConnType’ redefined from 32778 to 32779; constant for KBUS and local bus connectors defined |
| 25.05.2022 | 1.0.0.0 | u015479 | based on V0.0.0.4; interface and data types added; GCL renamed to GCL_WSKTCIC |

WagoSysKbusTerminalControl_Internal_Common.library

WagoSysKbusTerminalControl_Internal_Common.library

### Other Components


## 10 Interfaces


- I_DynamicDriverAccess (ITF) I_DynamicDriverAccess.IoDrvCalculateSlotNumber (METH) - I_DynamicDriverAccess.IoDrvGetConfMapState (METH) - I_DynamicDriverAccess.IoDrvUpdateConfiguration_dynamic (METH) - I_DynamicDriverAccess.IoDrvUpdateMapping_dynamic (METH)

## 40 Data Types


- eCONFIG_CTRL (ENUM) - eCONFIG_STS (ENUM) - eKBTC_LIB_STATUS_CODES (ENUM) - eMAPPING_CTRL (ENUM) - eMAPPING_STS (ENUM)

## eCONFIG_CTRL (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CONFIG_CTRL_CLEAR | 0 | remove dynamic configuration |
| CONFIG_CTRL_DYNAMIC | 3 | establish dynamic configuration |

## eCONFIG_STS (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CONFIG_STS_NOT_CONF | 0 | module not configured |
| CONFIG_STS_STAT_CONF | 1 | module static configured |
| CONFIG_STS_DYN_CONF | 2 | module dynamic configured |

## eKBTC_LIB_STATUS_CODES (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| KBTC_OK | 0 | evaluation OK |
| KBTC_E_AUTO_INITIALIZED | 1 | error module is auto initialized |
| KBTC_E_SLOT_NO | 2 | invalid slot number |
| KBTC_E_INPUT_REFFERENCE | 3 | input pointer and size do not fit |
| KBTC_E_OUTPUT_REFFERENCE | 4 | output pointer and size do not fit |
| KBTC_E_DEV_DESC | 5 | inconsistent parameter set in device description |
| KBTC_E_DEV_DESC_INPUT | 6 | inconsistent input parameter set in device description |
| KBTC_E_DEV_DESC_OUTPUT | 7 | inconsistent output parameter set in device description |
| KBTC_E_EVENT_HANDLER | 8 | error from event handler |
| KBTC_E_TASK_HANDLE | 9 | invalid task handle |
| KBTC_E_DRIVER_NOT_FOUND | 10 | no access to driver |
| KBTC_E_ACTIVE_PDE | 11 | active process data exchange |
| KBTC_E_IO_MANAGER | 12 | error from io manager |
| KBTC_E_NOT_AUTO_INITIALIZED | 13 | error module is not auto initialized |
| KBTC_E_MODULE_NOT_FOUND | 14 | error module not connected to BUS |
| KBTC_E_CONFIGURATION | 15 | configuration error |
| KBTC_E_MODULE_STOPPED | 16 | error module stopped |
| KBTC_E_NOT_ENABLED | 17 | error manual process data exchange is not enabled |
| KBTC_E_DEV_DESC_TYPE | 18 | unsupported process data type in device description |
| KBTC_E_PD_PREV_ALLOC | 19 | process data has been previously allocated |
| KBTC_E_NO_MEMORY | 20 | error no memory available |
| KBTC_E_UNSUPPORTED_UID | 21 | error unsopported terminal type addressed |
| KBTC_E_FB_REFFERENCE | 22 | invalid function block refference |
| KBTC_E_MAN_INITIALIZED | 23 | error module is manual initialized |
| KBTC_E_CON_NOT_FOUND | 24 | error connector not found |
| KBTC_E_DRIVER_UC | 25 | error from driver update configuration |
| KBTC_E_DRIVER_UM | 26 | error from driver update mapping |
| KBTC_E_DRIVER_RI | 27 | error from driver read inputs |
| KBTC_E_DRIVER_WO | 28 | error from driver write outputs |
| KBTC_E_DEACTIVATED | 29 | error connector is deactivated |
| KBTC_NO_OF_STATUS_CODES |  |  |

## eMAPPING_CTRL (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| MAPPING_CTRL_CLEAR | 0 | remove dynamic mapping |
| MAPPING_CTRL_DYNAMIC | 3 | establish dynamic mapping (override static mapping) |

## eMAPPING_STS (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| MAPPING_STS_NOT_MAPPED | 0 | modul data not mapped |
| MAPPING_STS_STAT_MAPPED | 1 | modul data static mapped |
| MAPPING_STS_DYN_MAPPED | 2 | modul data dynamic mapped |
| MAPPING_STS_OVERRIDE_STAT | 3 | static modul data mapping overridden |