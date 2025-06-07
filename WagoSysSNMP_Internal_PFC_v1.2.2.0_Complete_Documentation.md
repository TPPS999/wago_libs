# WagoSysSNMP_Internal_PFC v1.2.2.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysSNMP_Internal_PFC
- **Version:** 1.2.2.0
- **Categories:** WAGO Internal|Target|PFC
- **Namespace:** WagoSysSNMPInternal
- **Author:** WAGO / u013972

### Description ¶


This document is automatically generated.

This library provide SNMP-Services

This document is automatically generated. This library provide SNMP-Services

### Contents: ¶


Contents: - Project Information - Library Information - Function Blocks SNMP_GET (FB) - SNMP_GET_V3 (FB) - SNMP_SEND_INFORM_TO_ADR (FB) - SNMP_SEND_INFORM_TO_ADR_V3 (FB) - SNMP_SET (FB) - SNMP_SET_V3 (FB) Functions - SNMP_DINT_TO_TLV (FUN) - SNMP_GET_CUSTOM_OID_VALUE (FUN) - SNMP_GET_ERROR_STRING (FUN) - SNMP_NULL_TO_TLV (FUN) - SNMP_REGISTER_CUSTOM_OID (FUN) - SNMP_SEND_ENT_TRAP (FUN) - SNMP_SEND_TRAP (FUN) - SNMP_SEND_TRAP_TO_ADR_V1 (FUN) - SNMP_SEND_TRAP_TO_ADR_V2C (FUN) - SNMP_SEND_TRAP_TO_ADR_V3 (FUN) - ... and 7 more Methods - SNMP_GET.FB_Exit (METH) - SNMP_GET.FB_Init (METH) - SNMP_GET_V3.FB_Exit (METH) - SNMP_GET_V3.FB_Init (METH) - SNMP_SEND_INFORM_TO_ADR.FB_Exit (METH) - SNMP_SEND_INFORM_TO_ADR.FB_Init (METH) - SNMP_SEND_INFORM_TO_ADR_V3.FB_Exit (METH) - SNMP_SEND_INFORM_TO_ADR_V3.FB_Init (METH) - SNMP_SET.FB_Exit (METH) - SNMP_SET.FB_Init (METH) - ... and 2 more Program Organization Internal Components Global Variable Lists Other Components - Agent - Manager - TLV - TLV_TO_X - Trap - X_TO_TLV

### Indices and tables ¶


Based on WagoSysSNMP_Internal_PFC.library, last modified 29.05.2024, 20:40:01. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysSNMP_Internal_PFC.library, last modified 29.05.2024, 20:40:01. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysSNMP_Internal_PFC.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:40:02 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:40:01 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| DefaultNamespace | WagoSysSNMPInternal |
| Released | bool | False |
| Company | string | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysSNMP_Internal_PFC |
| NoPlaceholder |  |
| Version | version | 1.2.2.0 |
| Title | string | WagoSysSNMP_Internal_PFC |
| LibraryCategories | library-category-list | WAGO Internal\|Target\|PFC |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesSNMP Library Identification : Placeholder: WagoTypesSNMP Default Resolution: WagoTypesSNMP, * (WAGO) Namespace: WagoTypesSNMP Library Properties :

### Function Blocks


## SNMP_GET (FB)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | xExecute | BOOL | Enable SNMP-request |
| sHost | STRING(127) | Hostname or IP-address in “dotted decimal format” |
| sOID | STRING(127) | SNMP unique object identifier(OID) of requested data, e.g. ‘1.3.6.1.2.1.1.6.0’ for “sysLocation” |
| sCommunity | STRING(63) | Community string typical: “public” |
| liTimeout_ms | LINT | Request timeout in milliseconds |
| liRetries | LINT | Number of retries until timeout is reported. Total timeout = uiTimeout_ms * (uiReties + 1) |
| Output | xDone | BOOL | Function block has done its work an outgoing data can be used |
| xBusy | BOOL | Function block is already Busy |
| xError | BOOL | Function block is in error state |
| diStatus | DINT | Return-Code |
| typData | typSNMP_TLV | Structured response data in Type-Length-Value(TLV) format |

Interface variables - SNMP_GET.FB_Exit (METH) - SNMP_GET.FB_Init (METH)

