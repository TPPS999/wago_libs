# WagoTypesKbusTerminalControl v1.0.1.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesKbusTerminalControl
- **Version:** 1.0.1.2
- **Categories:** WAGO Internal|Feature|LocalBus|K-Bus
- **Namespace:** WagoTypesKbusTerminalControl
- **Author:** WAGO
- **Placeholder:** WagoTypesKbusTerminalControl

### Description ¶


This document is automatically generated.

data types for dynamic module configuration

This document is automatically generated. data types for dynamic module configuration

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Methods I_SetTerminalRef.AllocateProcessData_PS (METH) - I_SetTerminalRef.AllocateProcessData_SD (METH) - I_SetTerminalRef.FreeProcessData (METH) - I_SetTerminalRef.Start_PDE_In_CurrentTask (METH) - I_SetTerminalRef.Stop_PDE (METH) Interfaces Program Organization Global Variable Lists - DataDescriptions (GVL) - NoOfEntriesInDataDesc (GVL) - VersionHistory (GVL) Other Components - 01 Inputs - 01 Inputs - 01 Inputs - 01 Specific - 01 Specific - 01 Structured Data SD - 02 Generic - 02 Outputs - 02 Outputs - 02 Outputs - ... and 40 more

### Indices and tables ¶


Based on WagoTypesKbusTerminalControl.library, last modified 29.05.2024, 19:55:43. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesKbusTerminalControl.library, last modified 29.05.2024, 19:55:43. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesKbusTerminalControl Library Documentation


| Company: | WAGO |
| Title: | WagoTypesKbusTerminalControl |
| Version: | 1.0.1.2 |
| Categories: | WAGO Internal\|Feature\|LocalBus\|K-Bus |
| Namespace: | WagoTypesKbusTerminalControl |
| Author: | WAGO |
| Placeholder: | WagoTypesKbusTerminalControl |

### Description


This document is automatically generated.

data types for dynamic module configuration

This document is automatically generated. data types for dynamic module configuration

### Contents:


- 20 Program Organization Units 23 Interfaces - 40 Data Types VersionHistory (GVL)

### Indices and tables


Based on WagoTypesKbusTerminalControl.library, last modified 29.05.2024, 19:55:43. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesKbusTerminalControl.library, last modified 29.05.2024, 19:55:43. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesKbusTerminalControl.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:55:43 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:55:43 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesKbusTerminalControl |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesKbusTerminalControl |
| DefaultNamespace | WagoTypesKbusTerminalControl |
| Version | version | 1.0.1.2 |
| Title | string | WagoTypesKbusTerminalControl |
| Released | bool | False |
| LibraryCategories | library-category-list | WAGO Internal\|Feature\|LocalBus\|K-Bus |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False HideWhenReferencedAsDependency: True | QualifiedOnly: False SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. Base Interfaces Library Identification : Name: Base Interfaces Version: newest Company: System Namespace: IBaseLibrary Library Properties : IoStandard Library Identification : Placeholder: IoStandard Default Resolution: IoStandard, * (System) Namespace: IoStandard Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysTypedefs_Internal_32Bit Library Identification : Placeholder: WagoSysTypedefsInternal Default Resolution: WagoSysTypedefs_Internal_32Bit, * (WAGO) Namespace: WagoTypesInternal Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties :

### Methods


## I_SetTerminalRef.AllocateProcessData_PS (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | AllocateProcessData_PS | WagoTypes.eResultCode |  |
| Input | usiSlotNo | USINT | terminal slot number |
| udiModuleId | UDINT | unified module identification number |
| Output | uiInputSize | UINT | number of active input bytes |
| pInputData | POINTER TO BYTE | pointer to input data structure |
| uiOutputSize | UINT | number of active output bytes |
| pOutputData | POINTER TO BYTE | pointer to output data structure |

| Result Codes |
| 0 | Success |
| 210 | No access to driver |
| 211 | Active process data exchange |
| 212 | Error from io manager |
| 214 | Error module not connected to KBUS |
| 215 | Configuration error |
| 216 | Error module stopped |

