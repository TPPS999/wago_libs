# WagoTypesSNMP v1.5.4.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesSNMP
- **Version:** 1.5.4.1
- **Categories:** Application; WAGO LayerView|Types and Interfaces; WAGO Internal|Feature|Network|SNMP; WAGO FunctionalView|Connectivity|Network
- **Namespace:** WagoTypesSNMP
- **Author:** WAGO / u013972
- **Placeholder:** WagoTypesSNMP

### Description ¶


This document is automatically generated.

Types for SNMP

This document is automatically generated. Types for SNMP

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Functions - Other Components eSNMP_AuthenticationProtocol (ENUM) - eSNMP_PrivacyProtocol (ENUM) - eSNMP_SecurityLevel (ENUM) - eSNMP_TLV_DATATYPE (ENUM) - eSNMP_TRAP_TYPE (ENUM) - typSNMP_TLV (STRUCT)

### Indices and tables ¶


Based on WagoTypesSNMP.library, last modified 15.04.2024, 20:31:44. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesSNMP.library, last modified 15.04.2024, 20:31:44. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesSNMP Library Documentation


| Company: | WAGO |
| Title: | WagoTypesSNMP |
| Version: | 1.5.4.1 |
| Categories: | Application; WAGO LayerView\|Types and Interfaces; WAGO Internal\|Feature\|Network\|SNMP; WAGO FunctionalView\|Connectivity\|Network |
| Namespace: | WagoTypesSNMP |
| Author: | WAGO / u013972 |
| Placeholder: | WagoTypesSNMP |

### Description


This document is automatically generated.

Types for SNMP

This document is automatically generated. Types for SNMP

### Contents:


- FuGetVersionHistory (FUN) - eSNMP_AuthenticationProtocol (ENUM) - eSNMP_PrivacyProtocol (ENUM) - eSNMP_SecurityLevel (ENUM) - eSNMP_TLV_DATATYPE (ENUM) - eSNMP_TRAP_TYPE (ENUM) - typSNMP_TLV (STRUCT)

### Indices and tables


Based on WagoTypesSNMP.library, last modified 15.04.2024, 20:31:44. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesSNMP.library, last modified 15.04.2024, 20:31:44. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesSNMP.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:39:59 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 15.04.2024, 20:31:44 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesSNMP |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesSNMP |
| DefaultNamespace | WagoTypesSNMP |
| Version | version | 1.5.4.1 |
| Title | string | WagoTypesSNMP |
| Released | bool | True |
| LibraryCategories | library-category-list | Application; WAGO LayerView\|Types and Interfaces; WAGO Internal\|Feature\|Network\|SNMP; WAGO FunctionalView\|Connectivity\|Network |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces.

### Functions


## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 08.04.2024 | 1.5.4.1 | u013312 | calculate array size in dependency of 32/64 bit systems |
| 08.04.2024 | 1.5.4.0 | u013312 | support for 64Bit systems |
| 26.02.2024 | 1.5.3.1 | u0103719 | modified environment (SP16 Patch 3) |
| 25.07.2022 | 1.5.3.0 | u016903 | Add additional privacy and authentication types |
| 08.01.2019 | 1.5.2.0 | u015842 | Properties: free placeholder added |
| 09.09.2015 | 1.5.1.0 | WAGO / u013972 | Release Version |

WagoTypesSNMP

Interface variables WagoTypesSNMP

### Other Components


## eSNMP_AuthenticationProtocol (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| SNMP_AUTHP_NONE | 0 | No Authentication Hash Type |
| SNMP_AUTHP_MD5 | 1 | Use MD5 to create Authentication Hash |
| SNMP_AUTHP_SHA | 2 | Use SHA1 to create Authentication Hash |
| SNMP_AUTHP_SHA224 | 3 | Use SHA224 to create Authentication Hash |
| SNMP_AUTHP_SHA256 | 4 | Use SHA256 to create Authentication Hash |
| SNMP_AUTHP_SHA384 | 5 | Use SHA384 to create Authentication Hash |
| SNMP_AUTHP_SHA512 | 6 | Use SHA512 to create Authentication Hash |

## eSNMP_PrivacyProtocol (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| SNMP_PRIVP_NONE | 0 | No Privacy Protocol Type |
| SNMP_PRIVP_DES | 1 | Use DES encryption |
| SNMP_PRIVP_AES | 2 | Use AES encryption |
| SNMP_PRIVP_AES128 | 3 | Use AES128 encryption |
| SNMP_PRIVP_AES192 | 4 | Use AES192 encryption |
| SNMP_PRIVP_AES192C | 5 | Use AES192C encryption |
| SNMP_PRIVP_AES256 | 6 | Use AES256 encryption |
| SNMP_PRIVP_AES256C | 7 | Use AES256C encryption |

## eSNMP_SecurityLevel (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| SNMP_SECURITY_NoAuthNoPriv | 1 | do not use Authentication or Privacy |
| SNMP_SECURITY_AuthNoPriv | 2 | Authenticate but no privacy |
| SNMP_SECURITY_AuthPriv | 3 | Authenticate and privacy |

## eSNMP_TLV_DATATYPE (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| SNMP_TLV_INTEGER | 2 | DINT |
| SNMP_TLV_BITS | 3 | STRING |
| SNMP_TLV_STRING | 4 | STRING |
| SNMP_TLV_OBJECT_ID | 6 | STRING |
| SNMP_TLV_IP_ADDRESS | 64 | STRING |
| SNMP_TLV_COUNTER | 65 | UDINT |
| SNMP_TLV_GAUGE | 66 | UDINT |
| SNMP_TLV_TIMETICKS | 67 | UDINT |
| SNMP_TLV_UINTEGER | 71 | SNMP_TLV_COUNTER64 := 70, ULINT UNUSABLE UDINT |

## eSNMP_TRAP_TYPE (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| SNMPT_TRAP_COLDSTART | 0 | cold start |
| SNMPT_TRAP_WARMSTART | 1 | warm start |
| SNMPT_TRAP_LINKDOWN | 2 | link down |
| SNMPT_TRAP_LINKUP | 3 | link up |
| SNMPT_TRAP_AUTHFAILS | 4 | authentication failure |
| SNMPT_TRAP_EGPNEIGHBORLOSS | 5 | egp neighbor loss |
| SNMPT_TRAP_ENTERPRISESPECIFIC | 6 | enterprise specific |

## typSNMP_TLV (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| net_snmp_variable_list | ARRAY [0..((SIZEOF(__XWORD) * 137) + 39)] OF BYTE | this array reserves the memory for an instance of an net_snmpvariable_list element |