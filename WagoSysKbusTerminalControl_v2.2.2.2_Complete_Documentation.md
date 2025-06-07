# WagoSysKbusTerminalControl v2.2.2.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysKbusTerminalControl
- **Version:** 2.2.2.2
- **Categories:** WAGO LayerView|Sys; WAGO Internal|Feature|LocalBus|K-Bus
- **Namespace:** WagoSysKbusTerminalControl
- **Author:** WAGO / u015479
- **Placeholder:** WagoSysKbusTerminalControl

### Description ¶


This document is automatically generated.

functionblocks to control Kbus terminals

This document is automatically generated. functionblocks to control Kbus terminals

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks FbGetKbusDrvRef (FB) - FbGetTerminalRef (FB) - FbSetTerminalRef (FB) Methods - FbGetTerminalRef.AllocateProcessData (METH) - FbGetTerminalRef.FreeProcessData (METH) - FbGetTerminalRef.GetConfMapState (METH) - FbGetTerminalRef.GetSlotNo (METH) - FbGetTerminalRef.ManualInitialize (METH) - FbSetTerminalRef.AllocateProcessData_PS (METH) - FbSetTerminalRef.AllocateProcessData_SD (METH) - FbSetTerminalRef.FreeProcessData (METH) - FbSetTerminalRef.Start_PDE_In_CurrentTask (METH) - FbSetTerminalRef.Stop_PDE (METH) - ... and 2 more Program Organization Global Variable Lists - ResultItems (GVL) - VersionHistory (GVL) Other Components - 20 Function Blocks - 40 Data Types - ePARTICULAR_CODES (ENUM)

### Indices and tables ¶


Based on WagoSysKbusTerminalControl.library, last modified 20.06.2024, 00:06:29. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysKbusTerminalControl.library, last modified 20.06.2024, 00:06:29. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysKbusTerminalControl Library Documentation


| Company: | WAGO |
| Title: | WagoSysKbusTerminalControl |
| Version: | 2.2.2.2 |
| Categories: | WAGO LayerView\|Sys; WAGO Internal\|Feature\|LocalBus\|K-Bus |
| Namespace: | WagoSysKbusTerminalControl |
| Author: | WAGO / u015479 |
| Placeholder: | WagoSysKbusTerminalControl |

### Description


This document is automatically generated.

functionblocks to control Kbus terminals

This document is automatically generated. functionblocks to control Kbus terminals

### Contents:


- 20 Program Organization Units 20 Function Blocks - 40 Data Types ResultItems (GVL) VersionHistory (GVL)

### Indices and tables


Based on WagoSysKbusTerminalControl.library, last modified 20.06.2024, 00:06:29. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysKbusTerminalControl.library, last modified 20.06.2024, 00:06:29. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysKbusTerminalControl.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 20.06.2024, 00:06:30 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 20.06.2024, 00:06:29 |
| Description | string | See: Description |
| Copyright | © 2014 – 2024 WAGO GmbH & Co. KG, Germany - All rights reserved. |
| Author | WAGO / u015479 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysKbusTerminalControl |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysKbusTerminalControl |
| DefaultNamespace | WagoSysKbusTerminalControl |
| Version | version | 2.2.2.2 |
| Title | string | WagoSysKbusTerminalControl |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys; WAGO Internal\|Feature\|LocalBus\|K-Bus |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. Base Interfaces Library Identification : Name: Base Interfaces Version: newest Company: System Namespace: IBaseLibrary Library Properties : CmpApp Library Identification : Placeholder: CmpApp Default Resolution: CmpApp, * (System) Namespace: CmpApp Library Properties : CmpErrors2 Interfaces Library Identification : Name: CmpErrors2 Interfaces Version: newest Company: System Namespace: CmpErrors Library Properties : CmpEventMgr Library Identification : Placeholder: CmpEventMgr Default Resolution: CmpEventMgr, * (System) Namespace: CmpEventMgr Library Properties : CmpIecTask Library Identification : Placeholder: CmpIecTask Default Resolution: CmpIecTask, * (System) Namespace: CmpIecTask Library Properties : CmpIoDrvC Library Identification : Placeholder: CmpIoDrvC Default Resolution: CmpIoDrvC, * (System) Namespace: CmpIoDrvCLibrary Library Properties : CmpLog Library Identification : Placeholder: CmpLog Default Resolution: CmpLog, * (System) Namespace: CmpLog Library Properties : IoStandard Library Identification : Placeholder: IoStandard Default Resolution: IoStandard, 3.5.4.0 (System) Namespace: IoStandard Library Properties : SysMem Library Identification : Placeholder: SysMem Default Resolution: SysMem, * (System) Namespace: SysMem Library Properties : SysSem Library Identification : Placeholder: SysSem Default Resolution: SysSem, * (System) Namespace: SysSem Library Properties : SysTask Library Identification : Placeholder: SysTask Default Resolution: SysTask, * (System) Namespace: SysTask Library Properties : WagoSysKbusTerminalControl_Internal_Common Library Identification : Placeholder: WagoSysKbusTerminalControl_Internal_Common Default Resolution: WagoSysKbusTerminalControl_Internal_Common, * (WAGO) Namespace: WagoSysKbusTerminalControlInternal_Common Library Properties : WagoSysKbusTerminalControl_Internal_PFC Library Identification : Placeholder: WagoSysKbusTerminalControlInternal Default Resolution: WagoSysKbusTerminalControl_Internal_PFC, * (WAGO) Namespace: WagoSysKbusTerminalControlInternal Library Properties : WagoSysPlainMem Library Identification : Placeholder: WagoSysPlainMem Default Resolution: WagoSysPlainMem, * (WAGO) Namespace: WagoSysPlainMem Library Properties : WagoSysTypedefs_Internal_32Bit Library Identification : Placeholder: WagoSysTypedefsInternal Default Resolution: WagoSysTypedefs_Internal_32Bit, * (WAGO) Namespace: WagoTypesInternal Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties : WagoTypesKbusTerminalControl Library Identification : Placeholder: WagoTypesKbusTerminalControl Default Resolution: WagoTypesKbusTerminalControl, * (WAGO) Namespace: WagoTypesKbusTerminalControl Library Properties :

### Function Blocks


## FbGetKbusDrvRef (FB) ¶


## FbGetTerminalRef (FB)


This is the fundamental FB of this library.

This is the fundamental FB of this library. This function block gives access to module proccess data. Caution: Behaviour for outputs in stop is independent of PLC settings in control! Outputs will be set to default in stop! - FbGetTerminalRef.AllocateProcessData (METH) - FbGetTerminalRef.FreeProcessData (METH) - FbGetTerminalRef.GetConfMapState (METH) - FbGetTerminalRef.GetSlotNo (METH) - FbGetTerminalRef.ManualInitialize (METH)

## FbSetTerminalRef (FB)


Caution: Behaviour for outputs in stop is independent of PLC settings in control! Outputs will be set to default in stop! - FbSetTerminalRef.AllocateProcessData_PS (METH) - FbSetTerminalRef.AllocateProcessData_SD (METH) - FbSetTerminalRef.FreeProcessData (METH) - FbSetTerminalRef.Start_PDE_In_CurrentTask (METH) - FbSetTerminalRef.Stop_PDE (METH)

### Methods


## FbGetTerminalRef.AllocateProcessData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | AllocateProcessData | WagoTypes.eResultCode |  |
| Input | usiSlotNo | USINT | terminal slot number |
| udiModuleId | UDINT | unified module identification number |

| Result Codes |
| 0 | Success |
| 215 | Configuration error |

This method allocates module process data.

This method provides module process data.

Interface variables This method allocates module process data. This method provides module process data. Note: Result code of this function is OK (0) or EAPP (200) plus an error specific value see ePARTICULAR_CODES.

## FbGetTerminalRef.FreeProcessData (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FreeProcessData | WagoTypes.eResultCode |