## SNMP_GET_V3 (FB)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | xExecute | BOOL | Enable SNMP-request |
| sHost | STRING(127) | Hostname or IP-address in “dotted decimal format” |
| sOID | STRING(127) | SNMP unique object identifier(OID) of requested data, e.g. ‘1.3.6.1.2.1.1.6.0’ for “sysLocation” |
| sUsername | STRING(127) | SNMP-Username. |
| typSecLevel | eSNMP_SecurityLevel | Definition of SNMP-security-level |
| typAuthProt | eSNMP_AuthenticationProtocol | Definition of SNMP-authentication-protocol to be used for user-password hash |
| sAuthPass | STRING(127) | Password for the given username |
| typPrivProt | eSNMP_PrivacyProtocol | Definition of SNMP-privacy-protocol to be used for session encryption |
| sPrivPass | STRING(127) | Passphrase for the given encryption type and username |
| liTimeout_ms | LINT | Request timeout in milliseconds |
| liRetries | LINT | Number of retries until timeout is reported. Total timeout = uiTimeout_ms * (uiReties + 1) |
| Output | xDone | BOOL | Function block has done its work an outgoing data can be used |
| xBusy | BOOL | Function block is already busy |
| xError | BOOL | Function block has an error |
| diStatus | DINT | Return-code |
| typData | typSNMP_TLV | Structured response data in Type-Length-Value (TLV) format |

Interface variables - SNMP_GET_V3.FB_Exit (METH) - SNMP_GET_V3.FB_Init (METH)

## SNMP_SEND_INFORM_TO_ADR (FB)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Input | xExecute | BOOL |  | Enable SNMP-request |
| sHost | STRING(127) |  | Hostname or IP-address in “dotted decimal format” |
| sEnterprise | STRING(127) | ‘1.3.6.1.4.1.13576.1’ | SNMP unique object identifier(OID) of trap sender e.g.: 1.3.6.1.4.1.13576.1 |
| sCommunity | STRING(63) |  | Community string typical: “public” |
| sOID | STRING(127) |  | SNMP unique object identifier(OID) used for sending a additional value withe the trap. sy ‘’for only sending the trap |
| typData | typSNMP_TLV |  | Send a specific variable with the trap. |
| Output | xDone | BOOL |  | Function block has done its work an outgoing data can be used |
| xBusy | BOOL |  | Function block is already Busy |
| xError | BOOL |  |  |
| diStatus | DINT |  | Return-code |

Interface variables - SNMP_SEND_INFORM_TO_ADR.FB_Exit (METH) - SNMP_SEND_INFORM_TO_ADR.FB_Init (METH)

## SNMP_SEND_INFORM_TO_ADR_V3 (FB)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Input | xExecute | BOOL |  | Enable SNMP-request |
| sHost | STRING(127) |  | Hostname or IP-address in “dotted decimal format” |
| sEnterprise | STRING(127) | ‘1.3.6.1.4.1.13576.1’ | SNMP unique object identifier(OID) of trap sender e.g. 1.3.6.1.4.1.13576.1 |
| sEngineID | STRING(127) | ‘’ |  |
| sUsername | STRING(127) |  | SNMP-Username. |
| typSecLevel | eSNMP_SecurityLevel |  | Definition of SNMP-security-level |
| typAuthProt | eSNMP_AuthenticationProtocol |  | Definition of SNMP-authentication-protocol to be used for user-password hash |
| sAuthPass | STRING(127) |  | Password for the given username |
| typPrivProt | eSNMP_PrivacyProtocol |  | Definition of SNMP-privacy-protocol to be used for session encryption |
| sPrivPass | STRING(127) |  | Passphrase for the given encryption type and username |
| sOID | STRING(127) |  | SNMP unique object identifier(OID) used for sending an additional value with the trap. Give an empty string ‘’ for only sending the trap |
| typData | typSNMP_TLV |  | Send a specific variable with the trap |
| Output | xDone | BOOL |  | Function block has done its work an outgoing data can be used |
| xBusy | BOOL |  | Function block is already Busy |
| xError | BOOL |  |  |
| diStatus | DINT |  | Return-code |

Interface variables - SNMP_SEND_INFORM_TO_ADR_V3.FB_Exit (METH) - SNMP_SEND_INFORM_TO_ADR_V3.FB_Init (METH)

