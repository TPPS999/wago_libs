# WagoSysKbusAsyncCom v1.7.1.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysKbusAsyncCom
- **Version:** 1.7.1.2
- **Categories:** WAGO LayerView|Sys; WAGO FunctionalView|Connectivity|LocalBus; WAGO Internal|Feature|LocalBus|K-Bus; Application
- **Namespace:** WagoSysKbusAsyncCom
- **Author:** WAGO / u015479
- **Placeholder:** WagoSysKbusAsyncCom

### Description ¶


This document is automatically generated.

funktionblocks for asynchronous kbus communication

This document is automatically generated. funktionblocks for asynchronous kbus communication

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks FbReadModuleId (FB) - FbReadParameter (FB) - FbReadParameterList (FB) - FbReadRegister (FB) - FbReadRegisterList (FB) - FbReadTiming (FB) - FbWriteParameter (FB) - FbWriteParameterList (FB) - FbWriteRegister (FB) - FbWriteRegisterList (FB) Functions Program Organization Global Variable Lists - ResultItems (GVL) - VersionHistory (GVL) Other Components - 10 Register - 20 Parameter - 40 Data Types - 50 Miscellaneous - ePARTICULAR_CODES (ENUM) - typPARAMETER_ARRAY (ALIAS) - typREGISTER_ARRAY (ALIAS)

### Indices and tables ¶


Based on WagoSysKbusAsyncCom.library, last modified 29.05.2024, 19:55:39. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysKbusAsyncCom.library, last modified 29.05.2024, 19:55:39. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysKbusAsyncCom Library Documentation


| Company: | WAGO |
| Title: | WagoSysKbusAsyncCom |
| Version: | 1.7.1.2 |
| Categories: | WAGO LayerView\|Sys; WAGO FunctionalView\|Connectivity\|LocalBus; WAGO Internal\|Feature\|LocalBus\|K-Bus; Application |
| Namespace: | WagoSysKbusAsyncCom |
| Author: | WAGO / u015479 |
| Placeholder: | WagoSysKbusAsyncCom |

### Description


This document is automatically generated.

funktionblocks for asynchronous kbus communication

This document is automatically generated. funktionblocks for asynchronous kbus communication

### Contents:


- 20 Program Organization Units 10 Register - 20 Parameter - 40 Data Types - 50 Miscellaneous ResultItems (GVL) VersionHistory (GVL)

### Indices and tables


Based on WagoSysKbusAsyncCom.library, last modified 29.05.2024, 19:55:39. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysKbusAsyncCom.library, last modified 29.05.2024, 19:55:39. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysKbusAsyncCom.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:55:39 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:55:39 |
| Description | string | See: Description |
| DocFormat | reStructuredText |
| Author | WAGO / u015479 |
| DefaultNamespace | WagoSysKbusAsyncCom |
| Placeholder | WagoSysKbusAsyncCom |
| Company | WAGO |
| Title | WagoSysKbusAsyncCom |
| Project | WagoSysKbusAsyncCom |
| Version | version | 1.7.1.2 |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys; WAGO FunctionalView\|Connectivity\|LocalBus; WAGO Internal\|Feature\|LocalBus\|K-Bus; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CmpApp Library Identification : Placeholder: CmpApp Default Resolution: CmpApp, * (System) Namespace: CmpApp Library Properties : CmpErrors2 Interfaces Library Identification : Name: CmpErrors2 Interfaces Version: newest Company: System Namespace: CmpErrors Library Properties : CmpIecTask Library Identification : Placeholder: CmpIecTask Default Resolution: CmpIecTask, * (System) Namespace: CmpIecTask Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysBehaviourModels Library Identification : Placeholder: WagoSysBehaviourModels Default Resolution: WagoSysBehaviourModels, * (WAGO) Namespace: WagoSysBehaviourModels Library Properties : WagoSysKbusAsyncCom_Internal_Common Library Identification : Placeholder: WagoSysKbusAsyncCom_Internal_Common Default Resolution: WagoSysKbusAsyncCom_Internal_Common, * (WAGO) Namespace: WagoSysKbusAsyncCom_Internal_Common Library Properties : WagoSysKbusAsyncCom_Internal_PFC Library Identification : Placeholder: WagoSysKbusAsyncComInternal Default Resolution: WagoSysKbusAsyncCom_Internal_PFC, * (WAGO) Namespace: WagoSysKbusAsyncCom_Internal Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties :

### Function Blocks


## FbReadModuleId (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Input | xExecute | BOOL | Triggers the execution of the action. | FbBehaviourModelWagoExecute |
| Output | xDone | BOOL | Successful completion of the action. | FbBehaviourModelWagoExecute |
| xBusy | BOOL | Action is still in progress. | FbBehaviourModelWagoExecute |
| xError | BOOL | Indicates an error. | FbBehaviourModelWagoExecute |
| eStatus | eResultCode | Result code status | FbBehaviourModelWagoExecute |
| Input | usiSlotNo | USINT (1..250) | slot number |  |
| Output | udiValue | UDINT | unified module identification number |  |

| Result Codes |
| OK | Success |
| EAPP + GEN_ERROR | Unspecified internal error occurred |
| EAPP + ERROR_SLOT_NO | Invalid slot number / module not present |

This function block gives read access to module identification.

Interface variables This function block gives read access to module identification.

## FbReadParameter (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Input | xExecute | BOOL | Triggers the execution of the action. | FbBehaviourModelWagoExecute |
| Output | xDone | BOOL | Successful completion of the action. | FbBehaviourModelWagoExecute |
| xBusy | BOOL | Action is still in progress. | FbBehaviourModelWagoExecute |
| xError | BOOL | Indicates an error. | FbBehaviourModelWagoExecute |
| eStatus | eResultCode | Result code status | FbBehaviourModelWagoExecute |
| Input | usiSlotNo | USINT (1..250) | slot number | FbParameterAccess |
| usiParameterNo | USINT (0..255) | parameter number | FbParameterAccess |
| Output | uiStatus | UINT | content of status register 57 | FbParameterAccess |
| uiValue | UINT | content of addressed register |  |

| Result Codes |
| OK | Success |
| EAPP + GEN_ERROR | Unspecified internal error occurred |
| EAPP + ERROR_SLOT_NO | Invalid slot number / module not present |
| EAPP + NO_REGISTER_COM | Module does not support register communication |
| EAPP + NO_PARAMETER_CHAN | Module does not support parameter channel |
| EAPP + ERROR_REG_PAR_NO | Invalid parameter number |
| EAPP + ERROR_TIMEOUT_TERM | Parameter access status from module: TIMEOUT |
| EAPP + ERROR_BUF_OVF_TERM | Parameter access status from module: BUFFER OVERFLOW |
| EAPP + ERROR_PRM_ERR_TERM | Parameter access status from module: PARAMETER ERROR |

This function block gives read access to one addressed parameter of a module.

Interface variables This function block gives read access to one addressed parameter of a module. Caution: Function block interrupts process data exchange several times for several cycles!

## FbReadParameterList (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Input | xExecute | BOOL | Triggers the execution of the action. | FbBehaviourModelWagoExecute |
| Output | xDone | BOOL | Successful completion of the action. | FbBehaviourModelWagoExecute |
| xBusy | BOOL | Action is still in progress. | FbBehaviourModelWagoExecute |
| xError | BOOL | Indicates an error. | FbBehaviourModelWagoExecute |
| eStatus | eResultCode | Result code status | FbBehaviourModelWagoExecute |
| Input | usiSlotNo | USINT (1..250) | slot number | FbParameterAccess |
| usiParameterNo | USINT (0..255) | parameter number | FbParameterAccess |
| Output | uiStatus | UINT | content of status register 57 | FbParameterAccess |
| Input | uiParameterCnt | UINT (1..256) | number of parameters |  |
| Inout | aValue | typPARAMETER_ARRAY | content of addressed parameters |  |