| Result Codes |
| 0 | Success |
| 211 | Active process data exchange |
| 225 | Error from io driver update configuration |

This method frees module process data.

This method frees module process data.

Interface variables This method frees module process data. This method frees module process data. Note: Result code of this function is OK (0) or EAPP (200) plus an error specific value see ePARTICULAR_CODES.

## FbGetTerminalRef.GetConfMapState (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetConfMapState | RTS_IEC_RESULT |  |
| Inout | eCnfSts | eCONFIG_STS | output: modul configuration state |
| eMapSts | eMAPPING_STS | output: modul data mapping state |

## FbGetTerminalRef.GetSlotNo (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetSlotNo | RTS_IEC_RESULT |  |
| Inout | usiSlotNo | USINT | output: slot number of traget KBUS modul |

## FbGetTerminalRef.ManualInitialize (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | ManualInitialize | WagoTypes.eResultCode |  |  |
| Input | usiSlotNo | USINT | 0 | terminal slot number |
| uiInputSize | UINT | 0 | number of input bytes |
| pInputData | POINTER TO BYTE | 0 | pointer to input data structure |
| uiOutputSize | UINT | 0 | number of output bytes |
| pOutputData | POINTER TO BYTE | 0 | pointer to output data structure |

| Result Codes |
| 0 | Success |
| 201 | Error module is auto initialized and can’t be reinitialized |
| 202 | Invalid slot number |
| 203 | Input pointer and size do not fit |
| 204 | Output pointer and size do not fit |

This method initialize process data references.

Interface variables This method initialize process data references. Note: Pre-condition for using this method: Function block is not auto initialized. Note: If all input values are null, method call will reset internal values. Note: Result code of this function is OK (0) or EAPP (200) plus an error specific value see ePARTICULAR_CODES.

## FbSetTerminalRef.AllocateProcessData_PS (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | AllocateProcessData_PS | WagoTypes.eResultCode |  |
| Input | usiSlotNo | USINT | terminal slot number |
| udiModuleId | UDINT | unified module identification number |
| Output | uiInputSize | UINT | number of active input bytes |
| pInputData | POINTER TO BYTE | pointer to input data structure |
| uiOutputSize | UINT | number of active output bytes |
| pOutputData | POINTER TO BYTE | pointer to output data structure |

| Result Codes |
| 0 | Success |
| 210 | No access to driver |
| 211 | Active process data exchange |
| 212 | Error from io manager |
| 214 | Error module not connected to KBUS |
| 215 | Configuration error |
| 216 | Error module stopped |
| 225 | Error from driver update configuration |

This method allocates module process data.

This method provides packed module process data.

Interface variables This method allocates module process data. This method provides packed module process data. Note: Method calls update configuration in driver. Note: Result code of this function is OK (0) or EAPP (200) plus an error specific value see ePARTICULAR_CODES.

## FbSetTerminalRef.AllocateProcessData_SD (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | AllocateProcessData_SD | WagoTypes.eResultCode |  |  |
| Input | usiSlotNo | USINT | 0 | terminal slot number |
| udiModuleId | UDINT | 0 | unified module identification number |
| pInDesc | POINTER TO typeDataDesc |  | pointer to array of input data descriptions |
| uiNoInDesc | UINT | 0 | number of elements input data descriptions |
| pOutDesc | POINTER TO typeDataDesc |  | pointer to array of output data descriptions |
| uiNoOutDesc | UINT | 0 | number of elements output data descriptions |
| Output | uiInputSize | UINT | 0 | number of active input bytes |
| pInputData | POINTER TO BYTE | WagoTypesInternal.Udint_to_Pointer(0) | pointer to input data structure |
| uiOutputSize | UINT | 0 | number of active output bytes |
| pOutputData | POINTER TO BYTE | WagoTypesInternal.Udint_to_Pointer(0) | pointer to output data structure |

| Result Codes |
| 0 | Success |
| 210 | No access to driver |
| 211 | Active process data exchange |
| 212 | Error from io manager |
| 214 | Error module not connected to KBUS |
| 215 | Configuration error |
| 216 | Error module stopped |
| 225 | Error from driver update configuration |