This method allocates module process data.

This method provides packed module process data.

Interface variables This method allocates module process data. This method provides packed module process data. Note: Result code of this function is OK (0) or EAPP (200) plus an error specific value see ePARTICULAR_CODES.

## I_SetTerminalRef.AllocateProcessData_SD (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | AllocateProcessData_SD | WagoTypes.eResultCode |  |  |
| Input | usiSlotNo | USINT | 0 | terminal slot number |
| udiModuleId | UDINT | 0 | unified module identification number |
| pInDesc | POINTER TO typeDataDesc |  | pointer to array of input data descriptions |
| uiNoInDesc | UINT | 0 | number of elements input data descriptions |
| pOutDesc | POINTER TO typeDataDesc |  | pointer to array of output data descriptions |
| uiNoOutDesc | UINT | 0 | number of elements output data descriptions |
| Output | uiInputSize | UINT | 0 | number of active input bytes |
| pInputData | POINTER TO BYTE | WagoTypesInternal.Udint_to_Pointer(0) | pointer to input data structure |
| uiOutputSize | UINT | 0 | number of active output bytes |
| pOutputData | POINTER TO BYTE | WagoTypesInternal.Udint_to_Pointer(0) | pointer to output data structure |

| Result Codes |
| 0 | Success |
| 210 | No access to driver |
| 211 | Active process data exchange |
| 212 | Error from io manager |
| 214 | Error module not connected to KBUS |
| 215 | Configuration error |
| 216 | Error module stopped |
| 225 | Error from driver update configuration |

This method allocates module process data structures.

This method provides module process data structures.

Interface variables This method allocates module process data structures. This method provides module process data structures. Note: Result code of this function is OK (0) or EAPP (200) plus an error specific value see ePARTICULAR_CODES.

## I_SetTerminalRef.FreeProcessData (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FreeProcessData | WagoTypes.eResultCode |

| Result Codes |
| 0 | Success |
| 210 | No access to driver |
| 211 | Active process data exchange |
| 212 | Error from io manager |

This method resets dynamic module process data exchange.

This method delets dynamic module configuration in driver.

Interface variables This method resets dynamic module process data exchange. This method delets dynamic module configuration in driver. Note: Method calls update configuration in driver. Note: Result code of this function is OK (0) or EAPP (200) plus an error specific value see ePARTICULAR_CODES.

## I_SetTerminalRef.Start_PDE_In_CurrentTask (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Start_PDE_In_CurrentTask | WagoTypes.eResultCode |

| Result Codes |
| 0 | Success |
| 206 | Inconsistent input parameter set in device description |
| 207 | Inconsistent output parameter set in device description |
| 208 | Error from event handler |
| 209 | Invalid task handle |
| 210 | No access to driver |
| 211 | Active process data exchange |
| 212 | Error from io manager |
| 213 | Error module is not auto initialized |
| 214 | Error module not connected to KBUS |
| 215 | Configuration error |
| 216 | Error module stopped |
| 218 | Unsupported process data type in device description |
| 226 | Error from driver update mapping |

This method starts program controlled process data exchange.

This method connects module IO - update to current IEC task.

Interface variables This method starts program controlled process data exchange. This method connects module IO - update to current IEC task. Note: Pre-condition for using this method: Function block has to be auto initialized. Note: Result code of this function is OK (0) or EAPP (200) plus an error specific value see ePARTICULAR_CODES.

## I_SetTerminalRef.Stop_PDE (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Stop_PDE | WagoTypes.eResultCode |

| Result Codes |
| 0 | Success |
| 208 | Error from event handler |
| 225 | Error from driver update configuration |
| 226 | Error from driver update mapping |

This method stops program controlled process data exchange.

This method disconnects module IO - update from any IEC task.

Interface variables This method stops program controlled process data exchange. This method disconnects module IO - update from any IEC task. Note: Method calls driver. Note: Pre-condition for using this method: Function block has to be auto initialized. Note: Result code of this function is OK (0) or EAPP (200) plus an error specific value see ePARTICULAR_CODES.

### Interfaces


