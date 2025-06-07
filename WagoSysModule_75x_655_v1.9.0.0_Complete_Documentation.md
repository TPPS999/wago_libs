# WagoSysModule_75x_655 v1.9.0.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysModule_75x_655
- **Version:** 1.9.0.0
- **Categories:** WAGO LayerView|Sys; Application
- **Author:** WAGO/u010663
- **Placeholder:** WagoSysModule_75x_655

### Description ¶


This document is automatically generated.

Handling module 750-655 and 753-655

This document is automatically generated. Handling module 750-655 and 753-655

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks - Methods FbModule_75x_655.GetProcessInByte (METH) - FbModule_75x_655.GetProcessOutByte (METH) - FbModule_75x_655.SetProcessOutByte (METH) - FbModule_75x_655.protCheckPaSIze (METH) Program Organization Global Variable Lists

### Indices and tables ¶


Based on WagoSysModule_75x_655.library, last modified 29.05.2024, 20:25:18. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysModule_75x_655.library, last modified 29.05.2024, 20:25:18. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysModule_75x_655 Library Documentation


| Company: | WAGO |
| Title: | WagoSysModule_75x_655 |
| Version: | 1.9.0.0 |
| Categories: | WAGO LayerView\|Sys; Application |
| Author: | WAGO/u010663 |
| Placeholder: | WagoSysModule_75x_655 |

### Description


This document is automatically generated.

Handling module 750-655 and 753-655

This document is automatically generated. Handling module 750-655 and 753-655

### Contents:


- 20 Program Organization Units FbModule_75x_655 (FB) VersionHistory (GVL)

### Indices and tables


Based on WagoSysModule_75x_655.library, last modified 29.05.2024, 20:25:18. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysModule_75x_655.library, last modified 29.05.2024, 20:25:18. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysModule_75x_655.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:25:19 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:25:18 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO/u010663 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysModule_75x_655 |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysModule_75x_655 |
| Version | version | 1.9.0.0 |
| Version string | string |  |
| Title | WagoSysModule_75x_655 |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False Optional: False | QualifiedOnly: True SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysModuleBase Library Identification : Placeholder: WagoSysModuleBase Default Resolution: WagoSysModuleBase, * (WAGO) Namespace: WagoSysModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX_OUTPUT_SIZE = 47 Parameter: MAX_MODULE_QUANTITY = 250 Parameter: MAX_MODULE_INPUT_SIZE = 48 Parameter: MBX_PIPE_SIZE = 1024 Parameter: MAX_MODULE_OUTPUT_SIZE = 48 Parameter: MAX_MBX_INPUT_SIZE = 47 WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesBusServices Library Identification : Placeholder: WagoTypesBusServices Default Resolution: WagoTypesBusServices, * (WAGO) Namespace: WagoTypesBusServices Library Properties : WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : WagoTypesModule_75x_655 Library Identification : Name: WagoTypesModule_75x_655 Version: newest Company: WAGO Namespace: WagoTypesModule_75x_655 Library Properties :

### Function Blocks


## FbModule_75x_655 (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

Access to the module 750-655

Function description

This block is needed for each module. The instance of this function block is either automatically generated by the K-Bus configuration or has to be manually added in case of the dynamic configuration.

Interface variables Function Access to the module 750-655 Function description This block is needed for each module. The instance of this function block is either automatically generated by the K-Bus configuration or has to be manually added in case of the dynamic configuration. - FbModule_75x_655.GetProcessInByte (METH) - FbModule_75x_655.GetProcessOutByte (METH) - FbModule_75x_655.SetProcessOutByte (METH) - FbModule_75x_655.protCheckPaSIze (METH)

### Methods


## FbModule_75x_655.GetProcessInByte (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetProcessInByte | BYTE |  |
| Input | ByteNo | UINT | range 0..(_uiInputSize - 1) |

## FbModule_75x_655.GetProcessOutByte (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetProcessOutByte | BYTE |  |
| Input | ByteNo | UINT | range 0..(_uiInputSize - 1) |

## FbModule_75x_655.SetProcessOutByte (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | ByteNo | UINT | range 0..(_uiOutputSize - 1) |
| OutData | BYTE |  |

## FbModule_75x_655.protCheckPaSIze (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | protCheckPaSIze | BOOL |  |  |
| Input | uiPaNominalBitSize | UINT |  | The expected bit size of the module |
| ITerminal | WagoTypesBusServices.I_TerminalBase | 0 | Interface to terminal at that this module is registered |

This method is called at static configuration for Kbus-Modules only. If this method returns with TRUE a reboot of the controller will be initiated.

At the derivated method you have to manipulate the registers of the module to change for the wanted uiPaNominalBitSize .

The wanted uiPaNominalBitSize is calculated by the devcie description.

You have not to return before the needed register change was done by your implementation.

Interface variables This method is called at static configuration for Kbus-Modules only. If this method returns with TRUE a reboot of the controller will be initiated. At the derivated method you have to manipulate the registers of the module to change for the wanted uiPaNominalBitSize . The wanted uiPaNominalBitSize is calculated by the devcie description. Note You have not to return before the needed register change was done by your implementation.

### Program Organization


## 20 Program Organization Units


- FbModule_75x_655 (FB) FbModule_75x_655.GetProcessInByte (METH) - FbModule_75x_655.GetProcessOutByte (METH) - FbModule_75x_655.SetProcessOutByte (METH) - FbModule_75x_655.protCheckPaSIze (METH)

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 17.10.2023 | 1.9.0.0 | u010663 | New library according to CoDeSys V3.5.xx |
| 08.01.2019 | 1.8.1.0 | u015842 | Properties: free placeholder added |
| 14.11.2017 | 1.8.0.0 | u010663 | allow resize PA |
| 28.08.2017 | 1.5.0.4 | u010545 | handling of fillbyte modified |
| 03.05.2017 | 1.5.0.3 | u010663 | compiler version increased |
| 12.04.2017 | 1.5.0.2 | U10545 | License changed |
| 29.09.2015 | 1.5.0.1 | u010663 | Libraries inserted by placeholder |
| 24.08.2015 | 1.5.0.0 | u010663 | Placeholder added |
| 02.06.2015 | 1.0.0.2 | u010663 | new method implemented |
| 20.04.2015 | 1.0.0.0 | u010663 | init |

WagoSysModule_75x_655.library

Release Notes:

WagoSysModule_75x_655.library Release Notes: