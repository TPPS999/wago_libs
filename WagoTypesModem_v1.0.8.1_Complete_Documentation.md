# WagoTypesModem v1.0.8.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesModem
- **Version:** 1.0.8.1
- **Categories:** Application; WAGO Internal|Common|Types and Interfaces; WAGO LayerView|Types and Interfaces
- **Author:** WAGO / u013972
- **Placeholder:** WagoTypesModem

### Description ¶


This document is automatically generated.

This is an library that include types for the functions of the modem

The function blocks of this library are thread safe and can be called simultaneously from different CODESYS tasks.

This document is automatically generated. This is an library that include types for the functions of the modem The function blocks of this library are thread safe and can be called simultaneously from different CODESYS tasks.

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Methods typNetworkRegistrationSettings (STRUCT) - typWdsSettings (STRUCT) Global Variable Lists Other Components - 29 Types - 80 Status - eModemState (ENUM) - eNetworkOperatorState (ENUM) - eNetworkRegistrationMode (ENUM) - eNetworkState (ENUM) - eNetworkTechnology (ENUM) - eResult (ENUM) - eSimLockType (ENUM) - eSimState (ENUM) - ... and 10 more

### Indices and tables ¶


Based on WagoTypesModem.library, last modified 29.05.2024, 20:50:06. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesModem.library, last modified 29.05.2024, 20:50:06. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesModem Library Documentation


| Company: | WAGO |
| Title: | WagoTypesModem |
| Version: | 1.0.8.1 |
| Categories: | Application; WAGO Internal\|Common\|Types and Interfaces; WAGO LayerView\|Types and Interfaces |
| Author: | WAGO / u013972 |
| Placeholder: | WagoTypesModem |

### Description


This document is automatically generated.

This is an library that include types for the functions of the modem

The function blocks of this library are thread safe and can be called simultaneously from different CODESYS tasks.

This document is automatically generated. This is an library that include types for the functions of the modem The function blocks of this library are thread safe and can be called simultaneously from different CODESYS tasks.

### Contents:


- 29 Types eModemState (ENUM) - eNetworkOperatorState (ENUM) - eNetworkRegistrationMode (ENUM) - eNetworkState (ENUM) - eNetworkTechnology (ENUM) - eSimLockType (ENUM) - eSimState (ENUM) - eWdsAuthType (ENUM) - eWdsState (ENUM) - typModemDeviceInfo (STRUCT) - typNetworkAccessInfo (STRUCT) - typNetworkRegistrationSettings (STRUCT) - typNetworkScanInfo (STRUCT) - typSimInfo (STRUCT) - typSmsMetaData (STRUCT) - typSmsMsgPDU (STRUCT) - typSmsMsgText (STRUCT) - typWdsInfo (STRUCT) - typWdsSettings (STRUCT) 80 Status - eResult (ENUM) VersionHistory (GVL)

### Indices and tables


Based on WagoTypesModem.library, last modified 29.05.2024, 20:50:06. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesModem.library, last modified 29.05.2024, 20:50:06. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesModem.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:50:06 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:50:06 |
| Description | string | See: Description |
| Copyright | © WAGO GmbH & Co. KG, Germany 2020 – All rights reserved. |
| Author | WAGO / u013972 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesModem |
| Company | WAGO |
| DocFormat | reStructuredText |
| SourceLibrary | bool | False |
| Project | string | WagoTypesModem |
| DefaultNamespace |  |
| Version | version | 1.0.8.1 |
| ThreadSafe | string | True |
| Title | WagoTypesModem |
| Released | bool | False |
| LibraryCategories | library-category-list | Application; WAGO Internal\|Common\|Types and Interfaces; WAGO LayerView\|Types and Interfaces |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |
| IsEndUserLibrary | bool | False |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties :

### Methods


## typNetworkRegistrationSettings (STRUCT)


| Name | Type |
| --- | --- |
| eMode | eNetworkRegistrationMode |
| sOperatorIdentifier | STRING |
| xFallbackToAuto | BOOL |
| eAccessTechnology | eNetworkTechnology |

## typWdsSettings (STRUCT)


| Name | Type |
| --- | --- |
| sApn | STRING(30) |
| sUser | STRING(30) |
| sPassword | STRING(30) |
| eAuthType | eWdsAuthType |

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| Date | Version | Author | Change |
| 19.05.2021 | 1.0.8.1 | WAGO / u0103719 | modified environment (SP16 Patch 3) |
| 19.05.2021 | 1.0.8.0 | WAGO / u0103719 | WAT35633: Add typSmsMsgText for SMS Text Mode |
| 18.01.2021 | 1.0.7.1 | WAGO / u0100179 | Add EMODEMBUSY to enum eResult |
| 14.01.2021 | 1.0.7.0 | WAGO / u013972 | Add sOperatorShort, sOperatorId, sCellId and sLocalAreaCode |
| 08.01.2021 | 1.0.6.1 | WAGO / u0100179 | Bugfix: add attribute to_string to eNetworkOperatorState and eNetworkRegistrationMode |
| 07.01.2021 | 1.0.6.0 | WAGO / u0100179 | Add types for network scan |
| 18.12.2020 | 1.0.5.0 | WAGO / u013972 | Add eNetworkTechnology to typNetworkRegistrationSettings |
| 02.12.2020 | 1.0.4.0 | WAGO / u013972 | Add types for network registration settings |
| 30.10.2020 | 1.0.3.0 | WAGO / u013972 | Add types for sms handling |
| 20.08.2020 | 1.0.1.1 | WAGO / u013972 | Add {attribute ‘to_string’} to eResult |
| 18.08.2020 | 1.0.1.0 | WAGO / u013972 | Add eResult |
| 29.07.2020 | 1.0.0.1 | WAGO / u013972 | Release Version |

WagoTypesModem

### Other Components


## 29 Types


- eModemState (ENUM) - eNetworkOperatorState (ENUM) - eNetworkRegistrationMode (ENUM) - eNetworkState (ENUM) - eNetworkTechnology (ENUM) - eSimLockType (ENUM) - eSimState (ENUM) - eWdsAuthType (ENUM) - eWdsState (ENUM) - typModemDeviceInfo (STRUCT) - typNetworkAccessInfo (STRUCT) - typNetworkRegistrationSettings (STRUCT) - typNetworkScanInfo (STRUCT) - typSimInfo (STRUCT) - typSmsMetaData (STRUCT) - typSmsMsgPDU (STRUCT) - typSmsMsgText (STRUCT) - typWdsInfo (STRUCT) - typWdsSettings (STRUCT)

## 80 Status ¶


## eModemState (ENUM)


| Name | Initial |
| --- | --- |
| UNKNOWN | 0 |
| NOT_READY |  |
| DETECTION_FAILED |  |
| READY |  |

Attributes: qualified_only InOut:

## eNetworkOperatorState (ENUM)


| Name | Initial |
| --- | --- |
| AVAILABLE | 0 |
| CURRENT |  |
| FORBIDDEN |  |
| UNKNOWN |  |

Attributes: qualified_only InOut:

## eNetworkRegistrationMode (ENUM)


| Name | Initial |
| --- | --- |
| Auto | 0 |
| Manual |  |

Attributes: qualified_only InOut:

## eNetworkState (ENUM)


| Name | Initial |
| --- | --- |
| NOT_REGISTERED | 0 |
| REGISTERED_HOME | 1 |
| SEARCHING | 2 |
| REGISTRATION_DENIED | 3 |
| UNKNOWN | 4 |
| REGISTERED_ROAMING | 5 |
| REGISTERED_SMS_ONLY_HOME | 6 |
| REGISTERED_SMS_ONLY_ROAMING | 7 |
| EMERGENCY_SERVICE | 8 |

Attributes: qualified_only InOut:

## eNetworkTechnology (ENUM)


