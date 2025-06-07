# WagoSysFifo v1.6.1.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysFifo
- **Version:** 1.6.1.0
- **Categories:** WAGO Internal|Common
- **Author:** WAGO / u013972
- **Placeholder:** WagoSysFifo

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Fifo Support [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Fifo Support [1]

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks - Methods FbFIFO.AdvanceReadIndex (METH) - FbFIFO.AdvanceWriteIndex (METH) - FbFIFO.Initialize (METH) - FbFIFO.ReAttachBufferSpace (METH) - FbFIFO.Read (METH) - FbFIFO.ReadPointer (PROP) - FbFIFO.Reset (METH) - FbFIFO.Write (METH) - FbFIFO.WritePointer (PROP) Program Organization Main Interfaces Global Variable Lists - LibraryResult (GVL) - ResultItems (GVL) - VersionHistory (GVL) Other Components - 20 Direct Memory Access - 30 Properties - 40 Administration - FbFIFO.FreeSpace (PROP) - FbFIFO.IsDataAvailable (PROP) - FbFIFO.IsValid (PROP) - FbFIFO.NDataAvailable (PROP) - FbFIFO.NLinearDataContent (PROP) - FbFIFO.NLinearFreeSpace (PROP)

### Indices and tables ¶


| [1] | Based on WagoSysFifo.library, last modified 14.01.2019, 16:34:01. The content of this file was automatically generated with None on 14.01.2019, 16:34:04 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysFifo Library Documentation


| Company: | WAGO |
| Title: | WagoSysFifo |
| Version: | 1.6.1.0 |
| Categories: | WAGO Internal\|Common |
| Author: | WAGO / u013972 |
| Placeholder: | WagoSysFifo |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Fifo Support [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Fifo Support [1]

### Contents:


- 20 Program Organization Units FbFIFO (FB) LibraryResult (GVL) ResultItems (GVL) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysFifo.library, last modified 14.01.2019, 16:34:01. The content of this file was automatically generated with None on 14.01.2019, 16:34:04 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysFifo.library |
| contentFile | WagoSysFifo_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 16:34:04 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 16:34:01 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysFifo |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysFifo |
| DefaultNamespace |  |
| Version | version | 1.6.1.0 |
| Title | string | WagoSysFifo |
| LibraryCategories | library-category-list | WAGO Internal\|Common |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. SysMem Library Identification : Placeholder: SysMem Default Resolution: SysMem, * (System) Namespace: SysMem Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoSysPlainMem Library Identification : Placeholder: WagoSysPlainMem Default Resolution: WagoSysPlainMem, * (WAGO) Namespace: WagoSysPlainMem Library Properties : WagoSysTypedefs_Internal_32Bit Library Identification : Placeholder: WagoSysTypedefsInternal Default Resolution: WagoSysTypedefs_Internal_32Bit, * (WAGO) Namespace: WagoTypesInternal Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties :

### Function Blocks


## FbFIFO (FB)


```
VAR
    FiFo  : FbFifo;
    Space : array[1..cAvailableSize] of BYTE;
    n     : UDINT;
END_VAR

FiFo.initialize(ADR(Space[1]), cAvailableSize);

n := FiFo.FreeSpace;
IF (n>=myMessageSize) THEN
    FiFo.Write(pMyMessage, myMessageSize);
END_IF;

IF FiFo.IsDataAvailable THEN
```

General administration tool for buffering data.

The Fb contains only descriptive elements, while the buffer space itself has to be provided externally.

General administration tool for buffering data. The Fb contains only descriptive elements, while the buffer space itself has to be provided externally. Usage: - 10 Main Interface FbFIFO.Initialize (METH) - FbFIFO.Read (METH) - FbFIFO.Reset (METH) - FbFIFO.Write (METH) 20 Direct Memory Access - FbFIFO.AdvanceReadIndex (METH) - FbFIFO.AdvanceWriteIndex (METH) - FbFIFO.NLinearDataContent (PROP) - FbFIFO.NLinearFreeSpace (PROP) - FbFIFO.ReadPointer (PROP) - FbFIFO.WritePointer (PROP) 30 Properties - FbFIFO.FreeSpace (PROP) - FbFIFO.IsDataAvailable (PROP) - FbFIFO.IsValid (PROP) - FbFIFO.NDataAvailable (PROP) 40 Administration - FbFIFO.ReAttachBufferSpace (METH)

### Methods


## FbFIFO.AdvanceReadIndex (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | AdvanceReadIndex | eResultCode |  |
| Input | udiRxNBytes | UDINT | amount of data to be skipped |

| result codes |
| 0 | Success |
| ENODATA | More data skipped than contained in the buffer. |

marks a number of bytes as already read.

Purpose: update of read index after having transferred a linear chunk of data externally.

Interface variables marks a number of bytes as already read. Purpose: update of read index after having transferred a linear chunk of data externally.

## FbFIFO.AdvanceWriteIndex (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | AdvanceWriteIndex | eResultCode |  |
| Input | udiTxNBytes | UDINT | amount of data to be logged in |

| result codes |
| 0 | Success |
| ENOSPC | More data skipped than contained in the buffer. |

marks a number of bytes in the buffer as ‘written’.

purpose: update of read index after having transferred a linear chunk of data externally

Interface variables marks a number of bytes in the buffer as ‘written’. purpose: update of read index after having transferred a linear chunk of data externally

## FbFIFO.Initialize (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Initialize | eResultCode |  |
| Input | pBuffer | POINTER TO BYTE | where is the buffer range |
| udiBufferSize | UDINT | what size has the buffer range |

| result codes |
| 0 | success |
| EINVAL | Null-pointer or size <2 or size >2G |

attaches Buffer Space to the object.

Interface variables attaches Buffer Space to the object.

## FbFIFO.ReAttachBufferSpace (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ReAttachBufferSpace | eResultCode |  |
| Input | pBuffer | POINTER TO BYTE | where is the buffer range |
| udiBufferSize | UDINT | what size has the buffer range |

attaches new buffer space to the fifo and move old contents to the new space

Interface variables attaches new buffer space to the fifo and move old contents to the new space Attn: - this functionality might be obsoleted in near future - it is not clear, if this is needed at all

## FbFIFO.Read (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Read | eResultCode |  |
| Input | pRxBuffer | POINTER TO BYTE | where to write the read data |
| udiRxBufferSize | UDINT | how many bytes to read maximum |
| Output | udiRxNBytes | UDINT | how many bytes are actually read. |

| result codes |
| 0 | success |
| ENODATA | no data in buffer |
| EINVAL | null-pointer or size <2 or size >2G |

Reads data from the fifo

The amount auf actually read bytes is returned via udiRxNBytes. If 0 bytes are to be read, the method returns silently without real action.

Interface variables Reads data from the fifo The amount auf actually read bytes is returned via udiRxNBytes. If 0 bytes are to be read, the method returns silently without real action.

## FbFIFO.ReadPointer (PROP)


yields a pointer to the actual read data

Purpose: get location of a linear data chunk.

yields a pointer to the actual read data Purpose: get location of a linear data chunk.

## FbFIFO.Reset (METH)


Puts the FiFo to the state ‘empty’

Puts the FiFo to the state ‘empty’

## FbFIFO.Write (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Write | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | source of the data |
| udiTxNBytes | UDINT | how many bytes to write |

| result codes |
| 0 | success |
| ENOSPC | not enough buffer space available for new data. |
| EINVAL | null-pointer or size <2 or size >2G |

Write a chunk of data into the FiFo.

If there is too less space in the FIFO the write fails completely without partial writing.

Interface variables Write a chunk of data into the FiFo. If there is too less space in the FIFO the write fails completely without partial writing.

## FbFIFO.WritePointer (PROP) ¶


### Program Organization


## 20 Program Organization Units


- FbFIFO (FB) 10 Main Interface FbFIFO.Initialize (METH) - FbFIFO.Read (METH) - FbFIFO.Reset (METH) - FbFIFO.Write (METH) 20 Direct Memory Access - FbFIFO.AdvanceReadIndex (METH) - FbFIFO.AdvanceWriteIndex (METH) - FbFIFO.NLinearDataContent (PROP) - FbFIFO.NLinearFreeSpace (PROP) - FbFIFO.ReadPointer (PROP) - FbFIFO.WritePointer (PROP) 30 Properties - FbFIFO.FreeSpace (PROP) - FbFIFO.IsDataAvailable (PROP) - FbFIFO.IsValid (PROP) - FbFIFO.NDataAvailable (PROP) 40 Administration - FbFIFO.ReAttachBufferSpace (METH)

### Main Interfaces


## 10 Main Interface


- FbFIFO.Initialize (METH) - FbFIFO.Read (METH) - FbFIFO.Reset (METH) - FbFIFO.Write (METH)

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
| Constant | ERROR | ARRAY [0..3] OF typResultItem | [STRUCT(ID := OK, Severity := eSeverity.none, Text := ‘OK’), STRUCT(ID := ENODATA, Severity := eSeverity.info, Text := ‘No (more) data to process.’), STRUCT(ID := EINVAL, Severity := eSeverity.error, Text := ‘Invalid arguments.’), STRUCT(ID := ENOSPC, Severity := eSeverity.error, Text := ‘Not enough buffer space available for new data.’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 08.01.2019 | 1.6.1.0 | u015842 | Properties: free placeholder added |
| 02.02.2016 | 1.6.0.0 | WAGO / u010545 | WagoAppErrorBase changed to WagoSysErrorBase / WagoTypesErrorBase |
| 22.10.2015 | 1.5.3.0 | WAGO / u013972 | Publish WagoPlainMem and WagoTypesCommon |
| 29.09.2015 | 1.5.2.0 | WAGO / u013972 | Resolve libraries with palceholders |
| 23.09.2015 | 1.5.1.0 | WAGO / u013972 | Add Placeholder |
| 03.07.2015 | 1.5.0.0 | WAGO / u013972 | Release Version |

WagoSysFifo.library

### Other Components


## 20 Direct Memory Access


- FbFIFO.AdvanceReadIndex (METH) - FbFIFO.AdvanceWriteIndex (METH) - FbFIFO.NLinearDataContent (PROP) - FbFIFO.NLinearFreeSpace (PROP) - FbFIFO.ReadPointer (PROP) - FbFIFO.WritePointer (PROP)

## 30 Properties


- FbFIFO.FreeSpace (PROP) - FbFIFO.IsDataAvailable (PROP) - FbFIFO.IsValid (PROP) - FbFIFO.NDataAvailable (PROP)

## 40 Administration


- FbFIFO.ReAttachBufferSpace (METH)

## FbFIFO.FreeSpace (PROP)


retrieves the maximum amount of bytes which can be written into the buffer

Note: for an empty buffer this is ‘Bufferspace’ -1.

retrieves the maximum amount of bytes which can be written into the buffer Note: for an empty buffer this is ‘Bufferspace’ -1.

## FbFIFO.IsDataAvailable (PROP)


tells if any data is written into the Fifo

tells if any data is written into the Fifo

## FbFIFO.IsValid (PROP)


Tells if the Fifo is properly initialized

Tells if the Fifo is properly initialized

## FbFIFO.NDataAvailable (PROP)


tells how many data is contained in the fifo

tells how many data is contained in the fifo

## FbFIFO.NLinearDataContent (PROP)


yields the size of the chunk of read data which can be copied linearly via ReadPointer

yields the size of the chunk of read data which can be copied linearly via ReadPointer

## FbFIFO.NLinearFreeSpace (PROP)


yields the size of the chunk of linear data to be written

yields the size of the chunk of linear data to be written