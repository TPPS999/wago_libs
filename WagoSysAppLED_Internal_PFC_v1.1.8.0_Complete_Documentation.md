# WagoSysAppLED_Internal_PFC v1.1.8.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysAppLED_Internal_PFC
- **Version:** 1.1.8.0
- **Categories:** WAGO Internal|Target|PFC; WAGO Internal|Feature|Common|AppLED
- **Namespace:** WagoSysAppLedInternal
- **Author:** WAGO / u013972

### Description ¶


This document is automatically generated.

App LED code for multiple PFC s

This document is automatically generated. App LED code for multiple PFC s

### Contents: ¶


Contents: - Project Information - Library Information - Functions LED_Set_Blink (FUN) - LED_Set_Flash (FUN) - LED_Set_Static (FUN) - Tsc_Color (FUN) - Tsc_LedID (FUN) - WagoAppLED_GetColorModel (FUN) - WagoAppLED_GetFirstAppLedID (FUN) - WagoAppLED_GetMaxAppLedID (FUN) - WagoAppLED_GetOnColor (FUN) - WagoAppLED_IsColorSupported (FUN) - ... and 5 more Program Organization Function Groups Main Interfaces Internal Components - 90 Internal - WagoSysAppLED_Internal_PFC Library Documentation Global Variable Lists - LibraryResult (GVL) - ResultItems (GVL) - VersionHistory (GVL) Other Components - 01 Direct Wrapping - 11 Transpositions - TSC - eLedColor_Tsc (ENUM) - eLedID_Tsc (ENUM) - eLedState (ENUM)

### Indices and tables ¶


Based on WagoSysAppLED_Internal_PFC.library, last modified 29.05.2024, 19:53:43. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysAppLED_Internal_PFC.library, last modified 29.05.2024, 19:53:43. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysAppLED_Internal_PFC.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:53:43 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:53:43 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| DefaultNamespace | WagoSysAppLedInternal |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysAppLED_Internal_PFC |
| NoPlaceholder |  |
| Version | version | 1.1.8.0 |
| Title | string | WagoSysAppLED_Internal_PFC |
| LibraryCategories | library-category-list | WAGO Internal\|Target\|PFC; WAGO Internal\|Feature\|Common\|AppLED |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False Optional: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. SysTarget Library Identification : Placeholder: SysTarget Default Resolution: SysTarget, * (System) Namespace: SysTarget Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesAppLED Library Identification : Placeholder: WagoTypesAppLED Default Resolution: WagoTypesAppLED, * (WAGO) Namespace: WagoTypesAppLED Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : Library Parameter : Parameter: MAX_STRING_LENGTH = 255 Parameter: MAX_WSTRING_LENGTH = 255 WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties :

### Functions


## LED_Set_Blink (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | LED_Set_Blink | DWORD |
| Input | LedId | eLedID_Tsc |
| timTime1 | TIME |
| timTime2 | TIME |
| color1 | eLedColor_Tsc |
| color2 | eLedColor_Tsc |

| result codes |
| 0 | success |
| EALREADY | LED is already in this state |
| EINVAL | Illegal color code |
| ENODEV | Unsupported LED ID |
| ETIME | Illegal timing set |

make the LED blink, i.e. switch between two color states cyclically

On error, no change of the LED state takes place.

Interface variables make the LED blink, i.e. switch between two color states cyclically On error, no change of the LED state takes place.

## LED_Set_Flash (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | LED_Set_Flash | DWORD |
| Input | LedId | eLedID_Tsc |
| timFlash_time | TIME |
| eFlash_color | eLedColor_Tsc |
| eStatic_color | eLedColor_Tsc |

| result codes |
| 0 | success |
| EINVAL | Illegal color code |
| ENODEV | Unsupported LED ID |
| EINVAL | Illegal color code |

and then display continuously a second color (which also could be ‘off’)

While the first phase of the flashis in progress, the xBusy-Output of the FB is TRUE.

When applying this function while the LED is still ‘flash’ing, the flash time will be retriggered.

When the flash time is expired, the LED transits to the ‘static’ mode.

On error, no change of the LED state takes place.

Interface variables and then display continuously a second color (which also could be ‘off’) While the first phase of the flashis in progress, the xBusy-Output of the FB is TRUE. When applying this function while the LED is still ‘flash’ing, the flash time will be retriggered. When the flash time is expired, the LED transits to the ‘static’ mode. On error, no change of the LED state takes place.

## LED_Set_Static (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | LED_Set_Static | DWORD |
| Input | LedId | eLedID_Tsc |
| color | eLedColor_Tsc |

