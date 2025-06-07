# WagoSysTime_Internal_Common v1.1.0.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysTime_Internal_Common
- **Version:** 1.1.0.2
- **Categories:** WAGO Internal|Common
- **Namespace:** WagoSysTimeInternalCommon
- **Author:** WAGO / u013972
- **Placeholder:** WagoSysTime_Internal_Common

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling Time and Timezones [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling Time and Timezones [1]

### Contents: ¶


Contents: - Project Information - Library Information - Functions FuGetVersionHistory (FUN) - _CalcCalendarWeek (FUN) - _ConvertUtcToLocalTimeComponents (FUN) - _IsLeapYear (FUN) Program Organization Internal Components Global Variable Lists - LibraryResult (GVL) - ResultItems (GVL)

### Indices and tables ¶


| [1] | Based on WagoSysTime_Internal_Common.library, last modified 14.01.2019, 16:36:56. The content of this file was automatically generated with None on 14.01.2019, 16:36:58 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysTime_Internal_Common.library |
| contentFile | WagoSysTime_Internal_Common_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 14.01.2019, 16:36:58 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 14.01.2019, 16:36:56 |
| Description | string | See: Description |
| DocFormat | reStructuredText |
| Author | WAGO / u013972 |
| DefaultNamespace | WagoSysTimeInternalCommon |
| Placeholder | WagoSysTime_Internal_Common |
| Company | WAGO |
| Title | WagoSysTime_Internal_Common |
| Project | WagoSysTime_Internal_Common |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Version | version | 1.1.0.2 |
| LibraryCategories | library-category-list | WAGO Internal\|Common |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False PublishSymbolsInContainer: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoSysPlainMem Library Identification : Placeholder: WagoSysPlainMem Default Resolution: WagoSysPlainMem, * (WAGO) Namespace: WagoSysPlainMem Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties :

### Functions


## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 08.01.2019 | 1.0.0.2 | u015842 | Properties: copyright added |
| 26.06.2016 | 1.1.0.1 | WAGO / u013972 | Change Version in the Version History and Update the compiler version to 3.5.9.6 |
| 02.03.2015 | 1.1.0.0 | WAGO / u013972 | Replace WagoAppErrorBase with WagoSysErrorBase |
| 29.09.2015 | 1.0.1.0 | WAGO / u013972 | Workaround for C0351-Bug, Resolve Libraries with placeholders |

WagoSysTime_Internal_Common

Interface variables WagoSysTime_Internal_Common

## _CalcCalendarWeek (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | _CalcCalendarWeek | eResultCode |  |
| Input | uiYear | UINT | Year (e.g. 2006) |
| uiDayOfWeek | UINT | Day of week (1..7: Monday = 1, Sunday = 7 |
| uiYday | UINT | Day of year (1..365): January 1 = 1, [...] |
| Output | uiWeekOfYear | UINT | Calendar Week according to ISO8601 |
| iYearOffsetForWoY | INT | Offset for the year when near year boundaries. |

| result codes |
| Ok | Success (nothing else is returned here). |

Calculates the calendar week to a given date.

The output iYearOffsetForWoY is normally 0, -1 if the week is the last week of previous year, and +1 if the week is the first week of following year. E.g.: Dez-31-2015 is CW 01-2016, which is an offset of +1.

Attention: This function expects preprocessed input (correct day-of-week matching to day-of-year).

Interface variables Calculates the calendar week to a given date. The output iYearOffsetForWoY is normally 0, -1 if the week is the last week of previous year, and +1 if the week is the first week of following year. E.g.: Dez-31-2015 is CW 01-2016, which is an offset of +1. Attention: This function expects preprocessed input (correct day-of-week matching to day-of-year).

## _ConvertUtcToLocalTimeComponents (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | ltStamp | LTIME | Nanoseconds since 1.1.1970 |
| Inout | Buffer | typWagoTimeComponents | Result structure |

splits a timestamp into its components WITHOUT regarding the proper timezone

Interface variables splits a timestamp into its components WITHOUT regarding the proper timezone

## _IsLeapYear (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | _IsLeapYear | BOOL |  |
| Input | uiYear | UINT | Year (e.g. 2006) |

Tells, if a year number is a leap year or not.

Limitations: The Gregorian rules for leap years are applied here, so for year numbers before the Gregorian calendar (i.e. 1582), this function may be deliver inaccurate results.

Interface variables Tells, if a year number is a leap year or not. Limitations: The Gregorian rules for leap years are applied here, so for year numbers before the Gregorian calendar (i.e. 1582), this function may be deliver inaccurate results.

### Program Organization


## 20 Program Organization Units


- _CalcCalendarWeek (FUN) - _ConvertUtcToLocalTimeComponents (FUN) - _IsLeapYear (FUN)

### Internal Components


## WagoSysTime_Internal_Common Library Documentation


| Company: | WAGO |
| Title: | WagoSysTime_Internal_Common |
| Version: | 1.1.0.2 |
| Categories: | WAGO Internal\|Common |
| Namespace: | WagoSysTimeInternalCommon |
| Author: | WAGO / u013972 |
| Placeholder: | WagoSysTime_Internal_Common |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling Time and Timezones [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling Time and Timezones [1]

### Contents:


- 20 Program Organization Units _CalcCalendarWeek (FUN) - _ConvertUtcToLocalTimeComponents (FUN) - _IsLeapYear (FUN) FuGetVersionHistory (FUN) LibraryResult (GVL) ResultItems (GVL)

### Indices and tables


| [1] | Based on WagoSysTime_Internal_Common.library, last modified 14.01.2019, 16:36:56. The content of this file was automatically generated with None on 14.01.2019, 16:36:58 |

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
| Constant | ERROR | ARRAY [0..0] OF typResultItem | [STRUCT(ID := OK, Severity := eSeverity.none, Text := ‘OK’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.