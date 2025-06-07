# WagoSysEvent_Internal_PFC v1.0.2.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysEvent_Internal_PFC
- **Version:** 1.0.2.1
- **Categories:** Application; WAGO Internal|Target|PFC
- **Author:** WAGO / u013972

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling Events [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling Events [1]

### Contents: ¶


Contents: - Project Information - Library Information - Functions GetWagoEventPostingPermission (FUN) - GetWagoEventRegistrationPermission (FUN) Program Organization Internal Components Global Variable Lists - LibraryResult (GVL) - ResultItems (GVL) - VersionHistory (GVL)

### Indices and tables ¶


| [1] | Based on WagoSysEvent_Internal_PFC.library, last modified 14.01.2019, 17:03:25. The content of this file was automatically generated with None on 14.01.2019, 17:03:27 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysEvent_Internal_PFC.library |
| contentFile | WagoSysEvent_Internal_PFC_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 17:03:27 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 17:03:25 |
| Description | string | See: Description |
| DocFormat | reStructuredText |
| Author | WAGO / u013972 |
| DefaultNamespace |  |
| Company | WAGO |
| Title | WagoSysEvent_Internal_PFC |
| Project | WagoSysEvent_Internal_PFC |
| NoPlaceholder |  |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Version | version | 1.0.2.1 |
| LibraryCategories | library-category-list | Application; WAGO Internal\|Target\|PFC |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties : WagoTypesEvent Library Identification : Placeholder: WagoTypesEvent Default Resolution: WagoTypesEvent, * (WAGO) Namespace: WagoTypesEvent Library Properties :

### Functions


## GetWagoEventPostingPermission (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetWagoEventPostingPermission | eResultCode |
| Input | eEventID | eWagoEventID |

| Result Codes |
| 0 | Event may be used without restriction |
| ENOENT | The Event ID is unknown |
| EPERM | The Event must not be posted via WagoAppEvent |

Retrieves , whether the user is allowed to post a specified event.

Possible answers are “Yes”, “No”, and “Event is Unknown”.

This status might be depending on the target. It is evaluated in WagoAppEvent.library.

Interface variables Retrieves , whether the user is allowed to post a specified event. Possible answers are “Yes”, “No”, and “Event is Unknown”. This status might be depending on the target. It is evaluated in WagoAppEvent.library.

## GetWagoEventRegistrationPermission (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetWagoEventRegistrationPermission | eResultCode |
| Input | eEventID | eWagoEventID |

| Result Codes |
| 0 | The Event may be used without restriction |
| ENOENT | The Event ID is unknown |
| EPERM | The Event must not be registerted upon. |

Retrieves , whether the user us allowed to register on a specified event.

Possible answers are “Yes”, “No”, and “Event is Unknown”.

This status might be depending on the target. It is evaluated in WagoAppEvent.library.

Interface variables Retrieves , whether the user us allowed to register on a specified event. Possible answers are “Yes”, “No”, and “Event is Unknown”. This status might be depending on the target. It is evaluated in WagoAppEvent.library.

### Program Organization


## 20 Program Organization Units


- GetWagoEventPostingPermission (FUN) - GetWagoEventRegistrationPermission (FUN)

### Internal Components


## WagoSysEvent_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysEvent_Internal_PFC |
| Version: | 1.0.2.1 |
| Categories: | Application; WAGO Internal\|Target\|PFC |
| Author: | WAGO / u013972 |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling Events [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling Events [1]

### Contents:


- 20 Program Organization Units GetWagoEventPostingPermission (FUN) - GetWagoEventRegistrationPermission (FUN) LibraryResult (GVL) ResultItems (GVL) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoSysEvent_Internal_PFC.library, last modified 14.01.2019, 17:03:25. The content of this file was automatically generated with None on 14.01.2019, 17:03:27 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

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
| Constant | ERROR | ARRAY [0..2] OF typResultItem | [STRUCT(ID := OK, Severity := eSeverity.none, Text := ‘OK’), STRUCT(ID := ENOENT, Severity := eSeverity.error, Text := ‘The event is unknown in this context.’), STRUCT(ID := EPERM, Severity := eSeverity.error, Text := ‘This event must not be posted or egistered via WagoAppEvent.’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 08.01.2019 | 1.0.2.1 | u015842 | Properties: copyright added |
| 04.03.2016 | 1.0.2.0 | WAGO / u013972 | Replace WagoAppErrorBase with WagoSysErrorBase |
| 29.09.2015 | 1.0.1.0 | WAGO / u013972 | Resolve libraries with placeholder |
| 06.03.2015 | 1.0.0.0 | RE | Release Version |