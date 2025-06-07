# WagoSysKbusModule v1.8.6.4 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysKbusModule
- **Version:** 1.8.6.4
- **Categories:** WAGO LayerView|Sys; Application
- **Author:** WAGO / u010545
- **Placeholder:** WagoSysKbusModule

### Description ¶


This document is automatically generated.

Base Functionblocks for Module Access via Kbus

This document is automatically generated. Base Functionblocks for Module Access via Kbus

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks FbModuleMbx1 (FB) - FbModuleMbx2 (FB) - FbModuleMbx2Ext (FB) - FbModuleParameter (FB) - FbModuleParameterMbx1 (FB) - FbModuleParameterMbx2 (FB) - FbModuleProcessInputs (FB) - FbModuleProcessInputsOutputs (FB) - FbModuleProcessOutputs (FB) - FbModuleRegister (FB) - ... and 53 more Internal Components Global Variable Lists Other Components - 20 KBus_AutoModule (TYP 1) - 21 KBus_AutoModule (TYP 2) - 750 - 750 - 753 - 75x - 75x - Module_753_163x - Module_75x_48x - Module_75x_49x - ... and 2 more

### Indices and tables ¶


Based on WagoSysKbusModule.library, last modified 29.05.2024, 20:28:39. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysKbusModule.library, last modified 29.05.2024, 20:28:39. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysKbusModule Library Documentation


| Company: | WAGO |
| Title: | WagoSysKbusModule |
| Version: | 1.8.6.4 |
| Categories: | WAGO LayerView\|Sys; Application |
| Author: | WAGO / u010545 |
| Placeholder: | WagoSysKbusModule |

### Description


This document is automatically generated.

Base Functionblocks for Module Access via Kbus

This document is automatically generated. Base Functionblocks for Module Access via Kbus

### Contents:


- 20 KBus_AutoModule (TYP 1) 750 - 753 - 75x 21 KBus_AutoModule (TYP 2) - 750 - 75x 22 KBus_InternalModule - FbModuleMbx1 (FB) - FbModuleMbx2 (FB) - FbModuleMbx2Ext (FB) - FbModuleParameter (FB) - FbModuleParameterMbx1 (FB) - FbModuleParameterMbx2 (FB) - FbModuleProcessInputs (FB) - FbModuleProcessInputsOutputs (FB) - FbModuleProcessOutputs (FB) - FbModuleRegister (FB) VersionHistory (GVL)

### Indices and tables