This method allocates module process data structures.

This method provides module process data structures.

Interface variables This method allocates module process data structures. This method provides module process data structures. Note: Method calls update configuration in driver. Note: Result code of this function is OK (0) or EAPP (200) plus an error specific value see ePARTICULAR_CODES.

## FbSetTerminalRef.FreeProcessData (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FreeProcessData | WagoTypes.eResultCode |

| Result Codes |
| 0 | Success |
| 211 | Active process data exchange |
| 225 | Error from io driver update configuration |

This method resets dynamic module process data exchange.

This method delets dynamic module configuration in driver.

Interface variables This method resets dynamic module process data exchange. This method delets dynamic module configuration in driver. Note: Method calls update configuration in driver. Note: Result code of this function is OK (0) or EAPP (200) plus an error specific value see ePARTICULAR_CODES.

## FbSetTerminalRef.Start_PDE_In_CurrentTask (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Start_PDE_In_CurrentTask | WagoTypes.eResultCode |

| Result Codes |
| 0 | Success |
| 206 | Inconsistent input parameter set in device description |
| 207 | Inconsistent output parameter set in device description |
| 208 | Error from event handler |
| 209 | Invalid task handle |
| 210 | No access to driver |
| 211 | Active process data exchange |
| 212 | Error from io manager |
| 213 | Error module is not auto initialized |
| 214 | Error module not connected to KBUS |
| 215 | Configuration error |
| 216 | Error module stopped |
| 218 | Unsupported process data type in device description |
| 226 | Error from driver update mapping |

This method starts program controlled process data exchange.

This method connects module IO - update to current IEC task.

Interface variables This method starts program controlled process data exchange. This method connects module IO - update to current IEC task. Note: Pre-condition for using this method: Function block has to be auto initialized. Note: Result code of this function is OK (0) or EAPP (200) plus an error specific value see ePARTICULAR_CODES.

## FbSetTerminalRef.Stop_PDE (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Stop_PDE | WagoTypes.eResultCode |

| Result Codes |
| 0 | Success |
| 208 | Error from event handler |
| 225 | Error from driver update configuration |
| 226 | Error from driver update mapping |

This method stops program controlled process data exchange.

This method disconnects module IO - update from any IEC task.

Interface variables This method stops program controlled process data exchange. This method disconnects module IO - update from any IEC task. Note: Method calls driver. Note: Pre-condition for using this method: Function block has to be auto initialized. Note: Result code of this function is OK (0) or EAPP (200) plus an error specific value see ePARTICULAR_CODES.

## eGET_TERM_REF_STATES (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| GTRS_NotInitialized | 0 | State bevore call of ‘FB_Init’ or after call of ‘FB_Exit’ |
| GTRS_Initialized | 1 | State after call of ‘FB_Init’, ‘ManualInitialize’ or ‘FreeProcessData’ |
| GTRS_ManualInit | 2 | State after call of ‘ManualInitialize’ |
| GTRS_AutoInit | 3 | State after call of ‘AutoInitialize’ or ‘Stop_PDE’ |
| GTRS_PDE_I_Active | 4 | State after call of ‘StartPDE_InCurrentTask’ |
| GTRS_Manual_PDE | 5 | State after call of ‘EnalbleManual_PDE’ |
| GTRS_PD_Available | 6 | State after call of ‘AllocateProcessData’ or ‘Stop_PDE’ |
| GTRS_PDE_II_Active | 7 | State after call of ‘StartPDE_InCurrentTask’ |
| GTRS_Manual_PDE_II | 8 | State after call of ‘EnalbleManual_PDE’ |

## eSET_TERM_REF_STATES (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| STRS_NotInitialized | 0 | State bevore call of ‘FB_Init’ or after call of ‘FB_Exit’ |
| STRS_Initialized | 1 | State after call of ‘FB_Init’ or ‘FreeProcessData’ |
| STRS_PD_Available | 2 | State after call of ‘AllocateProcessData_xx’ or ‘Stop_PDE’ |
| STRS_PDE_Active | 3 | State after call of ‘StartPDE_InCurrentTask’ |
| STRS_Manual_PDE | 4 | State after call of ‘EnalbleManual_PDE’ |