## I_SetTerminalRef (ITF)


- I_SetTerminalRef.AllocateProcessData_PS (METH) - I_SetTerminalRef.AllocateProcessData_SD (METH) - I_SetTerminalRef.FreeProcessData (METH) - I_SetTerminalRef.Start_PDE_In_CurrentTask (METH) - I_SetTerminalRef.Stop_PDE (METH)

### Program Organization


## 20 Program Organization Units


- 23 Interfaces I_SetTerminalRef (ITF) I_SetTerminalRef.AllocateProcessData_PS (METH) - I_SetTerminalRef.AllocateProcessData_SD (METH) - I_SetTerminalRef.FreeProcessData (METH) - I_SetTerminalRef.Start_PDE_In_CurrentTask (METH) - I_SetTerminalRef.Stop_PDE (METH) 40 Data Types - 01 Structured Data SD 01 Specific 01 Inputs type0750_0493_I (STRUCT) - type0750_0652_I_08 (ALIAS) - type0750_0652_I_24 (ALIAS) - type0750_0652_I_48 (ALIAS) - type0753_0647_I (ALIAS) 02 Outputs - type0750_0493_O (STRUCT) - type0750_0652_O_08 (ALIAS) - type0750_0652_O_24 (ALIAS) - type0750_0652_O_48 (ALIAS) - type0753_0647_O (ALIAS) 02 Packed Structures PD - 01 Specific 01 Inputs type0750_0493_I_PD (STRUCT) - type0750_0652_I_08_PD (ALIAS) - type0750_0652_I_24_PD (ALIAS) - type0750_0652_I_48_PD (ALIAS) - type0753_0647_I_PD (ALIAS) 02 Outputs - type0750_0493_O_PD (STRUCT) - type0750_0652_O_08_PD (ALIAS) - type0750_0652_O_24_PD (ALIAS) - type0750_0652_O_48_PD (ALIAS) - type0753_0647_O_PD (ALIAS) 02 Generic - 01 Inputs type075x_16DI_PD (STRUCT) - type075x_2AI_PD (STRUCT) - type075x_2DI_PD (STRUCT) - type075x_4AI_PD (STRUCT) - type075x_4DI_PD (STRUCT) - type075x_8AI_PD (STRUCT) - type075x_8DI_PD (STRUCT) 02 Outputs - type075x_16DO_PD (STRUCT) - type075x_2AO_PD (STRUCT) - type075x_2DO_PD (STRUCT) - type075x_4AO_PD (STRUCT) - type075x_4DO_PD (STRUCT) - type075x_8AO_PD (STRUCT) - type075x_8DO_PD (STRUCT) 03 Common - eDATA_SIZE_TYPE (ENUM) - typeDataDesc (STRUCT) DataDescriptions (GVL) NoOfEntriesInDataDesc (GVL)

### Global Variable Lists