| Result Codes |
| OK | Success |
| EAPP + GEN_ERROR | Unspecified internal error occurred |
| EAPP + ERROR_SLOT_NO | Invalid slot number / module not present |
| EAPP + NO_REGISTER_COM | Module does not support register communication |
| EAPP + NO_PARAMETER_CHAN | Module does not support parameter channel |
| EAPP + ERROR_REG_PAR_NO | Invalid parameter number |
| EAPP + ERROR_REQ_COUNT | Number of requested words leads to invalid parameter number |
| EAPP + ERROR_TIMEOUT_TERM | Parameter access status from module: TIMEOUT |
| EAPP + ERROR_BUF_OVF_TERM | Parameter access status from module: BUFFER OVERFLOW |
| EAPP + ERROR_PRM_ERR_TERM | Parameter access status from module: PARAMETER ERROR |

This function block gives read access to addressed parameters of a module.

Interface variables This function block gives read access to addressed parameters of a module. Caution: Function block interrupts process data exchange several times for several cycles! Note: Output list will be filled from first index (zero) independent of requested start parameter.

## FbReadRegister (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Input | xExecute | BOOL | Triggers the execution of the action. | FbBehaviourModelWagoExecute |
| Output | xDone | BOOL | Successful completion of the action. | FbBehaviourModelWagoExecute |
| xBusy | BOOL | Action is still in progress. | FbBehaviourModelWagoExecute |
| xError | BOOL | Indicates an error. | FbBehaviourModelWagoExecute |
| eStatus | eResultCode | Result code status | FbBehaviourModelWagoExecute |
| Input | usiSlotNo | USINT (1..250) | slot number | FbRegisterAccess |
| usiChannelNo | USINT (0..7) | channel number | FbRegisterAccess |
| usiRegisterNo | USINT (0..63) | register number | FbRegisterAccess |
| Output | uiValue | UINT | content of addressed register |  |

| Result Codes |
| OK | Success |
| EAPP + GEN_ERROR | Unspecified internal error occurred |
| EAPP + ERROR_SLOT_NO | Invalid slot number / module not present |
| EAPP + NO_REGISTER_COM | Module does not support register communication |
| EAPP + ERROR_CHANNEL_NO | Invalid channel number |
| EAPP + ERROR_REG_PAR_NO | Invalid register number |

This function block gives read access to one addressed register of a module.

Interface variables This function block gives read access to one addressed register of a module. Caution: Function block interrupts process data exchange several times for several cycles!

## FbReadRegisterList (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Input | xExecute | BOOL | Triggers the execution of the action. | FbBehaviourModelWagoExecute |
| Output | xDone | BOOL | Successful completion of the action. | FbBehaviourModelWagoExecute |
| xBusy | BOOL | Action is still in progress. | FbBehaviourModelWagoExecute |
| xError | BOOL | Indicates an error. | FbBehaviourModelWagoExecute |
| eStatus | eResultCode | Result code status | FbBehaviourModelWagoExecute |
| Input | usiSlotNo | USINT (1..250) | slot number | FbRegisterAccess |
| usiChannelNo | USINT (0..7) | channel number | FbRegisterAccess |
| usiRegisterNo | USINT (0..63) | register number | FbRegisterAccess |
| usiRegisterCnt | USINT (1..64) | number of registers |  |
| Inout | aValue | typREGISTER_ARRAY | content of addressed registers |  |

| Result Codes |
| OK | Success |
| EAPP + GEN_ERROR | Unspecified internal error occurred |
| EAPP + ERROR_SLOT_NO | Invalid slot number / module not present |
| EAPP + NO_REGISTER_COM | Module does not support register communication |
| EAPP + ERROR_CHANNEL_NO | Invalid channel number |
| EAPP + ERROR_REG_PAR_NO | Invalid register number |
| EAPP + ERROR_REQ_COUNT | Number of requested words leads to invalid register number |

This function block gives read access to addressed registers of a module.

Interface variables This function block gives read access to addressed registers of a module. Caution: Function block interrupts process data exchange several times for several cycles! Note: Output list will be filled from first index (zero) independent of requested start register.

