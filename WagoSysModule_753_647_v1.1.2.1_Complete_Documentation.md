# WagoSysModule_753_647 v1.1.2.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysModule_753_647
- **Version:** 1.1.2.1
- **Categories:** WAGO LayerView|Sys
- **Namespace:** WagoSysModule_753_647
- **Author:** WAGO / u010729
- **Placeholder:** WagoSysModule_753_647

### Description ¶


This document is automatically generated.

This library allows the access to the DALI-Multi-Master Module 753-647

This document is automatically generated. This library allows the access to the DALI-Multi-Master Module 753-647

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks - Methods FbModule_753_647.BusReset (PROP) - FbModule_753_647.FB_exit (METH) - FbModule_753_647.FB_init (METH) - FbModule_753_647.GetActualLevel (METH) - FbModule_753_647.GetAllActualLevels (PROP) - FbModule_753_647.GetResponseData (METH) - FbModule_753_647.GetSensorEvent (METH) - FbModule_753_647.GetSensorValue (METH) - FbModule_753_647.ModuleReset (PROP) - FbModule_753_647.ReadShortAddress (PROP) - ... and 6 more Global Variable Lists Other Components - 20 Modules - 20 Program Orgarnisation Units - FbModule_753_647.AddressingIsRunning (PROP) - FbModule_753_647.AvailableShortAddresses (PROP) - FbModule_753_647.CommandToken (PROP) - FbModule_753_647.Firmware (PROP) - FbModule_753_647.Sequence_ID (PROP) - FbModule_753_647.StableCommunication (PROP) - FbModule_753_647.StatusModul (PROP) - I_Port_753_647 - ... and 3 more

### Indices and tables ¶


Based on WagoSysModule_753_647.library, last modified 20.09.2024, 21:34:10. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysModule_753_647.library, last modified 20.09.2024, 21:34:10. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysModule_753_647 Library Documentation


| Company: | WAGO |
| Title: | WagoSysModule_753_647 |
| Version: | 1.1.2.1 |
| Categories: | WAGO LayerView\|Sys |
| Namespace: | WagoSysModule_753_647 |
| Author: | WAGO / u010729 |
| Placeholder: | WagoSysModule_753_647 |

### Description


This document is automatically generated.

This library allows the access to the DALI-Multi-Master Module 753-647

This document is automatically generated. This library allows the access to the DALI-Multi-Master Module 753-647

### Contents:


- 20 Program Orgarnisation Units 20 Modules ParameterList (PARAMS) VersionHistory (GVL)

### Indices and tables


Based on WagoSysModule_753_647.library, last modified 20.09.2024, 21:34:10. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysModule_753_647.library, last modified 20.09.2024, 21:34:10. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysModule_753_647.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 20.09.2024, 21:34:11 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 20.09.2024, 21:34:10 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u010729 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoSysModule_753_647 |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysModule_753_647 |
| DefaultNamespace | WagoSysModule_753_647 |
| Version | version | 1.1.2.1 |
| Title | string | WagoSysModule_753_647 |
| Released | bool | False |
| LibraryCategories | library-category-list | WAGO LayerView\|Sys |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CmpApp Library Identification : Name: CmpApp Version: newest Company: System Namespace: CmpApp Library Properties : CmpErrors2 Interfaces Library Identification : Name: CmpErrors2 Interfaces Version: newest Company: System Namespace: CmpErrors Library Properties : CmpEventMgr Library Identification : Name: CmpEventMgr Version: newest Company: System Namespace: CmpEventMgr Library Properties : CmpIecTask Library Identification : Name: CmpIecTask Version: newest Company: System Namespace: CmpIecTask Library Properties : WagoSysModuleBase Library Identification : Placeholder: WagoSysModuleBase Default Resolution: WagoSysModuleBase, * (WAGO) Namespace: WagoSysModuleBase Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesModuleBase Library Identification : Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase Library Properties : WagoTypesModule_753_647 Library Identification : Placeholder: WagoTypesModule_753_647 Default Resolution: WagoTypesModule_753_647, * (WAGO) Namespace: WagoTypesModule_753_647 Library Properties :

### Function Blocks


## FbModule_753_647 (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Output | oError | WagoSysErrorBase.FbResult |  | FbModuleBase |
| CallBackCounter | UINT | callbacks from cycle control point | FbModuleMbx2 |

