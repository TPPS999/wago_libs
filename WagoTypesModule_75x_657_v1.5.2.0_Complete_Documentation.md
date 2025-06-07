# WagoTypesModule_75x_657 v1.5.2.0 (WAGO) - Complete Documentation


### Documentation Index


## WagoTypesModule_75x_657 Library Documentation


WagoTypesModule_75x_657

WAGO LayerView|Types and Interfaces

WagoTypesModule_75x_657

This document is automatically generated.

Handling IO-Link module 750-657

Based on WagoTypesModule_75x_657.library, last modified 15.05.2023, 18:33:21. LibDoc 4.1.1.0

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

Company WAGO Title WagoTypesModule_75x_657 Version 1.5.2.0 Categories WAGO LayerView|Types and Interfaces Author WAGO Placeholder WagoTypesModule_75x_657 This document is automatically generated. Handling IO-Link module 750-657 - FuGetVersionHistory (Function) - I_Module_75x_657 (Interface) DoConfigMbx2 (Method) - DoResetMbx2 (Method) - DoStartMbx2 (Method) - GetNextIOLinkMessageOverMbx2 (Method) - Mbx2IsReady (Method) - PropM0blocked (Property) - PropM1InUse (Property) - PropM2InUse (Property) - PropM3InUse (Property) - PropM4InUse (Property) - SendIOLinkMessageOverMbx2 (Method) - File and Project Information - Library Reference Based on WagoTypesModule_75x_657.library, last modified 15.05.2023, 18:33:21. LibDoc 4.1.1.0 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | creationDateTime | date | 15.05.2023, 18:33:21 |
| companyName | string | WAGO |
| libraryFile | string | WagoTypesModule_75x_657.library |
| productName | string | e!COCKPIT |
| contentFile | string | doc.clean.json |
| ProjectInformation | ActivateSigning | bool | False |
| ProjectInformation | AutoResolveUnbound | bool | True |
| ProjectInformation | LastModificationDateTime | 15.05.2023, 18:33:21 |
| ProjectInformation | LibraryCategories | library-category-list | WAGO LayerView\|Types and Interfaces |
| ProjectInformation | Author | string | WAGO |
| ProjectInformation | Company | string | WAGO |
| ProjectInformation | CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |
| ProjectInformation | Copyright | string | © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. |
| ProjectInformation | Description | string | See: Description |
| ProjectInformation | DocFormat | string | reStructuredText |
| ProjectInformation | Placeholder | string | WagoTypesModule_75x_657 |
| ProjectInformation | Project | string | WagoTypesModule_75x_657 |
| ProjectInformation | Title | string | WagoTypesModule_75x_657 |
| ProjectInformation | Version string | string |  |
| ProjectInformation | Version | version | 1.5.2.0 |

### Library Information


| LinkAllContent: False Optional: False | QualifiedOnly: True | SystemLibrary: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX1_SIZE = 18 Parameter: MAX_MBX_INPUT_SIZE = 47 Parameter: MAX_MBX_OUTPUT_SIZE = 47 Parameter: MAX_MBX_SIZE = 18 Parameter: MAX_MODULE_INPUT_SIZE = 48 Parameter: MAX_MODULE_OUTPUT_SIZE = 48 Parameter: MBX_PIPE_SIZE = 1024

### Functions


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 26.10.2022 | 1.5.2.0 | u010663 | Allow access to PrameterList methods |
| 08.01.2019 | 1.5.1.0 | u015842 | Properties: free placeholder added |
| 26.02.2016 | 1.5.0.2 | u010663 | WagoSysVersion eliminated |
| 02.12.2015 | 1.5.0.1 | u010663 | Method DoRemoveMbx2 added |
| 24.08.2015 | 1.5.0.0 | u010663 | Placeholder added |
| 08.05.2015 | 0.0.0.1 | u010663 | init |

WagoTypesModule_75x_657.library

Interface variables WagoTypesModule_75x_657.library

### Methods


## I_Module_75x_657.DoConfigMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DoConfigMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |
| Input | bInputOffset | BYTE |
| Input | bOutputOffset | BYTE |

## I_Module_75x_657.DoResetMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DoResetMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |

## I_Module_75x_657.DoStartMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | DoStartMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |

## I_Module_75x_657.GetNextIOLinkMessageOverMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetNextIOLinkMessageOverMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |
| Input | pMsgBuffer | POINTER TO BYTE |
| Input | udiMsgBufferSize | BYTE |
| Output | udiMsgLen | UDINT |

## I_Module_75x_657.Mbx2IsReady (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Mbx2IsReady | BOOL |
| Input | bIO_LinkPort | BYTE |

## I_Module_75x_657.SendIOLinkMessageOverMbx2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SendIOLinkMessageOverMbx2 | BOOL |
| Input | bIO_LinkPort | BYTE |
| Input | pData | POINTER TO BYTE |
| Input | udiNData | UDINT |

### Interfaces


## I_Module_75x_657 (ITF)


- DoConfigMbx2 (Method) - DoResetMbx2 (Method) - DoStartMbx2 (Method) - GetNextIOLinkMessageOverMbx2 (Method) - Mbx2IsReady (Method) - PropM0blocked (Property) - PropM1InUse (Property) - PropM2InUse (Property) - PropM3InUse (Property) - PropM4InUse (Property) - SendIOLinkMessageOverMbx2 (Method)

### Other Components


## I_Module_75x_657.PropM0blocked (PROP) ¶


## I_Module_75x_657.PropM1InUse (PROP) ¶


## I_Module_75x_657.PropM2InUse (PROP) ¶


## I_Module_75x_657.PropM3InUse (PROP) ¶


## I_Module_75x_657.PropM4InUse (PROP) ¶