## SNMP_SET (FB)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | xExecute | BOOL | Enable SNMP-request |
| sHost | STRING(127) | Hostname or IP-address in “dotted decimal format” |
| sOID | STRING(127) | SNMP unique object identifier(OID) of requested data, e.g. ‘1.3.6.1.2.1.1.6.0’ for “sysLocation” |
| sCommunity | STRING(63) | Community string typical: “public” |
| typData | typSNMP_TLV | Structured response data in Type-Length-Value(TLV) format |
| liTimeout_ms | LINT | Request timeout in milliseconds |
| liRetries | LINT | Number of retries until timeout is reported. Total timeout = uiTimeout_ms * (uiReties + 1) |
| Output | xDone | BOOL | Function block has done its work an outgoing data can be used |
| xBusy | BOOL | Function block is already busy |
| xError | BOOL | Function block is already busy |
| diStatus | DINT | Return-code |

Interface variables - SNMP_SET.FB_Exit (METH) - SNMP_SET.FB_Init (METH)

## SNMP_SET_V3 (FB)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | xExecute | BOOL | Enable SNMP-request |
| sHost | STRING(127) | Hostname or IP-address in “dotted decimal format” |
| sOID | STRING(127) | SNMP unique object identifier(OID) of requested data, e.g. ‘1.3.6.1.2.1.1.6.0’ for “sysLocation” |
| sUsername | STRING(127) | SNMP-username. |
| typSecLevel | eSNMP_SecurityLevel | Definition of SNMP-security-level |
| typAuthProt | eSNMP_AuthenticationProtocol | Definition of SNMP-authentication-protocol to be used for user-password hash |
| sAuthPass | STRING(127) | Password for the given username |
| typPrivProt | eSNMP_PrivacyProtocol | Definition of SNMP-privacy-protocol to be used for session encryption |
| sPrivPass | STRING(127) | Passphrase for the given encryption type and username |
| typData | typSNMP_TLV | Structured response data in Type-Length-Value(TLV) format |
| liTimeout_ms | LINT | Request timeout in milliseconds |
| liRetries | LINT | Number of retries until timeout is reported. Total timeout = uiTimeout_ms * (uiReties + 1) |
| Output | xDone | BOOL | Function block has done its work and outgoing data can be used |
| xBusy | BOOL | Function block is already busy |
| xError | BOOL | Function block had an error |
| diStatus | DINT | Return-code |

Interface variables - SNMP_SET_V3.FB_Exit (METH) - SNMP_SET_V3.FB_Init (METH)

### Functions


## SNMP_DINT_TO_TLV (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SNMP_DINT_TO_TLV | DINT |  |
| Input | diInput | DINT | Input-Value |
| typDatatype | eSNMP_TLV_DATATYPE | Choose the SNMP-Datatype |
| Inout | typData | typSNMP_TLV | Container for TLV |

## SNMP_GET_CUSTOM_OID_VALUE (FUN)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Return | SNMP_GET_CUSTOM_OID_VALUE | DINT |  |
| Input | sOID | STRING(128) | ‘’ |
| Inout | typData | typSNMP_TLV |  |

## SNMP_GET_ERROR_STRING (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SNMP_GET_ERROR_STRING | DINT |
| Input | diErrorCode | DINT |
| Output | sString | STRING |

## SNMP_NULL_TO_TLV (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SNMP_NULL_TO_TLV | DINT |  |
| Inout | typData | typSNMP_TLV | Container for TLV |

## SNMP_REGISTER_CUSTOM_OID (FUN)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Return | SNMP_REGISTER_CUSTOM_OID | DINT |  |
| Input | sOID | STRING(128) | ‘’ |
| typDefaultData | typSNMP_TLV |  |
| xReadOnly | BOOL | FALSE |

## SNMP_SEND_ENT_TRAP (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SNMP_SEND_ENT_TRAP | DINT |  |
| Input | wTrap | WORD | Enterprise trap number |

## SNMP_SEND_TRAP (FUN)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | SNMP_SEND_TRAP | DINT |  |  |
| Input | sEnterprise | STRING(127) | ‘1.3.6.1.4.1.13576.1’ | SNMP unique object identifier(OID) of trap sender e.g. 1.3.6.1.4.1.13576.1 |
| typTrapType | eSNMP_TRAP_TYPE |  | Choose trap-type |
| wSpecificType | WORD |  | define specific trap-type |
| sOID | STRING(127) |  | SNMP unique object identifier(OID) used for sending an additional value with the trap. Give an empty string ‘’ for only sending the trap |
| typData | typSNMP_TLV |  | Send a specific variable with the trap |

## SNMP_SEND_TRAP_TO_ADR_V1 (FUN)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | SNMP_SEND_TRAP_TO_ADR_V1 | DINT |  |  |
| Input | sHost | STRING(127) |  | Hostname or IP-address in “dotted decimal format” |
| sEnterprise | STRING(127) | ‘1.3.6.1.4.1.13576.1’ | SNMP unique object identifier(OID) of trap sender e.g. 1.3.6.1.4.1.13576.1 |
| sCommunity | STRING(63) |  | Community string typical: “public” |
| typTrapType | eSNMP_TRAP_TYPE |  | Choose trap-type |
| wSpecificType | WORD |  | define specific trap-type |
| sOID | STRING(127) |  | SNMP unique object identifier(OID) used for sending an additional value with the trap. Give an empty string ‘’ for only sending the trap |
| typData | typSNMP_TLV |  | Send a specific variable with the trap |

## SNMP_SEND_TRAP_TO_ADR_V2C (FUN)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | SNMP_SEND_TRAP_TO_ADR_V2C | DINT |  |  |
| Input | sHost | STRING(127) |  | Hostname or Ip-address in “dotted decimal format” |
| sEnterprise | STRING(127) | ‘1.3.6.1.4.1.13576.1’ | SNMP unique object identifier(OID) of trap sender e.g. 1.3.6.1.4.1.13576.1 |
| sCommunity | STRING(63) |  | Community string typical: “public” |
| sOID | STRING(127) |  | SNMP unique object identifier(OID) used for sending an additional value with the trap. Give an empty string ‘’ for only sending the trap |
| typData | typSNMP_TLV |  | Send a specific variable with the trap |

## SNMP_SEND_TRAP_TO_ADR_V3 (FUN)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | SNMP_SEND_TRAP_TO_ADR_V3 | DINT |  |  |
| Input | sHost | STRING(127) |  | Hostname or IP-address in “dotted decimal format” |
| sEnterprise | STRING(127) | ‘1.3.6.1.4.1.13576.1’ | SNMP unique object identifier(OID) of trap sender e.g. 1.3.6.1.4.1.13576.1 |
| sEngineID | STRING(127) | ‘’ |  |
| sUsername | STRING(127) |  | SNMP-Username. |
| typSecLevel | eSNMP_SecurityLevel |  | Definition of SNMP-security-level |
| typAuthProt | eSNMP_AuthenticationProtocol |  | Definition of SNMP-authentication-protocol to be used for user-password hash |
| sAuthPass | STRING(127) |  | Password for the given username |
| typPrivProt | eSNMP_PrivacyProtocol |  | Definition of SNMP-Privacy-Protocol to be used for session encryption |
| sPrivPass | STRING(127) |  | Passphrase for the given encryption type and username |
| sOID | STRING(127) |  | SNMP unique object identifier(OID) used for sending an additional value with the trap. Give an empty string ‘’ for only sending the trap |
| typData | typSNMP_TLV |  | Send a specific variable with the trap |

## SNMP_SET_CUSTOM_OID_VALUE (FUN)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Return | SNMP_SET_CUSTOM_OID_VALUE | DINT |  |
| Input | sOID | STRING(128) | ‘’ |
| typData | typSNMP_TLV |  |

## SNMP_STRING_TO_TLV (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SNMP_STRING_TO_TLV | DINT |  |
| Input | sInput | STRING(255) | Input-Value |
| typDatatype | eSNMP_TLV_DATATYPE | Choose the SNMP-Datatype |
| Inout | typData | typSNMP_TLV | Container for TLV |

## SNMP_TLV_GET_TYPE (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SNMP_TLV_GET_TYPE | eSNMP_TLV_DATATYPE |
| Input | typData | typSNMP_TLV |

## SNMP_TLV_TO_DINT (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SNMP_TLV_TO_DINT | DINT |  |
| Input | typData | typSNMP_TLV | Prefilled TLV-Container |
| Inout | diValue | DINT | container for Output value |

## SNMP_TLV_TO_STRING (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SNMP_TLV_TO_STRING | DINT |  |
| Input | typData | typSNMP_TLV | Prefilled TLV-Container |
| Inout | sValue | STRING(255) | container for Output value |

## SNMP_TLV_TO_UDINT (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SNMP_TLV_TO_UDINT | DINT |  |
| Input | typData | typSNMP_TLV | Prefilled TLV-Container |
| Inout | udiValue | UDINT | container for Output value |

## SNMP_UDINT_TO_TLV (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SNMP_UDINT_TO_TLV | DINT |  |
| Input | udiInput | UDINT | Input-Value |
| typDatatype | eSNMP_TLV_DATATYPE | Choose the SNMP-Datatype |
| Inout | typData | typSNMP_TLV | Container for TLV |

### Methods


## SNMP_GET.FB_Exit (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FB_Exit | BOOL |
| Input | bInCopyCode | BOOL |

## SNMP_GET.FB_Init (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FB_Init | BOOL |
| Input | bInitRetains | BOOL |
| bInCopyCode | BOOL |

## SNMP_GET_V3.FB_Exit (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FB_Exit | BOOL |
| Input | bInCopyCode | BOOL |

## SNMP_GET_V3.FB_Init (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FB_Init | BOOL |
| Input | bInitRetains | BOOL |
| bInCopyCode | BOOL |

## SNMP_SEND_INFORM_TO_ADR.FB_Exit (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FB_Exit | BOOL |
| Input | bInCopyCode | BOOL |

## SNMP_SEND_INFORM_TO_ADR.FB_Init (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FB_Init | BOOL |
| Input | bInitRetains | BOOL |
| bInCopyCode | BOOL |

## SNMP_SEND_INFORM_TO_ADR_V3.FB_Exit (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FB_Exit | BOOL |
| Input | bInCopyCode | BOOL |

## SNMP_SEND_INFORM_TO_ADR_V3.FB_Init (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FB_Init | BOOL |
| Input | bInitRetains | BOOL |
| bInCopyCode | BOOL |

## SNMP_SET.FB_Exit (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FB_Exit | BOOL |
| Input | bInCopyCode | BOOL |

## SNMP_SET.FB_Init (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FB_Init | BOOL |
| Input | bInitRetains | BOOL |
| bInCopyCode | BOOL |

## SNMP_SET_V3.FB_Exit (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FB_Exit | BOOL |
| Input | bInCopyCode | BOOL |

## SNMP_SET_V3.FB_Init (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FB_Init | BOOL |
| Input | bInitRetains | BOOL |
| bInCopyCode | BOOL |

### Program Organization


## 20 Program Organization Units


- Agent SNMP_GET_CUSTOM_OID_VALUE (FUN) - SNMP_REGISTER_CUSTOM_OID (FUN) - SNMP_SET_CUSTOM_OID_VALUE (FUN) Manager - SNMP_GET (FB) SNMP_GET.FB_Exit (METH) - SNMP_GET.FB_Init (METH) SNMP_GET_V3 (FB) - SNMP_GET_V3.FB_Exit (METH) - SNMP_GET_V3.FB_Init (METH) SNMP_SET (FB) - SNMP_SET.FB_Exit (METH) - SNMP_SET.FB_Init (METH) SNMP_SET_V3 (FB) - SNMP_SET_V3.FB_Exit (METH) - SNMP_SET_V3.FB_Init (METH) SNMP_GET_ERROR_STRING (FUN) TLV - SNMP_TLV_GET_TYPE (FUN) - TLV_TO_X SNMP_TLV_TO_DINT (FUN) - SNMP_TLV_TO_STRING (FUN) - SNMP_TLV_TO_UDINT (FUN) X_TO_TLV - SNMP_DINT_TO_TLV (FUN) - SNMP_NULL_TO_TLV (FUN) - SNMP_STRING_TO_TLV (FUN) - SNMP_UDINT_TO_TLV (FUN) Trap - SNMP_SEND_ENT_TRAP (FUN) - SNMP_SEND_INFORM_TO_ADR (FB) SNMP_SEND_INFORM_TO_ADR.FB_Exit (METH) - SNMP_SEND_INFORM_TO_ADR.FB_Init (METH) SNMP_SEND_INFORM_TO_ADR_V3 (FB) - SNMP_SEND_INFORM_TO_ADR_V3.FB_Exit (METH) - SNMP_SEND_INFORM_TO_ADR_V3.FB_Init (METH) SNMP_SEND_TRAP (FUN) SNMP_SEND_TRAP_TO_ADR_V1 (FUN) SNMP_SEND_TRAP_TO_ADR_V2C (FUN) SNMP_SEND_TRAP_TO_ADR_V3 (FUN)

### Internal Components


## WagoSysSNMP_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysSNMP_Internal_PFC |
| Version: | 1.2.2.0 |
| Categories: | WAGO Internal\|Target\|PFC |
| Namespace: | WagoSysSNMPInternal |
| Author: | WAGO / u013972 |

### Description


This document is automatically generated.

This library provide SNMP-Services

This document is automatically generated. This library provide SNMP-Services

### Contents:


- 20 Program Organization Units Agent - Manager - SNMP_GET_ERROR_STRING (FUN) - TLV - Trap VersionHistory (GVL)

### Indices and tables


Based on WagoSysSNMP_Internal_PFC.library, last modified 29.05.2024, 20:40:01. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysSNMP_Internal_PFC.library, last modified 29.05.2024, 20:40:01. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| Date | Version | Author | Change |
| 15.04.2024 | 1.2.2.0 | u013312 | calculate array size in dependency of 32/64 bit systems |
| 08.04.2024 | 1.2.1.0 | u013312 | support for 64Bit systems |
| 21.02.2024 | 1.2.0.1 | u010663 | Compiled SP16.3 |
| 04.08.2023 | 1.2.0.0 | u018342 | Fix internal variables for 64bit |
| 17.06.2019 | 1.1.0.0 | u014042 | Add timeout parameters |
| 08.01.2019 | 1.0.2.2 | u015842 | Properties: copyright added |
| 18.04.2018 | 1.0.2.1 | WAGO / u013972 | Resolve documentation error |
| 29.09.2015 | 1.0.2.0 | WAGO / u013972 | Release Version |

WagoSysSNMP_Internal_PFC

WagoSysSNMP_Internal_PFC

### Other Components


## Agent


- SNMP_GET_CUSTOM_OID_VALUE (FUN) - SNMP_REGISTER_CUSTOM_OID (FUN) - SNMP_SET_CUSTOM_OID_VALUE (FUN)

## Manager


- SNMP_GET (FB) SNMP_GET.FB_Exit (METH) - SNMP_GET.FB_Init (METH) SNMP_GET_V3 (FB) - SNMP_GET_V3.FB_Exit (METH) - SNMP_GET_V3.FB_Init (METH) SNMP_SET (FB) - SNMP_SET.FB_Exit (METH) - SNMP_SET.FB_Init (METH) SNMP_SET_V3 (FB) - SNMP_SET_V3.FB_Exit (METH) - SNMP_SET_V3.FB_Init (METH)

## TLV


- SNMP_TLV_GET_TYPE (FUN) - TLV_TO_X SNMP_TLV_TO_DINT (FUN) - SNMP_TLV_TO_STRING (FUN) - SNMP_TLV_TO_UDINT (FUN) X_TO_TLV - SNMP_DINT_TO_TLV (FUN) - SNMP_NULL_TO_TLV (FUN) - SNMP_STRING_TO_TLV (FUN) - SNMP_UDINT_TO_TLV (FUN)

## TLV_TO_X


- SNMP_TLV_TO_DINT (FUN) - SNMP_TLV_TO_STRING (FUN) - SNMP_TLV_TO_UDINT (FUN)

## Trap


- SNMP_SEND_ENT_TRAP (FUN) - SNMP_SEND_INFORM_TO_ADR (FB) SNMP_SEND_INFORM_TO_ADR.FB_Exit (METH) - SNMP_SEND_INFORM_TO_ADR.FB_Init (METH) SNMP_SEND_INFORM_TO_ADR_V3 (FB) - SNMP_SEND_INFORM_TO_ADR_V3.FB_Exit (METH) - SNMP_SEND_INFORM_TO_ADR_V3.FB_Init (METH) SNMP_SEND_TRAP (FUN) SNMP_SEND_TRAP_TO_ADR_V1 (FUN) SNMP_SEND_TRAP_TO_ADR_V2C (FUN) SNMP_SEND_TRAP_TO_ADR_V3 (FUN)

## X_TO_TLV


- SNMP_DINT_TO_TLV (FUN) - SNMP_NULL_TO_TLV (FUN) - SNMP_STRING_TO_TLV (FUN) - SNMP_UDINT_TO_TLV (FUN)