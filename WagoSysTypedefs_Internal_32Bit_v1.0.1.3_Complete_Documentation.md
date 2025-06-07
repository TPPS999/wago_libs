# WagoSysTypedefs_Internal_32Bit v1.0.1.3 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysTypedefs_Internal_32Bit
- **Version:** 1.0.1.3
- **Categories:** WAGO Internal|Target|PAC; WAGO Internal|Target|PFC; WAGO Internal|Target|SoftPLC-V3 32Bit; WAGO Internal|Target|Speedway
- **Namespace:** WagoTypesInternal
- **Author:** WAGO / u013972
- **Placeholder:** WagoSysTypedefsInternal

### Description ¶


This document is automatically generated.

Type Definitions specific for 32-Bit-Machines

This document is automatically generated. Type Definitions specific for 32-Bit-Machines

### Contents: ¶


Contents: - Project Information - Library Information - Functions Dint_to_Pointer (FUN) - FuGetVersionHistory (FUN) - Pointer_To_Udint (FUN) - Udint_to_Pointer (FUN) Internal Components Other Components - 21 mem - auxiliary - ptr (ENUM)

### Indices and tables ¶


Based on WagoSysTypedefs_Internal_32Bit.library, last modified 29.05.2024, 19:48:30. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysTypedefs_Internal_32Bit.library, last modified 29.05.2024, 19:48:30. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysTypedefs_Internal_32Bit.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:48:30 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:48:30 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| DefaultNamespace | WagoTypesInternal |
| Placeholder | WagoSysTypedefsInternal |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysTypedefs_Internal_32Bit |
| Version | version | 1.0.1.3 |
| Title | string | WagoSysTypedefs_Internal_32Bit |
| LibraryCategories | library-category-list | WAGO Internal\|Target\|PAC; WAGO Internal\|Target\|PFC; WAGO Internal\|Target\|SoftPLC-V3 32Bit; WAGO Internal\|Target\|Speedway |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces.

### Functions


## Dint_to_Pointer (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Dint_to_Pointer | POINTER TO BYTE |  |
| Input | di | DINT | the pointer which is to be typecasted |

converts a POINTER into an unsigned double integer without throwing warnings.

Note: When this function is needed, it mostly indicates a principal design flaw of the POUs which require its usage. Nevertheless, in some situations we encounter some functions in external libraries, where things are completely messed up, e.g. in SysFile, where a file handle is once declared as Pointer in Open() and in the same context SysFileGetSizeByHandle() expects a UDINT as handle.

Interface variables converts a POINTER into an unsigned double integer without throwing warnings. Note: When this function is needed, it mostly indicates a principal design flaw of the POUs which require its usage. Nevertheless, in some situations we encounter some functions in external libraries, where things are completely messed up, e.g. in SysFile, where a file handle is once declared as Pointer in Open() and in the same context SysFileGetSizeByHandle() expects a UDINT as handle.

## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 26.02.2018 | 1.0.1.3 | WAGO / u010663 | Compiled SP16.3 |
| 10.01.2018 | 1.0.1.2 | WAGO / u013972 | Add placeholder property |
| 08.01.2019 | 1.0.1.1 | u015842 | Properties: copyright added |
| 29.09.2015 | 1.0.1.0 | WAGO / u013972 | Add NoPlaceholder property |
| 06.03.2015 | 1.0.0.0 | WAGO / u013972 | Release Version |

WagoSysTypedefs-Internal - 32Bit

This library deals with some few pointer issues, which are target specific, mainly:

Release Note

Interface variables WagoSysTypedefs-Internal - 32Bit Overview This library deals with some few pointer issues, which are target specific, mainly: - conversion from pointers to udints. This is necessary in many system calls where both types are assumed to be 32 bit and mixed together in a rather non-uniform and obscure manner. This mixing often leads to compiler warnings. Those are avoided by introducing a type conversion function Pointer_To_Udint() from this libraray. Release Note - This library is supposed to work only on 32-Bit systems, not on 64-Bit systems. - Normally, the compiler should do all the work of this library without introducing the overhead of a function call in the middle. (Indeed it does so, but it throws warnings, which may obscure other warnings.) - When resolved by placeholders from the device description (in 32-bit systems only), this lib provide a save way of mixing pointers and udints.

## Pointer_To_Udint (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Pointer_To_Udint | UDINT |  |
| Input | p | POINTER TO BYTE | the pointer which is to be typecasted |

converts a POINTER into an unsigned double integer without throwing warnings.

Note: When this function is needed, it mostly indicates a principal design flaw of the POUs which require its usage. Nevertheless, in some situations we encounter some functions in external libraries, where things are completely messed up, e.g. in SysFile, where a file handle is once declared as Pointer in Open() and in the same context SysFileGetSizeByHandle() expects a UDINT as handle.

Interface variables converts a POINTER into an unsigned double integer without throwing warnings. Note: When this function is needed, it mostly indicates a principal design flaw of the POUs which require its usage. Nevertheless, in some situations we encounter some functions in external libraries, where things are completely messed up, e.g. in SysFile, where a file handle is once declared as Pointer in Open() and in the same context SysFileGetSizeByHandle() expects a UDINT as handle.

## Udint_to_Pointer (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Udint_to_Pointer | POINTER TO BYTE |  |
| Input | udi | UDINT | the pointer which is to be typecasted |

converts a POINTER into an unsigned double integer without throwing warnings.

Note: When this function is needed, it mostly indicates a principal design flaw of the POUs which require its usage. Nevertheless, in some situations we encounter some functions in external libraries, where things are completely messed up, e.g. in SysFile, where a file handle is once declared as Pointer in Open() and in the same context SysFileGetSizeByHandle() expects a UDINT as handle.

Interface variables converts a POINTER into an unsigned double integer without throwing warnings. Note: When this function is needed, it mostly indicates a principal design flaw of the POUs which require its usage. Nevertheless, in some situations we encounter some functions in external libraries, where things are completely messed up, e.g. in SysFile, where a file handle is once declared as Pointer in Open() and in the same context SysFileGetSizeByHandle() expects a UDINT as handle.

### Internal Components


## WagoSysTypedefs_Internal_32Bit Library Documentation


| Company: | WAGO |
| Title: | WagoSysTypedefs_Internal_32Bit |
| Version: | 1.0.1.3 |
| Categories: | WAGO Internal\|Target\|PAC; WAGO Internal\|Target\|PFC; WAGO Internal\|Target\|SoftPLC-V3 32Bit; WAGO Internal\|Target\|Speedway |
| Namespace: | WagoTypesInternal |
| Author: | WAGO / u013972 |
| Placeholder: | WagoSysTypedefsInternal |

### Description


This document is automatically generated.

Type Definitions specific for 32-Bit-Machines

This document is automatically generated. Type Definitions specific for 32-Bit-Machines

### Contents:


- 21 mem auxiliary - ptr (ENUM) FuGetVersionHistory (FUN)

### Indices and tables


Based on WagoSysTypedefs_Internal_32Bit.library, last modified 29.05.2024, 19:48:30. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysTypedefs_Internal_32Bit.library, last modified 29.05.2024, 19:48:30. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Other Components


## 21 mem


- auxiliary Dint_to_Pointer (FUN) - Pointer_To_Udint (FUN) - Udint_to_Pointer (FUN) ptr (ENUM)

## auxiliary


- Dint_to_Pointer (FUN) - Pointer_To_Udint (FUN) - Udint_to_Pointer (FUN)

## ptr (ENUM)


| Name | Initial |
| --- | --- |
| NULL | 0 |
| RTS_IEC_INVALID | 16#FFFFFFFF |