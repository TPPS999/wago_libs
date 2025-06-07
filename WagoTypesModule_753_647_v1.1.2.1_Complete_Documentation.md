# WagoTypesModule_753_647 v1.1.2.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesModule_753_647
- **Version:** 1.1.2.1
- **Categories:** WAGO LayerView|Types and Interfaces
- **Namespace:** WagoTypesModule_753_647
- **Author:** WAGO / u010729
- **Placeholder:** WagoTypesModule_753_647

### Description ¶


This document is automatically generated.

This library defines the Interface to the DALI-Multi-Master Module 753-647

This document is automatically generated. This library defines the Interface to the DALI-Multi-Master Module 753-647

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Methods I_Port_753_647.BusReset (PROP) - I_Port_753_647.GetActualLevel (METH) - I_Port_753_647.GetAllActualLevels (PROP) - I_Port_753_647.GetResponseData (METH) - I_Port_753_647.GetSensorEvent (METH) - I_Port_753_647.GetSensorValue (METH) - I_Port_753_647.ModuleReset (PROP) - I_Port_753_647.ReadShortAddress (PROP) - I_Port_753_647.ResetEventData (METH) - I_Port_753_647.SetActualLevel (METH) - ... and 3 more Interfaces - I_Port_753_647 (ITF) - I_Port_753_647_ext_1 (ITF) Global Variable Lists Other Components - 10 Data Types - 12 Interfaces - 20 Program Orgarnisation Units - I_Port_753_647.AvailableShortAddresses (PROP) - I_Port_753_647.CommandToken (PROP) - I_Port_753_647.Firmware (PROP) - I_Port_753_647.Sequence_ID (PROP) - I_Port_753_647.StableCommunication (PROP) - I_Port_753_647.StatusModul (PROP) - I_Port_753_647_ext_1.AddressingIsRunning (PROP) - ... and 2 more

### Indices and tables ¶


Based on WagoTypesModule_753_647.library, last modified 20.09.2024, 21:34:07. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesModule_753_647.library, last modified 20.09.2024, 21:34:07. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesModule_753_647 Library Documentation


| Company: | WAGO |
| Title: | WagoTypesModule_753_647 |
| Version: | 1.1.2.1 |
| Categories: | WAGO LayerView\|Types and Interfaces |
| Namespace: | WagoTypesModule_753_647 |
| Author: | WAGO / u010729 |
| Placeholder: | WagoTypesModule_753_647 |

### Description


This document is automatically generated.

This library defines the Interface to the DALI-Multi-Master Module 753-647

This document is automatically generated. This library defines the Interface to the DALI-Multi-Master Module 753-647

### Contents:


- 20 Program Orgarnisation Units 10 Data Types - 12 Interfaces - ParameterList (PARAMS) VersionHistory (GVL)

### Indices and tables


Based on WagoTypesModule_753_647.library, last modified 20.09.2024, 21:34:07. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesModule_753_647.library, last modified 20.09.2024, 21:34:07. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesModule_753_647.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 20.09.2024, 21:34:07 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 20.09.2024, 21:34:07 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u010729 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesModule_753_647 |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesModule_753_647 |
| DefaultNamespace | WagoTypesModule_753_647 |
| Version | version | 1.1.2.1 |
| Title | string | WagoTypesModule_753_647 |
| Released | bool | False |
| LibraryCategories | library-category-list | WAGO LayerView\|Types and Interfaces |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : Library Parameter : Parameter: MAX_MBX_SIZE = 18

### Methods


## I_Port_753_647.BusReset (PROP) ¶


## I_Port_753_647.GetActualLevel (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetActualLevel | BYTE |  |
| Input | bIndex | BYTE | Index of the actual dim level array (0-63 = short address; 64 - 95 = group; 96 = broadcast) |

## I_Port_753_647.GetAllActualLevels (PROP) ¶


## I_Port_753_647.GetResponseData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetResponseData | typDaliResponse |  |
| Input | bIndex | BYTE | Number of the response |

## I_Port_753_647.GetSensorEvent (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | GetSensorEvent | BOOL |  |  |
| Input | bSensorType | BYTE | 1 | Sensor type (Sensor Type 1 = Osram; Sensor Type 2 = Tridonic) |
| bShortAddress | BYTE |  | Short address of the sensor |

## I_Port_753_647.GetSensorValue (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | GetSensorValue | DWORD |  |  |
| Input | bSensorType | BYTE | 1 | Sensor type (Sensor Type 1 = Osram; Sensor Type 2 = Tridonic) |
| bShortAddress | BYTE |  | Short address of the sensor |

## I_Port_753_647.ModuleReset (PROP) ¶


## I_Port_753_647.ReadShortAddress (PROP) ¶


## I_Port_753_647.ResetEventData (METH) ¶


## I_Port_753_647.SetActualLevel (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | bIndex | BYTE | Index of the actual dim level array (0-63 = short address; 64 - 95 = group; 96 = broadcast) |
| bValue | BYTE | Actual dim level as raw value |

## I_Port_753_647.SetResponseData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | bIndex | BYTE | Number of the response |
| typDaliResponse | typDaliResponse | data |

## I_Port_753_647.SetSensorEvent (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Input | bSensorType | BYTE | 1 | Sensor type (Sensor Type 1 = Osram; Sensor Type 2 = Tridonic) |
| bShortAddress | BYTE |  | Short address of the sensor |

## I_Port_753_647.SetSensorValues (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Input | bSensorType | BYTE | 1 | Sensor type (Sensor Type 1 = Osram; Sensor Type 2 = Tridonic) |
| bShortAddress | BYTE |  | Short address of the sensor |
| dwSensorValue | DWORD |  | Actual sensor value as raw value; DWORD for DALI2 |

