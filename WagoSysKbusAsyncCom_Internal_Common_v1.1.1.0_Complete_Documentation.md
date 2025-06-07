# WagoSysKbusAsyncCom_Internal_Common v1.1.1.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysKbusAsyncCom_Internal_Common
- **Version:** 1.1.1.0
- **Categories:** WAGO Internal|Feature|LocalBus|K-Bus
- **Namespace:** WagoSysKbusAsyncCom_Internal_Common
- **Author:** u015479
- **Placeholder:** WagoSysKbusAsyncCom_Internal_Common

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

common data types [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. common data types [1]

### Contents: ¶


Contents: - Project Information - Library Information - Methods I_ConfigureCommon.Close (METH) - I_ConfigureCommon.Open (METH) - I_ConfigureParameter.PollRead (METH) - I_ConfigureParameter.PollReadList (METH) - I_ConfigureParameter.PollWrite (METH) - I_ConfigureParameter.PollWriteList (METH) - I_ConfigureParameter.StartRead (METH) - I_ConfigureParameter.StartReadList (METH) - I_ConfigureParameter.StartWrite (METH) - I_ConfigureParameter.StartWriteList (METH) - ... and 14 more Interfaces - I_ConfigureCommon (ITF) - I_ConfigureParameter (ITF) - I_ConfigureRegister (ITF) - I_ConfigureRegisterCommon (ITF) - I_GetModuleInformation (ITF) - I_GetTimingInformation (ITF) Program Organization Internal Components Global Variable Lists - GlobalConstantList (GVL) - VersionHistory (GVL) Other Components - 10 Interfaces - 40 Data Types - eKBAC_LIB_STATUS_CODES (ENUM)

### Indices and tables ¶


| [1] | Based on WagoSysKbusAsyncCom_Internal_Common.library, last modified 19.02.2022, 00:08:13. LibDoc 3.5.15.30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysKbusAsyncCom_Internal_Common.library |
| contentFile | WagoSysKbusAsyncCom_Internal_Common_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 19.02.2022, 00:08:16 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 19.02.2022, 00:08:13 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | u015479 |
| DefaultNamespace | WagoSysKbusAsyncCom_Internal_Common |
| Placeholder | WagoSysKbusAsyncCom_Internal_Common |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysKbusAsyncCom_Internal_Common |
| Version | version | 1.1.1.0 |
| Title | string | WagoSysKbusAsyncCom_Internal_Common |
| LibraryCategories | library-category-list | WAGO Internal\|Feature\|LocalBus\|K-Bus |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces.

### WagoSysVersion


#### Library Identification


Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion

#### Library Properties


| LinkAllContent: False HideWhenReferencedAsDependency: True | QualifiedOnly: False Key: WagoSysVersion, 1.0.0.0 (WAGO) | SystemLibrary: False Optional: False |

### Methods


## I_ConfigureCommon.Close (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Close | eKBAC_LIB_STATUS_CODES |

## I_ConfigureCommon.Open (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Open | eKBAC_LIB_STATUS_CODES |

## I_ConfigureParameter.PollRead (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollRead | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | parameter number in module |
| Output | uiValue | UINT | content of addressed parameter |
| uiStatus | UINT | content of status register 57 |

## I_ConfigureParameter.PollReadList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollReadList | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | first parameter to read |
| uiParameterCnt | UINT | number of parameters to read (1 .. 256) |
| Inout | aValue | ARRAY [0..255] OF UINT | content for addressed parameters |
| Output | uiStatus | UINT | content of status register 57 |

## I_ConfigureParameter.PollWrite (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollWrite | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | parameter number in module |
| uiValue | UINT | content for addressed parameter |
| Output | uiStatus | UINT | content of status register 57 |

## I_ConfigureParameter.PollWriteList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollWriteList | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | first parameter number to write |
| uiParameterCnt | UINT | number of parameters to write (1 .. 256) |
| Output | uiStatus | UINT | content of status register 57 |

## I_ConfigureParameter.StartRead (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartRead | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | parameter number in module |

## I_ConfigureParameter.StartReadList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartReadList | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | first parameter number to read |
| uiParameterCnt | UINT | number of parameters to read (1 .. 256) |

## I_ConfigureParameter.StartWrite (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartWrite | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module ‘ |
| usiParameterNo | USINT | parameter number in module |
| uiValue | UINT | content for addressed parameter |

## I_ConfigureParameter.StartWriteList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartWriteList | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiParameterNo | USINT | first parameter to write |
| uiParameterCnt | UINT | number of parameters to write (1 .. 256) |
| Inout | aValue | ARRAY [0..255] OF UINT | content for addressed parameters |

## I_ConfigureRegister.StartWrite (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartWrite | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | register number in module |
| uiValue | UINT | content for addressed register |

## I_ConfigureRegister.StartWriteList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartWriteList | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | first register to write |
| usiRegisterCnt | USINT | number of registers to write (1 .. 64) |
| Inout | aValue | ARRAY [0..63] OF UINT | content for addressed registers |

## I_ConfigureRegisterCommon.PollRead (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollRead | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | register number in module |
| Output | uiValue | UINT | content of addressed register |

## I_ConfigureRegisterCommon.PollReadList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollReadList | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | first register to read |
| usiRegisterCnt | USINT | number of registers to read (1 .. 64) |
| Inout | aValue | ARRAY [0..63] OF UINT | content for addressed registers |

## I_ConfigureRegisterCommon.PollWrite (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollWrite | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | register number in module |
| uiValue | UINT | content for addressed register |

## I_ConfigureRegisterCommon.PollWriteList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollWriteList | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | first register to write |
| usiRegisterCnt | USINT | number of registers to write (1 .. 64) |

## I_ConfigureRegisterCommon.StartRead (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartRead | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | register number in module |

## I_ConfigureRegisterCommon.StartReadList (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartReadList | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| usiChannelNo | USINT | channel number in module |
| usiRegisterNo | USINT | first register to read |
| usiRegisterCnt | USINT | number of registers to read (1 .. 64) |

## I_GetModuleInformation.PollRead_UID (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollRead_UID | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| Output | udiUID | UDINT | unified identification number |

## I_GetModuleInformation.StartRead_UID (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartRead_UID | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |

## I_GetTimingInformation.PollRead (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollRead | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |
| Output | diCurDuration | DINT | current duration in [us] |
| diMinDuration | DINT | minimum duration in [us] |
| diMaxDuration | DINT | maximum duration in [us] |
| diAvrDuration | DINT | average duration in [us] |

## I_GetTimingInformation.PollReset (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | PollReset | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |

## I_GetTimingInformation.StartRead (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartRead | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |

## I_GetTimingInformation.StartReset (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | StartReset | eKBAC_LIB_STATUS_CODES |  |
| Input | usiSlotNo | USINT | slot number of module |

### Interfaces


## I_ConfigureCommon (ITF)


- I_ConfigureCommon.Close (METH) - I_ConfigureCommon.Open (METH)

## I_ConfigureParameter (ITF)


- I_ConfigureParameter.PollRead (METH) - I_ConfigureParameter.PollReadList (METH) - I_ConfigureParameter.PollWrite (METH) - I_ConfigureParameter.PollWriteList (METH) - I_ConfigureParameter.StartRead (METH) - I_ConfigureParameter.StartReadList (METH) - I_ConfigureParameter.StartWrite (METH) - I_ConfigureParameter.StartWriteList (METH)

## I_ConfigureRegister (ITF)


- I_ConfigureRegister.StartWrite (METH) - I_ConfigureRegister.StartWriteList (METH)

## I_ConfigureRegisterCommon (ITF)


- I_ConfigureRegisterCommon.PollRead (METH) - I_ConfigureRegisterCommon.PollReadList (METH) - I_ConfigureRegisterCommon.PollWrite (METH) - I_ConfigureRegisterCommon.PollWriteList (METH) - I_ConfigureRegisterCommon.StartRead (METH) - I_ConfigureRegisterCommon.StartReadList (METH)

## I_GetModuleInformation (ITF)


- I_GetModuleInformation.PollRead_UID (METH) - I_GetModuleInformation.StartRead_UID (METH)

## I_GetTimingInformation (ITF)


- I_GetTimingInformation.PollRead (METH) - I_GetTimingInformation.PollReset (METH) - I_GetTimingInformation.StartRead (METH) - I_GetTimingInformation.StartReset (METH)

### Program Organization


## 20 Program Organization Units


- 10 Interfaces I_ConfigureCommon (ITF) I_ConfigureCommon.Close (METH) - I_ConfigureCommon.Open (METH) I_ConfigureParameter (ITF) - I_ConfigureParameter.PollRead (METH) - I_ConfigureParameter.PollReadList (METH) - I_ConfigureParameter.PollWrite (METH) - I_ConfigureParameter.PollWriteList (METH) - I_ConfigureParameter.StartRead (METH) - I_ConfigureParameter.StartReadList (METH) - I_ConfigureParameter.StartWrite (METH) - I_ConfigureParameter.StartWriteList (METH) I_ConfigureRegister (ITF) - I_ConfigureRegister.StartWrite (METH) - I_ConfigureRegister.StartWriteList (METH) I_ConfigureRegisterCommon (ITF) - I_ConfigureRegisterCommon.PollRead (METH) - I_ConfigureRegisterCommon.PollReadList (METH) - I_ConfigureRegisterCommon.PollWrite (METH) - I_ConfigureRegisterCommon.PollWriteList (METH) - I_ConfigureRegisterCommon.StartRead (METH) - I_ConfigureRegisterCommon.StartReadList (METH) I_GetModuleInformation (ITF) - I_GetModuleInformation.PollRead_UID (METH) - I_GetModuleInformation.StartRead_UID (METH) I_GetTimingInformation (ITF) - I_GetTimingInformation.PollRead (METH) - I_GetTimingInformation.PollReset (METH) - I_GetTimingInformation.StartRead (METH) - I_GetTimingInformation.StartReset (METH) 40 Data Types - eKBAC_LIB_STATUS_CODES (ENUM)

### Internal Components


## WagoSysKbusAsyncCom_Internal_Common Library Documentation


| Company: | WAGO |
| Title: | WagoSysKbusAsyncCom_Internal_Common |
| Version: | 1.1.1.0 |
| Categories: | WAGO Internal\|Feature\|LocalBus\|K-Bus |
| Namespace: | WagoSysKbusAsyncCom_Internal_Common |
| Author: | u015479 |
| Placeholder: | WagoSysKbusAsyncCom_Internal_Common |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

common data types [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. common data types [1]

### Contents:


- 20 Program Organization Units 10 Interfaces - 40 Data Types GlobalConstantList (GVL) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysKbusAsyncCom_Internal_Common.library, last modified 19.02.2022, 00:08:13. LibDoc 3.5.15.30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## GlobalConstantList (GVL) ¶


## VersionHistory (GVL)


| date | version | author | change |
| 23.11.2021 | 1.1.1.0 | u015479 | version 1.2.x.x discarded, version 1.1.0.1 reactivated and version number set to 1.1.1.0 |
| 12.08.2021 | 1.2.1.0 | u015479 | errors in comments corrected; global constant list ‘wskac_ic_GlobalConstantList’ renamed in ‘GlobalConstantList’ |
| 11.08.2021 | 1.2.0.0 | u015479 | version reduced to 1.2.0.0; global constant list ‘wskac_ic_GlobalConstantList’ added |
| 09.08.2021 | 2.0.0.0 | HLR | interfaces added to support KBUS gateway in advanced systems; new error code ‘LPKD_REQ_EVA_ERROR_MASTER_SLOT_NO’ added |
| 08.01.2019 | 1.1.0.1 | u015842 | Properties: copyright added |
| 05.06.2018 | 1.1.0.0 | HLR | interfaces added |
| 18.09.2015 | 1.0.0.2 | HLR | placeholder added |
| 18.09.2014 | 1.0.0.1 | HLR | Categories deleted |
| 01.09.2014 | 1.0.0.0 | HLR | First version |

WagoSysKbusAsyncCom_Internal_Common.library

WagoSysKbusAsyncCom_Internal_Common.library

### Other Components


## 10 Interfaces


- I_ConfigureCommon (ITF) I_ConfigureCommon.Close (METH) - I_ConfigureCommon.Open (METH) I_ConfigureParameter (ITF) - I_ConfigureParameter.PollRead (METH) - I_ConfigureParameter.PollReadList (METH) - I_ConfigureParameter.PollWrite (METH) - I_ConfigureParameter.PollWriteList (METH) - I_ConfigureParameter.StartRead (METH) - I_ConfigureParameter.StartReadList (METH) - I_ConfigureParameter.StartWrite (METH) - I_ConfigureParameter.StartWriteList (METH) I_ConfigureRegister (ITF) - I_ConfigureRegister.StartWrite (METH) - I_ConfigureRegister.StartWriteList (METH) I_ConfigureRegisterCommon (ITF) - I_ConfigureRegisterCommon.PollRead (METH) - I_ConfigureRegisterCommon.PollReadList (METH) - I_ConfigureRegisterCommon.PollWrite (METH) - I_ConfigureRegisterCommon.PollWriteList (METH) - I_ConfigureRegisterCommon.StartRead (METH) - I_ConfigureRegisterCommon.StartReadList (METH) I_GetModuleInformation (ITF) - I_GetModuleInformation.PollRead_UID (METH) - I_GetModuleInformation.StartRead_UID (METH) I_GetTimingInformation (ITF) - I_GetTimingInformation.PollRead (METH) - I_GetTimingInformation.PollReset (METH) - I_GetTimingInformation.StartRead (METH) - I_GetTimingInformation.StartReset (METH)

## 40 Data Types ¶


- eKBAC_LIB_STATUS_CODES (ENUM)

## eKBAC_LIB_STATUS_CODES (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| LPKD_REQ_EVA_STATUS_OK | 0 | request/evaluation OK |
| LPKD_REQ_EVA_GEN_ERROR | 1 | unspecified internal error occurred |
| LPKD_REQ_EVA_WRP_ENABLED | 2 | write protection is enabled |
| LPKD_REQ_EVA_ERROR_TERM_IDX | 3 | invalid module index / module not present |
| LPKD_REQ_EVA_NO_REGISTER_COM | 4 | module does not support register communication |
| LPKD_REQ_EVA_NO_PARAMETER_CHAN | 5 | module does not support parameter channel |
| LPKD_REQ_EVA_ERROR_TABLE_IDX | 6 | invalid table/channel index |
| LPKD_REQ_EVA_ERROR_REG_PAR_IDX | 7 | invalid register/parameter index |
| LPKD_REQ_EVA_ERROR_REQ_COUNT | 8 | number of requested words leads to invalid register/parameter index |
| LPKD_REQ_EVA_ERROR_WRONG_STATE | 9 | new request started during ongoing request |
| LPKD_REQ_EVA_ERROR_TIMEOUT_PAR | 10 | timeout during parameter access |
| LPKD_REQ_EVA_ERROR_PAR_COM | 11 | parameter communication error |
| LPKD_REQ_EVA_AA_NO_REG_RD_ACC | 12 | during application is active module does not support register read access |
| LPKD_REQ_EVA_AA_NO_REG_WR_ACC | 13 | during application is active module does not support register write access |
| LPKD_REQ_EVA_AA_NO_PAR_ACC | 14 | during application is active module does not support parameter access |
| LPKD_REQ_EVA_ERROR_INV_HANDLE | 15 | parameter error invalid handle |
| LPKD_REQ_EVA_ERROR_VALUE_PTR | 16 | parameter error invalid pointer |
| LPKD_REQ_EVA_ERROR_CON_IN_USE | 17 | evaluation error connection is in use |
| LPKD_REQ_EVA_INFO_CON_ACTIVE | 18 | evaluation information connection is active -> poll again |
| LPKD_REQ_EVA_ERROR_NOT_INIT | 19 | library module is not initialized |
| LPKD_REQ_EVA_ERROR_NO_KBUS_ACC | 20 | library module has no KBUS access |
| LPKD_REQ_EVA_ERROR_NO_HANDLE_GEN | 21 | library module has no handle generated |
| LPKD_REQ_EVA_ERROR_CONT_NOT_FIT | 22 | content does not fit to request |
| LPKD_REQ_EVA_ERROR_STS_NOT_FIT | 23 | status does not fit to request |
| LPKD_REQ_EVA_ERROR_TIMEOUT_TERM | 24 | parameter access status from module: TIMEOUT |
| LPKD_REQ_EVA_ERROR_BUF_OVF_TERM | 25 | parameter access status from module: BUFFER OVERFLOW |
| LPKD_REQ_EVA_ERROR_PRM_ERR_TERM | 26 | parameter access status from module: PARAMETER ERROR |
| NUMBER_OF_LPKD_REQ_EVA_VALUES |  | number of defined return values |

return values