Based on WagoSysKbusModule.library, last modified 29.05.2024, 20:28:39. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysKbusModule.library, last modified 29.05.2024, 20:28:39. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysKbusModule.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:28:42 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:28:39 |
| Description | string | See: Description |
| Copyright | © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u010545 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysKbusModule |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysKbusModule |
| DefaultNamespace |  |
| Version | version | 1.8.6.4 |
| Title | string | WagoSysKbusModule |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False PublishSymbolsInContainer: True | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CmpEventMgr Library Identification : Placeholder: CmpEventMgr Default Resolution: CmpEventMgr, * (System) Namespace: CmpEventMgr Library Properties : IoStandard Library Identification : Placeholder: IoStandard Default Resolution: IoStandard, * (System) Namespace: IoStandard Library Properties : Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : WagoSysKbusServices Library Identification : Placeholder: WagoSysKbusServices Default Resolution: WagoSysKbusServices, * (WAGO) Namespace: WagoSysKbusServices Library Properties : WagoSysModuleBase Library Identification : Placeholder: WagoSysModuleBase Default Resolution: WagoSysModuleBase, * (WAGO) Namespace: WagoSysModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX_OUTPUT_SIZE = 47 Parameter: MAX_MODULE_QUANTITY = 250 Parameter: MAX_MODULE_INPUT_SIZE = 48 Parameter: MAX_RUNNABLES = MAX_MODULE_QUANTITY Parameter: MBX_PIPE_SIZE = 1024 Parameter: MAX_MODULE_OUTPUT_SIZE = 48 Parameter: MAX_MBX_INPUT_SIZE = 47 WagoSysModule_750_450 Library Identification : Placeholder: WagoSysModule_750_450 Default Resolution: WagoSysModule_750_450, * (WAGO) Namespace: WagoSysModule_750_450 Library Properties : WagoSysModule_750_451 Library Identification : Placeholder: WagoSysModule_750_451 Default Resolution: WagoSysModule_750_451, * (WAGO) Namespace: WagoSysModule_750_451 Library Properties : WagoSysModule_750_463 Library Identification : Placeholder: WagoSysModule_750_463 Default Resolution: WagoSysModule_750_463, * (WAGO) Namespace: WagoSysModule_750_463 Library Properties : WagoSysModule_750_464 Library Identification : Placeholder: WagoSysModule_750_464 Default Resolution: WagoSysModule_750_464, * (WAGO) Namespace: WagoSysModule_750_464 Library Properties : WagoSysModule_750_630 Library Identification : Placeholder: WagoSysModule_750_630 Default Resolution: WagoSysModule_750_630, * (WAGO) Namespace: WagoSysModule_750_630 Library Properties : WagoSysModule_750_636 Library Identification : Placeholder: WagoSysModule_750_636 Default Resolution: WagoSysModule_750_636, * (WAGO) Namespace: WagoSysModule_750_636 Library Properties : WagoSysModule_750_642 Library Identification : Placeholder: WagoSysModule_750_642 Default Resolution: WagoSysModule_750_642, * (WAGO) Namespace: WagoSysModule_750_642 Library Properties : WagoSysModule_750_643 Library Identification : Placeholder: WagoSysModule_750_643 Default Resolution: WagoSysModule_750_643, * (WAGO) Namespace: WagoSysModule_750_643 Library Properties : WagoSysModule_753_163x Library Identification : Placeholder: WagoSysModule_753_163x Default Resolution: WagoSysModule_753_163x, * (WAGO) Namespace: WagoSysModule_753_163x Library Properties : WagoSysModule_753_646 Library Identification : Placeholder: WagoSysModule_753_646 Default Resolution: WagoSysModule_753_646, * (WAGO) Namespace: WagoSysModule_753_646 Library Properties : WagoSysModule_753_647 Library Identification : Placeholder: WagoSysModule_753_647 Default Resolution: WagoSysModule_753_647, * (WAGO) Namespace: WagoSysModule_753_647 Library Properties : Library Parameter : Parameter: DEBUG_MODE = FALSE WagoSysModule_753_649 Library Identification : Placeholder: WagoSysModule_753_649 Default Resolution: WagoSysModule_753_649, * (WAGO) Namespace: WagoSysModule_753_649 Library Properties : WagoSysModule_75x_1491 Library Identification : Placeholder: WagoSysModule_75x_1491 Default Resolution: WagoSysModule_75x_1491, * (WAGO) Namespace: WagoSysModule_75x_1491 Library Properties : WagoSysModule_75x_1632 Library Identification : Placeholder: WagoSysModule_75x_1632 Default Resolution: WagoSysModule_75x_1632, * (WAGO) Namespace: WagoSysModule_75x_1632 Library Properties : WagoSysModule_75x_1657 Library Identification : Placeholder: WagoSysModule_75x_1657 Default Resolution: WagoSysModule_75x_1657, * (WAGO) Namespace: WagoSysModule_75x_1657 Library Properties : Library Parameter : Parameter: MAX_MBX2 = 4 WagoSysModule_75x_458 Library Identification : Placeholder: WagoSysModule_75x_458 Default Resolution: WagoSysModule_75x_458, * (WAGO) Namespace: WagoSysModule_75x_458 Library Properties : WagoSysModule_75x_461 Library Identification : Placeholder: WagoSysModule_75x_461 Default Resolution: WagoSysModule_75x_461, * (WAGO) Namespace: WagoSysModule_75x_461 Library Properties : WagoSysModule_75x_469 Library Identification : Placeholder: WagoSysModule_75x_469 Default Resolution: WagoSysModule_75x_469, * (WAGO) Namespace: WagoSysModule_75x_469 Library Properties : WagoSysModule_75x_471 Library Identification : Placeholder: WagoSysModule_75x_471 Default Resolution: WagoSysModule_75x_471, * (WAGO) Namespace: WagoSysModule_75x_471 Library Properties : WagoSysModule_75x_481 Library Identification : Placeholder: WagoSysModule_75x_481 Default Resolution: WagoSysModule_75x_481, * (WAGO) Namespace: WagoSysModule_75x_481 Library Properties : WagoSysModule_75x_486 Library Identification : Placeholder: WagoSysModule_75x_486 Default Resolution: WagoSysModule_75x_486, * (WAGO) Namespace: WagoSysModule_75x_486 Library Properties : WagoSysModule_75x_487 Library Identification : Placeholder: WagoSysModule_75x_487 Default Resolution: WagoSysModule_75x_487, * (WAGO) Namespace: WagoSysModule_75x_487 Library Properties : WagoSysModule_75x_489 Library Identification : Placeholder: WagoSysModule_75x_489 Default Resolution: WagoSysModule_75x_489, * (WAGO) Namespace: WagoSysModule_75x_489 Library Properties : WagoSysModule_75x_48x Library Identification : Placeholder: WagoSysModule_75x_48x Default Resolution: WagoSysModule_75x_48x, * (WAGO) Namespace: WagoSysModule_75x_48x Library Properties : WagoSysModule_75x_496 Library Identification : Placeholder: WagoSysModule_75x_496 Default Resolution: WagoSysModule_75x_496, * (WAGO) Namespace: WagoSysModule_75x_496 Library Properties : WagoSysModule_75x_497 Library Identification : Placeholder: WagoSysModule_75x_497 Default Resolution: WagoSysModule_75x_497, * (WAGO) Namespace: WagoSysModule_75x_497 Library Properties : WagoSysModule_75x_498 Library Identification : Placeholder: WagoSysModule_75x_498 Default Resolution: WagoSysModule_75x_498, * (WAGO) Namespace: WagoSysModule_75x_498 Library Properties : WagoSysModule_75x_49x Library Identification : Placeholder: WagoSysModule_75x_49x Default Resolution: WagoSysModule_75x_49x, * (WAGO) Namespace: WagoSysModule_75x_49x Library Properties : WagoSysModule_75x_511 Library Identification : Placeholder: WagoSysModule_75x_511 Default Resolution: WagoSysModule_75x_511, * (WAGO) Namespace: WagoSysModule_75x_511 Library Properties : WagoSysModule_75x_562 Library Identification : Placeholder: WagoSysModule_75x_562 Default Resolution: WagoSysModule_75x_562, * (WAGO) Namespace: WagoSysModule_75x_562 Library Properties : WagoSysModule_75x_563 Library Identification : Placeholder: WagoSysModule_75x_563 Default Resolution: WagoSysModule_75x_563, * (WAGO) Namespace: WagoSysModule_75x_563 Library Properties : WagoSysModule_75x_564 Library Identification : Placeholder: WagoSysModule_75x_564 Default Resolution: WagoSysModule_75x_564, * (WAGO) Namespace: WagoSysModule_75x_564 Library Properties : WagoSysModule_75x_597 Library Identification : Placeholder: WagoSysModule_75x_597 Default Resolution: WagoSysModule_75x_597, * (WAGO) Namespace: WagoSysModule_75x_597 Library Properties : WagoSysModule_75x_632 Library Identification : Placeholder: WagoSysModule_75x_632 Default Resolution: WagoSysModule_75x_632, * (WAGO) Namespace: WagoSysModule_75x_632 Library Properties : WagoSysModule_75x_633 Library Identification : Placeholder: WagoSysModule_75x_633 Default Resolution: WagoSysModule_75x_633, * (WAGO) Namespace: WagoSysModule_75x_633 Library Properties : WagoSysModule_75x_635 Library Identification : Placeholder: WagoSysModule_75x_635 Default Resolution: WagoSysModule_75x_635, * (WAGO) Namespace: WagoSysModule_75x_635 Library Properties : WagoSysModule_75x_640 Library Identification : Placeholder: WagoSysModule_75x_640 Default Resolution: WagoSysModule_75x_640, * (WAGO) Namespace: WagoSysModule_75x_640 Library Properties : WagoSysModule_75x_644 Library Identification : Placeholder: WagoSysModule_75x_644 Default Resolution: WagoSysModule_75x_644, * (WAGO) Namespace: WagoSysModule_75x_644 Library Properties : WagoSysModule_75x_645 Library Identification : Placeholder: WagoSysModule_75x_645 Default Resolution: WagoSysModule_75x_645, * (WAGO) Namespace: WagoSysModule_75x_645 Library Properties : WagoSysModule_75x_655 Library Identification : Placeholder: WagoSysModule_75x_655 Default Resolution: WagoSysModule_75x_655, * (WAGO) Namespace: WagoSysModule_75x_655 Library Properties : WagoSysModule_75x_657 Library Identification : Placeholder: WagoSysModule_75x_657 Default Resolution: WagoSysModule_75x_657, * (WAGO) Namespace: WagoSysModule_75x_657 Library Properties : Library Parameter : Parameter: MAX_MBX2 = 4 WagoSysModule_75x_658 Library Identification : Placeholder: WagoSysModule_75x_658 Default Resolution: WagoSysModule_75x_658, * (WAGO) Namespace: WagoSysModule_75x_658 Library Properties : Library Parameter : Parameter: CAN_CONFIG_TIMEOUT = TIME#8s0ms Parameter: CAN_DIAG_BUFFER = 10 Parameter: SDO_WATCHDOG_DEFAULT = TIME#500ms Parameter: MAX_MESSAGES_METHOD_OPEN = 100 WagoSysModule_75x_65x Library Identification : Placeholder: WagoSysModule_75x_65x Default Resolution: WagoSysModule_75x_65x, * (WAGO) Namespace: WagoSysModule_75x_65x Library Properties : Library Parameter : Parameter: MAX_PIPE_SIZE = 1024 WagoSysModule_75x_66x Library Identification : Placeholder: WagoSysModule_75x_66x Default Resolution: WagoSysModule_75x_66x, * (WAGO) Namespace: WagoSysModule_75x_66x Library Properties : WagoSysModule_75x_677 Library Identification : Placeholder: WagoSysModule_75x_677 Default Resolution: WagoSysModule_75x_677, * (WAGO) Namespace: WagoSysModule_75x_677 Library Properties : WagoSysModule_75x_67x Library Identification : Placeholder: WagoSysModule_75x_67x Default Resolution: WagoSysModule_75x_67x, * (WAGO) Namespace: WagoSysModule_75x_67x Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesBusServices Library Identification : Placeholder: WagoTypesBusServices Default Resolution: WagoTypesBusServices, * (WAGO) Namespace: WagoTypesBusServices Library Properties : WagoTypesCom Library Identification : Placeholder: WagoTypesCom Default Resolution: WagoTypesCom, * (WAGO) Namespace: WagoTypesCom Library Properties : WagoTypesKbusTerminalControl Library Identification : Placeholder: WagoTypesKbusTerminalControl Default Resolution: WagoTypesKbusTerminalControl, * (WAGO) Namespace: WagoTypesKbusTerminalControl Library Properties : WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX_OUTPUT_SIZE = 47 Parameter: MAX_MODULE_INPUT_SIZE = 48 Parameter: MBX_PIPE_SIZE = 1024 Parameter: MAX_MBX1_SIZE = 18 Parameter: MAX_MODULE_OUTPUT_SIZE = 48 Parameter: MAX_MBX_INPUT_SIZE = 47 WagoTypesModule_750_450 Library Identification : Placeholder: WagoTypesModule_750_450 Default Resolution: WagoTypesModule_750_450, * (WAGO) Namespace: WagoTypesModule_750_450 Library Properties : WagoTypesModule_750_451 Library Identification : Placeholder: WagoTypesModule_750_451 Default Resolution: WagoTypesModule_750_451, * (WAGO) Namespace: WagoTypesModule_750_451 Library Properties : WagoTypesModule_750_463 Library Identification : Placeholder: WagoTypesModule_750_463 Default Resolution: WagoTypesModule_750_463, * (WAGO) Namespace: WagoTypesModule_750_463 Library Properties : WagoTypesModule_750_464 Library Identification : Placeholder: WagoTypesModule_750_464 Default Resolution: WagoTypesModule_750_464, * (WAGO) Namespace: WagoTypesModule_750_464 Library Properties : WagoTypesModule_750_630 Library Identification : Placeholder: WagoTypesModule_750_630 Default Resolution: WagoTypesModule_750_630, * (WAGO) Namespace: WagoTypesModule_750_630 Library Properties : WagoTypesModule_750_636 Library Identification : Placeholder: WagoTypesModule_750_636 Default Resolution: WagoTypesModule_750_636, * (WAGO) Namespace: WagoTypesModule_750_636 Library Properties : WagoTypesModule_750_642 Library Identification : Placeholder: WagoTypesModule_750_642 Default Resolution: WagoTypesModule_750_642, * (WAGO) Namespace: WagoTypesModule_750_642 Library Properties : WagoTypesModule_750_643 Library Identification : Placeholder: WagoTypesModule_750_643 Default Resolution: WagoTypesModule_750_643, * (WAGO) Namespace: WagoTypesModule_750_643 Library Properties : WagoTypesModule_753_163x Library Identification : Placeholder: WagoTypesModule_753_163x Default Resolution: WagoTypesModule_753_163x, * (WAGO) Namespace: WagoTypesModule_753_163x Library Properties : WagoTypesModule_753_646 Library Identification : Placeholder: WagoTypesModule_753_646 Default Resolution: WagoTypesModule_753_646, * (WAGO) Namespace: WagoTypesModule_753_646 Library Properties : WagoTypesModule_753_647 Library Identification : Placeholder: WagoTypesModule_753_647 Default Resolution: WagoTypesModule_753_647, * (WAGO) Namespace: WagoTypesModule_753_647 Library Properties : Library Parameter : Parameter: GP_MAXRESPONSEDATA = 70 Parameter: GP_MAXRESPONSES = 2 WagoTypesModule_753_649 Library Identification : Placeholder: WagoTypesModule_753_649 Default Resolution: WagoTypesModule_753_649, * (WAGO) Namespace: WagoTypesModule_753_649 Library Properties : WagoTypesModule_75x_1491 Library Identification : Placeholder: WagoTypesModule_75x_1491 Default Resolution: WagoTypesModule_75x_1491, * (WAGO) Namespace: WagoTypesModule_75x_1491 Library Properties : WagoTypesModule_75x_1632 Library Identification : Placeholder: WagoTypesModule_75x_1632 Default Resolution: WagoTypesModule_75x_1632, * (WAGO) Namespace: WagoTypesModule_75x_1632 Library Properties : WagoTypesModule_75x_1657 Library Identification : Placeholder: WagoTypesModule_75x_1657 Default Resolution: WagoTypesModule_75x_1657, * (WAGO) Namespace: WagoTypesModule_75x_1657 Library Properties : WagoTypesModule_75x_458 Library Identification : Placeholder: WagoTypesModule_75x_458 Default Resolution: WagoTypesModule_75x_458, * (WAGO) Namespace: WagoTypesModule_75x_458 Library Properties : WagoTypesModule_75x_461 Library Identification : Placeholder: WagoTypesModule_75x_461 Default Resolution: WagoTypesModule_75x_461, * (WAGO) Namespace: WagoTypesModule_75x_461 Library Properties : WagoTypesModule_75x_469 Library Identification : Placeholder: WagoTypesModule_75x_469 Default Resolution: WagoTypesModule_75x_469, * (WAGO) Namespace: WagoTypesModule_75x_469 Library Properties : WagoTypesModule_75x_471 Library Identification : Placeholder: WagoTypesModule_75x_471 Default Resolution: WagoTypesModule_75x_471, * (WAGO) Namespace: WagoTypesModule_75x_471 Library Properties : WagoTypesModule_75x_481 Library Identification : Placeholder: WagoTypesModule_75x_481 Default Resolution: WagoTypesModule_75x_481, * (WAGO) Namespace: WagoTypesModule_75x_481 Library Properties : WagoTypesModule_75x_486 Library Identification : Placeholder: WagoTypesModule_75x_486 Default Resolution: WagoTypesModule_75x_486, * (WAGO) Namespace: WagoTypesModule_75x_486 Library Properties : WagoTypesModule_75x_487 Library Identification : Placeholder: WagoTypesModule_75x_487 Default Resolution: WagoTypesModule_75x_487, * (WAGO) Namespace: WagoTypesModule_75x_487 Library Properties : WagoTypesModule_75x_489 Library Identification : Placeholder: WagoTypesModule_75x_489 Default Resolution: WagoTypesModule_75x_489, * (WAGO) Namespace: WagoTypesModule_75x_489 Library Properties : WagoTypesModule_75x_48x Library Identification : Placeholder: WagoTypesModule_75x_48x Default Resolution: WagoTypesModule_75x_48x, * (WAGO) Namespace: WagoTypesModule_75x_48x Library Properties : WagoTypesModule_75x_496 Library Identification : Placeholder: WagoTypesModule_75x_496 Default Resolution: WagoTypesModule_75x_496, * (WAGO) Namespace: WagoTypesModule_75x_496 Library Properties : WagoTypesModule_75x_497 Library Identification : Placeholder: WagoTypesModule_75x_497 Default Resolution: WagoTypesModule_75x_497, * (WAGO) Namespace: WagoTypesModule_75x_497 Library Properties : WagoTypesModule_75x_498 Library Identification : Placeholder: WagoTypesModule_75x_498 Default Resolution: WagoTypesModule_75x_498, * (WAGO) Namespace: WagoTypesModule_75x_498 Library Properties : WagoTypesModule_75x_49x Library Identification : Placeholder: WagoTypesModule_75x_49x Default Resolution: WagoTypesModule_75x_49x, * (WAGO) Namespace: WagoTypesModule_75x_49x Library Properties : WagoTypesModule_75x_511 Library Identification : Placeholder: WagoTypesModule_75x_511 Default Resolution: WagoTypesModule_75x_511, * (WAGO) Namespace: WagoTypesModule_75x_511 Library Properties : WagoTypesModule_75x_562 Library Identification : Placeholder: WagoTypesModule_75x_562 Default Resolution: WagoTypesModule_75x_562, * (WAGO) Namespace: WagoTypesModule_75x_562 Library Properties : WagoTypesModule_75x_563 Library Identification : Placeholder: WagoTypesModule_75x_563 Default Resolution: WagoTypesModule_75x_563, * (WAGO) Namespace: WagoTypesModule_75x_563 Library Properties : WagoTypesModule_75x_564 Library Identification : Placeholder: WagoTypesModule_75x_564 Default Resolution: WagoTypesModule_75x_564, * (WAGO) Namespace: WagoTypesModule_75x_564 Library Properties : WagoTypesModule_75x_597 Library Identification : Placeholder: WagoTypesModule_75x_597 Default Resolution: WagoTypesModule_75x_597, * (WAGO) Namespace: WagoTypesModule_75x_597 Library Properties : WagoTypesModule_75x_632 Library Identification : Placeholder: WagoTypesModule_75x_632 Default Resolution: WagoTypesModule_75x_632, * (WAGO) Namespace: WagoTypesModule_75x_632 Library Properties : WagoTypesModule_75x_633 Library Identification : Placeholder: WagoTypesModule_75x_633 Default Resolution: WagoTypesModule_75x_633, * (WAGO) Namespace: WagoTypesModule_75x_633 Library Properties : WagoTypesModule_75x_635 Library Identification : Placeholder: WagoTypesModule_75x_635 Default Resolution: WagoTypesModule_75x_635, * (WAGO) Namespace: WagoTypesModule_75x_635 Library Properties : WagoTypesModule_75x_640 Library Identification : Placeholder: WagoTypesModule_75x_640 Default Resolution: WagoTypesModule_75x_640, * (WAGO) Namespace: WagoTypesModule_75x_640 Library Properties : WagoTypesModule_75x_644 Library Identification : Placeholder: WagoTypesModule_75x_644 Default Resolution: WagoTypesModule_75x_644, * (WAGO) Namespace: WagoTypesModule_75x_644 Library Properties : WagoTypesModule_75x_645 Library Identification : Placeholder: WagoTypesModule_75x_645 Default Resolution: WagoTypesModule_75x_645, * (WAGO) Namespace: WagoTypesModule_75x_645 Library Properties : WagoTypesModule_75x_655 Library Identification : Placeholder: WagoTypesModule_75x_655 Default Resolution: WagoTypesModule_75x_655, * (WAGO) Namespace: WagoTypesModule_75x_655 Library Properties : WagoTypesModule_75x_657 Library Identification : Placeholder: WagoTypesModule_75x_657 Default Resolution: WagoTypesModule_75x_657, * (WAGO) Namespace: WagoTypesModule_75x_657 Library Properties : WagoTypesModule_75x_658 Library Identification : Placeholder: WagoTypesModule_75x_658 Default Resolution: WagoTypesModule_75x_658, * (WAGO) Namespace: WagoTypesModule_75x_658 Library Properties : Library Parameter : Parameter: CAN_RX_MAX_MESSAGES = 100 Parameter: CAN_TX_MAX_MESSAGES = 100 WagoTypesModule_75x_65x Library Identification : Placeholder: WagoTypesModule_75x_65x Default Resolution: WagoTypesModule_75x_65x, * (WAGO) Namespace: WagoTypesModule_75x_65x Library Properties : WagoTypesModule_75x_66x Library Identification : Placeholder: WagoTypesModule_75x_66x Default Resolution: WagoTypesModule_75x_66x, * (WAGO) Namespace: WagoTypesModule_75x_66x Library Properties : WagoTypesModule_75x_677 Library Identification : Placeholder: WagoTypesModule_75x_677 Default Resolution: WagoTypesModule_75x_677, * (WAGO) Namespace: WagoTypesModule_75x_677 Library Properties : WagoTypesModule_75x_67x Library Identification : Placeholder: WagoTypesModule_75x_67x Default Resolution: WagoTypesModule_75x_67x, * (WAGO) Namespace: WagoTypesModule_75x_67x Library Properties :