### Program Organization


## 20 Program Organization Units


- 20 Function Blocks FbGetKbusDrvRef (FB) - FbGetTerminalRef (FB) FbGetTerminalRef.AllocateProcessData (METH) - FbGetTerminalRef.FreeProcessData (METH) - FbGetTerminalRef.GetConfMapState (METH) - FbGetTerminalRef.GetSlotNo (METH) - FbGetTerminalRef.ManualInitialize (METH) FbSetTerminalRef (FB) - FbSetTerminalRef.AllocateProcessData_PS (METH) - FbSetTerminalRef.AllocateProcessData_SD (METH) - FbSetTerminalRef.FreeProcessData (METH) - FbSetTerminalRef.Start_PDE_In_CurrentTask (METH) - FbSetTerminalRef.Stop_PDE (METH) 40 Data Types - eGET_TERM_REF_STATES (ENUM) - ePARTICULAR_CODES (ENUM) - eSET_TERM_REF_STATES (ENUM)

### Global Variable Lists


## ResultItems (GVL)


| Scope | Name | Type |
| --- | --- | --- |
| Constant | ERROR | ARRAY [0..28] OF typResultItem |

| Value | Level | Description |
| --- | --- | --- |
| OK | eSeverity.none | ‘evaluation OK’ |
| E_AUTO_INITIALIZED | eSeverity.error | ‘error module is auto initialized’ |
| E_SLOT_NO | eSeverity.error | ‘invalid slot number’ |
| E_INPUT_REFFERENCE | eSeverity.error | ‘input pointer and size do not fit’ |
| E_OUTPUT_REFFERENCE | eSeverity.error | ‘output pointer and size do not fit’ |
| E_DEV_DESC | eSeverity.error | ‘inconsistent parameter set in device description’ |
| E_DEV_DESC_INPUT | eSeverity.error | ‘inconsistent input parameter set in device description’ |
| E_DEV_DESC_OUTPUT | eSeverity.error | ‘inconsistent output parameter set in device description’ |
| E_EVENT_HANDLER | eSeverity.error | ‘error from event handler’ |
| E_TASK_HANDLE | eSeverity.error | ‘invalid task handle’ |
| E_DRIVER_NOT_FOUND | eSeverity.error | ‘no access to driver’ |
| E_ACTIVE_PDE | eSeverity.error | ‘active process data exchange’ |
| E_IO_MANAGER | eSeverity.error | ‘error from io manager’ |
| E_NOT_AUTO_INITIALIZED | eSeverity.error | ‘error module is not auto initialized’ |
| E_MODULE_NOT_FOUND | eSeverity.error | ‘error module not connected to KBUS’ |
| E_CONFIGURATION | eSeverity.error | ‘configuration error’ |
| E_MODULE_STOPPED | eSeverity.error | ‘error module stopped’ |
| E_NOT_ENABLED | eSeverity.error | ‘error manual process data exchange is not enabled’ |
| E_DEV_DESC_TYPE | eSeverity.error | ‘unsupported process data type in device description’ |
| E_PD_PREV_ALLOC | eSeverity.error | ‘process data has been previously allocated’ |
| E_NO_MEMORY | eSeverity.error | ‘error no memory available’ |
| E_UNSUPPORTED_UID | eSeverity.error | ‘error unsupported terminal type addressed’ |
| E_FB_REFFERENCE | eSeverity.error | ‘invalid function block refference’ |
| E_MAN_INITIALIZED | eSeverity.error | ‘error module is manual initialized’ |
| E_CON_NOT_FOUND | eSeverity.error | ‘error connector not found’ |
| E_DRIVER_UC | eSeverity.error | ‘error from driver update configuration’ |
| E_DRIVER_UM | eSeverity.error | ‘error from driver update mapping’ |
| E_DRIVER_RI | eSeverity.error | ‘error from driver read inputs’ |
| E_DRIVER_WO | eSeverity.error | ‘error FROM driver write outputs’ |

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 14.06.2024 | 2.2.2.2 | u015479 | quick fix for polarion WAT-36657: in ‘FbGetTerminalRef’ and ‘FbSetTerminalRef’ ‘UpdateInputs2()’ added; in ‘FbDataFromIoDriver’ ‘RdInputs()’ corrected |
| 07.02.2024 | 2.2.2.1 | u010663 | replace CmpErrors by CmpErrors2 |
| 21.09.2022 | 2.2.2.0 | u015479 | quick fix for polarion:VV-4253 |
| 25.08.2022 | 2.2.1.0 | u015479 | in methods ‘FbGetTerminalRef.EnableManual_PDE()’ and ‘FbGetTerminalRef.Start_PDE_In_CurrentTask()’ connector status check corrected; in method ‘FbGetTerminalRef.GetConfMapState()’ pointer to connector corrected |
| 18.08.2022 | 2.2.0.0 | u015479 | methods ‘FbGetTerminalRef.GetSlotNo()’ and ‘FbGetTerminalRef.GetConfMapState()’added; method ‘FbDataFromIoDriver.Conf_PDE()’ error codes corrected; in methods ‘FbGetTerminalRef.Start_PDE_In_CurrentTask()’ and ‘FbGetTerminalRef.EnableManual_PDE()’ connector status checked |
| 03.08.2022 | 2.1.3.0 | u015479 | in method ‘FbGetTerminalRef.AutoInitialize()’ attribut ‘_xValidData’ set to TRUE for device descriptions without parameter 4 resp. SlotNo |
| 03.08.2022 | 2.1.2.0 | u015479 | in methods ‘EnableManual_PDE()’ control value for update mapping set to ‘MAPPING_CTRL_DYNAMIC’ |
| 02.08.2022 | 2.1.1.0 | u015479 | in method ‘AutoInitialize()’ of ‘FbGetKbusRef’ warning message deactivated |
| 14.07.2022 | 2.1.0.0 | u015479 | ‘FbSetTerminalRef’: call of method ‘IoDrvUpdateConfiguration()’ replaced by IoDrvUpdateConfiguration_dynamic()’; io-drvier moduletype check changed from ‘gc_ParentConnType’ to ‘gc_LB_ChildConnType’; ‘GLC’: ‘gc_ParentConnType’ redefined from 32778 to 32779 and ‘gc_LB_ChildConnType’ with ‘32778’ added; |
| 06.07.2022 | 2.0.0.0 | u015479 | ‘FbDataFromIoDriver’: declaration of attribute ‘_DrvWrapper’ changed to ‘WagoSysKbusTerminalControlInternal.FbIoDrvWrapper’; methods ‘InitPDE()’, ‘ExitPDE()’ and ‘RegisterCallback()’ changed according to changed attribute; ‘FbSetTerminalref’: method ‘EnableManual_PDE()’ changed according to changed attribute; ‘FbGetTerminalref’: method ‘EnableManual_PDE()’ changed according to changed attribute; method ‘AutoInitialize()’ extended by temporary warning message ‘WagoSysKbusTerminalControl V2 under construction...’; based on version 1.7.6.1 |

WagoSysKbusTerminalControl.library

WagoSysKbusTerminalControl.library

### Other Components


## 20 Function Blocks


- FbGetKbusDrvRef (FB) - FbGetTerminalRef (FB) FbGetTerminalRef.AllocateProcessData (METH) - FbGetTerminalRef.FreeProcessData (METH) - FbGetTerminalRef.GetConfMapState (METH) - FbGetTerminalRef.GetSlotNo (METH) - FbGetTerminalRef.ManualInitialize (METH) FbSetTerminalRef (FB) - FbSetTerminalRef.AllocateProcessData_PS (METH) - FbSetTerminalRef.AllocateProcessData_SD (METH) - FbSetTerminalRef.FreeProcessData (METH) - FbSetTerminalRef.Start_PDE_In_CurrentTask (METH) - FbSetTerminalRef.Stop_PDE (METH)

## 40 Data Types


- eGET_TERM_REF_STATES (ENUM) - ePARTICULAR_CODES (ENUM) - eSET_TERM_REF_STATES (ENUM)

## ePARTICULAR_CODES (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| STATUS_OK | WagoTypes.eResultCode.OK + 0 | 0 evaluation OK |
| E_AUTO_INITIALIZED | WagoTypes.eResultCode.EAPP + 1 | 201 error module is auto initialized |
| E_SLOT_NO | WagoTypes.eResultCode.EAPP + 2 | 202 invalid slot number |
| E_INPUT_REFFERENCE | WagoTypes.eResultCode.EAPP + 3 | 203 input pointer and size do not fit |
| E_OUTPUT_REFFERENCE | WagoTypes.eResultCode.EAPP + 4 | 204 output pointer and size do not fit |
| E_DEV_DESC | WagoTypes.eResultCode.EAPP + 5 | 205 inconsistent parameter set in device description |
| E_DEV_DESC_INPUT | WagoTypes.eResultCode.EAPP + 6 | 206 inconsistent input parameter set in device description |
| E_DEV_DESC_OUTPUT | WagoTypes.eResultCode.EAPP + 7 | 207 inconsistent output parameter set in device description |
| E_EVENT_HANDLER | WagoTypes.eResultCode.EAPP + 8 | 208 error from event handler |
| E_TASK_HANDLE | WagoTypes.eResultCode.EAPP + 9 | 209 invalid task handle |
| E_DRIVER_NOT_FOUND | WagoTypes.eResultCode.EAPP + 10 | 210 no access to driver |
| E_ACTIVE_PDE | WagoTypes.eResultCode.EAPP + 11 | 211 active process data exchange |
| E_IO_MANAGER | WagoTypes.eResultCode.EAPP + 12 | 212 error from io manager |
| E_NOT_AUTO_INITIALIZED | WagoTypes.eResultCode.EAPP + 13 | 213 error module is not auto initialized |
| E_MODULE_NOT_FOUND | WagoTypes.eResultCode.EAPP + 14 | 214 error module not connected to KBUS |
| E_CONFIGURATION | WagoTypes.eResultCode.EAPP + 15 | 215 configuration error |
| E_MODULE_STOPPED | WagoTypes.eResultCode.EAPP + 16 | 216 error module stopped |
| E_NOT_ENABLED | WagoTypes.eResultCode.EAPP + 17 | 217 error manual process data exchange is not enabled |
| E_DEV_DESC_TYPE | WagoTypes.eResultCode.EAPP + 18 | 218 unsupported process data type in device description |
| E_PD_PREV_ALLOC | WagoTypes.eResultCode.EAPP + 19 | 219 process data has been previously allocated |
| E_NO_MEMORY | WagoTypes.eResultCode.EAPP + 20 | 220 error no memory available |
| E_UNSUPPORTED_UID | WagoTypes.eResultCode.EAPP + 21 | 221 error unsupported terminal type addressed |
| E_FB_REFFERENCE | WagoTypes.eResultCode.EAPP + 22 | 222 invalid function block refference |
| E_MAN_INITIALIZED | WagoTypes.eResultCode.EAPP + 23 | 223 error module is manual initialized |
| E_CON_NOT_FOUND | WagoTypes.eResultCode.EAPP + 24 | 224 error connector not found |
| E_DRIVER_UC | WagoTypes.eResultCode.EAPP + 25 | 225 error from driver update configuration |
| E_DRIVER_UM | WagoTypes.eResultCode.EAPP + 26 | 226 error from driver update mapping |
| E_DRIVER_RI | WagoTypes.eResultCode.EAPP + 27 | 227 error from driver read inputs |
| E_DRIVER_WO | WagoTypes.eResultCode.EAPP + 28 | 228 error from driver write outputs |

return values