## DataDescriptions (GVL)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | gc_DD_0750_0493_I | ARRAY [0..5] OF typeDataDesc | [STRUCT(eType := TYPE_1_BYTE, wNumber := 1), STRUCT(eType := TYPE_2_BYTE, wNumber := 1), STRUCT(eType := TYPE_1_BYTE, wNumber := 1), STRUCT(eType := TYPE_2_BYTE, wNumber := 1), STRUCT(eType := TYPE_1_BYTE, wNumber := 1), STRUCT(eType := TYPE_2_BYTE, wNumber := 1)] |
| gc_DD_0750_0493_O | ARRAY [0..5] OF typeDataDesc | [STRUCT(eType := TYPE_1_BYTE, wNumber := 1), STRUCT(eType := TYPE_2_BYTE, wNumber := 1), STRUCT(eType := TYPE_1_BYTE, wNumber := 1), STRUCT(eType := TYPE_2_BYTE, wNumber := 1), STRUCT(eType := TYPE_1_BYTE, wNumber := 1), STRUCT(eType := TYPE_2_BYTE, wNumber := 1)] |
| gc_DD_0750_0652_I_08 | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 8) |
| gc_DD_0750_0652_O_08 | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 8) |
| gc_DD_0750_0652_I_24 | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 24) |
| gc_DD_0750_0652_O_24 | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 24) |
| gc_DD_0750_0652_I_48 | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 48) |
| gc_DD_0750_0652_O_48 | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 48) |
| gc_DD_0753_0647_I | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 24) |
| gc_DD_0753_0647_O | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 24) |
| gc_DD_075x_2DI | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 1) |
| gc_DD_075x_4DI | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 1) |
| gc_DD_075x_8DI | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 1) |
| gc_DD_075x_16DI | typeDataDesc | STRUCT(eType := TYPE_2_BYTE, wNumber := 1) |
| gc_DD_075x_2AI | typeDataDesc | STRUCT(eType := TYPE_2_BYTE, wNumber := 2) |
| gc_DD_075x_4AI | typeDataDesc | STRUCT(eType := TYPE_2_BYTE, wNumber := 4) |
| gc_DD_075x_8AI | typeDataDesc | STRUCT(eType := TYPE_2_BYTE, wNumber := 8) |
| gc_DD_075x_2DO | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 1) |
| gc_DD_075x_4DO | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 1) |
| gc_DD_075x_8DO | typeDataDesc | STRUCT(eType := TYPE_1_BYTE, wNumber := 1) |
| gc_DD_075x_16DO | typeDataDesc | STRUCT(eType := TYPE_2_BYTE, wNumber := 1) |
| gc_DD_075x_2AO | typeDataDesc | STRUCT(eType := TYPE_2_BYTE, wNumber := 2) |
| gc_DD_075x_4AO | typeDataDesc | STRUCT(eType := TYPE_2_BYTE, wNumber := 4) |
| gc_DD_075x_8AO | typeDataDesc | STRUCT(eType := TYPE_2_BYTE, wNumber := 8) |

## NoOfEntriesInDataDesc (GVL)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | gc_uiNOE_0750_0493_I | UINT | 6 | SIZEOF( gc_DD_0750_0493_I ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_0750_0493_O | UINT | 6 | SIZEOF( gc_DD_0750_0493_O ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_0750_0652_I_08 | UINT | 1 | SIZEOF( gc_DD_0750_0652_I_08 ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_0750_0652_O_08 | UINT | 1 | SIZEOF( gc_DD_0750_0652_O_08 ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_0750_0652_I_24 | UINT | 1 | SIZEOF( gc_DD_0750_0652_I_24 ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_0750_0652_O_24 | UINT | 1 | SIZEOF( gc_DD_0750_0652_O_24 ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_0750_0652_I_48 | UINT | 1 | SIZEOF( gc_DD_0750_0652_I_48 ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_0750_0652_O_48 | UINT | 1 | SIZEOF( gc_DD_0750_0652_O_48 ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_0753_0647_I | UINT | 1 | SIZEOF( gc_DD_0753_0647_I ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_0753_0647_O | UINT | 1 | SIZEOF( gc_DD_0753_0647_O ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_2DI | UINT | 1 | SIZEOF( gc_DD_075x_2DI ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_4DI | UINT | 1 | SIZEOF( gc_DD_075x_4DI ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_8DI | UINT | 1 | SIZEOF( gc_DD_075x_8DI ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_16DI | UINT | 1 | SIZEOF( gc_DD_075x_16DI ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_2AI | UINT | 1 | SIZEOF( gc_DD_075x_2AI ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_4AI | UINT | 1 | SIZEOF( gc_DD_075x_4AI ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_8AI | UINT | 1 | SIZEOF( gc_DD_075x_8AI ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_2DO | UINT | 1 | SIZEOF( gc_DD_075x_2DO ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_4DO | UINT | 1 | SIZEOF( gc_DD_075x_4DO ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_8DO | UINT | 1 | SIZEOF( gc_DD_075x_8DO ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_16DO | UINT | 1 | SIZEOF( gc_DD_075x_16DO ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_2AO | UINT | 1 | SIZEOF( gc_DD_075x_2AO ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_4AO | UINT | 1 | SIZEOF( gc_DD_075x_4AO ) / SIZEOF( typeDataDesc ); |
| gc_uiNOE_075x_8AO | UINT | 1 | SIZEOF( gc_DD_075x_8AO ) / SIZEOF( typeDataDesc ); |

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 26.02.2024 | 1.0.1.2 | u0103719 | modified environment (SP16 Patch 3) |
| 24.10.2023 | 1.0.1.1 | u0103719 | replace SysTypes Interfaces via SysTypes2 Interfaces |
| 08.01.2019 | 1.0.1.0 | u015842 | Properties: free placeholder added |
| 19.01.2017 | 1.0.0.0 | HLR | global constants corrected and some added; internal type definitions deleted |
| 07.10.2015 | 0.0.0.9 | HLR | missing change in global variable ‘Info’ |
| 29.09.2015 | 0.0.0.8 | HLR | ‘WagoTypesCommon.library’ referenced via placeholder |
| 18.09.2015 | 0.0.0.7 | HLR | placeholder added |
| 08.07.2015 | 0.0.0.6 | HLR | brief description added to project information |
| 08.07.2015 | 0.0.0.5 | HLR | library ‘WagoSysKbusTerminalcontrol_Internal_Comon.library’ deleted |
| 06.07.2015 | 0.0.0.4 | HLR | interface ‘I_SetTerminalRef’ changed; data types added |
| 02.07.2015 | 0.0.0.3 | HLR | comments added/chaned; interfaces changed |
| 22.06.2015 | 0.0.0.2 | HLR | GCL Number of elements and interfaces added |
| 19.06.2015 | 0.0.0.1 | HLR | First version |

