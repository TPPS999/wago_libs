# WagoSysKbusAsyncCom_Internal_PFC v1.4.0.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysKbusAsyncCom_Internal_PFC
- **Version:** 1.4.0.1
- **Categories:** WAGO Internal|Feature|LocalBus|K-Bus
- **Namespace:** WagoSysKbusAsyncCom_Internal
- **Author:** WAGO / u015479

### Description ¶


This document is automatically generated.

target specific library for PFC

This document is automatically generated. target specific library for PFC

### Contents: ¶


Contents: - Project Information - Library Information - Function Blocks FbConfigureCommon (FB) - FbConfigureParameter (FB) - FbConfigureRegister (FB) - FbConfigureRegisterCommon (FB) - FbConfigureRegisterPW (FB) - FbGetModuleInformation (FB) - FbGetTimingInformation (FB) Functions - FuGetLocalbusTimingInfo (FUN) - FuResetLocalbusTimingInfo (FUN) Methods - FbConfigureCommon.Close (METH) - FbConfigureCommon.Open (METH) - FbConfigureParameter.PollRead (METH) - FbConfigureParameter.PollReadList (METH) - FbConfigureParameter.PollWrite (METH) - FbConfigureParameter.PollWriteList (METH) - FbConfigureParameter.StartRead (METH) - FbConfigureParameter.StartReadList (METH) - FbConfigureParameter.StartWrite (METH) - FbConfigureParameter.StartWriteList (METH) - ... and 22 more Interfaces Program Organization Function Groups Base Components Modular Components Main Interfaces - 10 Main Interface - 10 Main Interface - 10 Main Interface - 10 Main Interface - 10 Main Interface - 10 Main Interface - 10 Main Interface Internal Components - 90 Internal - WagoSysKbusAsyncCom_Internal_PFC Library Documentation Global Variable Lists

### Indices and tables ¶


Based on WagoSysKbusAsyncCom_Internal_PFC.library, last modified 29.05.2024, 19:55:34. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysKbusAsyncCom_Internal_PFC.library, last modified 29.05.2024, 19:55:34. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysKbusAsyncCom_Internal_PFC.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:55:34 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:55:34 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u015479 |
| DefaultNamespace | WagoSysKbusAsyncCom_Internal |
| Released | bool | False |
| Company | string | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysKbusAsyncCom_Internal_PFC |
| NoPlaceholder |  |
| Version | version | 1.4.0.1 |
| Title | string | WagoSysKbusAsyncCom_Internal_PFC |
| LibraryCategories | library-category-list | WAGO Internal\|Feature\|LocalBus\|K-Bus |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False HideWhenReferencedAsDependency: True | QualifiedOnly: False SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysKbusAsyncCom_Internal_Common Library Identification : Placeholder: WagoSysKbusAsyncCom_Internal_Common Default Resolution: WagoSysKbusAsyncCom_Internal_Common, * (WAGO) Namespace: WagoSysKbusAsyncCom_Internal_Common Library Properties : WagoSysTypedefs_Internal_32Bit Library Identification : Placeholder: WagoSysTypedefsInternal Default Resolution: WagoSysTypedefs_Internal_32Bit, * (WAGO) Namespace: WagoTypesInternal Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties :

### Function Blocks


## FbConfigureCommon (FB)


This is the fundamental FB of this library. This function block gives asynchronous access to module data. - 10 Main Interface FbConfigureCommon.Close (METH) - FbConfigureCommon.Open (METH)

## FbConfigureParameter (FB)


This function block gives access to module praraneter data.

This function block gives access to module praraneter data. - 10 Main Interface FbConfigureParameter.PollRead (METH) - FbConfigureParameter.PollReadList (METH) - FbConfigureParameter.PollWrite (METH) - FbConfigureParameter.PollWriteList (METH) - FbConfigureParameter.StartRead (METH) - FbConfigureParameter.StartReadList (METH) - FbConfigureParameter.StartWrite (METH) - FbConfigureParameter.StartWriteList (METH)

