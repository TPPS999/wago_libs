# WagoSysTime_Internal_PFC v1.1.0.6 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysTime_Internal_PFC
- **Version:** 1.1.0.6
- **Categories:** WAGO Internal|Target|PFC
- **Namespace:** WagoSysTimeInternal
- **Author:** WAGO / u013972

### Description ¶


This document is automatically generated.

Handling Time and Timezones

This document is automatically generated. Handling Time and Timezones

### Contents: ¶


Contents: - Project Information - Library Information - Function Blocks WagoTimesetZoneAsync (FB) - _FbTimeZoneSetter_Internal (FB) Functions - WagoTimeGetZoneInfo (FUN) - WagoTimeLocaltime (FUN) - WagoTimeSetZone (FUN) - _ConvertLstampToLocalTimeComponents (FUN) - _GetActualTimeZone (FUN) - _GetDateAndTime (FUN) - _GetLongSystemTime (FUN) - _GetLongTime (FUN) - _GetSystemTime (FUN) - _SYSTIMEDATE_to_TimeComponents (FUN) - ... and 4 more Methods - Setting The Clock - WagoTimesetZoneAsync.fb_exit (METH) - WagoTimesetZoneAsync.fb_init (METH) - _FbTimeZoneSetter_Internal.GetResult (METH) - _FbTimeZoneSetter_Internal.SetTimeZone (METH) Program Organization Internal Components Global Variable Lists - LibraryResult (GVL) - ResultItems (GVL) - VersionHistory (GVL) Other Components - 01 aux - 91 TSC - Legacy Types - Timestamps - Timezone - _typTM (STRUCT)

### Indices and tables ¶


Based on WagoSysTime_Internal_PFC.library, last modified 29.05.2024, 19:50:43. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysTime_Internal_PFC.library, last modified 29.05.2024, 19:50:43. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysTime_Internal_PFC.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:50:43 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:50:43 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| DefaultNamespace | WagoSysTimeInternal |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysTime_Internal_PFC |
| NoPlaceholder |  |
| Version | version | 1.1.0.6 |
| Title | string | WagoSysTime_Internal_PFC |
| LibraryCategories | library-category-list | WAGO Internal\|Target\|PFC |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False PublishSymbolsInContainer: True | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. SysTime Library Identification : Placeholder: SysTime Default Resolution: SysTime, * (System) Namespace: SysTime Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoSysPlainMem Library Identification : Placeholder: WagoSysPlainMem Default Resolution: WagoSysPlainMem, * (WAGO) Namespace: WagoSysPlainMem Library Properties : WagoSysTime_Internal_Common Library Identification : Placeholder: WagoSysTime_Internal_Common Default Resolution: WagoSysTime_Internal_Common, * (WAGO) Namespace: WagoSysTimeInternalCommon Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : Library Parameter : Parameter: MAX_STRING_LENGTH = 255 Parameter: MAX_WSTRING_LENGTH = 255 WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties :

### Function Blocks


## WagoTimesetZoneAsync (FB)


| Scope | Name | Type |
| --- | --- | --- |
| Input | bEN | BOOL |
| sDataBaseKey | STRING |
| Output | bDone | BOOL |
| bBusy | BOOL |
| eResult | eResultCode |

Interface variables - WagoTimesetZoneAsync.fb_exit (METH) - WagoTimesetZoneAsync.fb_init (METH)

## _FbTimeZoneSetter_Internal (FB)


you might have to poll GetResult() for several seconds until a result arrives

you might have to poll GetResult() for several seconds until a result arrives - _FbTimeZoneSetter_Internal.GetResult (METH) - _FbTimeZoneSetter_Internal.SetTimeZone (METH)

### Functions


## WagoTimeGetZoneInfo (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | udiPosixTime | UDINT | seconds from EPOCH |
| Output | stTimeZoneDescription | WagoTypes.typTimeZoneDescription |  |

returns the time zone description which is approriate for a given point in time,

Attn: does not fill the output structure properly. Use _wrapped_WagoTimeGetZoneInfo() instead.

