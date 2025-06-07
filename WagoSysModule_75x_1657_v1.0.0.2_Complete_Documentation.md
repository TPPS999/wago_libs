# WagoSysModule_75x_1657 v1.0.0.2 (WAGO) - Complete Documentation


### Documentation Index


## WagoSysModule_75x_1657 Library Documentation


WagoSysModule_75x_1657

WAGO LayerView|Sys; Application

WagoSysModule_75x_1657

This document is automatically generated.

Handling module 750-1657

Based on WagoSysModule_75x_1657.library, last modified 15.05.2023, 18:35:09. LibDoc 4.1.1.0

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

Company WAGO Title WagoSysModule_75x_1657 Version 1.0.0.2 Categories WAGO LayerView|Sys; Application Author WAGO Placeholder WagoSysModule_75x_1657 This document is automatically generated. Handling module 750-1657 - 20 Program Organization Units FbModule_75x_1657 (FunctionBlock) - typHandleMbx2 (Struct) ParameterList (ParamList) VersionHistory (GVL) - File and Project Information - Library Reference Based on WagoSysModule_75x_1657.library, last modified 15.05.2023, 18:35:09. LibDoc 4.1.1.0 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | creationDateTime | date | 15.05.2023, 18:35:09 |
| companyName | string | WAGO |
| libraryFile | string | WagoSysModule_75x_1657.library |
| productName | string | e!COCKPIT |
| contentFile | string | doc.clean.json |
| ProjectInformation | AutoResolveUnbound | bool | True |
| ProjectInformation | LastModificationDateTime | 15.05.2023, 18:35:09 |
| ProjectInformation | LibraryCategories | library-category-list | WAGO LayerView\|Sys; Application |
| ProjectInformation | Author | string | WAGO |
| ProjectInformation | Company | string | WAGO |
| ProjectInformation | CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |
| ProjectInformation | Copyright | string | © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. |
| ProjectInformation | Description | string | See: Description |
| ProjectInformation | DocFormat | string | reStructuredText |
| ProjectInformation | Placeholder | string | WagoSysModule_75x_1657 |
| ProjectInformation | Project | string | WagoSysModule_75x_1657 |
| ProjectInformation | Title | string | WagoSysModule_75x_1657 |
| ProjectInformation | Version string | string |  |
| ProjectInformation | Version | version | 1.0.0.2 |

### Library Information


| LinkAllContent: False Optional: False | QualifiedOnly: False | SystemLibrary: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False | SystemLibrary: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False | SystemLibrary: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True | SystemLibrary: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False | SystemLibrary: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False | SystemLibrary: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_NAME = ‘WagoSysResultLogger’ WagoSysModuleBase Library Identification : Placeholder: WagoSysModuleBase Default Resolution: WagoSysModuleBase, * (WAGO) Namespace: WagoSysModuleBase Library Properties : Library Parameter : Parameter: PARAMETER_COM_TIMEOUT = TIME#5s0ms Parameter: REGISTER_COM_TIMEOUT = TIME#5s0ms Parameter: STARTUP_MODE = eStartUpMode.NONE Parameter: SYSLOG_MBX2_LOGLEVEL = 2#10001 Parameter: SYSLOG_MBX2_MAX_STRING_LEN = 0 Parameter: SYSLOG_SERVER_IP = ‘127.0.0.1’ Parameter: SYSLOG_SERVER_PORT = 514 WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesBusServices Library Identification : Placeholder: WagoTypesBusServices Default Resolution: WagoTypesBusServices, * (WAGO) Namespace: WagoTypesBusServices Library Properties : Library Parameter : Parameter: MAX_MODULE_QUANTITY = 250 Parameter: MAX_RUNNABLES = MAX_MODULE_QUANTITY WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX1_SIZE = 18 Parameter: MAX_MBX_INPUT_SIZE = 47 Parameter: MAX_MBX_OUTPUT_SIZE = 47 Parameter: MAX_MODULE_INPUT_SIZE = 48 Parameter: MAX_MODULE_OUTPUT_SIZE = 48 Parameter: MBX_PIPE_SIZE = 1024 WagoTypesModule_75x_1657 Library Identification : Name: WagoTypesModule_75x_1657 Version: newest Company: WAGO Namespace: WagoTypesModule_75x_1657 Library Properties :

### Function Blocks


## FbModule_75x_1657 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