## FbConfigureRegister (FB)


This function block gives access to module register data.

This function block gives access to module register data. - 10 Main Interface FbConfigureRegister.StartWrite (METH) - FbConfigureRegister.StartWriteList (METH)

## FbConfigureRegisterCommon (FB)


This function block gives access to module register data.

This function block gives access to module register data. - 10 Main Interface FbConfigureRegisterCommon.PollRead (METH) - FbConfigureRegisterCommon.PollReadList (METH) - FbConfigureRegisterCommon.PollWrite (METH) - FbConfigureRegisterCommon.PollWriteList (METH) - FbConfigureRegisterCommon.StartRead (METH) - FbConfigureRegisterCommon.StartReadList (METH)

## FbConfigureRegisterPW (FB)


This function block gives access to module register data.

This function block gives access to module register data. - 10 Main Interface FbConfigureRegisterPW.StartWrite (METH) - FbConfigureRegisterPW.StartWriteList (METH)

## FbGetModuleInformation (FB)


This function block gives access to specific module informations.

This function block gives access to specific module informations. - 10 Main Interface FbGetModuleInformation.Close (METH) - FbGetModuleInformation.Open (METH) - FbGetModuleInformation.PollRead_UID (METH) - FbGetModuleInformation.StartRead_UID (METH)

## FbGetTimingInformation (FB)


This function block gives access to local bus timing informations.

This function block gives access to local bus timing informations. - 10 Main Interface FbGetTimingInformation.Close (METH) - FbGetTimingInformation.Open (METH) - FbGetTimingInformation.PollRead (METH) - FbGetTimingInformation.PollReset (METH) - FbGetTimingInformation.StartRead (METH) - FbGetTimingInformation.StartReset (METH)

### Functions


## FuGetLocalbusTimingInfo (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuGetLocalbusTimingInfo | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Output | diCurDuration | DINT | current duration in [us] |
| diMinDuration | DINT | minimum duration in [us] |
| diMaxDuration | DINT | maximum duration in [us] |
| diAvrDuration | DINT | average duration in [us] |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |

Function reads all measured durations in KBUS device driver.

Interface variables Function reads all measured durations in KBUS device driver.

## FuResetLocalbusTimingInfo (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuResetLocalbusTimingInfo | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |

Function resets measured minimum, maximum and average durations in KBUS device driver.

Interface variables Function resets measured minimum, maximum and average durations in KBUS device driver.

### Methods


## FbConfigureCommon.Close (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Close | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |

This method closes a channel for asynchronous communication.

Interface variables This method closes a channel for asynchronous communication.

## FbConfigureCommon.Open (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Open | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_VALUE_PTR | Parameter error invalid output pointer |
| LPKD_REQ_EVA_ERROR_NO_HANDLE_GEN | Library module has no handle generated |
| LPKD_REQ_EVA_GEN_ERROR | Unspecified internal error occurred |

This method opens a channel for asynchronous communication.

Interface variables This method opens a channel for asynchronous communication.

## FbConfigureParameter.PollRead (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollRead | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | parameter number in module |
| Output | uiValue | UINT | content of addressed parameter |
| uiStatus | UINT | content of status register 57 |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_INFO_CON_ACTIVE | Evaluation information connection is active -> poll again |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_ERROR_VALUE_PTR | Parameter error invalid output pointer |
| LPKD_REQ_EVA_ERROR_CONT_NOT_FIT | Content does not fit to request |
| LPKD_REQ_EVA_ERROR_TIMEOUT_TERM | Parameter access status from module: TIMEOUT |
| LPKD_REQ_EVA_ERROR_BUF_OVF_TERM | Parameter access status from module: BUFFER OVERFLOW |
| LPKD_REQ_EVA_ERROR_PRM_ERR_TERM | Parameter access status from module: PARAMETER ERROR |

This method polls a previous started read request.

Interface variables This method polls a previous started read request.

## FbConfigureParameter.PollReadList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollReadList | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | first parameter to read |
| uiParameterCnt | UINT | number of parameters to read (1 .. 256) |
| Inout | aValue | ARRAY [0..255] OF UINT | content for addressed parameters |
| Output | uiStatus | UINT | content of status register 57 |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_INFO_CON_ACTIVE | Evaluation information connection is active -> poll again |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_ERROR_VALUE_PTR | Parameter error invalid output pointer |
| LPKD_REQ_EVA_ERROR_CONT_NOT_FIT | Content does not fit to request |
| LPKD_REQ_EVA_ERROR_TIMEOUT_TERM | Parameter access status from module: TIMEOUT |
| LPKD_REQ_EVA_ERROR_BUF_OVF_TERM | Parameter access status from module: BUFFER OVERFLOW |
| LPKD_REQ_EVA_ERROR_PRM_ERR_TERM | Parameter access status from module: PARAMETER ERROR |

This method polls a previous started read list request.

Interface variables This method polls a previous started read list request. Note : Output list will be filled from first index (zero) independent of requested start parameter.

## FbConfigureParameter.PollWrite (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollWrite | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | parameter number in module |
| uiValue | UINT | content for addressed parameter |
| Output | uiStatus | UINT | content of status register 57 |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_INFO_CON_ACTIVE | Evaluation information connection is active -> poll again |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_ERROR_VALUE_PTR | Parameter error invalid output pointer |
| LPKD_REQ_EVA_ERROR_CONT_NOT_FIT | Content does not fit to request |
| LPKD_REQ_EVA_ERROR_TIMEOUT_TERM | Parameter access status from module: TIMEOUT |
| LPKD_REQ_EVA_ERROR_BUF_OVF_TERM | Parameter access status from module: BUFFER OVERFLOW |
| LPKD_REQ_EVA_ERROR_PRM_ERR_TERM | Parameter access status from module: PARAMETER ERROR |

This method polls a previous started write request.

Interface variables This method polls a previous started write request.

## FbConfigureParameter.PollWriteList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollWriteList | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | first parameter number to write |
| uiParameterCnt | UINT | number of parameters to write (1 .. 256) |
| Output | uiStatus | UINT | content of status register 57 |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_INFO_CON_ACTIVE | Evaluation information connection is active -> poll again |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_ERROR_VALUE_PTR | Parameter error invalid input pointer |
| LPKD_REQ_EVA_ERROR_CONT_NOT_FIT | Content does not fit to request |
| LPKD_REQ_EVA_ERROR_TIMEOUT_TERM | Parameter access status from module: TIMEOUT |
| LPKD_REQ_EVA_ERROR_BUF_OVF_TERM | Parameter access status from module: BUFFER OVERFLOW |
| LPKD_REQ_EVA_ERROR_PRM_ERR_TERM | Parameter access status from module: PARAMETER ERROR |

This method polls a previous started write list request.

Interface variables This method polls a previous started write list request.

## FbConfigureParameter.StartRead (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartRead | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | parameter number in module |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_GEN_ERROR | Unspecified internal error occurred |
| LPKD_REQ_EVA_ERROR_TERM_IDX | Invalid slot number / module not present |
| LPKD_REQ_EVA_NO_REGISTER_COM | Module does not support register communication |
| LPKD_REQ_EVA_ERROR_REG_PAR_IDX | Invalid parameter number |
| LPKD_REQ_EVA_NO_PARAMETER_CHAN | Module does not support parameter channel |

This method starts a read request.

Interface variables This method starts a read request.

## FbConfigureParameter.StartReadList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartReadList | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | first parameter number to read |
| uiParameterCnt | UINT | number of parameters to read (1 .. 256) |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_GEN_ERROR | Unspecified internal error occurred |
| LPKD_REQ_EVA_ERROR_TERM_IDX | Invalid slot number / module not present |
| LPKD_REQ_EVA_NO_REGISTER_COM | Module does not support register communication |
| LPKD_REQ_EVA_ERROR_REG_PAR_IDX | Invalid parameter number |
| LPKD_REQ_EVA_ERROR_REQ_COUNT | Number of requested words leads to invalid parameter number |
| LPKD_REQ_EVA_NO_PARAMETER_CHAN | Module does not support parameter channel |