Interface variables returns the time zone description which is approriate for a given point in time, Attn: does not fill the output structure properly. Use _wrapped_WagoTimeGetZoneInfo() instead.

## WagoTimeLocaltime (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | udiPosixTime | UDINT | seconds from EPOCH |
| Inout | buffer | _typTM |  |

wraps the POSIX function ‘localtime()’ yet.

Interface variables wraps the POSIX function ‘localtime()’ yet.

## WagoTimeSetZone (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | WagoTimeSetZone | eResultCode |  |
| Input | sDataBaseKey | STRING | The applied data base key, e.g. ‘New Zealand’ |

| result codes |
| 0 | success |
| ENOENT | The database key is unknown to the system |
| ENOSYS | function not implemented |

changes the actual timezone

Some special Keywords are accepted such as ‘Berlin’ and ‘London’, and others. It sets some internal fake variables in order to retrieve timezone information at other places.

This function returns one of the following result codes:

Interface variables changes the actual timezone Some special Keywords are accepted such as ‘Berlin’ and ‘London’, and others. It sets some internal fake variables in order to retrieve timezone information at other places. This function returns one of the following result codes:

## _ConvertLstampToLocalTimeComponents (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | ltStamp | LTIME | Nanoseconds since 1.1.1970 |
| xUseUTC | BOOL | TRUE: ignore timezones for conversion |
| Inout | Buffer | typWagoTimeComponents |  |

splits a timestamp into its components regarding the proper timezone

Return value : Localized time components

For conversion, the operationg system first determines, which time zone (and which DST / ST-Status) would be appropriate for the given timestamp and then applies the proper time zone for conversion. This allows to produce proper time components, according esp. to SoZV, par 2.2 (hours 2A:00 and 2B:00 when changing from DST to ST).

Interface variables splits a timestamp into its components regarding the proper timezone Return value : Localized time components For conversion, the operationg system first determines, which time zone (and which DST / ST-Status) would be appropriate for the given timestamp and then applies the proper time zone for conversion. This allows to produce proper time components, according esp. to SoZV, par 2.2 (hours 2A:00 and 2B:00 when changing from DST to ST).

## _GetActualTimeZone (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | _GetActualTimeZone | typTimeZoneDescription |

retrieves Information about the actually active Timezone

Return Value : The timezone wich is active now.

Note: Be careful that the timezone would not have changed between getting the time and getting the timezone.

Interface variables retrieves Information about the actually active Timezone Return Value : The timezone wich is active now. Note: Be careful that the timezone would not have changed between getting the time and getting the timezone.

## _GetDateAndTime (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | _GetDateAndTime | DT |

retrieves the POSIX time (UT)

Note: After Dec-2105 this will return 16#ffffffff due to an overflow of the variable type DATE_AND_TIME; It it is planned to go farther than that, use GetLongTime() instead, which will not overflow until 2500.

This function yields the actual POSIX-Time. This is traditionally used for timestamps in file systems and for calendar issues.

Note: The returned value is always given in UT / GMT, never in local time. For regarding local timezones for representing the date and time, those functions are used, which are summarized in ‘Calendar’ below.

Interface variables retrieves the POSIX time (UT) Note: After Dec-2105 this will return 16#ffffffff due to an overflow of the variable type DATE_AND_TIME; It it is planned to go farther than that, use GetLongTime() instead, which will not overflow until 2500. This function yields the actual POSIX-Time. This is traditionally used for timestamps in file systems and for calendar issues. Note: The returned value is always given in UT / GMT, never in local time. For regarding local timezones for representing the date and time, those functions are used, which are summarized in ‘Calendar’ below.

## _GetLongSystemTime (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | _GetLongSystemTime | LTIME |

Returns the nanoseconds since system start

In contrast to ‘GetLongTime()’, the return value of ‘GetLongSystemTime()’ is not related to an absolute calendar time, but to the start of the system. Consequently, any setting of the time a has no effect on ‘GetLongSystemTime()’ (but would have on ‘GetLongTime()’).

This is important for implementing strictly monotoneous relative timecounting in device drivers and related applications.

