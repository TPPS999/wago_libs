# WagoSysAtomic_Internal_32Bit v1.0.1.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysAtomic_Internal_32Bit
- **Version:** 1.0.1.1
- **Categories:** WAGO Internal|Target|PAC; WAGO Internal|Target|PFC; WAGO Internal|Target|Speedway
- **Namespace:** WagoSysAtomicInternal
- **Author:** WAGO / Jobst Wellensiek

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling Atomic Variable Access [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling Atomic Variable Access [1]

### Contents: ¶


Contents: - Project Information - Library Information - Functions FuGetVersionHistory (FUN) - Internal_Atomic_ADD_32 (FUN) - Internal_Atomic_ADD_ptr (FUN) - Internal_Atomic_AND_32 (FUN) - Internal_Atomic_CAS_32 (FUN) - Internal_Atomic_CAS_64 (FUN) - Internal_Atomic_CAS_ptr (FUN) - Internal_Atomic_OR_32 (FUN) - Internal_Atomic_READ_32 (FUN) - Internal_Atomic_READ_64 (FUN) - ... and 8 more Program Organization Internal Components Other Components - 01_DWORD - 02_LWORD - 03_PTR

### Indices and tables ¶


| [1] | Based on WagoSysAtomic_Internal_32Bit.library, last modified 14.01.2019, 17:01:18. The content of this file was automatically generated with None on 14.01.2019, 17:01:21 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysAtomic_Internal_32Bit.library |
| contentFile | WagoSysAtomic_Internal_32Bit_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 17:01:21 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 17:01:18 |
| Description | string | See: Description |
| DocFormat | reStructuredText |
| Author | WAGO / Jobst Wellensiek |
| DefaultNamespace | WagoSysAtomicInternal |
| Company | WAGO |
| Title | WagoSysAtomic_Internal_32Bit |
| Project | WagoSysAtomic_Internal_32Bit |
| NoPlaceholder |  |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Version | version | 1.0.1.1 |
| LibraryCategories | library-category-list | WAGO Internal\|Target\|PAC; WAGO Internal\|Target\|PFC; WAGO Internal\|Target\|Speedway |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. SysSem Library Identification : Placeholder: SysSem Default Resolution: SysSem, * (System) Namespace: SysSem Library Properties : SysShm Library Identification : Placeholder: SysShm Default Resolution: SysShm, * (System) Namespace: SysShm Library Properties : WagoSysTypedefs_Internal_32Bit Library Identification : Placeholder: WagoSysTypedefsInternal Default Resolution: WagoSysTypedefs_Internal_32Bit, * (WAGO) Namespace: WagoTypesInternal Library Properties :

### Functions


## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 08.01.2019 | 1.0.1.1 | u015842 | Properties: copyright added |
| 29.09.2015 | 1.0.1.0 | WAGO / u013972 | Add NoPlaceholder Property |
| 19.05.2015 | 1.0.0.0 | JW | Release Version |

library version

Release Note

Interface variables library version Release Note

## Internal_Atomic_ADD_32 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_ADD_32 | UDINT |  |
| Input | pVar | POINTER TO UDINT | variable with atomic access |
| diValue | DINT | adding value |

## Internal_Atomic_ADD_ptr (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_ADD_ptr | POINTER TO BYTE |  |
| Input | pVar | POINTER TO POINTER TO BYTE | variable with atomic access |
| diValue | DINT | adding value |

## Internal_Atomic_AND_32 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_AND_32 | DWORD |  |
| Input | pVar | POINTER TO DWORD | variable with atomic access |
| dwValue | DWORD | set value |

## Internal_Atomic_CAS_32 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_CAS_32 | BOOL |  |
| Input | pVar | POINTER TO UDINT | variable with atomic access |
| udiProbe | UDINT | probe value |
| udiValue | UDINT | set value |

## Internal_Atomic_CAS_64 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_CAS_64 | BOOL |  |
| Input | pVar | POINTER TO ULINT | variable with atomic access |
| uliProbe | ULINT | probe value |
| uliValue | ULINT | set value |

## Internal_Atomic_CAS_ptr (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_CAS_ptr | BOOL |  |
| Input | pVar | POINTER TO POINTER TO BYTE | variable with atomic access |
| pProbe | POINTER TO BYTE | probe value |
| pValue | POINTER TO BYTE | set value |

## Internal_Atomic_OR_32 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_OR_32 | DWORD |  |
| Input | pVar | POINTER TO DWORD | variable with atomic access |
| dwValue | DWORD | set value |

## Internal_Atomic_READ_32 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_READ_32 | UDINT |  |
| Input | pVar | POINTER TO UDINT | variable with atomic access |

## Internal_Atomic_READ_64 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_READ_64 | ULINT |  |
| Input | pVar | POINTER TO ULINT | variable with atomic access |

## Internal_Atomic_READ_ptr (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_READ_ptr | POINTER TO BYTE |  |
| Input | pVar | POINTER TO POINTER TO BYTE | variable with atomic access |

## Internal_Atomic_SWAP_32 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_SWAP_32 | UDINT |  |
| Input | pVar | POINTER TO UDINT | variable with atomic access |
| udiValue | UDINT | set calue |

## Internal_Atomic_SWAP_64 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_SWAP_64 | ULINT |  |
| Input | pVar | POINTER TO ULINT | variable with atomic access |
| uliValue | ULINT | set calue |

## Internal_Atomic_SWAP_ptr (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_SWAP_ptr | POINTER TO BYTE |  |
| Input | pVar | POINTER TO POINTER TO BYTE | variable with atomic access |
| pValue | POINTER TO BYTE | set calue |

## Internal_Atomic_TAR_32 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_TAR_32 | BOOL |  |
| Input | pVar | POINTER TO UDINT | variable with atomic access |
| udiBitNo | UDINT |  |

## Internal_Atomic_TAS_32 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_TAS_32 | BOOL |  |
| Input | pVar | POINTER TO UDINT | variable with atomic access |
| udiBitNo | UDINT |  |

## Internal_Atomic_TDEC_32 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_TDEC_32 | UDINT |  |
| Input | pVar | POINTER TO UDINT | variable with atomic access |

test and decrement

Interface variables test and decrement

## Internal_Atomic_XOR_32 (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Internal_Atomic_XOR_32 | DWORD |  |
| Input | pVar | POINTER TO DWORD | variable with atomic access |
| dwValue | DWORD | set value |

### Program Organization


## 20 Program Organization Units


- 01_DWORD Internal_Atomic_ADD_32 (FUN) - Internal_Atomic_AND_32 (FUN) - Internal_Atomic_CAS_32 (FUN) - Internal_Atomic_OR_32 (FUN) - Internal_Atomic_READ_32 (FUN) - Internal_Atomic_SWAP_32 (FUN) - Internal_Atomic_TAR_32 (FUN) - Internal_Atomic_TAS_32 (FUN) - Internal_Atomic_TDEC_32 (FUN) - Internal_Atomic_XOR_32 (FUN) 02_LWORD - Internal_Atomic_CAS_64 (FUN) - Internal_Atomic_READ_64 (FUN) - Internal_Atomic_SWAP_64 (FUN) 03_PTR - Internal_Atomic_ADD_ptr (FUN) - Internal_Atomic_CAS_ptr (FUN) - Internal_Atomic_READ_ptr (FUN) - Internal_Atomic_SWAP_ptr (FUN)

### Internal Components


## WagoSysAtomic_Internal_32Bit Library Documentation


| Company: | WAGO |
| Title: | WagoSysAtomic_Internal_32Bit |
| Version: | 1.0.1.1 |
| Categories: | WAGO Internal\|Target\|PAC; WAGO Internal\|Target\|PFC; WAGO Internal\|Target\|Speedway |
| Namespace: | WagoSysAtomicInternal |
| Author: | WAGO / Jobst Wellensiek |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling Atomic Variable Access [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling Atomic Variable Access [1]

### Contents:


- 20 Program Organization Units 01_DWORD - 02_LWORD - 03_PTR FuGetVersionHistory (FUN)

### Indices and tables


| [1] | Based on WagoSysAtomic_Internal_32Bit.library, last modified 14.01.2019, 17:01:18. The content of this file was automatically generated with None on 14.01.2019, 17:01:21 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Other Components


## 01_DWORD


- Internal_Atomic_ADD_32 (FUN) - Internal_Atomic_AND_32 (FUN) - Internal_Atomic_CAS_32 (FUN) - Internal_Atomic_OR_32 (FUN) - Internal_Atomic_READ_32 (FUN) - Internal_Atomic_SWAP_32 (FUN) - Internal_Atomic_TAR_32 (FUN) - Internal_Atomic_TAS_32 (FUN) - Internal_Atomic_TDEC_32 (FUN) - Internal_Atomic_XOR_32 (FUN)

## 02_LWORD


- Internal_Atomic_CAS_64 (FUN) - Internal_Atomic_READ_64 (FUN) - Internal_Atomic_SWAP_64 (FUN)

## 03_PTR


- Internal_Atomic_ADD_ptr (FUN) - Internal_Atomic_CAS_ptr (FUN) - Internal_Atomic_READ_ptr (FUN) - Internal_Atomic_SWAP_ptr (FUN)