This method starts a read list request.

Interface variables This method starts a read list request.

## FbConfigureParameter.StartWrite (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartWrite | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module ‘ |
| usiParameterNo | USINT | parameter number in module |
| uiValue | UINT | content for addressed parameter |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_GEN_ERROR | Unspecified internal error occurred |
| LPKD_REQ_EVA_ERROR_TERM_IDX | Invalid slot number / module not present |
| LPKD_REQ_EVA_NO_REGISTER_COM | Module does not support register communication |
| LPKD_REQ_EVA_ERROR_REG_PAR_IDX | Invalid parameter number |
| LPKD_REQ_EVA_NO_PARAMETER_CHAN | Module does not support parameter channel |

This method starts a write request.

Interface variables This method starts a write request.

## FbConfigureParameter.StartWriteList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartWriteList | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | first parameter to write |
| uiParameterCnt | UINT | number of parameters to write (1 .. 256) |
| Inout | aValue | ARRAY [0..255] OF UINT | content for addressed parameters |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_ERROR_VALUE_PTR | Parameter error invalid input pointer |
| LPKD_REQ_EVA_GEN_ERROR | Unspecified internal error occurred |
| LPKD_REQ_EVA_ERROR_TERM_IDX | Invalid slot number / module not present |
| LPKD_REQ_EVA_NO_REGISTER_COM | Module does not support register communication |
| LPKD_REQ_EVA_ERROR_REG_PAR_IDX | Invalid parameter number |
| LPKD_REQ_EVA_ERROR_REQ_COUNT | Number of requested words leads to invalid parameter number |
| LPKD_REQ_EVA_NO_PARAMETER_CHAN | Module does not support parameter channel |

This method starts a write list request.

Interface variables This method starts a write list request. Note : Input list will be copied from first index (zero) independent of requested start parameter.

## FbConfigureRegister.StartWrite (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartWrite | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | register number in module |
| uiValue | UINT | content for addressed register |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_GEN_ERROR | Unspecified internal error occurred |
| LPKD_REQ_EVA_ERROR_TERM_IDX | Invalid slot number / module not present |
| LPKD_REQ_EVA_NO_REGISTER_COM | Module does not support register communication |
| LPKD_REQ_EVA_ERROR_TABLE_IDX | Invalid channel number |
| LPKD_REQ_EVA_ERROR_REG_PAR_IDX | Invalid register number |

This method starts a write request.

Interface variables This method starts a write request.

## FbConfigureRegister.StartWriteList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartWriteList | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | first register to write |
| usiRegisterCnt | USINT | number of registers to write (1 .. 64) |
| Inout | aValue | ARRAY [0..63] OF UINT | content for addressed registers |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_ERROR_VALUE_PTR | Parameter error invalid input pointer |
| LPKD_REQ_EVA_GEN_ERROR | Unspecified internal error occurred |
| LPKD_REQ_EVA_ERROR_TERM_IDX | Invalid slot number / module not present |
| LPKD_REQ_EVA_NO_REGISTER_COM | Module does not support register communication |
| LPKD_REQ_EVA_ERROR_TABLE_IDX | Invalid channel number |
| LPKD_REQ_EVA_ERROR_REG_PAR_IDX | Invalid register number |
| LPKD_REQ_EVA_ERROR_REQ_COUNT | Number of requested words leads to invalid register number |

This method starts a write list request.

Interface variables This method starts a write list request. Note : Input list will be copied from first index (zero) independent of requested start parameter.

## FbConfigureRegisterCommon.PollRead (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollRead | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | register number in module |
| Output | uiValue | UINT | content of addressed register |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_INFO_CON_ACTIVE | Evaluation information connection is active -> poll again |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_ERROR_VALUE_PTR | Parameter error invalid output pointer |
| LPKD_REQ_EVA_ERROR_CONT_NOT_FIT | Content does not fit to request |

This method polls a previous started read request.

Interface variables This method polls a previous started read request.

## FbConfigureRegisterCommon.PollReadList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollReadList | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | first register to read |
| usiRegisterCnt | USINT | number of registers to read (1 .. 64) |
| Inout | aValue | ARRAY [0..63] OF UINT | content for addressed registers |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_INFO_CON_ACTIVE | Evaluation information connection is active -> poll again |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_ERROR_VALUE_PTR | Parameter error invalid output pointer |
| LPKD_REQ_EVA_ERROR_CONT_NOT_FIT | Content does not fit to request |

This method polls a previous started read list request.

Interface variables This method polls a previous started read list request. Note : Output list will be filled from first index (zero) independent of requested start register.

## FbConfigureRegisterCommon.PollWrite (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollWrite | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | register number in module |
| uiValue | UINT | content for addressed register |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_INFO_CON_ACTIVE | Evaluation information connection is active -> poll again |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_ERROR_VALUE_PTR | Parameter error invalid output pointer |
| LPKD_REQ_EVA_ERROR_CONT_NOT_FIT | Content does not fit to request |

This method polls a previous started write request.

Interface variables This method polls a previous started write request.

## FbConfigureRegisterCommon.PollWriteList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollWriteList | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | first register to write |
| usiRegisterCnt | USINT | number of registers to write (1 .. 64) |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_INFO_CON_ACTIVE | Evaluation information connection is active -> poll again |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_ERROR_VALUE_PTR | Parameter error invalid input pointer |
| LPKD_REQ_EVA_ERROR_CONT_NOT_FIT | Content does not fit to request |

This method polls a previous started write list request.

Interface variables This method polls a previous started write list request. Note : Input list will be copied from first index (zero) independent of requested start register.

## FbConfigureRegisterCommon.StartRead (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartRead | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | register number in module |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_GEN_ERROR | Unspecified internal error occurred |
| LPKD_REQ_EVA_ERROR_TERM_IDX | Invalid slot number / module not present |
| LPKD_REQ_EVA_NO_REGISTER_COM | Module does not support register communication |
| LPKD_REQ_EVA_ERROR_TABLE_IDX | Invalid channel number |
| LPKD_REQ_EVA_ERROR_REG_PAR_IDX | Invalid register number |

This method starts a read request.

Interface variables This method starts a read request.

## FbConfigureRegisterCommon.StartReadList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartReadList | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | first register to read |
| usiRegisterCnt | USINT | number of registers to read (1 .. 64) |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_GEN_ERROR | Unspecified internal error occurred |
| LPKD_REQ_EVA_ERROR_TERM_IDX | Invalid slot number / module not present |
| LPKD_REQ_EVA_NO_REGISTER_COM | Module does not support register communication |
| LPKD_REQ_EVA_ERROR_TABLE_IDX | Invalid channel number |
| LPKD_REQ_EVA_ERROR_REG_PAR_IDX | Invalid register number |
| LPKD_REQ_EVA_ERROR_REQ_COUNT | Number of requested words leads to invalid register number |

This method starts a read list request.

Interface variables This method starts a read list request.

## FbConfigureRegisterPW.StartWrite (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartWrite | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | register number in module |
| uiPassWord | UINT | password to conrol write protection |
| uiValue | UINT | content for addressed register |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_GEN_ERROR | Unspecified internal error occurred |
| LPKD_REQ_EVA_ERROR_TERM_IDX | Invalid slot number / module not present |
| LPKD_REQ_EVA_NO_REGISTER_COM | Module does not support register communication |
| LPKD_REQ_EVA_ERROR_TABLE_IDX | Invalid channel number |
| LPKD_REQ_EVA_ERROR_REG_PAR_IDX | Invalid register number |

This method starts a write request.

Interface variables This method starts a write request.