| result codes |
| 0 | success |
| EALREADY | LED is already in this state |
| EINVAL | Illegal color code |
| ENODEV | Unsupported LED ID |

sets the LED to a static operating state

The parameter “eColor” denotes the new illumination color of the LED (which might also be “off”).

If the requested color is not supported by the hardware, this method fails with EINVAL (“Invalid Argument”);

On error, no change of the LED state takes place.

Interface variables sets the LED to a static operating state The parameter “eColor” denotes the new illumination color of the LED (which might also be “off”). If the requested color is not supported by the hardware, this method fails with EINVAL (“Invalid Argument”); On error, no change of the LED state takes place.

## Tsc_Color (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Tsc_Color | eLedColor_Tsc |
| Input | eColor | eLedColor |

converts a color description from type “eLedColor” to the TSC-internal coding

Interface variables converts a color description from type “eLedColor” to the TSC-internal coding

## Tsc_LedID (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Tsc_LedID | eLedID_Tsc |
| Input | eID | eLedID |

converts an LED identification from the type “eLedID” to the TSC-internal notation

Interface variables converts an LED identification from the type “eLedID” to the TSC-internal notation

## WagoAppLED_GetColorModel (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | WagoAppLED_GetColorModel | STRING |

returns a string which identifies the color model of the LEDs in a given PLC

Interface variables returns a string which identifies the color model of the LEDs in a given PLC

## WagoAppLED_GetFirstAppLedID (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | WagoAppLED_GetFirstAppLedID | eLedID |

returns the identifier of the first LED of a PLC

Interface variables returns the identifier of the first LED of a PLC

## WagoAppLED_GetMaxAppLedID (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | WagoAppLED_GetMaxAppLedID | eLedID |

returns the identifier of the last LED of a PLC

Interface variables returns the identifier of the last LED of a PLC

## WagoAppLED_GetOnColor (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | WagoAppLED_GetOnColor | eLedColor |

returns the default color which represents “ON”. This is depending on the capabilities of the PLC.

Interface variables returns the default color which represents “ON”. This is depending on the capabilities of the PLC.

## WagoAppLED_IsColorSupported (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | WagoAppLED_IsColorSupported | BOOL |  |
| Input | eColor | eLedColor | the color which is to be probed |

tells, if a given color code is supported by the hardware

Interface variables tells, if a given color code is supported by the hardware

## WagoAppLED_IsLedIdSupported (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | WagoAppLED_IsLedIdSupported | BOOL |  |
| Input | eID | eLedID | the LED which is to be tested |

tells if an given LED-identification is implemented on the given hardware

Interface variables tells if an given LED-identification is implemented on the given hardware

## WagoAppLED_SetAllLEDs (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | WagoAppLED_SetAllLEDs | eResultCode |  |
| Input | eColor | eLedColor | color for all LEDs |

sets all LEDs on a PLC to a static color. Mostly used for turning all LEDs off

Interface variables sets all LEDs on a PLC to a static color. Mostly used for turning all LEDs off

## WagoAppLED_Set_Blink (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | WagoAppLED_Set_Blink | eResultCode |  |
| Input | eId | eLedID | identifies the LED which is to set |
| tTime1 | TIME | duration of the first blink phase |
| tTime2 | TIME | duration of the second blink phase |
| eColor1 | eLedColor | color during the first phase |
| eColor2 | eLedColor | color during the other phase |

| result codes |
| 0 | success |
| ENOENT | “No Entity” The LED does not exist |
| EBADR | “Bad Request” Requested Color is not suported |
| EACCES | “Acess Fault” Access on Tsc-Level has faulted |
| ENOSYS | This functionality is not supported by the target hardware |
| ETIME | Bad timing parameters |
| EINVAL | otherwise invalid parameters |

Sets an LED to blink mode

Interface variables Sets an LED to blink mode

## WagoAppLED_Set_Flash (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | WagoAppLED_Set_Flash | eResultCode |  |
| Input | eId | eLedID | identifies the LED which is to set |
| tFlashTime | TIME | the duration of the flash pulse |
| eFlashColor | eLedColor | color of the flash pulse |
| eStaticColor | eLedColor | color after the flash. |

| result codes |
| 0 | success |
| ENOENT | “No Entity” The LED does not exist |
| EBADR | “Bad Request” Requested Color is not suported |
| EACCES | “Acess Fault” Access on Tsc-Level has faulted |
| ENOSYS | This functionality is not supported by the target hardware |
| ETIME | Bad timing parameters |
| EINVAL | otherwise invalid parameters |