## FbReadTiming (FB)


| Scope | Name | Type | Initial | Comment | Inherited from |
| --- | --- | --- | --- | --- | --- |
| Input | xExecute | BOOL |  | Triggers the execution of the action. | FbBehaviourModelWagoExecute |
| Output | xDone | BOOL |  | Successful completion of the action. | FbBehaviourModelWagoExecute |
| xBusy | BOOL |  | Action is still in progress. | FbBehaviourModelWagoExecute |
| xError | BOOL |  | Indicates an error. | FbBehaviourModelWagoExecute |
| eStatus | eResultCode |  | Result code status | FbBehaviourModelWagoExecute |
| Input | usiSlotNo | USINT (0..250) |  | slot number |  |
| xResetDurations | BOOL |  | true: reset and read durations; false: read durations |  |
| Output | diCurDuration | DINT |  | current duration in [us] |  |
| diMinDuration | DINT | 16#7FFFFFFF | minimum duration in [us] |  |
| diMaxDuration | DINT |  | maximum duration in [us] |  |
| diAvrDuration | DINT |  | average duration in [us] |  |

| Result Codes |
| OK | Success |
| EAPP + GEN_ERROR | Unspecified internal error occurred |
| EAPP + ERROR_SLOT_NO | Invalid slot number / module not present |
| EAPP + ERROR_NO_KBUS_ACC | Head station/addressed module has no KBUS access |

This function block gives read access to KBUS timing information.

Interface variables This function block gives read access to KBUS timing information.

## FbWriteParameter (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Input | xExecute | BOOL | Triggers the execution of the action. | FbBehaviourModelWagoExecute |
| Output | xDone | BOOL | Successful completion of the action. | FbBehaviourModelWagoExecute |
| xBusy | BOOL | Action is still in progress. | FbBehaviourModelWagoExecute |
| xError | BOOL | Indicates an error. | FbBehaviourModelWagoExecute |
| eStatus | eResultCode | Result code status | FbBehaviourModelWagoExecute |
| Input | usiSlotNo | USINT (1..250) | slot number | FbParameterAccess |
| usiParameterNo | USINT (0..255) | parameter number | FbParameterAccess |
| Output | uiStatus | UINT | content of status register 57 | FbParameterAccess |
| Input | uiValue | UINT | content for addressed register |  |

| Result Codes |
| OK | Success |
| EAPP + GEN_ERROR | Unspecified internal error occurred |
| EAPP + ERROR_SLOT_NO | Invalid slot number / module not present |
| EAPP + NO_REGISTER_COM | Module does not support register communication |
| EAPP + NO_PARAMETER_CHAN | Module does not support parameter channel |
| EAPP + ERROR_REG_PAR_NO | Invalid parameter number |
| EAPP + ERROR_TIMEOUT_TERM | Parameter access status from module: TIMEOUT |
| EAPP + ERROR_BUF_OVF_TERM | Parameter access status from module: BUFFER OVERFLOW |
| EAPP + ERROR_PRM_ERR_TERM | Parameter access status from module: PARAMETER ERROR |

This function block gives write access to one addressed parameter of a module.

Interface variables This function block gives write access to one addressed parameter of a module. Caution: Function block interrupts process data exchange several times for several cycles!

## FbWriteParameterList (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Input | xExecute | BOOL | Triggers the execution of the action. | FbBehaviourModelWagoExecute |
| Output | xDone | BOOL | Successful completion of the action. | FbBehaviourModelWagoExecute |
| xBusy | BOOL | Action is still in progress. | FbBehaviourModelWagoExecute |
| xError | BOOL | Indicates an error. | FbBehaviourModelWagoExecute |
| eStatus | eResultCode | Result code status | FbBehaviourModelWagoExecute |
| Input | usiSlotNo | USINT (1..250) | slot number | FbParameterAccess |
| usiParameterNo | USINT (0..255) | parameter number | FbParameterAccess |
| Output | uiStatus | UINT | content of status register 57 | FbParameterAccess |
| Input | uiParameterCnt | UINT (1..256) | number of parameterss |  |
| Inout | aValue | typPARAMETER_ARRAY | content for addressed parameters |  |

