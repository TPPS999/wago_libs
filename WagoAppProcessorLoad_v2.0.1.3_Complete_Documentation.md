# WagoAppProcessorLoad v2.0.1.3 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoAppProcessorLoad
- **Version:** 2.0.1.3
- **Categories:** Application
- **Namespace:** WagoAppProcessorLoad
- **Author:** WAGO / JSo
- **Placeholder:** WagoAppProcessorLoad

### Description ¶


This document is automatically generated.

Determines the current process load caused by the plc.

This document is automatically generated. Determines the current process load caused by the plc.

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks - Methods - Program Organization - Global Variable Lists - Other Components FbProcessorLoad.IsThreshold1Reached (PROP) - FbProcessorLoad.IsThreshold2Reached (PROP) - FbProcessorLoad.LogLevel (PROP) - FbProcessorLoad.OverloadAction (PROP) - FbProcessorLoad.ProcessorLoad (PROP) - FbProcessorLoad.Threshold1 (PROP) - FbProcessorLoad.Threshold2 (PROP)

### Indices and tables ¶


Based on WagoAppProcessorLoad.library, last modified 29.05.2024, 20:39:33. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoAppProcessorLoad.library, last modified 29.05.2024, 20:39:33. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoAppProcessorLoad Library Documentation


| Company: | WAGO |
| Title: | WagoAppProcessorLoad |
| Version: | 2.0.1.3 |
| Categories: | Application |
| Namespace: | WagoAppProcessorLoad |
| Author: | WAGO / JSo |
| Placeholder: | WagoAppProcessorLoad |

### Description


This document is automatically generated.

Determines the current process load caused by the plc.

This document is automatically generated. Determines the current process load caused by the plc.

### Contents:


- 20 Program Organization Units FbProcessorLoad (FB) VersionHistory (GVL)

### Indices and tables


Based on WagoAppProcessorLoad.library, last modified 29.05.2024, 20:39:33. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoAppProcessorLoad.library, last modified 29.05.2024, 20:39:33. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoAppProcessorLoad.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:39:33 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:39:33 |
| Description | string | See: Description |
| Copyright | © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / JSo |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoAppProcessorLoad |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoAppProcessorLoad |
| DefaultNamespace | WagoAppProcessorLoad |
| Version | version | 2.0.1.3 |
| Title | string | WagoAppProcessorLoad |
| Released | bool | False |
| LibraryCategories | library-category-list | Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. IoStandard Library Identification : Placeholder: IoStandard Default Resolution: IoStandard, * (System) Namespace: IoStandard Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysProcessorLoad Library Identification : Placeholder: WagoSysProcessorLoad Default Resolution: WagoSysProcessorLoad, * (WAGO) Namespace: WagoSysProcessorLoad Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesProcessorLoad Library Identification : Placeholder: WagoTypesProcessorLoad Default Resolution: WagoTypesProcessorLoad, * (WAGO) Namespace: WagoTypesProcessorLoad Library Properties :

### Function Blocks


## FbProcessorLoad (FB)


Provides access to the current processor load.

Provides access to the current processor load. - FbProcessorLoad.IsThreshold1Reached (PROP) - FbProcessorLoad.IsThreshold2Reached (PROP) - FbProcessorLoad.LogLevel (PROP) - FbProcessorLoad.OverloadAction (PROP) - FbProcessorLoad.ProcessorLoad (PROP) - FbProcessorLoad.Reinitialize (METH) - FbProcessorLoad.Threshold1 (PROP) - FbProcessorLoad.Threshold2 (PROP)

### Methods


## FbProcessorLoad.Reinitialize (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Reinitialize | eResultCode |  |
| Input | usiThreshold1 | USINT (0..100) | lower threshold for the processor load rel. to usiIecShare [0-usiThreshold2] |
| usiThreshold2 | USINT (0..100) | upper threshold for the processor load rel. to usiIecShare [usiThreshold1-100] |
| usiIecShare | USINT (1..100) | percentage of the processor share for iec-tasks. [1-100] |
| eOverloadAction | WagoTypesProcessorLoad.eOverloadAction | Reaction in case of overload (i.e. ProcessorLoad >= usiIecShare ). |
| eLogLevel | WagoTypesProcessorLoad.eLogLevel |  |

| result codes | meaning |
| OK | Success |
| EINVAL | Parameter out of range |

Re-initializes the fb.

Interface variables Re-initializes the fb.

### Program Organization


## 20 Program Organization Units


- FbProcessorLoad (FB) FbProcessorLoad.IsThreshold1Reached (PROP) - FbProcessorLoad.IsThreshold2Reached (PROP) - FbProcessorLoad.LogLevel (PROP) - FbProcessorLoad.OverloadAction (PROP) - FbProcessorLoad.ProcessorLoad (PROP) - FbProcessorLoad.Reinitialize (METH) - FbProcessorLoad.Threshold1 (PROP) - FbProcessorLoad.Threshold2 (PROP)

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| Date | Version | Author | Change |
| 18.04.2024 | 2.0.1.3 | u013939 | Comments for Multicore and FW > 26 added |
| 30.10.2023 | 2.0.1.2 | u010663 | SysTypes2Interfaces inserted |
| 17.12.2020 | 2.0.1.1 | u010545 | WAT22866 Limitation ProcessorLoad |
| 08.01.2019 | 2.0.1.0 | u015842 | Properties: free placeholder added |
| 12/08/2016 | 2.0.0.0 | LS | Fix for multiple instances from Fb_Init, fixes Reset Button Problem |
| 04/21/2016 | 1.0.0.2 | JSo | Fix misspelled placeholder and remove unused library references. |
| 06/10/2015 |  | JMü | ADD Placeholder AND resolve libraries with placeholders |
| 08/25/2015 | 1.0.0.1 | JSo | Fix IsThresholdXReached beeing TRUE for lower loads. Fix IsThresholdXReached beeing TRUE when not initialized. Publish all IEC Symbols from WagoTypesProcessorLoad. |
| 07/09/2015 | 1.0.0.0 | JSo | Created |

WagoAppProcessorLoad

### Other Components


## FbProcessorLoad.IsThreshold1Reached (PROP)


Is load above Threshold1 ?

Is load above Threshold1 ?

## FbProcessorLoad.IsThreshold2Reached (PROP)


Is load above Threshold2 ?

Is load above Threshold2 ?

## FbProcessorLoad.LogLevel (PROP) ¶


## FbProcessorLoad.OverloadAction (PROP)


OverloadAction

## FbProcessorLoad.ProcessorLoad (PROP)


Current processor load in percent

Update in FW 27 for multicore systems:

On Multicore systems the return value is modified to represent a significant system load.

To represent this the highest load of all cores is evaluated

Three levels of system load are distinguished:

1: all core loads are below 50% > the average load is resulted 2: highest core load is above 50 % > then medium value between the highest and the average value is the result 3: highest core load is above 75% > the highest core load is resulted

Current processor load in percent NOTE: Update in FW 27 for multicore systems: On Multicore systems the return value is modified to represent a significant system load. To represent this the highest load of all cores is evaluated Three levels of system load are distinguished: 1: all core loads are below 50% > the average load is resulted 2: highest core load is above 50 % > then medium value between the highest and the average value is the result 3: highest core load is above 75% > the highest core load is resulted

## FbProcessorLoad.Threshold1 (PROP)


Threshold1: Lower limit for the processor load

Threshold1: Lower limit for the processor load

## FbProcessorLoad.Threshold2 (PROP)


Threshold2: Upper limit for the processor load

Threshold2: Upper limit for the processor load