Interface variables - I_Port_753_647 FbModule_753_647.AvailableShortAddresses (PROP) - FbModule_753_647.BusReset (PROP) - FbModule_753_647.CommandToken (PROP) - FbModule_753_647.Firmware (PROP) - FbModule_753_647.GetActualLevel (METH) - FbModule_753_647.GetAllActualLevels (PROP) - FbModule_753_647.GetResponseData (METH) - FbModule_753_647.GetSensorEvent (METH) - FbModule_753_647.GetSensorValue (METH) - FbModule_753_647.ModuleReset (PROP) - FbModule_753_647.ReadShortAddress (PROP) - FbModule_753_647.ResetEventData (METH) - FbModule_753_647.Sequence_ID (PROP) - FbModule_753_647.SetActualLevel (METH) - FbModule_753_647.SetResponseData (METH) - FbModule_753_647.SetSensorEvent (METH) - FbModule_753_647.SetSensorValues (METH) - FbModule_753_647.StableCommunication (PROP) - FbModule_753_647.StatusModul (PROP) I_Port_753_647_ext_1 - FbModule_753_647.AddressingIsRunning (PROP) onStartPlc - init FbModule_753_647.FB_exit (METH) - FbModule_753_647.FB_init (METH)

### Methods


## FbModule_753_647.BusReset (PROP) ¶


## FbModule_753_647.FB_exit (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FB_exit | BOOL |  |
| Input | bInCopyCode | BOOL | TRUE: the exit method is called in order to leave the instance, which will be copied afterward (Online Change). |

## FbModule_753_647.FB_init (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FB_init | BOOL |  |
| Input | bInitRetains | BOOL | TRUE: the Retain-variables are initialized (reset warm / reset cold) |
| bInCopyCode | BOOL | TRUE the instance will be copied to the copy-code afterward (online change) |

## FbModule_753_647.GetActualLevel (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetActualLevel | BYTE |  |
| Input | bIndex | BYTE | Index of the actual dim level array (0-63 = short address; 64 - 95 = group; 96 = broadcast) |

## FbModule_753_647.GetAllActualLevels (PROP) ¶


## FbModule_753_647.GetResponseData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetResponseData | WagoTypesModule_753_647.typDaliResponse |  |
| Input | bIndex | BYTE | Number of the response |

## FbModule_753_647.GetSensorEvent (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | GetSensorEvent | BOOL |  |  |
| Input | bSensorType | BYTE | 1 | Sensor type (Sensor Type 1 = Osram; Sensor Type 2 = Tridonic) |
| bShortAddress | BYTE |  | Short address of the sensor |

## FbModule_753_647.GetSensorValue (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | GetSensorValue | DWORD |  |  |
| Input | bSensorType | BYTE | 1 | Sensor type (Sensor Type 1 = Osram; Sensor Type 2 = Tridonic) |
| bShortAddress | BYTE |  | Short address of the sensor |

## FbModule_753_647.ModuleReset (PROP) ¶


## FbModule_753_647.ReadShortAddress (PROP) ¶


## FbModule_753_647.ResetEventData (METH) ¶


## FbModule_753_647.SetActualLevel (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | bIndex | BYTE | Index of the actual dim level array (0-63 = short address; 64 - 95 = group; 96 = broadcast) |
| bValue | BYTE | Actual dim level as raw value |

## FbModule_753_647.SetResponseData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | bIndex | BYTE | Number of the response |
| typDaliResponse | typDaliResponse | data |

## FbModule_753_647.SetSensorEvent (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Input | bSensorType | BYTE | 1 | Sensor type (Sensor Type 1 = Osram; Sensor Type 2 = Tridonic) |
| bShortAddress | BYTE |  | Short address of the sensor |

## FbModule_753_647.SetSensorValues (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Input | bSensorType | BYTE | 1 | Sensor type (Sensor Type 1 = Osram; Sensor Type 2 = Tridonic) |
| bShortAddress | BYTE |  | Short address of the sensor |
| dwSensorValue | DWORD |  | Actual sensor value as raw value; DWORD for DALI2 |

## onStartPlc


- init FbModule_753_647.FB_exit (METH) - FbModule_753_647.FB_init (METH)

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | WagoSysVersion.ProjectInfo |

| date | version | author | change |
| 11.07.2024 | 1.1.2.1 | u0103719 | update library file (context: build server,compile file) |
| 30.08.2023 | 1.1.2.0 | u0105598 | Adding the AddressingIsRunning property (WAT-36000) |
| 01.03.2022 | 1.1.1.1 | u010663 | cmpErrorInterface2 inserted |
| 08.01.2019 | 1.0.1.0 | u015842 | Properties: free placeholder added |
| 16.10.2018 | 1.1.0.2 | U015842 | Mailbox init to module changed |
| 18.04.2018 | 1.1.0.1 | U015842 | new Property CommandToken |
| 03.01.2018 | 1.1.0.0 | U015842 | SensorValue DWORD for DALI2Sensors |
| 27.09.2017 | 1.0.1.1 | U10545 | Workaround for MBX2 |
| 05.05.2017 | 1.0.1.0 | U10545 | Compilerversion updated to 3.5.9.0 and license changed |
| 13.04.2016 | 1.0.0.2 | u010729 | Debug Mode eingefügt |
| 01.03.2016 | 1.0.0.1 | u010729 | Release |