### Function Blocks


## FbModuleMbx1 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModuleMbx2 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

## FbModuleMbx2Ext (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

## FbModuleParameter (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModuleParameterMbx1 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModuleParameterMbx2 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

## FbModuleProcessInputs (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModuleProcessInputsOutputs (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModuleProcessOutputs (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModuleRegister (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_750_450 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_750_451 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_750_463 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_750_464 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_750_630 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_750_636 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_750_642 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_750_643 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_753_163x (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

## FbModule_753_646 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_753_647 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

## FbModule_753_649 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

## FbModule_75x_1491 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_1632 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

## FbModule_75x_1652 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_1657 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

## FbModule_75x_458 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_461 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_469 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_471 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_481 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_482 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_484 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_486 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_487 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_489 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_493 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_494 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_495 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_496 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_497 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_511 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_562 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_563 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_564 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_597 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_632 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

## FbModule_75x_633 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_635 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_640 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| todLocalTime | TOD |  | FbModule_75x_640 |
| dLocalDate | DATE |  | FbModule_75x_640 |
| dtUTC_Time | DT |  | FbModule_75x_640 |
| bWeekday | BYTE |  | FbModule_75x_640 |
| dwChannelFlags | DWORD |  | FbModule_75x_640 |
| dwServiceFlags | DWORD |  | FbModule_75x_640 |
| dwDiagnostic | DWORD |  | FbModule_75x_640 |
| dwAuto | DWORD | — configuration ————————– | FbModule_75x_640 |
| diTimeZone | DINT | +/- [sec] | FbModule_75x_640 |
| diDstBias | DINT | +/- [sec] | FbModule_75x_640 |
| dwAntenna | DWORD |  | FbModule_75x_640 |
| aTimer | ARRAY [0..RTC_QUANTITY_TIMER] OF typRtcConfigTimer |  | FbModule_75x_640 |
| aOperating_Hours | ARRAY [0..RTC_QUANTITY_OPERATING_HOURS_COUNTER] OF typRtcOperatingHours |  | FbModule_75x_640 |