Sets an LED to Flash Mode.

After the flash is finished, the LED returns to static mode.

Interface variables Sets an LED to Flash Mode. After the flash is finished, the LED returns to static mode. Flash mode: The LED is at eColor1 for the duration of the flash time and transits to eColor2 afterwards.

## WagoAppLED_Set_Static (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | WagoAppLED_Set_Static | eResultCode |  |
| Input | eId | eLedID | identifies the LED which is to set |
| eColor | eLedColor | selects the color for that LED |

| result codes |
| 0 | success |
| ENOENT | “No Entity” The LED does not exist |
| EBADR | “Bad Request” Requested Color is not suported |
| EACCES | “Acess Fault” Access on Tsc-Level has faulted |
| ENOSYS | This functionality is not supported by the target hardware |
| EINVAL | otherwise invalid parameters |

Sets an LED to static mode (including “off”)

Interface variables Sets an LED to static mode (including “off”)

### Program Organization


## 20 Program Organization Units


- 01 Direct Wrapping WagoAppLED_Set_Blink (FUN) - WagoAppLED_Set_Flash (FUN) - WagoAppLED_Set_Static (FUN) 02 Emulated Functions - WagoAppLED_GetColorModel (FUN) - WagoAppLED_GetFirstAppLedID (FUN) - WagoAppLED_GetMaxAppLedID (FUN) - WagoAppLED_GetOnColor (FUN) - WagoAppLED_IsColorSupported (FUN) - WagoAppLED_IsLedIdSupported (FUN) - WagoAppLED_SetAllLEDs (FUN)

### Function Groups


## 02 Emulated Functions


- WagoAppLED_GetColorModel (FUN) - WagoAppLED_GetFirstAppLedID (FUN) - WagoAppLED_GetMaxAppLedID (FUN) - WagoAppLED_GetOnColor (FUN) - WagoAppLED_IsColorSupported (FUN) - WagoAppLED_IsLedIdSupported (FUN) - WagoAppLED_SetAllLEDs (FUN)

### Main Interfaces


## 10 Main Interface


- LED_Set_Blink (FUN) - LED_Set_Flash (FUN) - LED_Set_Static (FUN) - eLedColor_Tsc (ENUM) - eLedID_Tsc (ENUM) - eLedState (ENUM)

### Internal Components


## 90 Internal


- TSC 10 Main Interface LED_Set_Blink (FUN) - LED_Set_Flash (FUN) - LED_Set_Static (FUN) - eLedColor_Tsc (ENUM) - eLedID_Tsc (ENUM) - eLedState (ENUM) 11 Transpositions - Tsc_Color (FUN) - Tsc_LedID (FUN)

## WagoSysAppLED_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysAppLED_Internal_PFC |
| Version: | 1.1.8.0 |
| Categories: | WAGO Internal\|Target\|PFC; WAGO Internal\|Feature\|Common\|AppLED |
| Namespace: | WagoSysAppLedInternal |
| Author: | WAGO / u013972 |

### Description


This document is automatically generated.

App LED code for multiple PFC s

This document is automatically generated. App LED code for multiple PFC s

### Contents:


- 20 Program Organization Units 01 Direct Wrapping - 02 Emulated Functions 90 Internal - TSC LibraryResult (GVL) ResultItems (GVL) VersionHistory (GVL)

### Indices and tables


Based on WagoSysAppLED_Internal_PFC.library, last modified 29.05.2024, 19:53:43. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysAppLED_Internal_PFC.library, last modified 29.05.2024, 19:53:43. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

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
| Constant | ERROR | ARRAY [0..8] OF typResultItem | [STRUCT(ID := OK, Severity := eSeverity.none, Text := ‘OK.’), STRUCT(ID := EALREADY, Severity := eSeverity.info, Text := ‘LED is already in this state.’), STRUCT(ID := ENOENT, Severity := eSeverity.error, Text := ‘The LED does not exist.’), STRUCT(ID := EBADR, Severity := eSeverity.error, Text := ‘Requested Color is not suported.’), STRUCT(ID := EACCES, Severity := eSeverity.error, Text := ‘Access on Tsc-Level has faulted.’), STRUCT(ID := ENOSYS, Severity := eSeverity.error, Text := ‘This functionality is not supported by the target hardware.’), STRUCT(ID := ETIME, Severity := eSeverity.error, Text := ‘Bad timing parameters.’), STRUCT(ID := EINVAL, Severity := eSeverity.error, Text := ‘Otherwise invalid parameters.’), STRUCT(ID := ENODEV, Severity := eSeverity.error, Text := ‘Unsupported LED ID (TSC-Layer).’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 08.05.2024 | 1.1.8.0 | WAGO / u013972 | Add supported Device (0751-9401) |
| 05.02.2024 | 1.1.7.1 | u010663 | compiled as SP16.3 |
| 15.08.2023 | 1.1.7.0 | WAGO / u013972 | Add supported Device (0750-8302) |
| 17.07.2023 | 1.1.6.3 | WAGO / u013972 | Add supported Device (0750-811X) |
| 24.11.2022 | 1.1.6.2 | u0103719 | Add supported Device (0750-8210/0040-0001, 0750-8211/0040-0001, 0750-8212/0025-0001, 0750-8212/0040-0001, 0750-8212/0025-0002, 0750-8216/0025-0001) |
| 23.11.2022 | 1.1.6.1 | u0103719 | Add supported Device (0750/0xx-001) |
| 26.01.2022 | 1.1.6.0 | WAGO / u013972 | Add supported Device (0751-9301) |
| 17.06.2020 | 1.1.5.0 | WAGO / u013972 | Add supported Device (750-8210, 750-8217) |
| 08.01.2019 | 1.1.4.1 | u015842 | Properties: copyright added |
| 24.09.2018 | 1.1.4.0 | WAGO / u013972 | Add supported Device (750-8212/000-100) |
| 24.08.2017 | 1.1.3.0 | WAGO / u013972 | Add supported Device (750-8215) |
| 07.06.2017 | 1.1.2.0 | WAGO / u013972 | Add supported Device (750-8212, 750-8213, 750-8214, 750-8216) |
| 10.03.2017 | 1.1.1.1 | WAGO / u013543 | Add supported Device (2850-3111, 2850-3112) |
| 04.03.2016 | 1.1.1.0 | WAGO / u013972 | Replace WagoAppErrorBase with WagoSysErrorBase and WagoTypesErrorBase |
| 15.12.2015 | 1.1.0.0 | WAGO / u013972 | Add PFC100 and 8207 |
| 29.09.2015 | 1.0.1.0 | WAGO / u013972 | Workaround for 0351-Bug |
| 04.02.2015 | 1.0.0.0 | WAGO / u013972 | Release Version |

WagoSysAppLED_Internal_PFC.library

Release Notes:

WagoSysAppLED_Internal_PFC.library Release Notes: - AppLED-Internal libraries are highly specifical for individual targets, as other targets have different numbers of LEDs and possibly different colors. - Error-Codes from TSC now honored.

### Other Components


## 01 Direct Wrapping


- WagoAppLED_Set_Blink (FUN) - WagoAppLED_Set_Flash (FUN) - WagoAppLED_Set_Static (FUN)

## 11 Transpositions


- Tsc_Color (FUN) - Tsc_LedID (FUN)

## TSC


- 10 Main Interface LED_Set_Blink (FUN) - LED_Set_Flash (FUN) - LED_Set_Static (FUN) - eLedColor_Tsc (ENUM) - eLedID_Tsc (ENUM) - eLedState (ENUM) 11 Transpositions - Tsc_Color (FUN) - Tsc_LedID (FUN)

## eLedColor_Tsc (ENUM)


| Name | Initial |
| --- | --- |
| Tsc_Off | 0 |
| Tsc_Green | 1 |
| Tsc_Red | 2 |
| Tsc_Yellow | 3 |
| Tsc_Blue | 4 |
| Tsc_Cyan | 5 |
| Tsc_Magenta | 6 |
| Tsc_White | 7 |

## eLedID_Tsc (ENUM)


| Name | Initial |
| --- | --- |
| Tsc_none | 0 |
| Tsc_AppLED_1 | 1 |
| Tsc_AppLED_2 | 2 |
| Tsc_AppLED_3 | 3 |
| Tsc_AppLED_4 | 4 |
| Tsc_AppLED_5 | 5 |
| Tsc_AppLED_6 | 6 |
| Tsc_AppLED_7 | 7 |

identifies one of the LEDs which can be operated with FbAppLED

InOut: identifies one of the LEDs which can be operated with FbAppLED

## eLedState (ENUM)


| Name | Initial |
| --- | --- |
| Tsc_FAIL | 0 |
| Tsc_OFF | 1 |
| Tsc_STATIC | 2 |
| Tsc_BLINK | 3 |
| Tsc_FLASH | 4 |