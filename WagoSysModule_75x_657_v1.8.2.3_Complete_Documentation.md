# WagoSysModule_75x_657 v1.8.2.3 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysModule_75x_657
- **Version:** 1.8.2.3
- **Categories:** WAGO LayerView|Sys; Application
- **Author:** WAGO
- **Placeholder:** WagoSysModule_75x_657

### Description ¶


This document is automatically generated.

Handling module 750-657

This document is automatically generated. Handling module 750-657

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks - Methods FbModule_75x_657.DoConfigMbx2 (METH) - FbModule_75x_657.DoResetMbx2 (METH) - FbModule_75x_657.DoStartMbx2 (METH) - FbModule_75x_657.GetNextIOLinkMessageOverMbx2 (METH) - FbModule_75x_657.Mbx2IsReady (METH) - FbModule_75x_657.SendIOLinkMessageOverMbx2 (METH) - FbModule_75x_657.protCheckPaSIze (METH) Program Organization Global Variable Lists Other Components - FbModule_75x_657.PropM0blocked (PROP) - FbModule_75x_657.PropM1InUse (PROP) - FbModule_75x_657.PropM2InUse (PROP) - FbModule_75x_657.PropM3InUse (PROP) - FbModule_75x_657.PropM4InUse (PROP) - ParameterList (PARAMS) - typHandleMbx2 (STRUCT)

### Indices and tables ¶


Based on WagoSysModule_75x_657.library, last modified 29.05.2024, 20:25:10. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysModule_75x_657.library, last modified 29.05.2024, 20:25:10. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysModule_75x_657 Library Documentation


| Company: | WAGO |
| Title: | WagoSysModule_75x_657 |
| Version: | 1.8.2.3 |
| Categories: | WAGO LayerView\|Sys; Application |
| Author: | WAGO |
| Placeholder: | WagoSysModule_75x_657 |

### Description


This document is automatically generated.

Handling module 750-657

This document is automatically generated. Handling module 750-657

### Contents:


- 20 Program Organization Units FbModule_75x_657 (FB) - typHandleMbx2 (STRUCT) ParameterList (PARAMS) VersionHistory (GVL)

### Indices and tables


Based on WagoSysModule_75x_657.library, last modified 29.05.2024, 20:25:10. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysModule_75x_657.library, last modified 29.05.2024, 20:25:10. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysModule_75x_657.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 20:25:10 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 20:25:10 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysModule_75x_657 |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysModule_75x_657 |
| Version | version | 1.8.2.3 |
| Version string | string |  |
| Title | WagoSysModule_75x_657 |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : WagoSysModuleBase Library Identification : Placeholder: WagoSysModuleBase Default Resolution: WagoSysModuleBase, * (WAGO) Namespace: WagoSysModuleBase Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesBusServices Library Identification : Placeholder: WagoTypesBusServices Default Resolution: WagoTypesBusServices, * (WAGO) Namespace: WagoTypesBusServices Library Properties : WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX_SIZE = 18 WagoTypesModule_75x_657 Library Identification : Placeholder: WagoTypesModule_75x_657 Default Resolution: WagoTypesModule_75x_657, * (WAGO) Namespace: WagoTypesModule_75x_657 Library Properties :

### Function Blocks


## FbModule_75x_657 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

The instance of this function block is either automatically generated by the K-Bus configuration or has to be manually added in case of the dynamic configuration ****************************************************************************************************** Historie: 22.04.2014 Version 0.1 RC ******************************************************************************************************

Interface variables The instance of this function block is either automatically generated by the K-Bus configuration or has to be manually added in case of the dynamic configuration ****************************************************************************************************** Historie: 22.04.2014 Version 0.1 RC ****************************************************************************************************** - FbModule_75x_657.DoConfigMbx2 (METH) - FbModule_75x_657.DoResetMbx2 (METH) - FbModule_75x_657.DoStartMbx2 (METH) - FbModule_75x_657.GetNextIOLinkMessageOverMbx2 (METH) - FbModule_75x_657.Mbx2IsReady (METH) - FbModule_75x_657.PropM0blocked (PROP) - FbModule_75x_657.PropM1InUse (PROP) - FbModule_75x_657.PropM2InUse (PROP) - FbModule_75x_657.PropM3InUse (PROP) - FbModule_75x_657.PropM4InUse (PROP) - FbModule_75x_657.SendIOLinkMessageOverMbx2 (METH) - FbModule_75x_657.protCheckPaSIze (METH)

### Methods


## FbModule_75x_657.DoConfigMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DoConfigMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |
| bInputOffset | BYTE |
| bOutputOffset | BYTE |

## FbModule_75x_657.DoResetMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DoResetMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |

## FbModule_75x_657.DoStartMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DoStartMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |

## FbModule_75x_657.GetNextIOLinkMessageOverMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetNextIOLinkMessageOverMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |
| pMsgBuffer | POINTER TO BYTE |
| udiMsgBufferSize | BYTE |
| Output | udiMsgLen | UDINT |

## FbModule_75x_657.Mbx2IsReady (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Mbx2IsReady | BOOL |
| Input | bIO_LinkPort | BYTE |

## FbModule_75x_657.SendIOLinkMessageOverMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SendIOLinkMessageOverMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |
| pData | POINTER TO BYTE |
| udiNData | UDINT |

## FbModule_75x_657.protCheckPaSIze (METH)


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


- FbModule_75x_657 (FB) FbModule_75x_657.DoConfigMbx2 (METH) - FbModule_75x_657.DoResetMbx2 (METH) - FbModule_75x_657.DoStartMbx2 (METH) - FbModule_75x_657.GetNextIOLinkMessageOverMbx2 (METH) - FbModule_75x_657.Mbx2IsReady (METH) - FbModule_75x_657.PropM0blocked (PROP) - FbModule_75x_657.PropM1InUse (PROP) - FbModule_75x_657.PropM2InUse (PROP) - FbModule_75x_657.PropM3InUse (PROP) - FbModule_75x_657.PropM4InUse (PROP) - FbModule_75x_657.SendIOLinkMessageOverMbx2 (METH) - FbModule_75x_657.protCheckPaSIze (METH) typHandleMbx2 (STRUCT)

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 28.02.2024 | 1.8.2.3 | u010663 | compiled SP16.3 |
| 19.05.2023 | 1.8.2.2 | u0103719 | update compiler version |
| 06.09.2019 | 1.8.2.1 | u010663 | Bugfix FbModule_75x_657 |
| 08.01.2019 | 1.8.2.0 | u015842 | Properties: free placeholder added |
| 13.11.2017 | 1.8.1.0 | u010545 | update resize module PA |
| 03.05.2017 | 1.8.0.0 | u010663 | Allow change of pa size with FW>=10 |
| 06.09.2016 | 1.5.0.3 | u010663 | Bugfix |
| 02.12.2015 | 1.5.0.2 | u010663 | R3 release |

WagoSysModule_75x_657.library

Release Notes:

WagoSysModule_75x_657.library Release Notes:

### Other Components


## FbModule_75x_657.PropM0blocked (PROP) ¶


## FbModule_75x_657.PropM1InUse (PROP) ¶


## FbModule_75x_657.PropM2InUse (PROP) ¶


## FbModule_75x_657.PropM3InUse (PROP) ¶


## FbModule_75x_657.PropM4InUse (PROP) ¶


## ParameterList (PARAMS)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | MAX_MBX2 | INT | 4 | Up to 4 mailboxes may be needed for the fragmentation of IO- link ports |

## typHandleMbx2 (STRUCT)


| Name | Type |
| --- | --- |
| InUse | BOOL |
| InputOffset | BYTE |
| OutputOffset | BYTE |