## FbModule_75x_644 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_645 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_650 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_651 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_652 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_653 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_655 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_657 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

## FbModule_75x_658 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

## FbModule_75x_666 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_667 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_677 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

## FbModule_75x_67x (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

### Internal Components


## 22 KBus_InternalModule


- FbModuleMbx1 (FB) - FbModuleMbx2 (FB) - FbModuleMbx2Ext (FB) - FbModuleParameter (FB) - FbModuleParameterMbx1 (FB) - FbModuleParameterMbx2 (FB) - FbModuleProcessInputs (FB) - FbModuleProcessInputsOutputs (FB) - FbModuleProcessOutputs (FB) - FbModuleRegister (FB)

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 05.02.2024 | 1.8.6.4 | u0103719 | WAT36347: set new PA-Struct for FW23 modules (75x_677) + rename 750_511 to 75x_511 |
| 05.02.2024 | 1.8.6.3 | u0103719 | Compiled with SP16.3 |
| 19.01.2024 | 1.8.6.2 | u0103719 | WAT36293: set new PA-Struct for FW23 modules (75x_493,75x_645,75x_511,75x_633,75x_645) |
| 27.11.2023 | 1.8.6.1 | u0103719 | add 75x_66x (75x_666,75x_667) |
| 31.07.2023 | 1.8.6.0 | u0103719 | add 75x_666 |
| 24.04.2023 | 1.8.5.1 | u010663 | add 75x_667 |
| 27.06.2022 | 1.8.5.0 | u0103719 | add 75x_1632,75x_1657 |
| 14.12.2021 | 1.8.4.4 | u010545 | Update for 1652 |
| 13.08.2021 | 1.8.4.3 | u010545 | WAT33584 bugfix 672 at dyn. config. |
| 08.07.2021 | 1.8.4.2 | u010545 | 75x-489 added |
| 01.07.2021 | 1.8.4.1 | u010545 | bugfix library manager |
| 20.04.2021 | 1.8.4.0 | u010545 | 75x-677 / 75x-1652 added as empty base template |
| 25.11.2020 | 1.8.3.2 | u010545 | 75x_1491 bugfix -> dyn. config |
| 19.05.2020 | 1.8.3.1 | u010545 | 75x_1491 implemented |
| 23.09.2019 | 1.8.3.0 | u010545 | Struct 511, 633, 636, 645, 67x modified |
| 09.05.2019 | 1.8.2.2 | u010663 | 75x-564 added |
| 14.03.2019 | 1.8.2.1 | u010545 | 75x-482 / 75x-484 added -> 48x obsolete |
| 08.01.2019 | 1.8.2.0 | u015842 | Properties: free placeholder added |
| 09.04.2018 | 1.8.1.9 | u010545 | 75x-458 / 75x-486 / 75x-562 / 75x-633 added |
| 21.02.2018 | 1.8.1.8 | u010545 | 75x-563 / 75x-597 added |
| 15.02.2018 | 1.8.1.7 | u010545 | Bugfix library manager |
| 08.02.2018 | 1.8.1.6 | u010545 | 75x-496 / 75x-497 added |
| 14.12.2017 | 1.8.1.5 | u013972 | Remove WagoSysOsFuse_Internal_PFC |
| 30.11.2017 | 1.8.1.4 | u010545 | 75x-471 added |
| 14.10.2017 | 1.8.1.3 | u010545 | update placeholder |
| 13.10.2017 | 1.8.1.2 | u010545 | additional modules |
| 20.09.2017 | 1.8.1.1 | u010545 | WagoSysModule_750_511 changed to WagoSysModule_75x_511 |
| 03.03.2017 | 1.8.1.0 | u010545 | I_Fuse supported / AutoInitialize removed |
| 24.07.2017 | 1.8.0.2 | u010545 | additional modules |
| 20.07.2017 | 1.8.0.1 | u010545 | refactoríng SetModuleAccessService to SetModuleBaseAccessService |
| 03.07.2017 | 1.8.0.0 | u010545 | AutoInitialize updated for splitt WagoSysModuleBase |
| 08.05.2017 | 1.7.0.1 | u010545 | Kbus_InternalModules implemented |
| 24.04.2017 | 1.7.0.0 | u010545 | first release |
| 20.02.2017 | 0.0.0.1 | u010545 | created |

