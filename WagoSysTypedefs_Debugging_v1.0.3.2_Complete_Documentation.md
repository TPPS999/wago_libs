# WagoSysTypedefs_Debugging v1.0.3.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysTypedefs_Debugging
- **Version:** 1.0.3.2
- **Categories:** WAGO Internal|Common|Types and Interfaces
- **Author:** WAGO / u013972
- **Placeholder:** WagoSysTypedefs_Debugging

### Description ¶


This document is automatically generated.

Type definitions for debugging purpose

This document is automatically generated. Type definitions for debugging purpose

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Functions FuGetVersionHistory (FUN) - ResultCode_to_String (FUN) - _TransposeDebugResults (FUN) Internal Components Other Components

### Indices and tables ¶


Based on WagoSysTypedefs_Debugging.library, last modified 29.05.2024, 19:48:54. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysTypedefs_Debugging.library, last modified 29.05.2024, 19:48:54. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysTypedefs_Debugging Library Documentation


| Company: | WAGO |
| Title: | WagoSysTypedefs_Debugging |
| Version: | 1.0.3.2 |
| Categories: | WAGO Internal\|Common\|Types and Interfaces |
| Author: | WAGO / u013972 |
| Placeholder: | WagoSysTypedefs_Debugging |

### Description


This document is automatically generated.

Type definitions for debugging purpose

This document is automatically generated. Type definitions for debugging purpose

### Contents:


- 21 ResultCodes ResultCode_to_String (FUN) - _TransposeDebugResults (FUN) - eResultCode_Internal (ENUM) FuGetVersionHistory (FUN)

### Indices and tables


Based on WagoSysTypedefs_Debugging.library, last modified 29.05.2024, 19:48:54. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysTypedefs_Debugging.library, last modified 29.05.2024, 19:48:54. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysTypedefs_Debugging.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:48:54 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:48:54 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysTypedefs_Debugging |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysTypedefs_Debugging |
| DefaultNamespace |  |
| Version | version | 1.0.3.2 |
| Title | string | WagoSysTypedefs_Debugging |
| LibraryCategories | library-category-list | WAGO Internal\|Common\|Types and Interfaces |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False PublishSymbolsInContainer: True | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : Library Parameter : Parameter: MAX_STRING_LENGTH = 255 Parameter: MAX_WSTRING_LENGTH = 255

### Functions


## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 21.02.2024 | 1.0.3.2 | u010663 | Compiled SP16.3 |
| 24.10.2023 | 1.0.3.1 | u0103719 | replace SysTypes Interfaces via SysTypes2 Interfaces |
| 08.01.2019 | 1.0.3.0 | u015842 | Properties: free placeholder added |
| 28.10.2015 | 1.0.2.0 | WAGO / u013972 | Add WagoTypesCommon as Placeholder |
| 23.09.2015 | 1.0.1.0 | WAGO / u013972 | Warnings at 3.5.7.0 removed |
| 06.03.2015 | 1.0.0.0 | WAGO / u013972 | Release Version |

## ResultCode_to_String (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ResultCode_to_String | STRING |
| Input | eResultCode | eResultCode |

## _TransposeDebugResults (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | _TransposeDebugResults | eResultCode |
| Input | udiCodesysResult | SysTypes.RTS_IEC_RESULT |

transforms an RTS result code into a canonical result code

Purpose: debugging of library functions. In the regular case it is not specified, which codes are returned from library functions. So we have to find out empirically.

ATTN: This function for debugging only and it is not intended to be used in productive code!

Interface variables transforms an RTS result code into a canonical result code Purpose: debugging of library functions. In the regular case it is not specified, which codes are returned from library functions. So we have to find out empirically. ATTN: This function for debugging only and it is not intended to be used in productive code!

### Internal Components


## eResultCode_Internal (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| ECODESYS | 1000 | mapping for codesys-errors (if it is really necessary) |
| ECDSFAIL | 1001 | ERR_FAILED |
| ECDSPARA | 1002 | ERR_PARAMETER |
| ECDSTIMEOUT | 1005 | ERR_TIMEOUT |
| ECDSNOBUFFER | 1006 | ERR_NOBUFFER |
| ECDSNOENT | 1016 | ERR_NO_OBJECT |
| ECDSNOHANDLE | 1020 | ERR_INVALID_HANDLE |
| ECDSNOSYS | 1024 | ERR_NOT_SUPPORTED |
| ECDSSNOTINITED | 1513 | ERR_SOCK_NOTINITIALIZED 16#201 Socket errors (range: 0x0200 - 0x02FF) |
| ECDSSNOTSOCK | 1514 | ERR_SOCK_NOTSOCKET UDINT 16#202 The provided socket handle is invalid |
| ECDSSAFNOSUPPORT | 1515 | ERR_SOCK_AFUNSUPPORTED 16#203 The address family is NOT supported |
| ECDSSPROTONOSUPPORT | 1516 | ERR_SOCK_PROTOUNSUPPORTED 16#204 Protocol is NOT supported * / |
| ECDSSNOBUFS | 1517 | ERR_SOCK_NOBUFFER UDINT 16#205 NOT enough buffer TO handle the request * / |
| ECDSSWOULDBLOCK | 1518 | ERR_SOCK_WOULDBLOCK UDINT 16#206 Socket is in nonblocking mode but THIS call would block * / |
| ECDSSADDRINUSE | 1519 | ERR_SOCK_ADDRINUSE UDINT 16#207 The provided address is already in use * / |
| ECDSSADDRNOTAVAIL | 1520 | ERR_SOCK_ADDRNOTAVAILABLE 16#208 The provided address is NOT available on THIS computer * / |
| ECDSSCONNREFUSED | 1521 | ERR_SOCK_CONNREFUSED 16#209 Connection has been refused BY the remote host * / |
| ECDSSTIMEDOUT | 1522 | ERR_SOCK_TIMEDOUT 16#20A Operation timed out * / |
| ECDSSNOTFOUND | 1523 | ERR_SOCK_HOSTNOTFOUND 16#20B The host has NOT been found * / |
| ECDSSNETUNREACH | 1524 | ERR_SOCK_HOSTUNREACHABLE 16#20C Host is unreachable * / |
| ECDSSISCONN | 1525 | ERR_SOCK_ISCONNECTED 16#20D Socket is already connected * / |
| ECDSSNOTCONN | 1526 | ERR_SOCK_NOTCONNECTED 16#20E The socket is NOT connected * / |
| ECDSSSHUTDOWN | 1527 | ERR_SOCK_SHUTDOWN UDINT 16#20F Shutdown has been called on the socket * / |
| ECDSSMSGSIZE | 1528 | ERR_SOCK_MSGSIZE UDINT 16#210 FOR sockets OF TYPE DGRAM. The package TO send exceeds the maximum package size * / |
| ECDSSCLOSED | 1529 | ERR_SOCK_CLOSED UDINT 16#211 Socket has been gracefully closed. No more send/receives allowed * / |
| ECDSMAX | 2000 |  |

Operation status for debugging purposes

This list directly reflects the result codes from linux/posix-target firmware. The CDS codest is mapped to the range 1000..32767 for debugging purposes.

InOut: Operation status for debugging purposes This list directly reflects the result codes from linux/posix-target firmware. The CDS codest is mapped to the range 1000..32767 for debugging purposes.

### Other Components


## 21 ResultCodes


- ResultCode_to_String (FUN) - _TransposeDebugResults (FUN) - eResultCode_Internal (ENUM)