### Interfaces


## I_Port_753_647 (ITF)


- I_Port_753_647.AvailableShortAddresses (PROP) - I_Port_753_647.BusReset (PROP) - I_Port_753_647.CommandToken (PROP) - I_Port_753_647.Firmware (PROP) - I_Port_753_647.GetActualLevel (METH) - I_Port_753_647.GetAllActualLevels (PROP) - I_Port_753_647.GetResponseData (METH) - I_Port_753_647.GetSensorEvent (METH) - I_Port_753_647.GetSensorValue (METH) - I_Port_753_647.ModuleReset (PROP) - I_Port_753_647.ReadShortAddress (PROP) - I_Port_753_647.ResetEventData (METH) - I_Port_753_647.Sequence_ID (PROP) - I_Port_753_647.SetActualLevel (METH) - I_Port_753_647.SetResponseData (METH) - I_Port_753_647.SetSensorEvent (METH) - I_Port_753_647.SetSensorValues (METH) - I_Port_753_647.StableCommunication (PROP) - I_Port_753_647.StatusModul (PROP)

## I_Port_753_647_ext_1 (ITF)


- I_Port_753_647_ext_1.AddressingIsRunning (PROP)

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 11.07.2024 | 1.1.2.1 | u0103719 | update library compatibility (context: build server,compile file) |
| 30.08.2023 | 1.1.2.0 | u0105598 | Adding the AddressingIsRunning interface property (WAT-36000) |
| 08.01.2019 | 1.1.1.0 | u015842 | Properties: free placeholder added |
| 18.04.2018 | 1.1.0.1 | U015842 | new Property ActiveCommandChain |
| 03.01.2018 | 1.1.0.0 | U015842 | SensorValue 3 Byte for DALI2Sensors |
| 12.04.2017 | 1.0.0.1 | U10545 | License changed |
| 01.03.2016 | 1.0.0.0 | u010729 | Release 1 |

WagoTypesModule_753_647.library

Release Notes:

WagoTypesModule_753_647.library Release Notes:

### Other Components


## 10 Data Types ¶


- typDaliResponse (STRUCT)

## 12 Interfaces


- I_Port_753_647 (ITF) I_Port_753_647.AvailableShortAddresses (PROP) - I_Port_753_647.BusReset (PROP) - I_Port_753_647.CommandToken (PROP) - I_Port_753_647.Firmware (PROP) - I_Port_753_647.GetActualLevel (METH) - I_Port_753_647.GetAllActualLevels (PROP) - I_Port_753_647.GetResponseData (METH) - I_Port_753_647.GetSensorEvent (METH) - I_Port_753_647.GetSensorValue (METH) - I_Port_753_647.ModuleReset (PROP) - I_Port_753_647.ReadShortAddress (PROP) - I_Port_753_647.ResetEventData (METH) - I_Port_753_647.Sequence_ID (PROP) - I_Port_753_647.SetActualLevel (METH) - I_Port_753_647.SetResponseData (METH) - I_Port_753_647.SetSensorEvent (METH) - I_Port_753_647.SetSensorValues (METH) - I_Port_753_647.StableCommunication (PROP) - I_Port_753_647.StatusModul (PROP) I_Port_753_647_ext_1 (ITF) - I_Port_753_647_ext_1.AddressingIsRunning (PROP)

## 20 Program Orgarnisation Units


- 10 Data Types typDaliResponse (STRUCT) 12 Interfaces - I_Port_753_647 (ITF) I_Port_753_647.AvailableShortAddresses (PROP) - I_Port_753_647.BusReset (PROP) - I_Port_753_647.CommandToken (PROP) - I_Port_753_647.Firmware (PROP) - I_Port_753_647.GetActualLevel (METH) - I_Port_753_647.GetAllActualLevels (PROP) - I_Port_753_647.GetResponseData (METH) - I_Port_753_647.GetSensorEvent (METH) - I_Port_753_647.GetSensorValue (METH) - I_Port_753_647.ModuleReset (PROP) - I_Port_753_647.ReadShortAddress (PROP) - I_Port_753_647.ResetEventData (METH) - I_Port_753_647.Sequence_ID (PROP) - I_Port_753_647.SetActualLevel (METH) - I_Port_753_647.SetResponseData (METH) - I_Port_753_647.SetSensorEvent (METH) - I_Port_753_647.SetSensorValues (METH) - I_Port_753_647.StableCommunication (PROP) - I_Port_753_647.StatusModul (PROP) I_Port_753_647_ext_1 (ITF) - I_Port_753_647_ext_1.AddressingIsRunning (PROP) ParameterList (PARAMS)

## I_Port_753_647.AvailableShortAddresses (PROP) ¶


## I_Port_753_647.CommandToken (PROP) ¶


## I_Port_753_647.Firmware (PROP) ¶


## I_Port_753_647.Sequence_ID (PROP) ¶


## I_Port_753_647.StableCommunication (PROP) ¶


## I_Port_753_647.StatusModul (PROP) ¶


## I_Port_753_647_ext_1.AddressingIsRunning (PROP) ¶


## ParameterList (PARAMS)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | gp_MaxResponseData | BYTE | 70 | Max Datasize of an response |
| gp_MaxResponses | BYTE | 2 | Max. responses extract from the mailbox |

## typDaliResponse (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| uiLength | UINT | Length of the payload |
| bProtocol_ID | BYTE | Protocol ID |
| bSequence_ID | BYTE | Sequence ID (First Byte of the Payload) |
| bReturnCode | BYTE | Return code from the module |
| aData | ARRAY [0..gp_MaxResponseData] OF BYTE | Data |