note: ‘GetLongSystemTime()’ uses the same clock base as ‘GetLongTime()’, so both values will differ by an offset, but they will not drift apart from each other.

note: at the moment, this excessive resolution cannot be used by real hardware. Nevertheless, this is done in order to use standard time types.

Interface variables Returns the nanoseconds since system start In contrast to ‘GetLongTime()’, the return value of ‘GetLongSystemTime()’ is not related to an absolute calendar time, but to the start of the system. Consequently, any setting of the time a has no effect on ‘GetLongSystemTime()’ (but would have on ‘GetLongTime()’). This is important for implementing strictly monotoneous relative timecounting in device drivers and related applications. note: ‘GetLongSystemTime()’ uses the same clock base as ‘GetLongTime()’, so both values will differ by an offset, but they will not drift apart from each other. Returns a raw system timestamp in nanosecond resolution note: at the moment, this excessive resolution cannot be used by real hardware. Nevertheless, this is done in order to use standard time types.

## _GetLongTime (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | _GetLongTime | LTIME |

retrieves the global time (UT) since 1.1.1970 in LTIME format

gets an absolute TIME stamp with millisecond resulution since 01.01.1970

Interface variables retrieves the global time (UT) since 1.1.1970 in LTIME format gets an absolute TIME stamp with millisecond resulution since 01.01.1970

## _GetSystemTime (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | _GetSystemTime | TIME |

retrieves the system time

This function is useful for short term time interval with medium precision. It yields the 32-bit standard system time in milliseconds, as used in older days.

note: This is identical to TIME(). It is included here for the sake of completeness.

Interface variables retrieves the system time This function is useful for short term time interval with medium precision. It yields the 32-bit standard system time in milliseconds, as used in older days. note: This is identical to TIME(). It is included here for the sake of completeness.

## _SYSTIMEDATE_to_TimeComponents (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | _SYSTIMEDATE_to_TimeComponents | typWagoTimeComponents |  |
| Input | Base | SYSTIMEDATE | base class |

Copies the structure RTS_SYSTIMEDATE into the derived typWagoTimeComponents and leaves the extended components empty.

Interface variables Copies the structure RTS_SYSTIMEDATE into the derived typWagoTimeComponents and leaves the extended components empty.

## _SetClockFromLTime (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | _SetClockFromLTime | eResultCode |  |
| Input | ltDateTime | LTIME | Nanoseconds from EPOCH |

| result codes |
| 0 | success |
| ERANGE | time value is beyond a reasonable range (1970..2099) |
| ENOSYS | function not implemented |
| EACCES | Function failed due to firmware bugs |

sets the system clock (UT since 1.1.1970, Nanoseconds )

The function produces one of the following result codes:

Interface variables sets the system clock (UT since 1.1.1970, Nanoseconds ) The function produces one of the following result codes: sets the hardware clock to a given timestamp.

## _TimeComponents_to_SYSTIMEDATE (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | _TimeComponents_to_SYSTIMEDATE | SysTimeRtc.SYSTIMEDATE |  |
| Input | Base | typWagoTimeComponents | base class |

Copies the structure RTS_SYSTIMEDATE into the derived typWagoTimeComponents and leaves the extended components empty.

Interface variables Copies the structure RTS_SYSTIMEDATE into the derived typWagoTimeComponents and leaves the extended components empty.

## _obs_wrapped_WagoTimeLocaltime (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | udiPosixTime | UDINT | seconds from EPOCH |
| Inout | buffer | _typTM |  |

wraps the POSIX function ‘localtime()’ yet.

corrections for wrong results of WagoTimeLocaltime TscTime

Interface variables wraps the POSIX function ‘localtime()’ yet. corrections for wrong results of WagoTimeLocaltime TscTime

## _wrapped_WagoTimeGetZoneInfo (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | udiPosixTime | UDINT | seconds from EPOCH |
| Output | stTimeZoneDescription | WagoTypes.typTimeZoneDescription |  |

returns the time zone description which is approriate for a given point in time,

Needed at multiple places.

Interface variables returns the time zone description which is approriate for a given point in time, Needed at multiple places.

### Methods


## Setting The Clock ¶