WagoSysKbusModule

### Other Components


## 20 KBus_AutoModule (TYP 1)


- 750 FbModule_750_636 (FB) - FbModule_750_642 (FB) - FbModule_750_643 (FB) 753 - FbModule_753_646 (FB) - FbModule_753_647 (FB) - FbModule_753_649 (FB) - Module_753_163x FbModule_753_163x (FB) 75x - FbModule_75x_1632 (FB) - FbModule_75x_1657 (FB) - FbModule_75x_632 (FB) - FbModule_75x_635 (FB) - FbModule_75x_640 (FB) - FbModule_75x_644 (FB) - FbModule_75x_645 (FB) - FbModule_75x_655 (FB) - FbModule_75x_657 (FB) - FbModule_75x_658 (FB) - FbModule_75x_666 (FB) - FbModule_75x_667 (FB) - Module_75x_48x FbModule_75x_482 (FB) - FbModule_75x_484 (FB) Module_75x_49x - FbModule_75x_493 (FB) - FbModule_75x_494 (FB) - FbModule_75x_495 (FB) Module_75x_65x - FbModule_75x_1652 (FB) - FbModule_75x_650 (FB) - FbModule_75x_651 (FB) - FbModule_75x_652 (FB) - FbModule_75x_653 (FB) Module_75x_67x - FbModule_75x_67x (FB)

## 21 KBus_AutoModule (TYP 2)


- 750 FbModule_750_450 (FB) - FbModule_750_451 (FB) - FbModule_750_463 (FB) - FbModule_750_464 (FB) - FbModule_750_630 (FB) 75x - FbModule_75x_1491 (FB) - FbModule_75x_458 (FB) - FbModule_75x_461 (FB) - FbModule_75x_469 (FB) - FbModule_75x_471 (FB) - FbModule_75x_481 (FB) - FbModule_75x_486 (FB) - FbModule_75x_487 (FB) - FbModule_75x_489 (FB) - FbModule_75x_496 (FB) - FbModule_75x_497 (FB) - FbModule_75x_511 (FB) - FbModule_75x_562 (FB) - FbModule_75x_563 (FB) - FbModule_75x_564 (FB) - FbModule_75x_597 (FB) - FbModule_75x_633 (FB) - FbModule_75x_677 (FB)

## 750


- FbModule_750_636 (FB) - FbModule_750_642 (FB) - FbModule_750_643 (FB)

## 750


- FbModule_750_450 (FB) - FbModule_750_451 (FB) - FbModule_750_463 (FB) - FbModule_750_464 (FB) - FbModule_750_630 (FB)

## 753


- FbModule_753_646 (FB) - FbModule_753_647 (FB) - FbModule_753_649 (FB) - Module_753_163x FbModule_753_163x (FB)