## FbConfigureRegisterPW.StartWriteList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartWriteList | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | first register to write |
| usiRegisterCnt | USINT | number of registers to write (1 .. 64) |
| uiPassWord | UINT | password to conrol write protection |
| Inout | aValue | ARRAY [0..63] OF UINT | content for addressed registers |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | Parameter error invalid handle |
| LPKD_REQ_EVA_ERROR_VALUE_PTR | Parameter error invalid input pointer |
| LPKD_REQ_EVA_GEN_ERROR | Unspecified internal error occurred |
| LPKD_REQ_EVA_ERROR_TERM_IDX | Invalid slot number / module not present |
| LPKD_REQ_EVA_NO_REGISTER_COM | Module does not support register communication |
| LPKD_REQ_EVA_ERROR_TABLE_IDX | Invalid channel number |
| LPKD_REQ_EVA_ERROR_REG_PAR_IDX | Invalid register number |
| LPKD_REQ_EVA_ERROR_REQ_COUNT | Number of requested words leads to invalid register number |

This method starts a write list request.

Interface variables This method starts a write list request. Note : Input list will be copied from first index (zero) independent of requested start parameter.

## FbGetModuleInformation.Close (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Close | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |

Interface variables This method does not really close a channel. Therefore it returns always ‘LPKD_REQ_EVA_STATUS_OK’.

## FbGetModuleInformation.Open (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Open | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |

Interface variables This method does not really open a channel. Therefore it returns always ‘LPKD_REQ_EVA_STATUS_OK’.

## FbGetModuleInformation.PollRead_UID (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollRead_UID | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| Output | udiUID | UDINT | unified identification number |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_TERM_IDX | Invalid slot number / module not present |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |

This method polls a previous started read request.

Interface variables This method polls a previous started read request.

## FbGetModuleInformation.StartRead_UID (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartRead_UID | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |

Interface variables This method does not really starts a read access. Therefore it returns always ‘LPKD_REQ_EVA_STATUS_OK’.

## FbGetTimingInformation.Close (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Close | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |

Interface variables This method does not really close a channel. Therefore it returns always ‘LPKD_REQ_EVA_STATUS_OK’.

## FbGetTimingInformation.Open (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Open | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |

Interface variables This method does not really open a channel. Therefore it returns always ‘LPKD_REQ_EVA_STATUS_OK’.

## FbGetTimingInformation.PollRead (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollRead | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| Output | diCurDuration | DINT | current duration in [us] |
| diMinDuration | DINT | minimum duration in [us] |
| diMaxDuration | DINT | maximum duration in [us] |
| diAvrDuration | DINT | average duration in [us] |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_TERM_IDX | Invalid slot number / module not present |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |

This method polls a previous started read request.

Interface variables This method polls a previous started read request.

## FbGetTimingInformation.PollReset (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollReset | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |

| Status Codes |
| LPKD_REQ_EVA_STATUS_OK | Success |
| LPKD_REQ_EVA_ERROR_TERM_IDX | Invalid slot number / module not present |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | Library module has no KBUS access |

This method polls a previous started reset request.

Interface variables This method polls a previous started reset request.

## FbGetTimingInformation.StartRead (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartRead | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |

Interface variables This method does not really starts a read access. Therefore it returns always ‘LPKD_REQ_EVA_STATUS_OK’.

## FbGetTimingInformation.StartReset (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartReset | WagoSysKbusAsyncCom_Internal_Common.eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |

Interface variables This method does not really starts a reset request. Therefore it returns always ‘LPKD_REQ_EVA_STATUS_OK’.

## I_ConfigureRegisterPW.StartWrite (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartWrite | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | register number in module |
| uiPassWord | UINT | password to conrol write protection |
| uiValue | UINT | content for addressed register |

## I_ConfigureRegisterPW.StartWriteList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartWriteList | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | first register to write |
| usiRegisterCnt | USINT | number of registers to write (1 .. 64) |
| uiPassWord | UINT | password to conrol write protection |
| Inout | aValue | ARRAY [0..63] OF UINT | content for addressed registers |

### Interfaces