- _SetClockFromLTime (FUN)

## WagoTimesetZoneAsync.fb_exit (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | fb_exit | BOOL |
| Input | bInCopyCode | BOOL |

## WagoTimesetZoneAsync.fb_init (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | fb_init | BOOL |  |
| Input | bInitRetains | BOOL | bei TRUE werden die Retain-Variablen initialisiert (Warmstart / Kaltstart) |
| bInCopyCode | BOOL | bei TRUE wird die Instanz anschließend in den Copy-Code kopiert (Online Change) |

## _FbTimeZoneSetter_Internal.GetResult (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetResult | eResultCode |

| result codes |
| 0 | setting the time zone was successfully finished |
| EAGAIN | setting is still in progress, try again |
| ENOENT | The database key is unknown to the system |
| ENOSYS | function not implemented |

polls the result of a previous SetTimeZone() Call

Interface variables polls the result of a previous SetTimeZone() Call

## _FbTimeZoneSetter_Internal.SetTimeZone (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SetTimeZone | eResultCode |  |
| Input | sDataBaseKey | STRING | The applied data base key, e.g. ‘New Zealand’ |

| result codes |
| 0 | success |
| ENOENT | The database key is unknown to the system |
| ENOSYS | function not implemented |
| EINPROGRESS | Call was deferred so the result comes later |

changes the actual timezone

This function returns one of the following result codes:

Interface variables changes the actual timezone This function returns one of the following result codes:

### Program Organization


## 20 Program Organization Units


- Legacy Types _SYSTIMEDATE_to_TimeComponents (FUN) - _TimeComponents_to_SYSTIMEDATE (FUN) Setting The Clock - _SetClockFromLTime (FUN) Timestamps - _GetDateAndTime (FUN) - _GetLongSystemTime (FUN) - _GetLongTime (FUN) - _GetSystemTime (FUN) Timezone - _ConvertLstampToLocalTimeComponents (FUN) - _FbTimeZoneSetter_Internal (FB) _FbTimeZoneSetter_Internal.GetResult (METH) - _FbTimeZoneSetter_Internal.SetTimeZone (METH) _GetActualTimeZone (FUN)

### Internal Components


## WagoSysTime_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysTime_Internal_PFC |
| Version: | 1.1.0.6 |
| Categories: | WAGO Internal\|Target\|PFC |
| Namespace: | WagoSysTimeInternal |
| Author: | WAGO / u013972 |

### Description


This document is automatically generated.

Handling Time and Timezones

This document is automatically generated. Handling Time and Timezones

### Contents:


- 20 Program Organization Units Legacy Types - Setting The Clock - Timestamps - Timezone 91 TSC - 01 aux - WagoTimeGetZoneInfo (FUN) - WagoTimeLocaltime (FUN) - WagoTimeSetZone (FUN) - WagoTimesetZoneAsync (FB) - _typTM (STRUCT) LibraryResult (GVL) ResultItems (GVL) VersionHistory (GVL)

### Indices and tables


Based on WagoSysTime_Internal_PFC.library, last modified 29.05.2024, 19:50:43. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysTime_Internal_PFC.library, last modified 29.05.2024, 19:50:43. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

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
| Constant | ERROR | ARRAY [0..7] OF typResultItem | [STRUCT(ID := OK, Severity := eSeverity.none, Text := ‘OK’), STRUCT(ID := EINPROGRESS, Severity := eSeverity.info, Text := ‘Call was deferred so result comes later.’), STRUCT(ID := ERANGE, Severity := eSeverity.error, Text := ‘The value or one of its components is beyond its expected range.’), STRUCT(ID := ENOSYS, Severity := eSeverity.error, Text := ‘Function not implemented.’), STRUCT(ID := EACCES, Severity := eSeverity.error, Text := ‘Time could not be set due to PLC-internal reasons.’), STRUCT(ID := ENOENT, Severity := eSeverity.error, Text := ‘The database key is unknown to the system.’), STRUCT(ID := EUNSPECIFIC, Severity := eSeverity.error, Text := ‘Unspecified other errors from operating system.’), STRUCT(ID := EINVAL, Severity := eSeverity.error, Text := ‘Components denote invalid time stamps (e.g. Minute =60 or Day=0).’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 04.03.2024 | 1.1.0.6 | WAGO / u01663 | Compiled SP16.3 |
| 07.12.2023 | 1.1.0.5 | WAGO / u013972 | Fix for 64-Bit targets |
| 05.04.2022 | 1.1.0.4 | u10103719 | rename object type “char” to “eChar” |
| 08.01.2019 | 1.1.0.3 | u015842 | Properties: copyright added |
| 24.05.2017 | 1.1.0.2 | WAGO / u013972 | Change access modifier of WagoTimesetZoneAsync.fb_init() and WagoTimesetZoneAsync.fb_exit() |
| 16.06.2015 | 1.1.0.1 | WAGO / u013972 | Change _GetLongTime-Resolution |
| 02.03.2015 | 1.1.0.0 | WAGO / u013972 | Replace WagoAppErrorBase with WagoSysErrorBase |
| 20.01.2016 | 1.0.2.0 | WAGO / u013972 | WAT17801 - _GetDateAndTime and _GetLongTime record now Time-Changes form the WBM |
| 29.09.2015 | 1.0.1.0 | WAGO / u013972 | Resolve libraries with placeholders |
| 06.03.2015 | 1.0.0.0 | RE | Release Version |

WagoSysTime_Internal_PFC.library

Known Bugs:

WagoSysTime_Internal_PFC.library Known Bugs: - The RTS in version 3.5.4 obviously does not allow any time settings beyond the POSIX-Epoch, in spite of data ranges indicating otherwise..

### Other Components


## 01 aux


- _obs_wrapped_WagoTimeLocaltime (FUN) - _wrapped_WagoTimeGetZoneInfo (FUN)

## 91 TSC


- 01 aux _obs_wrapped_WagoTimeLocaltime (FUN) - _wrapped_WagoTimeGetZoneInfo (FUN) WagoTimeGetZoneInfo (FUN) WagoTimeLocaltime (FUN) WagoTimeSetZone (FUN) WagoTimesetZoneAsync (FB) - WagoTimesetZoneAsync.fb_exit (METH) - WagoTimesetZoneAsync.fb_init (METH) _typTM (STRUCT)

## Legacy Types


- _SYSTIMEDATE_to_TimeComponents (FUN) - _TimeComponents_to_SYSTIMEDATE (FUN)

## Timestamps


{attribute ‘displaysorting’ := ‘1’}

{attribute ‘displaysorting’ := ‘1’} - _GetDateAndTime (FUN) - _GetLongSystemTime (FUN) - _GetLongTime (FUN) - _GetSystemTime (FUN)

## Timezone


- _ConvertLstampToLocalTimeComponents (FUN) - _FbTimeZoneSetter_Internal (FB) _FbTimeZoneSetter_Internal.GetResult (METH) - _FbTimeZoneSetter_Internal.SetTimeZone (METH) _GetActualTimeZone (FUN)

## _typTM (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| tm_sec | INT | seconds |
| tm_min | INT | minutes |
| tm_hour | INT | hours |
| tm_mday | INT | day OF the month |
| tm_mon | INT | month |
| tm_year | INT | year |
| tm_wday | INT | day OF the week |
| tm_yday | INT | day in the year |
| tm_isdst | INT | daylight saving TIME |

The members of the tm structure are:

InOut: The members of the tm structure are: tm_sec The number of seconds after the minute, normally in the range 0 to 59, but can be up to 60 to allow for leap seconds. tm_min The number of minutes after the hour, in the range 0 to 59. tm_hour The number of hours past midnight, in the range 0 to 23. tm_mday The day of the month, in the range 1 to 31. tm_mon The number of months since January, in the range 0 to 11. tm_year The number of years since 1900. tm_wday The number of days since Sunday, in the range 0 to 6. tm_yday The number of days since January 1, in the range 0 to 365. tm_isdst A flag that indicates whether daylight saving time is in effect at the time described. The value is positive if daylight saving time is in effect, zero if it is not, and negative if the information is not available.