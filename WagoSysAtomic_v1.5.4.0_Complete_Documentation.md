# WagoSysAtomic v1.5.4.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysAtomic
- **Version:** 1.5.4.0
- **Categories:** WAGO Internal|Common
- **Namespace:** WagoSysAtomic
- **Author:** WAGO / u013972
- **Placeholder:** WagoSysAtomic

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling Atomic Variable Access [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling Atomic Variable Access [1]

### Contents: ¶


Contents: - Documentation Index 10 Documentation - WagoSysAtomic Library Documentation Project Information Library Information Function Blocks - doc10_General (FB) - doc90_Specifications (FB) Functions - Atomic_TestAndReset_Dword (FUN) - Atomic_TestAndSet_Dword (FUN) Program Organization Global Variable Lists - LibraryResult (GVL) - ResultItems (GVL) - VersionHistory (GVL) Other Components - 01 DWORD - 32-Bit

### Indices and tables ¶


| [1] | Based on WagoSysAtomic.library, last modified 14.01.2019, 17:01:55. The content of this file was automatically generated with None on 14.01.2019, 17:01:58 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## 10 Documentation


- doc10_General (FB) - doc90_Specifications (FB)

## WagoSysAtomic Library Documentation


| Company: | WAGO |
| Title: | WagoSysAtomic |
| Version: | 1.5.4.0 |
| Categories: | WAGO Internal\|Common |
| Namespace: | WagoSysAtomic |
| Author: | WAGO / u013972 |
| Placeholder: | WagoSysAtomic |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling Atomic Variable Access [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling Atomic Variable Access [1]

### Contents:


- 10 Documentation doc10_General (FB) - doc90_Specifications (FB) 20 Program Organization Units - 32-Bit LibraryResult (GVL) ResultItems (GVL) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysAtomic.library, last modified 14.01.2019, 17:01:55. The content of this file was automatically generated with None on 14.01.2019, 17:01:58 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysAtomic.library |
| contentFile | WagoSysAtomic_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 17:01:58 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 17:01:55 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysAtomic |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysAtomic |
| DefaultNamespace | WagoSysAtomic |
| Version | version | 1.5.4.0 |
| Title | string | WagoSysAtomic |
| LibraryCategories | library-category-list | WAGO Internal\|Common |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysAtomic_Internal_32Bit Library Identification : Placeholder: WagoSysAtomicInternal Default Resolution: WagoSysAtomic_Internal_32Bit, * (WAGO) Namespace: WagoSysAtomicInternal Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties :

### Function Blocks


## doc10_General (FB)


| Availability of Atomic Operations |
| --- |
| Op | DWORD | DINT | UDINT | TIME | DT | LINT | ULINT | LTIME | Pointer |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| CAS | + | + | + | + | + | + | + | + | + |
| Read | + | + | + | + | + | + | + | + | + |
| Swap | + | + | + | + | + | + | + | + | + |
| TAD | - | + | + | - | - | - | - | - | - |
| Add | - | + | + | - | - | - | - | - | + |
| Sub | - | + | + | - | - | - | - | - | + |
| Inc | - | + | + | - | - | - | - | - | + |
| Dec | - | + | + | - | - | - | - | - | + |
| And | + | - | - | - | - | - | - | - | - |
| Or | + | - | - | - | - | - | - | - | - |
| Xor | + | - | - | - | - | - | - | - | - |
| TAS | + | - | - | - | - | - | - | - | - |
| TAR | + | - | - | - | - | - | - | - | - |

This library provides an interface for atomic variable access.

For multiple data types a number of atomic access methods (description: see below) is provided: Not all methods apply to all types: While e.g. Read() applies to all data types, e.g. bitmanipulations are not provided for pointer types.

The operations are the following:

Core Operations

Atomic Integer Arithmetic

Atomic Bitfield Operations

This library provides an interface for atomic variable access. For multiple data types a number of atomic access methods (description: see below) is provided: Not all methods apply to all types: While e.g. Read() applies to all data types, e.g. bitmanipulations are not provided for pointer types. Caveats: - 8-Bit-Datatypes and 16-Bit-Datatypes are not covered by this library (specification[4]) - Datatype “Pointer” has a variable size, depending on the target native datasize (mostly 32-Bit, in future 64-Bit also) - Variables must be aligned to 4-Byte-boundaries or 8-Byte-boundaries. Normally, the Codesys-compiler automatically takes care to place these variables accordingly. The operations are the following: Core Operations CompareAndSet(&Variable, probeValue, newValue) : BOOL ( CAS ): Compares A variable against a probe and sets the variable to the new value if both are equal. Returns TRUE if both are equial, FALSE otherwise Swap(&variable, newValue) : oldvalue : Sets the variable to a new value and returns the old value Read(&Variable) : oldvalue : Delivers the value of a variable. TestAndDec(&variable) : oldvalue ( TAD ): Decreases a variable by one if it is greater than zero. The previous value is returned. If the variable was zero, it will not be modified. Atomic Integer Arithmetic Add/Sub(&Variable, summand) : result : Adds/Subtracts a value to/from a variable Inc/Dec(&Variable) : result : Increases/Decreases a variable atomically by one Atomic Bitfield Operations TestAndSet(&Variable, bitno) : BOOL ( TAS ): Sets a bit in a 32-Bit-Field and returns its previous value. The bitnumber counts from 0 (least significant Bit in Little-Endian-Representation) to 31. Other bitnumbers will be silently discarded. TestAndReset(&Variable, bitno) : BOOL ( TAR ): Resets a bit in a 32-Bit-Field and returns its previous value. The bitnumber counts from 0 (least significant Bit in Little-Endian-Representation) to 31. Other bitnumbers will be silently discarded. And/Or/Xor(&Variable, operand): newvalue : Logical operations to a variable.

## doc90_Specifications (FB)


This library refers to the following documents and specifications:

This library refers to the following documents and specifications: 1. Discussion on Meeting on October-1-2013 with Mark Rohlfing et al. (see: Minutes of Meeting “MC003457_BP_20131001_Reinholz.docx) 2. Telephonic Discussion on November-4-2013 with Jobst Wellensiek. 3. Wago Review 241 on November-6-2013 4. Discussion on Meeting on February-20-2014 with Mark Rohlfing et al. (see: Minutes of Meeting “MC003457_BP_20140220.docx)

### Functions


## Atomic_TestAndReset_Dword (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Atomic_TestAndReset_Dword | BOOL |  |
| Inout | V | DWORD | Variable to be atomically accessed to |
| Input | udiBitNo | UDINT |  |

Resets a bit in a 32-bit-bitfield and returns the previous value of that bit.

Interface variables Resets a bit in a 32-bit-bitfield and returns the previous value of that bit. The bitnumber counts from 0 (least significant bit in Little-Endian-Representation) to 31. Other bitnumbers will be silently discarded.

## Atomic_TestAndSet_Dword (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Atomic_TestAndSet_Dword | BOOL |  |
| Inout | V | DWORD | Variable to be atomically accessed to |
| Input | udiBitNo | UDINT |  |

Sets a bit in a 32-bit-bitfield and returns the previous value of that bit.

Interface variables Sets a bit in a 32-bit-bitfield and returns the previous value of that bit. The bitnumber counts from 0 (least significant bit in Little-Endian-Representation) to 31. Other bitnumbers will be silently discarded.

### Program Organization


## 20 Program Organization Units


- 32-Bit 01 DWORD Atomic_TestAndReset_Dword (FUN) - Atomic_TestAndSet_Dword (FUN)

### Global Variable Lists


## LibraryResult (GVL)


| Name | Type |
| --- | --- |
| Factory | FbResultFactory |

```
VAR
  eMyResult : eResultCode;  // result code whic is to be investigated
  oError    : FbResult;     // result object for use in highe levels.
END_VAR;

eMyResult := myFunction(...);
Namespace.LibraryResult.Factory.SetResult(eMyResult, oError);
```

Factory for standard result objects

Use this to translate result codes from this library into standard result objects.

where ‘Namespace’ denotes the namespace which is used for including the specific library and ‘myFunction()’ is an example for a general function from this library.

Factory for standard result objects Use this to translate result codes from this library into standard result objects. Usage: where ‘Namespace’ denotes the namespace which is used for including the specific library and ‘myFunction()’ is an example for a general function from this library.

## ResultItems (GVL)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | ERROR | ARRAY [0..0] OF typResultItem | [STRUCT(ID := OK, Severity := eSeverity.none, Text := ‘OK’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 08.01.2019 | 1.5.4.0 | u015842 | Properties: free placeholder added |
| 26.02.2016 | 1.5.3.2 | WAGO / u010545 | Change WagoAppErrorBase to WagoSysErrorBase / WagoTypesErrorBase |
| 23.09.2015 | 1.5.2.0 | WAGO / u013972 | Add WagoTypesCommon, Resolve libraries with placeholders |
| 03.07.2015 | 1.5.0.0 | WAGO / u013972 | Release Version |

WagoSysAtomic

### Other Components


## 01 DWORD


- Atomic_TestAndReset_Dword (FUN) - Atomic_TestAndSet_Dword (FUN)

## 32-Bit


- 01 DWORD Atomic_TestAndReset_Dword (FUN) - Atomic_TestAndSet_Dword (FUN)