## I_ConfigureRegisterPW (ITF)


- I_ConfigureRegisterPW.StartWrite (METH) - I_ConfigureRegisterPW.StartWriteList (METH)

### Program Organization


## 20 Program Organization Units


- 10 Functions FuGetLocalbusTimingInfo (FUN) - FuResetLocalbusTimingInfo (FUN) 20 Modular - FbConfigureParameter (FB) 10 Main Interface FbConfigureParameter.PollRead (METH) - FbConfigureParameter.PollReadList (METH) - FbConfigureParameter.PollWrite (METH) - FbConfigureParameter.PollWriteList (METH) - FbConfigureParameter.StartRead (METH) - FbConfigureParameter.StartReadList (METH) - FbConfigureParameter.StartWrite (METH) - FbConfigureParameter.StartWriteList (METH) FbConfigureRegister (FB) - 10 Main Interface FbConfigureRegister.StartWrite (METH) - FbConfigureRegister.StartWriteList (METH) FbConfigureRegisterPW (FB) - 10 Main Interface FbConfigureRegisterPW.StartWrite (METH) - FbConfigureRegisterPW.StartWriteList (METH) FbGetModuleInformation (FB) - 10 Main Interface FbGetModuleInformation.Close (METH) - FbGetModuleInformation.Open (METH) - FbGetModuleInformation.PollRead_UID (METH) - FbGetModuleInformation.StartRead_UID (METH) FbGetTimingInformation (FB) - 10 Main Interface FbGetTimingInformation.Close (METH) - FbGetTimingInformation.Open (METH) - FbGetTimingInformation.PollRead (METH) - FbGetTimingInformation.PollReset (METH) - FbGetTimingInformation.StartRead (METH) - FbGetTimingInformation.StartReset (METH) 30 Base - FbConfigureCommon (FB) 10 Main Interface FbConfigureCommon.Close (METH) - FbConfigureCommon.Open (METH) FbConfigureRegisterCommon (FB) - 10 Main Interface FbConfigureRegisterCommon.PollRead (METH) - FbConfigureRegisterCommon.PollReadList (METH) - FbConfigureRegisterCommon.PollWrite (METH) - FbConfigureRegisterCommon.PollWriteList (METH) - FbConfigureRegisterCommon.StartRead (METH) - FbConfigureRegisterCommon.StartReadList (METH)

### Function Groups


## 10 Functions


- FuGetLocalbusTimingInfo (FUN) - FuResetLocalbusTimingInfo (FUN)

### Base Components


## 30 Base


- FbConfigureCommon (FB) 10 Main Interface FbConfigureCommon.Close (METH) - FbConfigureCommon.Open (METH) FbConfigureRegisterCommon (FB) - 10 Main Interface FbConfigureRegisterCommon.PollRead (METH) - FbConfigureRegisterCommon.PollReadList (METH) - FbConfigureRegisterCommon.PollWrite (METH) - FbConfigureRegisterCommon.PollWriteList (METH) - FbConfigureRegisterCommon.StartRead (METH) - FbConfigureRegisterCommon.StartReadList (METH)

### Modular Components


## 20 Modular


- FbConfigureParameter (FB) 10 Main Interface FbConfigureParameter.PollRead (METH) - FbConfigureParameter.PollReadList (METH) - FbConfigureParameter.PollWrite (METH) - FbConfigureParameter.PollWriteList (METH) - FbConfigureParameter.StartRead (METH) - FbConfigureParameter.StartReadList (METH) - FbConfigureParameter.StartWrite (METH) - FbConfigureParameter.StartWriteList (METH) FbConfigureRegister (FB) - 10 Main Interface FbConfigureRegister.StartWrite (METH) - FbConfigureRegister.StartWriteList (METH) FbConfigureRegisterPW (FB) - 10 Main Interface FbConfigureRegisterPW.StartWrite (METH) - FbConfigureRegisterPW.StartWriteList (METH) FbGetModuleInformation (FB) - 10 Main Interface FbGetModuleInformation.Close (METH) - FbGetModuleInformation.Open (METH) - FbGetModuleInformation.PollRead_UID (METH) - FbGetModuleInformation.StartRead_UID (METH) FbGetTimingInformation (FB) - 10 Main Interface FbGetTimingInformation.Close (METH) - FbGetTimingInformation.Open (METH) - FbGetTimingInformation.PollRead (METH) - FbGetTimingInformation.PollReset (METH) - FbGetTimingInformation.StartRead (METH) - FbGetTimingInformation.StartReset (METH)

