# WagoSysDps v1.5.2.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysDps
- **Version:** 1.5.2.0
- **Categories:** Application; WAGO FunctionalView|Connectivity|FieldBus; WAGO Internal|Feature|Fieldbus|PROFIBUS Slave; WAGO LayerView|Sys
- **Namespace:** WagoSysDps
- **Author:** WAGO / rs
- **Placeholder:** WagoSysDps

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Profibus functions for diagnostic, alarm and I&M communication. [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Profibus functions for diagnostic, alarm and I&M communication. [1]

### Contents: ¶


Contents: - Documentation Index 10_Documentation - WagoSysDps Library Documentation Project Information Library Information Function Blocks Functions - FuGetDevState (FUN) - FuGetImDs (FUN) - FuGetSysDiag (FUN) - FuSendDiag (FUN) - FuSetAlarm (FUN) - FuSetChanRelDiag (FUN) - FuSetIdRelDiag (FUN) - FuSetImDs (FUN) - FuSetModStatDiag (FUN) - FuSetStatusMsg (FUN) Program Organization Global Variable Lists

### Indices and tables ¶


| [1] | Based on WagoSysDps.library, last modified 14.01.2019, 17:15:46. The content of this file was automatically generated with None on 14.01.2019, 17:15:49 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## 10_Documentation ¶


- doc10_errorcodes (FB)

## WagoSysDps Library Documentation


| Company: | WAGO |
| Title: | WagoSysDps |
| Version: | 1.5.2.0 |
| Categories: | Application; WAGO FunctionalView\|Connectivity\|FieldBus; WAGO Internal\|Feature\|Fieldbus\|PROFIBUS Slave; WAGO LayerView\|Sys |
| Namespace: | WagoSysDps |
| Author: | WAGO / rs |
| Placeholder: | WagoSysDps |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Profibus functions for diagnostic, alarm and I&M communication. [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Profibus functions for diagnostic, alarm and I&M communication. [1]

### Contents:


- 10_Documentation doc10_errorcodes (FB) 20 Program Organization Units - FuGetDevState (FUN) - FuGetImDs (FUN) - FuGetSysDiag (FUN) - FuSendDiag (FUN) - FuSetAlarm (FUN) - FuSetChanRelDiag (FUN) - FuSetIdRelDiag (FUN) - FuSetImDs (FUN) - FuSetModStatDiag (FUN) - FuSetStatusMsg (FUN) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysDps.library, last modified 14.01.2019, 17:15:46. The content of this file was automatically generated with None on 14.01.2019, 17:15:49 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysDps.library |
| contentFile | WagoSysDps_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 17:15:49 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 17:15:46 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / rs |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysDps |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysDps |
| DefaultNamespace | WagoSysDps |
| Version | version | 1.5.2.0 |
| Title | string | WagoSysDps |
| Released | bool | False |
| LibraryCategories | library-category-list | Application; WAGO FunctionalView\|Connectivity\|FieldBus; WAGO Internal\|Feature\|Fieldbus\|PROFIBUS Slave; WAGO LayerView\|Sys |
| IsEndUserLibrary | bool | False |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysDps_Internal_PFC Library Identification : Placeholder: WagoSysDpsInternal Default Resolution: WagoSysDps_Internal_PFC, * (WAGO) Namespace: WagoSysDps_Internal_PFC Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties :

### Function Blocks


## doc10_errorcodes (FB)


| ERRORCODES |
| 0x0000000 | Function is performed without error. |
| 0xC000000 | An unknown error has occurred. |
| 0xC000003 | The functionalities of the function were called in the incorrect sequence. |
| 0xC000005 | The information requested is not available. |
| 0xC000006 | Parameters passed to the function are invalid. |
| 0xC000008 | The specified data length is invalid. |
| 0xC00000A | The access to the specified data is denied. This might occur if a function in this library is used without PROFIBUS operation |
| 0xC00000D | The specified I & M data set is not supported. |
| 0xC00000E | The requested resource is busy. |
| 0xC000011 | The parameters passed are invalid. |
| 0xC000012 | No free memory available. |
| 0xC000013 | The specified slot is invalid. |
| 0xC000014 | The specified channel is invalid. |
| 0xC000015 | The specified parameter “specifier” in the diagnostic object “status message” is invalid. |
| 0xC000016 | The specified parameter “Channel Type” in the diagnostic object “channel-related diagnosis” is invalid. |
| 0xC000017 | The specified parameter “Channel Size” in the diagnostic object “channel-related diagnosis” is invalid. |
| 0xC000018 | The specified parameter “Error Type” in the diagnostic object “channel-related diagnosis” is invalid. |
| 0xC000019 | The specified parameter “Alarm Type” in the diagnostic object “Alarm” is invalid. |
| 0xC00001A | The specified parameter “alarm specifier” in the diagnostic object “Alarm” is invalid. |
| 0xC00001B | The specified parameter “Module status” with the diagnostic object “module state” is invalid. |
| 0xC00001E | The diagnosis given object is in the wrong state. |
| 0xC000027 | The specified parameter “Status Type” in the diagnostic object “status message” is invalid. |

The following table lists the possible status values ​​that apply for each function in the library. All status values ​​not listed in this table indicate an internal system error.

The following table lists the possible status values ​​that apply for each function in the library. All status values ​​not listed in this table indicate an internal system error.

### Functions


## FuGetDevState (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuGetDevState | DWORD |  |
| Output | bDevState | BYTE | Current state of the PROFIBUS interface |

| PROFIBUS SLAVE STATES |
| 0 | The PROFIBUS interface is not initialized. |
| 1 | The PROFIBUS interface is waiting for configuration data from CODESYS. |
| 2 | The PROFIBUS-C0-channel is opened. |
| 3 | The PROFIBUS-C0-channel is open. |
| 4 | If the configuration is processed. |
| 5 | The PROFIBUS-C2 channel is opened. |
| 6 | The PROFIBUS-C0-channel is started. |
| 7 | The PROFIBUS interface waits for valid PROFIBUS parameter data. |
| 8 | The PROFIBUS interface waits for modified PROFIBUS parameter or configuration data. |
| 9 | The PROFIBUS interface waits for valid PROFIBUS configuration data. |
| 10 | The PROFIBUS interface performs a check of the target and actual configuration. |
| 11 | The PROFIBUS parameters are processed. |
| 12 | The PROFIBUS process data exchange is started. |
| 13 | The PROFIBUS process data exchange is monitored. |
| 14 | The PROFIBUS-C0-channel is stopped. |
| 15 | The processing of the active diagnostic objects (eg alarms) will be canceled. |
| 16 | The PROFIBUS-C0-channel is closed. |
| 17 | The PROFIBUS-C2 channel is closed. |
| 18 | The PROFIBUS interface is closed. |
| 19 | The PROFIBUS interface is in an error state. |

## FuGetImDs (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuGetImDs | DWORD |  |
| Input | usiDsId | USINT | Specifies the number of the I & M data set. Records 0-4 are supported |
| pData | POINTER TO BYTE | Returns the pointer to the memory area for the record data |

category: Identification and maintenance (I&M)

Using function “FuGetImDs” the data of the defined I & M data set is read and stored in the specified memory area.

Interface variables category: Identification and maintenance (I&M) Using function “FuGetImDs” the data of the defined I & M data set is read and stored in the specified memory area.

## FuGetSysDiag (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuGetSysDiag | DWORD |  |
| Output | bSlot | BYTE | Slot |
| bCode | BYTE | error code |
| bArg | BYTE | error argument |
| bExtArg | BYTE | Advanced error argument |

category: diagnosis

Using function “FuGetSysDiag” the current information of the WAGO system diagnostics can be retrieved.

Interface variables category: diagnosis Using function “FuGetSysDiag” the current information of the WAGO system diagnostics can be retrieved.

## FuSendDiag (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSendDiag | DWORD |  |
| Input | xReq | BOOL | Controls the transmission process: TRUE: Starts sending the station diagnosis. FALSE: Just call the state of the transmission process. |
| Output | xBusy | BOOL | Returns the state OF the transmission process back: TRUE: Transmission is in progress FALSE: Sending completed |
| xDone | BOOL | Returns the state OF the transmission process: TRUE: Sending completed FALSE: Transmission is in progress |
| xDiagOvfl | BOOL | Indicates an overflow of the diagnostic data: TRUE: There are more diagnostic data than can fit in the available diagnostic data area. FALSE: The diagnostic data can fit in the available diagnostic data area. |

category: diagnosis

Using function “FuSendDiag” a diagnostics telegram of the diagnostic management can be sent to the DP master

Interface variables category: diagnosis Using function “FuSendDiag” a diagnostics telegram of the diagnostic management can be sent to the DP master

## FuSetAlarm (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSetAlarm | DWORD |  |
| Input | xReq | BOOL | Controls the transmission process: TRUE: Starts sending the station diagnosis. FALSE: Just call the state of the transmission process. |
| xSetDiag | BOOL | Controls the diagnostic object processing: TRUE: Diagnostic object is created. At the output of “DIAG_ID” the identification number of the new diagnostic object is output FALSE: Diagnostic object is deleted. At the entrance “DIAG_ID” the identification number of the erased diagnostic object must be specified |
| usiSlot | USINT | Specifies the slot information to the diagnostic objec |
| bAlarmType | BYTE | Specifies the type of the alarm |
| bAlarmSpec | BYTE | “Specifier” of the alarm. |
| xAddAck | BOOL |  |
| pUsrData | POINTER TO BYTE | Pointer to the memory area of the user data |
| usiUsrDataLen | USINT | Specifies the length of the user data in number of bytes. Supports user data with a maximum length of 4 bytes |
| Inout | dwDiagId | DWORD | Identification of the diagnostic object. When you create a diagnostic object the identification number is returned. When you delete a diagnostic object the corresponding identification number must be passed |
| Output | xBusy | BOOL | Returns the state OF the transmission process back: TRUE: Transmission is in progress FALSE: Sending completed |
| xDone | BOOL | Returns the state OF the transmission process: TRUE: Sending completed FALSE: Transmission is in progress |

category: diagnosis

Using function module “FuSetAlarm” the PROFIBUS alarms are entered in the alarm log of the diagnostic management. The administration of the diagnostic object assumes the diagnostic management in the PROFIBUS interface.

Interface variables category: diagnosis Using function module “FuSetAlarm” the PROFIBUS alarms are entered in the alarm log of the diagnostic management. The administration of the diagnostic object assumes the diagnostic management in the PROFIBUS interface.

## FuSetChanRelDiag (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSetChanRelDiag | DWORD |  |
| Input | xReq | BOOL | Controls the transmission process: TRUE: Starts sending the station diagnosis. FALSE: Just call the state of the transmission process. |
| xSetDiag | BOOL | Controls the diagnostic object processing: TRUE: Diagnostic object is created. At the output of “DIAG_ID” the identification number of the new diagnostic object is output FALSE: Diagnostic object is deleted. At the entrance “DIAG_ID” the identification number of the erased diagnostic object must be specified |
| usiSlot | USINT | Specifies the slot information to the diagnostic objec |
| usiChan | USINT | Specifies the channel number in the diagnostic object |
| bChanType | BYTE | Specifies the channel type of the diagnostic object |
| bChanSize | BYTE | Indicates the channel size on the diagnostic object |
| bErrType | BYTE | Specifies the type of error in the diagnostic object |
| Inout | dwDiagId | DWORD | Identification OF the diagnostic object. When you create a diagnostic object, here the identification number is returned. When you delete a diagnostic object here the corresponding identification number must be passed. |
| Output | xBusy | BOOL | Returns the state OF the transmission process back: TRUE: Transmission is in progress FALSE: Sending completed |
| xDone | BOOL | Returns the state OF the transmission process: TRUE: Sending completed FALSE: Transmission is in progress |

category: diagnosis

Using the “FuSetChanRelDiag” a channel diagnostic object can be created or deleted for the specified slot and channel. The administration of the diagnostic object assumes the diagnostic management in the PROFIBUS interface.

Interface variables category: diagnosis Using the “FuSetChanRelDiag” a channel diagnostic object can be created or deleted for the specified slot and channel. The administration of the diagnostic object assumes the diagnostic management in the PROFIBUS interface.

## FuSetIdRelDiag (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSetIdRelDiag | DWORD |  |
| Input | usiSlot | USINT | Specifies the slot information to the diagnostic objec |
| xErrFlag | BOOL | Error status OF the slot: TRUE: Error is present FALSE: No fault present |

category: diagnosis

Using function “FuSetIdRelDiag” a diagnostics telegram of the diagnostic management can be sent to the DP master

Interface variables category: diagnosis Using function “FuSetIdRelDiag” a diagnostics telegram of the diagnostic management can be sent to the DP master

## FuSetImDs (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSetImDs | DWORD |  |
| Input | usiDsId | USINT | Specifies the number OF the I & M data set. Records 0-4 are supported |
| pData | POINTER TO BYTE | Returns the pointer to the memory area for the record data |

category: Identification and maintenance (I&M)

Using function “FuSetImDs” the data of the defined I & M data set are written.

Interface variables category: Identification and maintenance (I&M) Using function “FuSetImDs” the data of the defined I & M data set are written.

## FuSetModStatDiag (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSetModStatDiag | DWORD |  |
| Input | usiSlot | USINT | Specifies the slot information to the diagnostic objec |
| bModStat | BYTE | Error status of the slot: 0x00 data valid 0x01 data invalid 0x10 incorrect Feldbusvariable 0x11 no Feldbusvariable |

category: diagnosis

Using “FuSetModStatDiag” a diagnosis in the Module Status diagnostic object can be controlled for the defined slot . The administration of the diagnostic object assumes the diagnostic management in the PROFIBUS interface.

Interface variables category: diagnosis Using “FuSetModStatDiag” a diagnosis in the Module Status diagnostic object can be controlled for the defined slot . The administration of the diagnostic object assumes the diagnostic management in the PROFIBUS interface.

## FuSetStatusMsg (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSetStatusMsg | DWORD |  |
| Input | xReq | BOOL | Controls the transmission process: TRUE: Starts sending the station diagnosis. FALSE: Just call the state of the transmission process. |
| xSetDiag | BOOL | Controls the diagnostic object processing: TRUE: Diagnostic object is created. At the output of “DIAG_ID” the identification number of the new diagnostic object is output. FALSE: Diagnostic object is deleted. At the entrance “DIAG_ID” the identification number of the erased diagnostic object must be specified |
| usiSlot | USINT | Specifies the slot information to the diagnostic objec |
| bStatusType | BYTE | Indicates the type of status message |
| bStatusSpec | BYTE | Specifies the “specifier” of the status message. |
| pUsrData | POINTER TO BYTE | Pointer to the memory area of the user data. |
| usiUsrDataLen | USINT | Specifies the length OF the user data in number OF bytes TO. User data with a maximum length of 4 bytes are supported. |
| Inout | dwDiagId | DWORD | Identification of the diagnostic object. When you create a diagnostic object the identification number is returned. When you delete a diagnostic object the corresponding identification number must be passed |
| Output | xBusy | BOOL | Returns the state OF the transmission process back: TRUE: Transmission is in progress FALSE: Sending completed |
| xDone | BOOL | Returns the state OF the transmission process: TRUE: Sending completed FALSE: Transmission is in progress |

category: diagnosis

Using “FuSetStatusMsg” user status messages are generated or deleted. The administration of the diagnostic object assumes the diagnostic management in the PROFIBUS interface.

Interface variables category: diagnosis Using “FuSetStatusMsg” user status messages are generated or deleted. The administration of the diagnostic object assumes the diagnostic management in the PROFIBUS interface.

### Program Organization


## 20 Program Organization Units


- FuGetDevState (FUN) - FuGetImDs (FUN) - FuGetSysDiag (FUN) - FuSendDiag (FUN) - FuSetAlarm (FUN) - FuSetChanRelDiag (FUN) - FuSetIdRelDiag (FUN) - FuSetImDs (FUN) - FuSetModStatDiag (FUN) - FuSetStatusMsg (FUN)

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

Release Note

This library provides diagnostic function access to the profibus slave.

The library also offers I&M data exchange

WagoSysDps Release Note This library provides diagnostic function access to the profibus slave. The library also offers I&M data exchange