The instance of this function block is either automatically generated by the K-Bus configuration or has to be manually added in case of the dynamic configuration ****************************************************************************************************** Historie: 09.06.2022 Version 1.0 22.04.2014 Version 0.1 RC ******************************************************************************************************

Interface variables The instance of this function block is either automatically generated by the K-Bus configuration or has to be manually added in case of the dynamic configuration ****************************************************************************************************** Historie: 09.06.2022 Version 1.0 22.04.2014 Version 0.1 RC ****************************************************************************************************** - DoConfigMbx2 (Method) - DoResetMbx2 (Method) - DoStartMbx2 (Method) - GetNextIOLinkMessageOverMbx2 (Method) - Mbx2IsReady (Method) - PropM0blocked (Property) - PropM1InUse (Property) - PropM2InUse (Property) - PropM3InUse (Property) - PropM4InUse (Property) - SendIOLinkMessageOverMbx2 (Method) - protCheckPaSIze (Method)

### Methods


## FbModule_75x_1657.DoConfigMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DoConfigMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |
| Input | bInputOffset | BYTE |
| Input | bOutputOffset | BYTE |

## FbModule_75x_1657.DoResetMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DoResetMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |

## FbModule_75x_1657.DoStartMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DoStartMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |

## FbModule_75x_1657.GetNextIOLinkMessageOverMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetNextIOLinkMessageOverMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |
| Input | pMsgBuffer | POINTER TO BYTE |
| Input | udiMsgBufferSize | BYTE |
| Output | udiMsgLen | UDINT |

## FbModule_75x_1657.Mbx2IsReady (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Mbx2IsReady | BOOL |
| Input | bIO_LinkPort | BYTE |

## FbModule_75x_1657.SendIOLinkMessageOverMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SendIOLinkMessageOverMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |
| Input | pData | POINTER TO BYTE |
| Input | udiNData | UDINT |

## FbModule_75x_1657.protCheckPaSIze (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | protCheckPaSIze | BOOL |  |  |
| Input | uiPaNominalBitSize | UINT |  | The expected bit size of the module |
| Input | ITerminal | WagoTypesBusServices.I_TerminalBase | 0 | Interface to terminal at that this module is registered |

This method is called at static configuration for Kbus-Modules only. If this method returns with TRUE a reboot of the controller will be initiated.

At the derivated method you have to manipulate the registers of the module to change for the wanted uiPaNominalBitSize .

The wanted uiPaNominalBitSize is calculated by the devcie description.

You have not to return before the needed register change was done by your implementation.

Interface variables This method is called at static configuration for Kbus-Modules only. If this method returns with TRUE a reboot of the controller will be initiated. At the derivated method you have to manipulate the registers of the module to change for the wanted uiPaNominalBitSize . The wanted uiPaNominalBitSize is calculated by the devcie description. Note You have not to return before the needed register change was done by your implementation.

### Program Organization


## 20 Program Organization Units


- FbModule_75x_1657 (FunctionBlock) DoConfigMbx2 (Method) - DoResetMbx2 (Method) - DoStartMbx2 (Method) - GetNextIOLinkMessageOverMbx2 (Method) - Mbx2IsReady (Method) - PropM0blocked (Property) - PropM1InUse (Property) - PropM2InUse (Property) - PropM3InUse (Property) - PropM4InUse (Property) - SendIOLinkMessageOverMbx2 (Method) - protCheckPaSIze (Method) typHandleMbx2 (Struct)

### Global Variable Lists


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 29.03.2023 | 1.0.0.2 | u010663 | Allow up to 48 Byte process image |
| 24.08.2022 | 1.0.0.1 | u010663 | Make use of WagoTypesModule_75x_1657 |
| 19.08.2022 | 1.0.0.0 | u010663 | Init |

WagoSysModule_75x_1657.library

Release Notes:

WagoSysModule_75x_1657.library Release Notes:

### Other Components


## FbModule_75x_1657.PropM0blocked (PROP) ¶


## FbModule_75x_1657.PropM1InUse (PROP) ¶


## FbModule_75x_1657.PropM2InUse (PROP) ¶


## FbModule_75x_1657.PropM3InUse (PROP) ¶


## FbModule_75x_1657.PropM4InUse (PROP) ¶


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | MAX_MBX2 | INT | 4 | Up to 4 mailboxes may be needed for the fragmentation of IO- link ports |

| Name | Type |
| --- | --- |
| InUse | BOOL |
| InputOffset | BYTE |
| OutputOffset | BYTE |