WagoTypesKbusTerminalControl.library

WagoTypesKbusTerminalControl.library

### Other Components


## 01 Inputs


- type075x_16DI_PD (STRUCT) - type075x_2AI_PD (STRUCT) - type075x_2DI_PD (STRUCT) - type075x_4AI_PD (STRUCT) - type075x_4DI_PD (STRUCT) - type075x_8AI_PD (STRUCT) - type075x_8DI_PD (STRUCT)

## 01 Inputs


- type0750_0493_I_PD (STRUCT) - type0750_0652_I_08_PD (ALIAS) - type0750_0652_I_24_PD (ALIAS) - type0750_0652_I_48_PD (ALIAS) - type0753_0647_I_PD (ALIAS)

## 01 Inputs


- type0750_0493_I (STRUCT) - type0750_0652_I_08 (ALIAS) - type0750_0652_I_24 (ALIAS) - type0750_0652_I_48 (ALIAS) - type0753_0647_I (ALIAS)

## 01 Specific


- 01 Inputs type0750_0493_I_PD (STRUCT) - type0750_0652_I_08_PD (ALIAS) - type0750_0652_I_24_PD (ALIAS) - type0750_0652_I_48_PD (ALIAS) - type0753_0647_I_PD (ALIAS) 02 Outputs - type0750_0493_O_PD (STRUCT) - type0750_0652_O_08_PD (ALIAS) - type0750_0652_O_24_PD (ALIAS) - type0750_0652_O_48_PD (ALIAS) - type0753_0647_O_PD (ALIAS)

## 01 Specific


- 01 Inputs type0750_0493_I (STRUCT) - type0750_0652_I_08 (ALIAS) - type0750_0652_I_24 (ALIAS) - type0750_0652_I_48 (ALIAS) - type0753_0647_I (ALIAS) 02 Outputs - type0750_0493_O (STRUCT) - type0750_0652_O_08 (ALIAS) - type0750_0652_O_24 (ALIAS) - type0750_0652_O_48 (ALIAS) - type0753_0647_O (ALIAS)

## 01 Structured Data SD


- 01 Specific 01 Inputs type0750_0493_I (STRUCT) - type0750_0652_I_08 (ALIAS) - type0750_0652_I_24 (ALIAS) - type0750_0652_I_48 (ALIAS) - type0753_0647_I (ALIAS) 02 Outputs - type0750_0493_O (STRUCT) - type0750_0652_O_08 (ALIAS) - type0750_0652_O_24 (ALIAS) - type0750_0652_O_48 (ALIAS) - type0753_0647_O (ALIAS)