| Name | Initial |
| --- | --- |
| GSM | 0 |
| GSM_Compact | 1 |
| UMTS | 2 |
| GSM_EGPRS | 3 |
| HSDPA | 4 |
| HSUPA | 5 |
| HSDPA_HSUPA | 6 |
| LTE | 7 |
| LTE_ADVANCED |  |
| UNKNOWN | 99 |
| AUTO | 100 |

Attributes: qualified_only InOut:

## eResult (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| OK | 0 | Success |
| EINVAL | 22 | Invalid argument |
| EUNSPECIFIC | 135 | Unspecific error, see sResultText for more details |
| EDEVICE | 201 | The device is not supported |
| ESTATE | 202 | The operation is in the current state not possible |
| EPINPUK | 203 | The pin/puk is not correct |
| EMODEMBUSY | 204 | The modem is currently busy |

Attributes: qualified_only InOut:

## eSimLockType (ENUM)


| Name | Initial |
| --- | --- |
| UNKNOWN | 0 |
| UNLOCKED |  |
| PIN |  |
| PIN2 |  |
| PUK |  |
| PUK2 |  |

Attributes: qualified_only InOut:

## eSimState (ENUM)


| Name | Initial |
| --- | --- |
| NOT_INITIALIZED | 0 |
| PIN_READY |  |
| SMS_READY |  |
| PB_READY |  |
| READY |  |
| NOT_PRESENT |  |
| LOCKED |  |
| ERROR |  |
| UNKNOWN |  |

Attributes: qualified_only InOut:

## eWdsAuthType (ENUM)


| Name | Initial |
| --- | --- |
| NONE | 0 |
| PAP | 1 |
| CHAP | 2 |
| PAP_OR_CHAP | 3 |
| UNKNOWN |  |

Attributes: qualified_only InOut:

## eWdsState (ENUM)


| Name |
| --- |
| CONNECTING |
| CONNECTED |
| DISCONNECTING |
| DISCONNECTED |
| ERROR |
| UNKNOWN |

Attributes: qualified_only InOut:

## typModemDeviceInfo (STRUCT)


| Name | Type |
| --- | --- |
| eState | eModemState |
| sManufacturer | STRING(50) |
| sModel | STRING(50) |
| sVersion | STRING(50) |
| sImei | STRING(16) |

## typNetworkAccessInfo (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| eState | eNetworkState |  |
| sOperator | STRING |  |
| sOperatorShort | STRING | network operator name (short format) |
| sOperatorId | STRING(10) | network operator name (MCC+MNC) |
| eTechnology | eNetworkTechnology |  |
| usiSignalStrength | USINT | in percent |
| iSignalRssi | INT |  |
| sLocalAreaCode | STRING(10) |  |
| sCellId | STRING(10) |  |

## typNetworkScanInfo (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| eState | eNetworkOperatorState |  |
| sOperLong | STRING | network operator name (long format) |
| sOperShort | STRING | network operator name (short format) |
| sOperId | STRING | network operator name (MCC+MNC) |
| eTechnology | eNetworkTechnology |  |

## typSimInfo (STRUCT)


| Name | Type |
| --- | --- |
| eState | eSimState |
| eLockType | eSimLockType |
| iRemainingAttempts | INT |
| sICCID | STRING(20) |

## typSmsMetaData (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| uiIndex | UINT | Index in storage location |
| tTimeStamp | DT | Timestamp of the sms |
| sSenderNumber | STRING(24) |  |

## typSmsMsgPDU (STRUCT)


| Name | Type |
| --- | --- |
| aData | ARRAY [0..256] OF BYTE |
| uiDataLength | UINT |

## typSmsMsgText (STRUCT)


| Name | Type |
| --- | --- |
| sReceiverNumber | STRING(24) |
| sSMSCNumber | STRING(23) |
| sText | STRING(160) |

## typWdsInfo (STRUCT)


| Name | Type |
| --- | --- |
| eState | eWdsState |
| sIp | STRING(45) |