| Result Codes |
| OK | Success |
| EAPP + ERROR_NO_KBUS_ACC | Library module has no KBUS access |
| EAPP + ERROR_INV_HANDLE | Parameter error invalid handle |
| EAPP + GEN_ERROR | Unspecified internal error occurred |
| EAPP + ERROR_SLOT_NO | Invalid slot number / module not present |
| EAPP + NO_REGISTER_COM | Module does not support register communication |
| EAPP + NO_PARAMETER_CHAN | Module does not support parameter channel |
| EAPP + ERROR_REG_PAR_NO | Invalid parameter number |
| EAPP + ERROR_REQ_COUNT | Number of requested words leads to invalid parameter number |
| EAPP + ERROR_VALUE_PTR | Parameter error invalid input pointer |
| EAPP + ERROR_STS_NOT_FIT | Status does not fit to request |
| EAPP + ERROR_TIMEOUT_TERM | Parameter access status from module: TIMEOUT |
| EAPP + ERROR_BUF_OVF_TERM | Parameter access status from module: BUFFER OVERFLOW |
| EAPP + ERROR_PRM_ERR_TERM | Parameter access status from module: PARAMETER ERROR |

This function block gives write access to addressed parameters of a module.

Interface variables This function block gives write access to addressed parameters of a module. Caution: Function block interrupts process data exchange several times for several cycles! Note: Input list will be copied from first index (zero) independent of requested start parameter.

## FbWriteRegister (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Input | xExecute | BOOL | Triggers the execution of the action. | FbBehaviourModelWagoExecute |
| Output | xDone | BOOL | Successful completion of the action. | FbBehaviourModelWagoExecute |
| xBusy | BOOL | Action is still in progress. | FbBehaviourModelWagoExecute |
| xError | BOOL | Indicates an error. | FbBehaviourModelWagoExecute |
| eStatus | eResultCode | Result code status | FbBehaviourModelWagoExecute |
| Input | usiSlotNo | USINT (1..250) | slot number | FbRegisterAccess |
| usiChannelNo | USINT (0..7) | channel number | FbRegisterAccess |
| usiRegisterNo | USINT (0..63) | register number | FbRegisterAccess |
| uiValue | UINT | content for addressed register |  |

| Result Codes |
| OK | Success |
| EAPP + GEN_ERROR | Unspecified internal error occurred |
| EAPP + ERROR_SLOT_NO | Invalid slot number / module not present |
| EAPP + NO_REGISTER_COM | Module does not support register communication |
| EAPP + ERROR_CHANNEL_NO | Invalid channel number |
| EAPP + ERROR_REG_PAR_NO | Invalid register number |

This function block gives write access to one addressed register of a module.

Interface variables This function block gives write access to one addressed register of a module. Caution: Function block interrupts process data exchange several times for several cycles! Caution: Modules do not return negative acknowledge! Write access to a read only register (e.g. SW version) will be accepted but not evaluated.

## FbWriteRegisterList (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Input | xExecute | BOOL | Triggers the execution of the action. | FbBehaviourModelWagoExecute |
| Output | xDone | BOOL | Successful completion of the action. | FbBehaviourModelWagoExecute |
| xBusy | BOOL | Action is still in progress. | FbBehaviourModelWagoExecute |
| xError | BOOL | Indicates an error. | FbBehaviourModelWagoExecute |
| eStatus | eResultCode | Result code status | FbBehaviourModelWagoExecute |
| Input | usiSlotNo | USINT (1..250) | slot number | FbRegisterAccess |
| usiChannelNo | USINT (0..7) | channel number | FbRegisterAccess |
| usiRegisterNo | USINT (0..63) | register number | FbRegisterAccess |
| usiRegisterCnt | USINT (1..64) | number of registers |  |
| Inout | aValue | typREGISTER_ARRAY | content for addressed registers |  |

| Result Codes |
| OK | Success |
| EAPP + GEN_ERROR | Unspecified internal error occurred |
| EAPP + ERROR_SLOT_NO | Invalid slot number / module not present |
| EAPP + NO_REGISTER_COM | Module does not support register communication |
| EAPP + ERROR_CHANNEL_NO | Invalid channel number |
| EAPP + ERROR_REG_PAR_NO | Invalid register number |
| EAPP + ERROR_REQ_COUNT | Number of requested words leads to invalid register number |

This function block gives write access to addressed registers of a module.

Interface variables This function block gives write access to addressed registers of a module. Caution: Function block interrupts process data exchange several times for several cycles! Caution: Modules do not return negative acknowledge! Write access to a read only register (e.g. SW version) will be accepted but not evaluated. Note: Input list will be copied from first index (zero) independent of requested start register.

### Functions


## FuReadLocalbusTiming (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuReadLocalbusTiming | WagoTypes.eResultCode |  |
| Input | xResetDurations | BOOL | true: reset and read durations; false: read durations |
| Output | diCurDuration | DINT | current duration in [us] |
| diMinDuration | DINT | minimum duration in [us] |
| diMaxDuration | DINT | maximum duration in [us] |
| diAvrDuration | DINT | average duration in [us] |

| Result Codes |
| OK | Success |
| EAPP + ERROR_NO_KBUS_ACC | Head station has no KBUS access |

Function reads all measured durations in KBUS localbus device driver.

Interface variables Function reads all measured durations in KBUS localbus device driver.

### Program Organization


## 20 Program Organization Units


- 10 Register FbReadRegister (FB) - FbReadRegisterList (FB) - FbWriteRegister (FB) - FbWriteRegisterList (FB) 20 Parameter - FbReadParameter (FB) - FbReadParameterList (FB) - FbWriteParameter (FB) - FbWriteParameterList (FB) 40 Data Types - ePARTICULAR_CODES (ENUM) - typPARAMETER_ARRAY (ALIAS) - typREGISTER_ARRAY (ALIAS) 50 Miscellaneous - FbReadModuleId (FB) - FbReadTiming (FB) - FuReadLocalbusTiming (FUN)

### Global Variable Lists


## ResultItems (GVL)


| Scope | Name | Type |
| --- | --- | --- |
| Constant | ERROR | ARRAY [0..23] OF typResultItem |

| Value | Level | Description |
| --- | --- | --- |
| STATUS_OK | eSeverity.none | ‘request/evaluation OK’ |
| GEN_ERROR | eSeverity.error | ‘unspecified INTERNAL error occurred’ |
| WRP_ENABLED | eSeverity.error | ‘write protection is enabled’ |
| ERROR_SLOT_NO | eSeverity.error | ‘invalid slot number / module not present’ |
| NO_REGISTER_COM | eSeverity.error | ‘module does not support register communication’ |
| NO_PARAMETER_CHAN | eSeverity.error | ‘module does not support parameter channel’ |
| ERROR_CHANNEL_NO | eSeverity.error | ‘invalid channel number’ |
| ERROR_REG_PAR_NO | eSeverity.error | ‘invalid register/parameter number’ |
| ERROR_REQ_COUNT | eSeverity.error | ‘number of requested words leads to invalid register/parameter number’ |
| ERROR_WRONG_STATE | eSeverity.error | ‘new request started during ongoing request’ |
| ERROR_TIMEOUT_PAR | eSeverity.error | ‘timeout during parameter access’ |
| ERROR_PAR_COM | eSeverity.error | ‘parameter communication error’ |
| ERROR_INV_HANDLE | eSeverity.error | ‘parameter error invalid handle’ |
| ERROR_VALUE_PTR | eSeverity.error | ‘parameter error invalid pointer’ |
| ERROR_CON_IN_USE | eSeverity.error | ‘evaluation error connection is in use’ |
| INFO_CON_ACTIVE | eSeverity.info | ‘evaluation information connection is active -> poll again’ |
| ERROR_NOT_INIT | eSeverity.error | ‘library module is not initialized’ |
| ERROR_NO_KBUS_ACC | eSeverity.error | ‘library module has no KBUS access’ |
| ERROR_NO_HANDLE_GEN | eSeverity.error | ‘library module has no handle generated’ |
| ERROR_CONT_NOT_FIT | eSeverity.error | ‘content does not fit to request’ |
| ERROR_STS_NOT_FIT | eSeverity.error | ‘status does not fit to request’ |
| ERROR_TIMEOUT_TERM | eSeverity.error | ‘parameter access status from module: TIMEOUT’ |
| ERROR_BUF_OVF_TERM | eSeverity.error | ‘parameter access status from module: BUFFER OVERFLOW’ |
| ERROR_PRM_ERR_TERM | eSeverity.error | ‘parameter access status from module: PARAMETER ERROR’ |

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 07.02.2024 | 1.7.1.2 | u010663 | replace cmperror by cmperror2 |
| 24.10.2023 | 1.7.1.1 | u0103719 | replace SysTypes Interfaces via SysTypes2 Interfaces |
| 25.01.2023 | 1.7.1.0 | u015479 | function ‘FuReadLocalbusTiming()’ review results added |
| 23.01.2023 | 1.7.0.0 | u015479 | function ‘FuReadLocalbusTiming()’ added |
| 22.11.2021 | 1.6.3.1 | u015479 | version 2.0.0.x discarded, version 1.6.3.0 reactivated and version number set to 1.6.3.1 |

WagoSysKbusAsyncCom.library

WagoSysKbusAsyncCom.library

### Other Components


## 10 Register


functionblocks for register access

functionblocks for register access - FbReadRegister (FB) - FbReadRegisterList (FB) - FbWriteRegister (FB) - FbWriteRegisterList (FB)

## 20 Parameter


functionblocks for parameter access

functionblocks for parameter access - FbReadParameter (FB) - FbReadParameterList (FB) - FbWriteParameter (FB) - FbWriteParameterList (FB)

## 40 Data Types


- ePARTICULAR_CODES (ENUM) - typPARAMETER_ARRAY (ALIAS) - typREGISTER_ARRAY (ALIAS)

## 50 Miscellaneous


- FbReadModuleId (FB) - FbReadTiming (FB) - FuReadLocalbusTiming (FUN)

## ePARTICULAR_CODES (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| STATUS_OK | WagoTypes.eResultCode.OK + 0 | 0 request/evaluation OK |
| GEN_ERROR | WagoTypes.eResultCode.EAPP + 1 | 201 unspecified INTERNAL error occurred |
| ERROR_SLOT_NO | WagoTypes.eResultCode.EAPP + 3 | 203 invalid slot number / module not present |
| NO_REGISTER_COM | WagoTypes.eResultCode.EAPP + 4 | 204 module does not support register communication |
| NO_PARAMETER_CHAN | WagoTypes.eResultCode.EAPP + 5 | 205 module does not support parameter channel |
| ERROR_CHANNEL_NO | WagoTypes.eResultCode.EAPP + 6 | 206 invalid channel number |
| ERROR_REG_PAR_NO | WagoTypes.eResultCode.EAPP + 7 | 207 invalid register/parameter number |
| ERROR_REQ_COUNT | WagoTypes.eResultCode.EAPP + 8 | 208 number of requested words leads to invalid register/parameter number |
| ERROR_TIMEOUT_TERM | WagoTypes.eResultCode.EAPP + 24 | 224 parameter access status from module: TIMEOUT |
| ERROR_BUF_OVF_TERM | WagoTypes.eResultCode.EAPP + 25 | 225 parameter access status from module: BUFFER OVERFLOW |
| ERROR_PRM_ERR_TERM | WagoTypes.eResultCode.EAPP + 26 | 226 parameter access status from module: PARAMETER ERROR |
| ERROR_INITIALIZATION | WagoTypes.eResultCode.EAPP + 99 | 299 function block initialization faild (e.g. instanced in a function) |

return values

## typPARAMETER_ARRAY (ALIAS) ¶


## typREGISTER_ARRAY (ALIAS) ¶