## 02 Generic


- 01 Inputs type075x_16DI_PD (STRUCT) - type075x_2AI_PD (STRUCT) - type075x_2DI_PD (STRUCT) - type075x_4AI_PD (STRUCT) - type075x_4DI_PD (STRUCT) - type075x_8AI_PD (STRUCT) - type075x_8DI_PD (STRUCT) 02 Outputs - type075x_16DO_PD (STRUCT) - type075x_2AO_PD (STRUCT) - type075x_2DO_PD (STRUCT) - type075x_4AO_PD (STRUCT) - type075x_4DO_PD (STRUCT) - type075x_8AO_PD (STRUCT) - type075x_8DO_PD (STRUCT)

## 02 Outputs


- type0750_0493_O (STRUCT) - type0750_0652_O_08 (ALIAS) - type0750_0652_O_24 (ALIAS) - type0750_0652_O_48 (ALIAS) - type0753_0647_O (ALIAS)

## 02 Outputs


- type0750_0493_O_PD (STRUCT) - type0750_0652_O_08_PD (ALIAS) - type0750_0652_O_24_PD (ALIAS) - type0750_0652_O_48_PD (ALIAS) - type0753_0647_O_PD (ALIAS)

## 02 Outputs


- type075x_16DO_PD (STRUCT) - type075x_2AO_PD (STRUCT) - type075x_2DO_PD (STRUCT) - type075x_4AO_PD (STRUCT) - type075x_4DO_PD (STRUCT) - type075x_8AO_PD (STRUCT) - type075x_8DO_PD (STRUCT)

## 02 Packed Structures PD


- 01 Specific 01 Inputs type0750_0493_I_PD (STRUCT) - type0750_0652_I_08_PD (ALIAS) - type0750_0652_I_24_PD (ALIAS) - type0750_0652_I_48_PD (ALIAS) - type0753_0647_I_PD (ALIAS) 02 Outputs - type0750_0493_O_PD (STRUCT) - type0750_0652_O_08_PD (ALIAS) - type0750_0652_O_24_PD (ALIAS) - type0750_0652_O_48_PD (ALIAS) - type0753_0647_O_PD (ALIAS) 02 Generic - 01 Inputs type075x_16DI_PD (STRUCT) - type075x_2AI_PD (STRUCT) - type075x_2DI_PD (STRUCT) - type075x_4AI_PD (STRUCT) - type075x_4DI_PD (STRUCT) - type075x_8AI_PD (STRUCT) - type075x_8DI_PD (STRUCT) 02 Outputs - type075x_16DO_PD (STRUCT) - type075x_2AO_PD (STRUCT) - type075x_2DO_PD (STRUCT) - type075x_4AO_PD (STRUCT) - type075x_4DO_PD (STRUCT) - type075x_8AO_PD (STRUCT) - type075x_8DO_PD (STRUCT)

## 03 Common


- eDATA_SIZE_TYPE (ENUM) - typeDataDesc (STRUCT)

## 23 Interfaces


- I_SetTerminalRef (ITF) I_SetTerminalRef.AllocateProcessData_PS (METH) - I_SetTerminalRef.AllocateProcessData_SD (METH) - I_SetTerminalRef.FreeProcessData (METH) - I_SetTerminalRef.Start_PDE_In_CurrentTask (METH) - I_SetTerminalRef.Stop_PDE (METH)

## 40 Data Types