## 75x


- FbModule_75x_1632 (FB) - FbModule_75x_1657 (FB) - FbModule_75x_632 (FB) - FbModule_75x_635 (FB) - FbModule_75x_640 (FB) - FbModule_75x_644 (FB) - FbModule_75x_645 (FB) - FbModule_75x_655 (FB) - FbModule_75x_657 (FB) - FbModule_75x_658 (FB) - FbModule_75x_666 (FB) - FbModule_75x_667 (FB) - Module_75x_48x FbModule_75x_482 (FB) - FbModule_75x_484 (FB) Module_75x_49x - FbModule_75x_493 (FB) - FbModule_75x_494 (FB) - FbModule_75x_495 (FB) Module_75x_65x - FbModule_75x_1652 (FB) - FbModule_75x_650 (FB) - FbModule_75x_651 (FB) - FbModule_75x_652 (FB) - FbModule_75x_653 (FB) Module_75x_67x - FbModule_75x_67x (FB)

## 75x


- FbModule_75x_1491 (FB) - FbModule_75x_458 (FB) - FbModule_75x_461 (FB) - FbModule_75x_469 (FB) - FbModule_75x_471 (FB) - FbModule_75x_481 (FB) - FbModule_75x_486 (FB) - FbModule_75x_487 (FB) - FbModule_75x_489 (FB) - FbModule_75x_496 (FB) - FbModule_75x_497 (FB) - FbModule_75x_511 (FB) - FbModule_75x_562 (FB) - FbModule_75x_563 (FB) - FbModule_75x_564 (FB) - FbModule_75x_597 (FB) - FbModule_75x_633 (FB) - FbModule_75x_677 (FB)

## Module_753_163x ¶


- FbModule_753_163x (FB)

## Module_75x_48x


- FbModule_75x_482 (FB) - FbModule_75x_484 (FB)

## Module_75x_49x


- FbModule_75x_493 (FB) - FbModule_75x_494 (FB) - FbModule_75x_495 (FB)

## Module_75x_65x


- FbModule_75x_1652 (FB) - FbModule_75x_650 (FB) - FbModule_75x_651 (FB) - FbModule_75x_652 (FB) - FbModule_75x_653 (FB)

## Module_75x_67x ¶


- FbModule_75x_67x (FB)