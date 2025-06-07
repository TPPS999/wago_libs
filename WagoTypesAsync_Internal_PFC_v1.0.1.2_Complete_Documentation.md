# WagoTypesAsync_Internal_PFC v1.0.1.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesAsync_Internal_PFC
- **Version:** 1.0.1.2
- **Categories:** WAGO FunctionalView|Base; WAGO LayerView|Types and Interfaces; Application; WAGO Internal|Target|PFC
- **Namespace:** WagoTypesAsyncInternal
- **Author:** WAGO / u013972

### Description ¶


This document is automatically generated.

Scheduling modes for product specific events

This document is automatically generated. Scheduling modes for product specific events

### Contents: ¶


Contents: - Project Information - Library Information - Functions FuGetVersionHistory (FUN) - SchedulingMode (FUN) - SchedulingMode_EventPriority (FUN) Internal Components Global Variable Lists Other Components

### Indices and tables ¶


Based on WagoTypesAsync_Internal_PFC.library, last modified 29.05.2024, 19:51:12. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesAsync_Internal_PFC.library, last modified 29.05.2024, 19:51:12. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesAsync_Internal_PFC.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:51:12 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:51:12 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| DefaultNamespace | WagoTypesAsyncInternal |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesAsync_Internal_PFC |
| NoPlaceholder |  |
| Version | version | 1.0.1.2 |
| Title | string | WagoTypesAsync_Internal_PFC |
| LibraryCategories | library-category-list | WAGO FunctionalView\|Base; WAGO LayerView\|Types and Interfaces; Application; WAGO Internal\|Target\|PFC |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties :

### Functions


## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 27.02.2024 | 1.0.1.2 | u010663 | Compiled SP16.3 |
| 08.01.2019 | 1.0.1.1 | u015842 | Properties: copyright added |
| 29.09.2015 | 1.0.1.0 | u013972 | Resolve libraries with placeholders |
| 06.03.2015 | 1.0.0.0 | RE | Release Version |

WagoTypesCommon

Interface variables WagoTypesCommon

## SchedulingMode (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SchedulingMode | eSchedulingMode |  |
| Input | eEvent | eSchedulingModeEvent | device specific scheduling mode |

```
VAR
   eSchedMode := eSchedulingMode; // regular scheduling mode from WagoTypesCommon.library
END_VAR

eSchedMode := SchedulingMode(eSchedulingModeEvent.Modbus_Watchdog_Expired);  // Device specific mode
eSchedMode := eSchedulingMode.Background;                                    // Regular mode
```

```
eSchedMode := eSchedulingModeEvent.Modbus_Watchdog_Expired;  // Device specific mode
```

Casts a device specific scheduling mode into a generic scheduling mode.

Note: Technically, the direct assignment

would also work as intended, but it would produce a warning message. This warning is avoided by using this typecasting function.

Interface variables Casts a device specific scheduling mode into a generic scheduling mode. Usage: Note: Technically, the direct assignment would also work as intended, but it would produce a warning message. This warning is avoided by using this typecasting function.

## SchedulingMode_EventPriority (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SchedulingMode_EventPriority | eSchedulingMode |  |
| Input | eEvent | eSchedulingModeEvent | device specific event id |
| ePrio | eSchedulingMode | desired priority |

```
VAR
   eSchedMode := eSchedulingMode; // regular scheduling mode from WagoTypesCommon.library
END_VAR

eSchedMode := SchedulingMode_EventPriority(eSchedulingModeEvent.Modbus_Watchdog_Expired,
                                           eSchedulingMode.Background);
```

Casts a device specific scheduling mode into a generic scheduling mode.

In extension to the type-casting function SchedulingMode() , this one allows for specification of an additional priority.

Interface variables Casts a device specific scheduling mode into a generic scheduling mode. In extension to the type-casting function SchedulingMode() , this one allows for specification of an additional priority. Usage:

### Internal Components


## WagoTypesAsync_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoTypesAsync_Internal_PFC |
| Version: | 1.0.1.2 |
| Categories: | WAGO FunctionalView\|Base; WAGO LayerView\|Types and Interfaces; Application; WAGO Internal\|Target\|PFC |
| Namespace: | WagoTypesAsyncInternal |
| Author: | WAGO / u013972 |

### Description


This document is automatically generated.

Scheduling modes for product specific events

This document is automatically generated. Scheduling modes for product specific events

### Contents:


- AsyncInternalConst (GVL) - FuGetVersionHistory (FUN) - SchedulingMode (FUN) - SchedulingMode_EventPriority (FUN) - eSchedulingModeEvent (ENUM)

### Indices and tables


Based on WagoTypesAsync_Internal_PFC.library, last modified 29.05.2024, 19:51:12. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesAsync_Internal_PFC.library, last modified 29.05.2024, 19:51:12. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## AsyncInternalConst (GVL)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | EventModePitch | eSchedulingMode | 16#40 |  |
| PrioritySchedMask | DWORD | 16#3F |  |
| EventSchedMask | DWORD | 16#FFFFFFC0 |  |
| LowestFreeRunning | eSchedulingMode | eSchedulingMode.RealTimeHigh | 1 |
| HighestFreeRunning | eSchedulingMode | eSchedulingMode.Background | 15 |

Specific constants for number ranges.

Attention: when defining new priorities, the upper two values of the range [0..PrioritySchedMask] MUST NOT be used because those values are reserved for special purposes.

(In this case ths would be 16#3E and 16#3F.)

Specific constants for number ranges. Attention: when defining new priorities, the upper two values of the range [0..PrioritySchedMask] MUST NOT be used because those values are reserved for special purposes. (In this case ths would be 16#3E and 16#3F.)

### Other Components


## eSchedulingModeEvent (ENUM)


| Name | Initial |
| --- | --- |
| Local_Bus_Cycle | 16#100 |
| Local_Bus_Event_1 | 16#200 |
| Local_Bus_Event_2 | 16#300 |
| Local_Bus_Event_3 | 16#400 |
| Local_Bus_Event_4 | 16#500 |
| Modbus_Watchdog_Expired | 16#1000 |
| Modbus_Watchdog_Running | 16#1100 |
| Modbus_Watchdog_Stopped | 16#1200 |

```
VAR
   eSchedMode := eSchedulingMode; // regular scheduling mode from WagoTypesCommon.library
END_VAR

eSchedMode := SchedulingMode(eSchedulingModeEvent.Modbus_Watchdog_Expired);  // Device specific mode
eSchedMode := eSchedulingMode.Background;                                    // Regular mode
eSchedMode := SchedulingMode_EventPriority(eSchedulingModeEvent.Modbus_Watchdog_Expired,
                                           eSchedulingMode.Background);
```

For attaching tasks to specific events.

These events are an extension to eSchedulingMode. Wherever a eSchedulingMode is expected, one of the modes enumerated below can also be used.

Note: To avoid warnings about the enumeration type, a type casing function SchedulingMode() or SchedulingMode_EventPriority() should be involved:

These type casting functions are also provided by this library.

InOut: For attaching tasks to specific events. These events are an extension to eSchedulingMode. Wherever a eSchedulingMode is expected, one of the modes enumerated below can also be used. Note: To avoid warnings about the enumeration type, a type casing function SchedulingMode() or SchedulingMode_EventPriority() should be involved: These type casting functions are also provided by this library.