- 01 Structured Data SD 01 Specific 01 Inputs type0750_0493_I (STRUCT) - type0750_0652_I_08 (ALIAS) - type0750_0652_I_24 (ALIAS) - type0750_0652_I_48 (ALIAS) - type0753_0647_I (ALIAS) 02 Outputs - type0750_0493_O (STRUCT) - type0750_0652_O_08 (ALIAS) - type0750_0652_O_24 (ALIAS) - type0750_0652_O_48 (ALIAS) - type0753_0647_O (ALIAS) 02 Packed Structures PD - 01 Specific 01 Inputs type0750_0493_I_PD (STRUCT) - type0750_0652_I_08_PD (ALIAS) - type0750_0652_I_24_PD (ALIAS) - type0750_0652_I_48_PD (ALIAS) - type0753_0647_I_PD (ALIAS) 02 Outputs - type0750_0493_O_PD (STRUCT) - type0750_0652_O_08_PD (ALIAS) - type0750_0652_O_24_PD (ALIAS) - type0750_0652_O_48_PD (ALIAS) - type0753_0647_O_PD (ALIAS) 02 Generic - 01 Inputs type075x_16DI_PD (STRUCT) - type075x_2AI_PD (STRUCT) - type075x_2DI_PD (STRUCT) - type075x_4AI_PD (STRUCT) - type075x_4DI_PD (STRUCT) - type075x_8AI_PD (STRUCT) - type075x_8DI_PD (STRUCT) 02 Outputs - type075x_16DO_PD (STRUCT) - type075x_2AO_PD (STRUCT) - type075x_2DO_PD (STRUCT) - type075x_4AO_PD (STRUCT) - type075x_4DO_PD (STRUCT) - type075x_8AO_PD (STRUCT) - type075x_8DO_PD (STRUCT) 03 Common - eDATA_SIZE_TYPE (ENUM) - typeDataDesc (STRUCT) DataDescriptions (GVL) NoOfEntriesInDataDesc (GVL)

## eDATA_SIZE_TYPE (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| TYPE_1_BYTE | INT_TO_WORD(TYPE_BYTE) | for data types which allocate one byte e.g.: TYPE_BYTE, TYPE_SINT, TYPE_USINT, ... |
| TYPE_2_BYTE | INT_TO_WORD(TYPE_WORD) | for data types which allocate two bytes e.g.: TYPE_WORD, TYPE_INT, TYPE_UINT, ... |
| TYPE_4_BYTE | INT_TO_WORD(TYPE_DWORD) | for data types which allocate four bytes e.g.: TYPE_DWORD, TYPE_DINT, TYPE_UDINT, REAL, ... |
| TYPE_8_BYTE | INT_TO_WORD(TYPE_LWORD) | for data types which allocate eight bytes e.g.: TYPE_LWORD, TYPE_LINT, TYPE_ULINT, LREAL, ... |

## type0750_0493_I (STRUCT)


| Name | Type |
| --- | --- |
| Status1 | BYTE |
| Channel1 | WORD |
| Status2 | BYTE |
| Channel2 | WORD |
| Status3 | BYTE |
| Channel3 | WORD |

## type0750_0493_I_PD (STRUCT)


| Name | Type |
| --- | --- |
| Status1 | BYTE |
| Channel1 | WORD |
| Status2 | BYTE |
| Channel2 | WORD |
| Status3 | BYTE |
| Channel3 | WORD |

## type0750_0493_O (STRUCT)


| Name | Type |
| --- | --- |
| Control1 | BYTE |
| Channel1 | WORD |
| Control2 | BYTE |
| Channel2 | WORD |
| Control3 | BYTE |
| Channel3 | WORD |

## type0750_0493_O_PD (STRUCT)


| Name | Type |
| --- | --- |
| Control1 | BYTE |
| Channel1 | WORD |
| Control2 | BYTE |
| Channel2 | WORD |
| Control3 | BYTE |
| Channel3 | WORD |

## type0750_0652_I_08 (ALIAS) ¶


## type0750_0652_I_08_PD (ALIAS) ¶


## type0750_0652_I_24 (ALIAS) ¶


## type0750_0652_I_24_PD (ALIAS) ¶


## type0750_0652_I_48 (ALIAS) ¶


## type0750_0652_I_48_PD (ALIAS) ¶


## type0750_0652_O_08 (ALIAS) ¶


## type0750_0652_O_08_PD (ALIAS) ¶


## type0750_0652_O_24 (ALIAS) ¶


## type0750_0652_O_24_PD (ALIAS) ¶


## type0750_0652_O_48 (ALIAS) ¶


## type0750_0652_O_48_PD (ALIAS) ¶


## type0753_0647_I (ALIAS) ¶


## type0753_0647_I_PD (ALIAS) ¶


## type0753_0647_O (ALIAS) ¶


## type0753_0647_O_PD (ALIAS) ¶


## type075x_16DI_PD (STRUCT)


| Name | Type |
| --- | --- |
| DI1 | BIT |
| DI2 | BIT |
| DI3 | BIT |
| DI4 | BIT |
| DI5 | BIT |
| DI6 | BIT |
| DI7 | BIT |
| DI8 | BIT |
| DI9 | BIT |
| DI10 | BIT |
| DI11 | BIT |
| DI12 | BIT |
| DI13 | BIT |
| DI14 | BIT |
| DI15 | BIT |
| DI16 | BIT |

## type075x_16DO_PD (STRUCT)


| Name | Type |
| --- | --- |
| DO1 | BIT |
| DO2 | BIT |
| DO3 | BIT |
| DO4 | BIT |
| DO5 | BIT |
| DO6 | BIT |
| DO7 | BIT |
| DO8 | BIT |
| DO9 | BIT |
| DO10 | BIT |
| DO11 | BIT |
| DO12 | BIT |
| DO13 | BIT |
| DO14 | BIT |
| DO15 | BIT |
| DO16 | BIT |

## type075x_2AI_PD (STRUCT)


| Name | Type |
| --- | --- |
| AI1 | WORD |
| AI2 | WORD |

## type075x_2AO_PD (STRUCT)


| Name | Type |
| --- | --- |
| AO1 | WORD |
| AO2 | WORD |

## type075x_2DI_PD (STRUCT)


| Name | Type |
| --- | --- |
| DI1 | BIT |
| DI2 | BIT |

## type075x_2DO_PD (STRUCT)


| Name | Type |
| --- | --- |
| DO1 | BIT |
| DO2 | BIT |

## type075x_4AI_PD (STRUCT)


| Name | Type |
| --- | --- |
| AI1 | WORD |
| AI2 | WORD |
| AI3 | WORD |
| AI4 | WORD |

## type075x_4AO_PD (STRUCT)


| Name | Type |
| --- | --- |
| AO1 | WORD |
| AO2 | WORD |
| AO3 | WORD |
| AO4 | WORD |

## type075x_4DI_PD (STRUCT)


| Name | Type |
| --- | --- |
| DI1 | BIT |
| DI2 | BIT |
| DI3 | BIT |
| DI4 | BIT |

## type075x_4DO_PD (STRUCT)


| Name | Type |
| --- | --- |
| DO1 | BIT |
| DO2 | BIT |
| DO3 | BIT |
| DO4 | BIT |

## type075x_8AI_PD (STRUCT)


| Name | Type |
| --- | --- |
| AI1 | WORD |
| AI2 | WORD |
| AI3 | WORD |
| AI4 | WORD |
| AI5 | WORD |
| AI6 | WORD |
| AI7 | WORD |
| AI8 | WORD |

## type075x_8AO_PD (STRUCT)


| Name | Type |
| --- | --- |
| AO1 | WORD |
| AO2 | WORD |
| AO3 | WORD |
| AO4 | WORD |
| AO5 | WORD |
| AO6 | WORD |
| AO7 | WORD |
| AO8 | WORD |

## type075x_8DI_PD (STRUCT)


| Name | Type |
| --- | --- |
| DI1 | BIT |
| DI2 | BIT |
| DI3 | BIT |
| DI4 | BIT |
| DI5 | BIT |
| DI6 | BIT |
| DI7 | BIT |
| DI8 | BIT |

## type075x_8DO_PD (STRUCT)


| Name | Type |
| --- | --- |
| DO1 | BIT |
| DO2 | BIT |
| DO3 | BIT |
| DO4 | BIT |
| DO5 | BIT |
| DO6 | BIT |
| DO7 | BIT |
| DO8 | BIT |

## typeDataDesc (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| eType | eDATA_SIZE_TYPE | size type of data element |
| wNumber | WORD | number of data elements |