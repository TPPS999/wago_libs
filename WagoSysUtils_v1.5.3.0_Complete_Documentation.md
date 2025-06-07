# WagoSysUtils v1.5.3.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysUtils
- **Version:** 1.5.3.0
- **Categories:** WAGO Internal|Common
- **Author:** WAGO / u013972
- **Placeholder:** WagoSysUtils

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Various Auxiliary Routines ATTN: unreviewed, may be moved elsewhere [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Various Auxiliary Routines ATTN: unreviewed, may be moved elsewhere [1]

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks - Functions DecBotByte (FUN) - DecBotDi (FUN) - DecBotI (FUN) - DecBotLi (FUN) - DecBotSi (FUN) - DecBotUdi (FUN) - DecBotUi (FUN) - DecBotUli (FUN) - DecByte (FUN) - DecDi (FUN) - ... and 22 more Methods - FbExclusivityHandler.AttachExclusively (METH) - FbExclusivityHandler.ForceDetachment (METH) - FbExclusivityHandler.IsAccessGranted (METH) - FbExclusivityHandler.ReleaseExclusivity (METH) - FbExclusivityHandler.TestExclusivity (METH) Program Organization Global Variable Lists - LibraryResult (GVL) - ResultItems (GVL) - VersionHistory (GVL) Other Components - 01 InplaceManipulation - 02 Exclusivity Handling

### Indices and tables ¶


| [1] | Based on WagoSysUtils.library, last modified 14.01.2019, 16:33:17. The content of this file was automatically generated with None on 14.01.2019, 16:33:21 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysUtils Library Documentation


| Company: | WAGO |
| Title: | WagoSysUtils |
| Version: | 1.5.3.0 |
| Categories: | WAGO Internal\|Common |
| Author: | WAGO / u013972 |
| Placeholder: | WagoSysUtils |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Various Auxiliary Routines ATTN: unreviewed, may be moved elsewhere [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Various Auxiliary Routines ATTN: unreviewed, may be moved elsewhere [1]

### Contents:


- 20 Program Organization Units 01 InplaceManipulation - 02 Exclusivity Handling LibraryResult (GVL) ResultItems (GVL) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysUtils.library, last modified 14.01.2019, 16:33:17. The content of this file was automatically generated with None on 14.01.2019, 16:33:21 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysUtils.library |
| contentFile | WagoSysUtils_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 16:33:21 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 16:33:17 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysUtils |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysUtils |
| DefaultNamespace |  |
| Version | version | 1.5.3.0 |
| Title | string | WagoSysUtils |
| LibraryCategories | library-category-list | WAGO Internal\|Common |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoSysTypedefs_Internal_32Bit Library Identification : Placeholder: WagoSysTypedefsInternal Default Resolution: WagoSysTypedefs_Internal_32Bit, * (WAGO) Namespace: WagoTypesInternal Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties :

### Function Blocks


## FbExclusivityHandler (FB)


This FB is to be embedded in other FBs, when the outer FB is to be accessed by several clients but during acces, each client desires exclusive access.

usage: see e.g. WagoSysCom_Internal_PFC

This FB is to be embedded in other FBs, when the outer FB is to be accessed by several clients but during acces, each client desires exclusive access. usage: see e.g. WagoSysCom_Internal_PFC - FbExclusivityHandler.AttachExclusively (METH) - FbExclusivityHandler.ForceDetachment (METH) - FbExclusivityHandler.IsAccessGranted (METH) - FbExclusivityHandler.ReleaseExclusivity (METH) - FbExclusivityHandler.TestExclusivity (METH)

### Functions


## DecBotByte (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecBotByte | BYTE |
| Inout | v | BYTE |

Decreases a byte if it is not zero and returns the value after modification. On Zero, the value will not be modified.

Interface variables Decreases a byte if it is not zero and returns the value after modification. On Zero, the value will not be modified.

## DecBotDi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecBotDi | DINT |
| Inout | v | DINT |

Decreases a double int if it is not zero and returns the value after modification. On Zero, the value will not be modified. On negative range limits the value wraps around.

Interface variables Decreases a double int if it is not zero and returns the value after modification. On Zero, the value will not be modified. On negative range limits the value wraps around.

## DecBotI (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecBotI | INT |
| Inout | v | INT |

Decreases an int if it is not zero and returns the value after modification. On Zero, the value will not be modified. On negative range limits the value wraps around.

Interface variables Decreases an int if it is not zero and returns the value after modification. On Zero, the value will not be modified. On negative range limits the value wraps around.

## DecBotLi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecBotLi | LINT |
| Inout | v | LINT |

Decreases a 64-bit int if it is not zero and returns the value after modification. On Zero, the value will not be modified. On negative range limits the value wraps around.

Interface variables Decreases a 64-bit int if it is not zero and returns the value after modification. On Zero, the value will not be modified. On negative range limits the value wraps around.

## DecBotSi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecBotSi | SINT |
| Inout | v | SINT |

Decreases a 8-bit-int if it is not zero and returns the value after modification. On Zero, the value will not be modified. On negative range limits the value wraps around.

Interface variables Decreases a 8-bit-int if it is not zero and returns the value after modification. On Zero, the value will not be modified. On negative range limits the value wraps around.

## DecBotUdi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecBotUdi | UDINT |
| Inout | v | UDINT |

Decreases an unsigned double-int if it is not zero and returns the value after modification. On Zero, the value will not be modified.

Interface variables Decreases an unsigned double-int if it is not zero and returns the value after modification. On Zero, the value will not be modified.

## DecBotUi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecBotUi | UINT |
| Inout | v | UINT |

Decreases an unsigned int if it is not zero and returns the value after modification. On Zero, the value will not be modified.

Interface variables Decreases an unsigned int if it is not zero and returns the value after modification. On Zero, the value will not be modified.

## DecBotUli (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecBotUli | ULINT |
| Inout | v | ULINT |

Decreases an unsigned 64-bit-int if it is not zero and returns the value after modification. On Zero, the value will not be modified.

Interface variables Decreases an unsigned 64-bit-int if it is not zero and returns the value after modification. On Zero, the value will not be modified.

## DecByte (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecByte | BYTE |
| Inout | v | BYTE |

Decreases a byte regardless of its value and returns the value after modification. At the range linits the value wraps around.

Interface variables Decreases a byte regardless of its value and returns the value after modification. At the range linits the value wraps around.

## DecDi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecDi | DINT |
| Inout | v | DINT |

Decreases a double-int regardless of its value and returns the value after modification. At the range linits the value wraps around.

Interface variables Decreases a double-int regardless of its value and returns the value after modification. At the range linits the value wraps around.

## DecI (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecI | INT |
| Inout | v | INT |

Decreases an int regardless of its value and returns the value after modification. At the range linits the value wraps around.

Interface variables Decreases an int regardless of its value and returns the value after modification. At the range linits the value wraps around.

## DecLi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecLi | LINT |
| Inout | v | LINT |

Decreases a 64-bit-int regardless of its value and returns the value after modification. At the range linits the value wraps around.

Interface variables Decreases a 64-bit-int regardless of its value and returns the value after modification. At the range linits the value wraps around.

## DecSi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecSi | SINT |
| Inout | v | SINT |

Decreases 8-bit-int regardless of its value and returns the value after modification. At the range linits the value wraps around.

Interface variables Decreases 8-bit-int regardless of its value and returns the value after modification. At the range linits the value wraps around.

## DecUdi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecUdi | UDINT |
| Inout | v | UDINT |

Decreases an unsigned double int regardless of its value and returns the value after modification. At the range linits the value wraps around.

Interface variables Decreases an unsigned double int regardless of its value and returns the value after modification. At the range linits the value wraps around.

## DecUi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecUi | UINT |
| Inout | v | UINT |

Decreases an unsigned int regardless of its value and returns the value after modification. At the range linits the value wraps around.

Interface variables Decreases an unsigned int regardless of its value and returns the value after modification. At the range linits the value wraps around.

## DecUli (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DecUli | ULINT |
| Inout | v | ULINT |

Decreases amn unsigned 64-bit-int regardless of its value and returns the value after modification. At the range linits the value wraps around.

Interface variables Decreases amn unsigned 64-bit-int regardless of its value and returns the value after modification. At the range linits the value wraps around.

## IncByte (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncByte | BYTE |
| Inout | v | BYTE |

Increases a byte and returns its value after modification. On the limits of its range, the value wraps around.

Interface variables Increases a byte and returns its value after modification. On the limits of its range, the value wraps around.

## IncDi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncDi | DINT |
| Inout | v | DINT |

Increases a double-int and returns its value after modification. On the limits of its range, the value wraps around.

Interface variables Increases a double-int and returns its value after modification. On the limits of its range, the value wraps around.

## IncI (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncI | INT |
| Inout | v | INT |

Increases an int and returns its value after modification. On the limits of its range, the value wraps around.

Interface variables Increases an int and returns its value after modification. On the limits of its range, the value wraps around.

## IncLi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncLi | LINT |
| Inout | v | LINT |

Increases a 64-bit-int and returns its value after modification. On the limits of its range, the value wraps around.

Interface variables Increases a 64-bit-int and returns its value after modification. On the limits of its range, the value wraps around.

## IncSi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncSi | SINT |
| Inout | v | SINT |

Increases an 8-bit-int and returns its value after modification. On the limits of its range, the value wraps around.

Interface variables Increases an 8-bit-int and returns its value after modification. On the limits of its range, the value wraps around.

## IncTopByte (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncTopByte | BYTE |
| Inout | v | BYTE |

Increases a byte if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

Interface variables Increases a byte if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

## IncTopDi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncTopDi | DINT |
| Inout | v | DINT |

Increases a double int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

Interface variables Increases a double int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

## IncTopI (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncTopI | INT |
| Inout | v | INT |

Increases an int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

Interface variables Increases an int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

## IncTopLi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncTopLi | LINT |
| Inout | v | LINT |

Increases a 64-bit-int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

Interface variables Increases a 64-bit-int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

## IncTopSi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncTopSi | SINT |
| Inout | v | SINT |

Increases a 8-bit-int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

Interface variables Increases a 8-bit-int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

## IncTopUdi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncTopUdi | UDINT |
| Inout | v | UDINT |

Increases an unsigned double-int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

Interface variables Increases an unsigned double-int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

## IncTopUi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncTopUi | UINT |
| Inout | v | UINT |

Increases an unsigned int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

Interface variables Increases an unsigned int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

## IncTopUli (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncTopUli | ULINT |
| Inout | v | ULINT |

Increases an unsigned 64-bit-int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

Interface variables Increases an unsigned 64-bit-int if it is not at the top border of its range and returns the value after modification. The value will not wrap around the top border of its range.

## IncUdi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncUdi | UDINT |
| Inout | v | UDINT |

Increases an unsigned double-int and returns its value after modification. On the limits of its range, the value wraps around.

Interface variables Increases an unsigned double-int and returns its value after modification. On the limits of its range, the value wraps around.

## IncUi (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncUi | UINT |
| Inout | v | UINT |

Increases an unsigned int and returns its value after modification. On the limits of its range, the value wraps around.

Interface variables Increases an unsigned int and returns its value after modification. On the limits of its range, the value wraps around.

## IncUli (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | IncUli | ULINT |
| Inout | v | ULINT |

Increases an unsigned 64-bit-int and returns its value after modification. On the limits of its range, the value wraps around.

Interface variables Increases an unsigned 64-bit-int and returns its value after modification. On the limits of its range, the value wraps around.

### Methods


## FbExclusivityHandler.AttachExclusively (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | AttachExclusively | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | address of the instance which wants to use the device exclusively |

| result codes |
| 0 | success, exclusive usage is granted |
| EBUSY | Usage is not granted. The device has been attached to another user already |
| EINVAL | Null instance is passed. (Null denotes a detached device) |

Tries to get grant of exclusive acces to the device.

Note (1): This mechanism provides a means for cooperatively using specific devices. However, It does not implement mechanisms for enforcing that policy.

Note (2): It seems suitable to pass the address of the attached high-level-FB as unique identification tag for the client which uses the device. The divece, however does not use any knowledge about those high-level-FBs, so virtually any unique number may be passed here.

Interface variables Tries to get grant of exclusive acces to the device. Note (1): This mechanism provides a means for cooperatively using specific devices. However, It does not implement mechanisms for enforcing that policy. Note (2): It seems suitable to pass the address of the attached high-level-FB as unique identification tag for the client which uses the device. The divece, however does not use any knowledge about those high-level-FBs, so virtually any unique number may be passed here.

## FbExclusivityHandler.ForceDetachment (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ForceDetachment | eResultCode |

| result codes |
| 0 | success (this operation does not fail) |

Forces detachment of the device.

This is used for initialization or for recovery from crashed client FBs which still hold a zombie lock to the device, which could not be released otherwise. This method is not intended for regular usage.

Interface variables Forces detachment of the device. This is used for initialization or for recovery from crashed client FBs which still hold a zombie lock to the device, which could not be released otherwise. This method is not intended for regular usage.

## FbExclusivityHandler.IsAccessGranted (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | IsAccessGranted | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | address of the instance which wants to use the device exclusively |

| result codes |
| 0 | success, exclusive usage is granted |
| EBUSY | Usage is not granted. The device has been attached to another FB already |

It does not check, whether the access is exclusively or not exclusively.

Interface variables It does not check, whether the access is exclusively or not exclusively.

## FbExclusivityHandler.ReleaseExclusivity (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ReleaseExclusivity | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | address of the instance which reseases its exclusivity |

| result codes |
| 0 | success, the device is detached again |
| EBUSY | Usage has not been granted to this FB. It is in use by another FB |
| EINVAL | Null instance is passed. (Null denotes a detached device) |

Releases the device from exclusive usage.

Interface variables Releases the device from exclusive usage.

## FbExclusivityHandler.TestExclusivity (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | TestExclusivity | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | address of the instance which wants to use the device exclusively |

| result codes |
| 0 | success, exclusive usage is granted |
| EUNATCH | the device is not attached at all |
| EBUSY | Usage is not granted. The device has been attached to another FB already |

Tests if an FB has been granted exclusive usage of the device without trying to attach it

Interface variables Tests if an FB has been granted exclusive usage of the device without trying to attach it

### Program Organization


## 20 Program Organization Units


- 01 InplaceManipulation DecBotByte (FUN) - DecBotDi (FUN) - DecBotI (FUN) - DecBotLi (FUN) - DecBotSi (FUN) - DecBotUdi (FUN) - DecBotUi (FUN) - DecBotUli (FUN) - DecByte (FUN) - DecDi (FUN) - DecI (FUN) - DecLi (FUN) - DecSi (FUN) - DecUdi (FUN) - DecUi (FUN) - DecUli (FUN) - IncByte (FUN) - IncDi (FUN) - IncI (FUN) - IncLi (FUN) - IncSi (FUN) - IncTopByte (FUN) - IncTopDi (FUN) - IncTopI (FUN) - IncTopLi (FUN) - IncTopSi (FUN) - IncTopUdi (FUN) - IncTopUi (FUN) - IncTopUli (FUN) - IncUdi (FUN) - IncUi (FUN) - IncUli (FUN) 02 Exclusivity Handling - FbExclusivityHandler (FB) FbExclusivityHandler.AttachExclusively (METH) - FbExclusivityHandler.ForceDetachment (METH) - FbExclusivityHandler.IsAccessGranted (METH) - FbExclusivityHandler.ReleaseExclusivity (METH) - FbExclusivityHandler.TestExclusivity (METH)

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
| Constant | ERROR | ARRAY [0..3] OF typResultItem | [STRUCT(ID := OK, Severity := eSeverity.none, Text := ‘OK’), STRUCT(ID := EINVAL, Severity := eSeverity.error, Text := ‘Invalid arguments.’), STRUCT(ID := EBUSY, Severity := eSeverity.error, Text := ‘Usage has not been granted to this FB. It is in use by another FB.’), STRUCT(ID := EUNATCH, Severity := eSeverity.error, Text := ‘The device is not attached at all.’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 08.01.2019 | 1.5.3.0 | u015842 | Properties: free placeholder added |
| 26.02.2016 | 1.5.2.1 | WAGO / u010545 | Change WagoAppErrorBase to WagoSysErrorBase / WagoTypesErrorBase |
| 28.10.2015 | 1.5.2.0 | WAGO / u013972 | Resolve Libraries with Placeholders |
| 23.09.2015 | 1.5.1.0 | WAGO / u013972 | Add Placeholder Property |
| 03.07.2015 | 1.5.0.0 | WAGO / u013972 | Release Version |

WagoAuxUtils (AKA WagoAuxiliaries)

WagoAuxUtils (AKA WagoAuxiliaries)

### Other Components


## 01 InplaceManipulation


- DecBotByte (FUN) - DecBotDi (FUN) - DecBotI (FUN) - DecBotLi (FUN) - DecBotSi (FUN) - DecBotUdi (FUN) - DecBotUi (FUN) - DecBotUli (FUN) - DecByte (FUN) - DecDi (FUN) - DecI (FUN) - DecLi (FUN) - DecSi (FUN) - DecUdi (FUN) - DecUi (FUN) - DecUli (FUN) - IncByte (FUN) - IncDi (FUN) - IncI (FUN) - IncLi (FUN) - IncSi (FUN) - IncTopByte (FUN) - IncTopDi (FUN) - IncTopI (FUN) - IncTopLi (FUN) - IncTopSi (FUN) - IncTopUdi (FUN) - IncTopUi (FUN) - IncTopUli (FUN) - IncUdi (FUN) - IncUi (FUN) - IncUli (FUN)

## 02 Exclusivity Handling


- FbExclusivityHandler (FB) FbExclusivityHandler.AttachExclusively (METH) - FbExclusivityHandler.ForceDetachment (METH) - FbExclusivityHandler.IsAccessGranted (METH) - FbExclusivityHandler.ReleaseExclusivity (METH) - FbExclusivityHandler.TestExclusivity (METH)