### Main Interfaces


## 10 Main Interface


- FbConfigureCommon.Close (METH) - FbConfigureCommon.Open (METH)

## 10 Main Interface


- FbGetTimingInformation.Close (METH) - FbGetTimingInformation.Open (METH) - FbGetTimingInformation.PollRead (METH) - FbGetTimingInformation.PollReset (METH) - FbGetTimingInformation.StartRead (METH) - FbGetTimingInformation.StartReset (METH)

## 10 Main Interface


- FbConfigureRegisterCommon.PollRead (METH) - FbConfigureRegisterCommon.PollReadList (METH) - FbConfigureRegisterCommon.PollWrite (METH) - FbConfigureRegisterCommon.PollWriteList (METH) - FbConfigureRegisterCommon.StartRead (METH) - FbConfigureRegisterCommon.StartReadList (METH)

## 10 Main Interface


- FbGetModuleInformation.Close (METH) - FbGetModuleInformation.Open (METH) - FbGetModuleInformation.PollRead_UID (METH) - FbGetModuleInformation.StartRead_UID (METH)

## 10 Main Interface


- FbConfigureRegisterPW.StartWrite (METH) - FbConfigureRegisterPW.StartWriteList (METH)

## 10 Main Interface


- FbConfigureParameter.PollRead (METH) - FbConfigureParameter.PollReadList (METH) - FbConfigureParameter.PollWrite (METH) - FbConfigureParameter.PollWriteList (METH) - FbConfigureParameter.StartRead (METH) - FbConfigureParameter.StartReadList (METH) - FbConfigureParameter.StartWrite (METH) - FbConfigureParameter.StartWriteList (METH)

## 10 Main Interface


- FbConfigureRegister.StartWrite (METH) - FbConfigureRegister.StartWriteList (METH)

### Internal Components


## 90 Internal


- I_ConfigureRegisterPW (ITF) I_ConfigureRegisterPW.StartWrite (METH) - I_ConfigureRegisterPW.StartWriteList (METH)

## WagoSysKbusAsyncCom_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysKbusAsyncCom_Internal_PFC |
| Version: | 1.4.0.1 |
| Categories: | WAGO Internal\|Feature\|LocalBus\|K-Bus |
| Namespace: | WagoSysKbusAsyncCom_Internal |
| Author: | WAGO / u015479 |

### Description


This document is automatically generated.

target specific library for PFC

This document is automatically generated. target specific library for PFC

### Contents:


- 20 Program Organization Units 10 Functions - 20 Modular - 30 Base 90 Internal - I_ConfigureRegisterPW (ITF) VersionHistory (GVL)

### Indices and tables


Based on WagoSysKbusAsyncCom_Internal_PFC.library, last modified 29.05.2024, 19:55:34. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysKbusAsyncCom_Internal_PFC.library, last modified 29.05.2024, 19:55:34. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 24.10.2023 | 1.4.0.1 | u010663 | 64-Bit adjustment ->SysTypes2Interfaces |
| 19.01.2023 | 1.4.0.0 | u015479 | functions ‘FuGetLocalbusTimingInfo()’ and ‘FuResetLocalbusTimingInfo()’ added |
| 23.11.2021 | 1.2.2.0 | u015479 | version 1.3.x.x discarded, version 1.2.1.0 reactivated and version number set to 1.2.2.0 |

WagoSysKbusAsyncCom_Internal_PFC.library

WagoSysKbusAsyncCom_Internal_PFC.library