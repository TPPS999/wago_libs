# WagoSysProcessorLoad v2.0.1.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysProcessorLoad
- **Version:** 2.0.1.2
- **Categories:** WAGO FunctionalView|Base
- **Namespace:** WagoSysProcessorLoad
- **Author:** WAGO / JSo

### Description ¶


This document is automatically generated.

Provides access to the current cpu load.

This document is automatically generated. Provides access to the current cpu load.

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks - Methods FbSysProcessorLoad.FB_exit (METH) - FbSysProcessorLoad.InitLoad (METH) - FbSysProcessorLoad.Reinitialize (METH) Program Organization Global Variable Lists Other Components

### Indices and tables ¶


Based on WagoSysProcessorLoad.library, last modified 29.05.2024, 20:39:30. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysProcessorLoad.library, last modified 29.05.2024, 20:39:30. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysProcessorLoad Library Documentation


| Company: | WAGO |
| Title: | WagoSysProcessorLoad |
| Version: | 2.0.1.2 |
| Categories: | WAGO FunctionalView\|Base |
| Namespace: | WagoSysProcessorLoad |
| Author: | WAGO / JSo |

### Description


This document is automatically generated.

Provides access to the current cpu load.

This document is automatically generated. Provides access to the current cpu load.

### Contents:


- 20 Program Organization Units FbSysProcessorLoad (FB) VersionHistory (GVL)

### Indices and tables


Based on WagoSysProcessorLoad.library, last modified 29.05.2024, 20:39:30. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysProcessorLoad.library, last modified 29.05.2024, 20:39:30. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysProcessorLoad.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:39:30 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:39:30 |
| NoPlaceholder | string |  |
| Description | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / JSo |
| AutoResolveUnbound | bool | False |
| Released | False |
| Company | string | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysProcessorLoad |
| DefaultNamespace | WagoSysProcessorLoad |
| Version | version | 2.0.1.2 |
| Title | string | WagoSysProcessorLoad |
| LibraryCategories | library-category-list | WAGO FunctionalView\|Base |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. SysTask Library Identification : Placeholder: SysTask Default Resolution: SysTask, * (System) Namespace: SysTask Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesProcessorLoad Library Identification : Placeholder: WagoTypesProcessorLoad Default Resolution: WagoTypesProcessorLoad, * (WAGO) Namespace: WagoTypesProcessorLoad Library Properties :

### Function Blocks


## FbSysProcessorLoad (FB)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Output | usiLoad | USINT | current processor load in percent |

Interface variables - FbSysProcessorLoad.FB_exit (METH) - FbSysProcessorLoad.InitLoad (METH) - FbSysProcessorLoad.Load (PROP) - FbSysProcessorLoad.Reinitialize (METH)

### Methods


## FbSysProcessorLoad.FB_exit (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FB_exit | BOOL |  |
| Input | bInCopyCode | BOOL | if TRUE, the exit method is called for exiting an instance that is copied afterwards (online change). |

## FbSysProcessorLoad.InitLoad (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | bInitRetains | BOOL | if TRUE, the retain variables are initialized (warm start / cold start) |
| bInCopyCode | BOOL | if TRUE, the instance afterwards gets moved into the copy code (online change) |
| udiInterval_us | UDINT | measurement cycle for the cpu load [250000 - ... ] |
| usiThreshold1 | USINT (0..100) | Threshold1 in percent ( 0 <= usiThreshold1 <= usiThreshold2 <= usiIecShare <= 100) |
| usiThreshold2 | USINT (0..100) | Threshold2 in percent ( 0 <= usiThreshold1 <= usiThreshold2 <= usiIecShare <= 100) |
| usiIecShare | USINT (0..100) | Max processor load in percent ( 0 <= usiThreshold1 <= usiThreshold2 <= usiIecShare <= 100) |
| udiOverloadTriggerLevel | UDINT | count of measurment cycles before overload action is triggered. [0 - ..] |
| eOverloadAction | WagoTypesProcessorLoad.eOverloadAction | action in case an overload is detected (i.e. current load is equal or above usiIecShare ) |
| bHandleOverloadEvent | BOOL |  |
| eLogLevel | WagoTypesProcessorLoad.eLogLevel |  |

## FbSysProcessorLoad.Reinitialize (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Reinitialize | eResultCode |  |
| Input | udiInterval_us | UDINT | measurement cycle for the cpu load |
| usiThreshold1 | USINT (1..100) | value for _usiThreshold1 |
| usiThreshold2 | USINT (1..100) | value for _usiThreshold2 |
| usiIecShare | USINT (0..100) | value for _usiIecShare |
| udiOverloadTriggerLevel | UDINT | count of measurment cycles before overload action is triggered. |
| eOverloadAction | WagoTypesProcessorLoad.eOverloadAction | action in case an overload is detected (i.e. current load is equal or above iecShare) |
| bHandleOverloadEvent | BOOL |  |
| eLogLevel | WagoTypesProcessorLoad.eLogLevel |  |

### Program Organization


## 20 Program Organization Units


- FbSysProcessorLoad (FB) FbSysProcessorLoad.FB_exit (METH) - FbSysProcessorLoad.InitLoad (METH) - FbSysProcessorLoad.Load (PROP) - FbSysProcessorLoad.Reinitialize (METH)

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| Date | Version | Author | Change |
| 05.03.2024 | 2.0.1.2 | WAGO / u013972 | Internal changes |
| 30.01.2018 | 2.0.1.1 | WAGO / u013972 | Internal changes |
| 12/08/2016 | 2.0.0.0 | LS | Fix for multiple instances from Fb_Init, fixes Reset Button Problem |
| 04/21/2016 | 1.0.0.1 | JSo | Remove unused library references |
| 06/10/2015 |  | JMü | ADD Placeholder AND resolve libraries with placeholders |
| 07/09/2015 | 1.0.0.0 | JSo | Created |

WagoSysProcessorLoad

### Other Components


## FbSysProcessorLoad.Load (PROP) ¶