WagoSysModule_753_647.library

Release Notes:

WagoSysModule_753_647.library Release Notes:

### Other Components


## 20 Modules


- FbModule_753_647 (FB) I_Port_753_647 FbModule_753_647.AvailableShortAddresses (PROP) - FbModule_753_647.BusReset (PROP) - FbModule_753_647.CommandToken (PROP) - FbModule_753_647.Firmware (PROP) - FbModule_753_647.GetActualLevel (METH) - FbModule_753_647.GetAllActualLevels (PROP) - FbModule_753_647.GetResponseData (METH) - FbModule_753_647.GetSensorEvent (METH) - FbModule_753_647.GetSensorValue (METH) - FbModule_753_647.ModuleReset (PROP) - FbModule_753_647.ReadShortAddress (PROP) - FbModule_753_647.ResetEventData (METH) - FbModule_753_647.Sequence_ID (PROP) - FbModule_753_647.SetActualLevel (METH) - FbModule_753_647.SetResponseData (METH) - FbModule_753_647.SetSensorEvent (METH) - FbModule_753_647.SetSensorValues (METH) - FbModule_753_647.StableCommunication (PROP) - FbModule_753_647.StatusModul (PROP) I_Port_753_647_ext_1 - FbModule_753_647.AddressingIsRunning (PROP) onStartPlc - init FbModule_753_647.FB_exit (METH) - FbModule_753_647.FB_init (METH)

## 20 Program Orgarnisation Units


- 20 Modules FbModule_753_647 (FB) I_Port_753_647 FbModule_753_647.AvailableShortAddresses (PROP) - FbModule_753_647.BusReset (PROP) - FbModule_753_647.CommandToken (PROP) - FbModule_753_647.Firmware (PROP) - FbModule_753_647.GetActualLevel (METH) - FbModule_753_647.GetAllActualLevels (PROP) - FbModule_753_647.GetResponseData (METH) - FbModule_753_647.GetSensorEvent (METH) - FbModule_753_647.GetSensorValue (METH) - FbModule_753_647.ModuleReset (PROP) - FbModule_753_647.ReadShortAddress (PROP) - FbModule_753_647.ResetEventData (METH) - FbModule_753_647.Sequence_ID (PROP) - FbModule_753_647.SetActualLevel (METH) - FbModule_753_647.SetResponseData (METH) - FbModule_753_647.SetSensorEvent (METH) - FbModule_753_647.SetSensorValues (METH) - FbModule_753_647.StableCommunication (PROP) - FbModule_753_647.StatusModul (PROP) I_Port_753_647_ext_1 - FbModule_753_647.AddressingIsRunning (PROP) onStartPlc - init FbModule_753_647.FB_exit (METH) - FbModule_753_647.FB_init (METH)

## FbModule_753_647.AddressingIsRunning (PROP) ¶


## FbModule_753_647.AvailableShortAddresses (PROP) ¶


## FbModule_753_647.CommandToken (PROP) ¶


## FbModule_753_647.Firmware (PROP) ¶


## FbModule_753_647.Sequence_ID (PROP) ¶


## FbModule_753_647.StableCommunication (PROP) ¶


## FbModule_753_647.StatusModul (PROP) ¶


## I_Port_753_647


- FbModule_753_647.AvailableShortAddresses (PROP) - FbModule_753_647.BusReset (PROP) - FbModule_753_647.CommandToken (PROP) - FbModule_753_647.Firmware (PROP) - FbModule_753_647.GetActualLevel (METH) - FbModule_753_647.GetAllActualLevels (PROP) - FbModule_753_647.GetResponseData (METH) - FbModule_753_647.GetSensorEvent (METH) - FbModule_753_647.GetSensorValue (METH) - FbModule_753_647.ModuleReset (PROP) - FbModule_753_647.ReadShortAddress (PROP) - FbModule_753_647.ResetEventData (METH) - FbModule_753_647.Sequence_ID (PROP) - FbModule_753_647.SetActualLevel (METH) - FbModule_753_647.SetResponseData (METH) - FbModule_753_647.SetSensorEvent (METH) - FbModule_753_647.SetSensorValues (METH) - FbModule_753_647.StableCommunication (PROP) - FbModule_753_647.StatusModul (PROP)

## I_Port_753_647_ext_1


- FbModule_753_647.AddressingIsRunning (PROP)

## ParameterList (PARAMS)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | DEBUG_MODE | BOOL | FALSE |

## init


- FbModule_753_647.FB_exit (METH) - FbModule_753_647.FB_init (METH)