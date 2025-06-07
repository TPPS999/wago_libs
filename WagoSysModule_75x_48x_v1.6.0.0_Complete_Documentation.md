# WagoSysModule_75x_48x v1.6.0.0 (WAGO) - Complete Documentation


### Documentation Index


## WagoSysModule_75x_48x Library Documentation


WagoSysModule_75x_48x

WAGO LayerView|Sys; Application

WagoSysModule_75x_48x

This document is automatically generated.

Handling modules 750-482 and 750-484

Based on WagoSysModule_75x_48x.library, last modified 15.05.2023, 18:35:41. LibDoc 4.1.1.0

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

Company WAGO Title WagoSysModule_75x_48x Version 1.6.0.0 Categories WAGO LayerView|Sys; Application Author WAGO Placeholder WagoSysModule_75x_48x This document is automatically generated. Handling modules 750-482 and 750-484 - 20 Program Organization Units FbModule_75x_48x (FunctionBlock) VersionHistory (GVL) - File and Project Information - Library Reference Based on WagoSysModule_75x_48x.library, last modified 15.05.2023, 18:35:41. LibDoc 4.1.1.0 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | creationDateTime | date | 15.05.2023, 18:35:41 |
| companyName | string | WAGO |
| libraryFile | string | WagoSysModule_75x_48x.library |
| productName | string | e!COCKPIT |
| contentFile | string | doc.clean.json |
| ProjectInformation | ActivateSigning | bool | False |
| ProjectInformation | AutoResolveUnbound | bool | True |
| ProjectInformation | LastModificationDateTime | 15.05.2023, 18:35:41 |
| ProjectInformation | LibraryCategories | library-category-list | WAGO LayerView\|Sys; Application |
| ProjectInformation | Author | string | WAGO |
| ProjectInformation | Company | string | WAGO |
| ProjectInformation | CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |
| ProjectInformation | Copyright | string | © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. |
| ProjectInformation | Description | string | See: Description |
| ProjectInformation | DocFormat | string | reStructuredText |
| ProjectInformation | Placeholder | string | WagoSysModule_75x_48x |
| ProjectInformation | Project | string | WagoSysModule_75x_48x |
| ProjectInformation | Title | string | WagoSysModule_75x_48x |
| ProjectInformation | Version string | string |  |
| ProjectInformation | Version | version | 1.6.0.0 |

### Library Information


| LinkAllContent: False Optional: False | QualifiedOnly: True | SystemLibrary: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False | SystemLibrary: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False | SystemLibrary: False |

| LinkAllContent: False Optional: False | QualifiedOnly: True | SystemLibrary: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysModuleBase Library Identification : Placeholder: WagoSysModuleBase Default Resolution: WagoSysModuleBase, * (WAGO) Namespace: WagoSysModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX_INPUT_SIZE = 47 Parameter: MAX_MBX_OUTPUT_SIZE = 47 Parameter: MAX_MODULE_INPUT_SIZE = 48 Parameter: MAX_MODULE_OUTPUT_SIZE = 48 Parameter: MAX_MODULE_QUANTITY = 250 Parameter: MBX_PIPE_SIZE = 1024 Parameter: STARTUP_MODE = eStartUpMode.NONE Parameter: SYSLOG_MBX2_LOGLEVEL = 2#10001 Parameter: SYSLOG_MBX2_MAX_STRING_LEN = 0 Parameter: SYSLOG_SERVER_IP = ‘127.0.0.1’ Parameter: SYSLOG_SERVER_PORT = 514 WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesBusServices Library Identification : Placeholder: WagoTypesBusServices Default Resolution: WagoTypesBusServices, * (WAGO) Namespace: WagoTypesBusServices Library Properties : Library Parameter : Parameter: MAX_MODULE_QUANTITY = 250 Parameter: MAX_RUNNABLES = MAX_MODULE_QUANTITY WagoTypesModule_75x_48x Library Identification : Placeholder: WagoTypesModule_75x_48x Default Resolution: WagoTypesModule_75x_48x, * (WAGO) Namespace: WagoTypesModule_75x_48x Library Properties :

### Function Blocks


## FbModule_75x_48x (FB)


| Scope | Name | Type | Inherited from |
| --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult | FbModuleBase |

Access to the module 750-482 and 750-484 and derivates

Function description

This block is needed for each module. The instance of this function block is either automatically generated by the K-Bus configuration or has to be manually added in case of the dynamic configuration.

Interface variables Function Access to the module 750-482 and 750-484 and derivates Function description This block is needed for each module. The instance of this function block is either automatically generated by the K-Bus configuration or has to be manually added in case of the dynamic configuration. - GetProcessInByte (Method) - GetProcessInWord (Method)

### Methods


## FbModule_75x_48x.GetProcessInByte (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetProcessInByte | BYTE |
| Input | ByteNo | UINT |

Get the process input byte specified by ByteNo of this module.

Graphical Illustration

Graphical Interface of FbModuleProcessInputs.GetProcessInByte

Interface variables Function Get the process input byte specified by ByteNo of this module. Graphical Illustration Graphical Interface of FbModuleProcessInputs.GetProcessInByte

## FbModule_75x_48x.GetProcessInWord (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetProcessInWord | WORD |
| Input | ByteNo | UINT |

Get the process input word specified by ByteNo of this module.

Graphical Illustration

Graphical Interface of FbModuleProcessInputs.GetProcessInWord

Interface variables Function Get the process input word specified by ByteNo of this module. Graphical Illustration Graphical Interface of FbModuleProcessInputs.GetProcessInWord

### Program Organization


## 20 Program Organization Units


- FbModule_75x_48x (FunctionBlock) GetProcessInByte (Method) - GetProcessInWord (Method)

### Global Variable Lists


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 21.03.2023 | 1.6.0.0 | u010663 | handling adjusted according to the new device description 2.x.x.x |
| 08.01.2019 | 1.5.1.0 | u015842 | Properties: free placeholder added |
| 06.02.2018 | 1.5.0.6 | u010545 | (WAT25431) Datatype changed GetMbxFillBytes() : USINT(0..1) |
| 28.08.2017 | 1.5.0.5 | u010663 | handling of fillbytes modified |
| 03.05.2017 | 1.5.0.4 | u010663 | compiler version increased |
| 29.09.2015 | 1.5.0.3 | u010663 | Used libraries included by placeholder |
| 28.09.2015 | 1.5.0.2 | u010663 | Used libraries included by * |
| 14.09.2015 | 1.5.0.1 | u010663 | Internal improvement |
| 24.08.2015 | 1.5.0.0 | u010663 | Placeholder added |
| 24.09.2014 | 1.0.0.0 | u010663 | init |

WagoSysModule_75x_48x.library

Release Notes:

WagoSysModule_75x_48x.library Release Notes: