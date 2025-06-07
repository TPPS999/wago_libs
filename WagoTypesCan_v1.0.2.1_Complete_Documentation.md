# WagoTypesCan v1.0.2.1 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesCan
- **Version:** 1.0.2.1
- **Categories:** WAGO FunctionalView|Connectivity|FieldBus; WAGO LayerView|Types and Interfaces; WAGO Internal|Feature|Fieldbus|CAN; Application
- **Namespace:** WagoTypesCan
- **Author:** AWü / WAGO
- **Placeholder:** WagoTypesCan

### Description ¶


This document is automatically generated.

Type Definitions for CAN-instances

This document is automatically generated. Type Definitions for CAN-instances

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Methods Can Open Types - I_WagoSysCanBase.CloseLayer2 (METH) - I_WagoSysCanBase.GetBusInfo (METH) - I_WagoSysCanBase.GetCanMode (METH) - I_WagoSysCanBase.GetDeviceInfo (METH) - I_WagoSysCanBase.GetFrame (METH) - I_WagoSysCanBase.GetFrameBuffer (METH) - I_WagoSysCanBase.GetFrameCounter (METH) - I_WagoSysCanBase.LibVersion (METH) - I_WagoSysCanBase.OpenLayer2 (METH) - ... and 26 more Interfaces - I_WagoSysCanBase (ITF) - I_WagoSysCanOpen (ITF) Internal Components Global Variable Lists Other Components - Can LED - Device - eCanDeviceError (ENUM) - eCanFlagRegister (ENUM) - eCanFnReturn (ENUM) - eCanLedMode (ENUM) - eCanMode (ENUM) - typCanBusInfo (STRUCT) - typCanDeviceInfo (STRUCT) - typCanTimestamp (STRUCT)

### Indices and tables ¶


Based on WagoTypesCan.library, last modified 29.05.2024, 19:55:59. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesCan.library, last modified 29.05.2024, 19:55:59. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesCan Library Documentation


| Company: | WAGO |
| Title: | WagoTypesCan |
| Version: | 1.0.2.1 |
| Categories: | WAGO FunctionalView\|Connectivity\|FieldBus; WAGO LayerView\|Types and Interfaces; WAGO Internal\|Feature\|Fieldbus\|CAN; Application |
| Namespace: | WagoTypesCan |
| Author: | AWü / WAGO |
| Placeholder: | WagoTypesCan |

### Description


This document is automatically generated.

Type Definitions for CAN-instances

This document is automatically generated. Type Definitions for CAN-instances

### Contents:


- Can LED eCanLedMode (ENUM) Can Open Types - eCanInternalState (ENUM) - eCanOpenState (ENUM) - typCanTimestamp (STRUCT) Device - eCanDeviceError (ENUM) - eCanFlagRegister (ENUM) - eCanFlagReset (ENUM) - eCanFnReturn (ENUM) - eCanMode (ENUM) - typCanBusInfo (STRUCT) - typCanDeviceInfo (STRUCT) I_WagoSysCanBase (ITF) - I_WagoSysCanBase.CloseLayer2 (METH) - I_WagoSysCanBase.GetBusInfo (METH) - I_WagoSysCanBase.GetCanMode (METH) - I_WagoSysCanBase.GetDeviceInfo (METH) - I_WagoSysCanBase.GetFrame (METH) - I_WagoSysCanBase.GetFrameBuffer (METH) - I_WagoSysCanBase.GetFrameCounter (METH) - I_WagoSysCanBase.LibVersion (METH) - I_WagoSysCanBase.OpenLayer2 (METH) - I_WagoSysCanBase.RegisterAll (METH) - I_WagoSysCanBase.RegisterId (METH) - I_WagoSysCanBase.ResetLayer2 (METH) - I_WagoSysCanBase.SendFrame (METH) - I_WagoSysCanBase.SetCanLed (METH) - I_WagoSysCanBase.SetDeviceInfo (METH) I_WagoSysCanOpen (ITF) - I_WagoSysCanOpen.ChangeState (METH) - I_WagoSysCanOpen.GetEmcy (METH) - I_WagoSysCanOpen.GetLastNode (METH) - I_WagoSysCanOpen.GetNodeDiag (METH) - I_WagoSysCanOpen.GetNodeEmcy (METH) - I_WagoSysCanOpen.GetNodeId (METH) - I_WagoSysCanOpen.GetTimestamp (METH) - I_WagoSysCanOpen.GuardError (METH) - I_WagoSysCanOpen.GuardErrorNode (METH) - I_WagoSysCanOpen.SdoAdd (METH) - I_WagoSysCanOpen.SdoReadAsync (METH) - I_WagoSysCanOpen.SdoReadData (METH) - I_WagoSysCanOpen.SdoReadSync (METH) - I_WagoSysCanOpen.SdoWriteAsync (METH) - I_WagoSysCanOpen.SdoWriteData (METH) - I_WagoSysCanOpen.SdoWriteSync (METH) - I_WagoSysCanOpen.SendEmcy (METH) - I_WagoSysCanOpen.SendTimestamp (METH) VersionHistory (GVL)

### Indices and tables


Based on WagoTypesCan.library, last modified 29.05.2024, 19:55:59. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesCan.library, last modified 29.05.2024, 19:55:59. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesCan.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:55:59 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:55:59 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | AWü / WAGO |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesCan |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesCan |
| DefaultNamespace | WagoTypesCan |
| Version | version | 1.0.2.1 |
| Title | string | WagoTypesCan |
| LibraryCategories | library-category-list | WAGO FunctionalView\|Connectivity\|FieldBus; WAGO LayerView\|Types and Interfaces; WAGO Internal\|Feature\|Fieldbus\|CAN; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties :

### Methods


## Can Open Types


- eCanInternalState (ENUM) - eCanOpenState (ENUM) - typCanTimestamp (STRUCT)

## I_WagoSysCanBase.CloseLayer2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | CloseLayer2 | eCanDeviceError |

Close CAN Layer2 Device

Returns: 0 = OK -1 = fail -6 not ready

Interface variables Close CAN Layer2 Device Returns: 0 = OK -1 = fail -6 not ready

## I_WagoSysCanBase.GetBusInfo (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetBusInfo | eCanFnReturn |  |
| Input | eResetflags | eCanFlagReset | reset error counters |
| Inout | typBusInfo | typCanBusInfo | CAN status struct |

Get CAN info struct

Returns: 0: OK -1: no active CAN device

Interface variables Get CAN info struct Returns: 0: OK -1: no active CAN device

## I_WagoSysCanBase.GetCanMode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetCanMode | eCanMode |

Get CAN device operational mode

Returns: 0: not used 1:CANopen Master 2:CANopen Local Device 3:CAN Layer2 Device 4:CAN Gateway on KBus

Interface variables Get CAN device operational mode Returns: 0: not used 1:CANopen Master 2:CANopen Local Device 3:CAN Layer2 Device 4:CAN Gateway on KBus

## I_WagoSysCanBase.GetDeviceInfo (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetDeviceInfo | eCanFnReturn |  |
| Inout | typCanInfo | typCanDeviceInfo | device info struct |

Fill CAN device info struct

Interface variables Fill CAN device info struct Returns: 0

## I_WagoSysCanBase.GetFrame (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetFrame | DINT |  |
| Input | udiTimeout | UDINT | timeout in ms |
| Inout | dwId | DWORD | CAN Id (updated id RegisterAll(1) was set) |
| aMsg | ARRAY [1..8] OF BYTE | message buffer |

Get layer2 frame from registered Id

Returns: DLC of message, 16#10 for RTR call or eCanL2ErrorCode

Interface variables Get layer2 frame from registered Id Returns: DLC of message, 16#10 for RTR call or eCanL2ErrorCode

## I_WagoSysCanBase.GetFrameBuffer (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetFrameBuffer | DINT |  |
| Input | dwId | DWORD | CAN Id (ignored if RegisterAll(1) was set) |

Get number of frames in buffer from registered Id

Returns: number of frames in buffer (maximum 8) or -1 if error -2 if no index entry + 0x1000 if buffer overflow

Interface variables Get number of frames in buffer from registered Id Returns: number of frames in buffer (maximum 8) or -1 if error -2 if no index entry + 0x1000 if buffer overflow

## I_WagoSysCanBase.GetFrameCounter (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetFrameCounter | DINT |  |
| Input | dwId | DWORD | CAN Id (ignored if RegisterAll(1) was set) |

Get layer2 frame counter for registered Id

Returns: 16 bit frame counter or -1 if error -2 if no index entry

Interface variables Get layer2 frame counter for registered Id Returns: 16 bit frame counter or -1 if error -2 if no index entry

## I_WagoSysCanBase.LibVersion (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | LibVersion | UDINT |

Return version of library interface in firmware

Interface variables Return version of library interface in firmware

## I_WagoSysCanBase.OpenLayer2 (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | OpenLayer2 | eCanDeviceError |  |
| Input | udiBaudrate | UDINT | baudrate in baud valid is 100baud...1Mbaud 0 = auto if supported |
| dwFlags | DWORD | reserved for future use |
| udiBusNr | UDINT | reserved for future use |

Open CAN connection in layer2 mode

Returns: 0 = OK -1 = fail -4 invalid baudrate -5 invalid port -6 not ready (error)

Interface variables Open CAN connection in layer2 mode Returns: 0 = OK -1 = fail -4 invalid baudrate -5 invalid port -6 not ready (error)

## I_WagoSysCanBase.RegisterAll (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | RegisterAll | eCanFnReturn |
| Input | eRegflag | eCanFlagRegister |

Register or unregister all Ids for layer2 rx

Returns: 0 = OK -1 = fail

Warning: all incoming messages must be handled by the application

Interface variables Register or unregister all Ids for layer2 rx Returns: 0 = OK -1 = fail Warning: all incoming messages must be handled by the application

## I_WagoSysCanBase.RegisterId (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | RegisterId | eCanFnReturn |  |
| Input | eRegflag | eCanFlagRegister | register or unregister |
| dwId | DWORD | CAN Id + 16#80000000 if 29Bit Id |

Register or unregister Id for layer2 rx

Returns: 0 = OK -1 = device fail -2 = no free index in register or no index in unregister

Interface variables Register or unregister Id for layer2 rx Returns: 0 = OK -1 = device fail -2 = no free index in register or no index in unregister

## I_WagoSysCanBase.ResetLayer2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ResetLayer2 | eCanDeviceError |

Reset and restart CAN communication in layer2 mode

Returns: 0 = OK -1 = fail -6 not ready

Interface variables Reset and restart CAN communication in layer2 mode Returns: 0 = OK -1 = fail -6 not ready

## I_WagoSysCanBase.SendFrame (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SendFrame | eCanFnReturn |  |
| Input | dwId | DWORD | CAN Id + 16#80000000 if 29Bit Adress |
| dwDlc | DWORD | CAN Dlc or 16#10 for RTR Call |
| udiTimeout | UDINT | timeout in ms (not used in layer2 device) |
| aMsg | ARRAY [1..8] OF BYTE | message |

Send layer2 frame

Returns: 0: OK -1: no active CAN device -5: bus off or buffer full

Interface variables Send layer2 frame Returns: 0: OK -1: no active CAN device -5: bus off or buffer full

## I_WagoSysCanBase.SetCanLed (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetCanLed | eCanFnReturn |
| Input | eMode | eCanLedMode |

Set CAN LED

Returns: 0 = OK -1 = Fail

Interface variables Set CAN LED Returns: 0 = OK -1 = Fail

## I_WagoSysCanBase.SetDeviceInfo (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetDeviceInfo | eCanFnReturn |
| Inout | typCanInfo | typCanDeviceInfo |

Set/Reset DeviceLock in CAN device info struct Returns: 0

Interface variables Set/Reset DeviceLock in CAN device info struct Returns: 0

## I_WagoSysCanOpen.ChangeState (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ChangeState | eCanFnReturn |  |
| Input | udiNodeId | UDINT | Node Id of device |
| eState | eCanOpenState | State to set |

Change state of CANopen device or master (valid only for own node in slave mode)

Returns: 0 = OK -1 = fail

Interface variables Change state of CANopen device or master (valid only for own node in slave mode) Returns: 0 = OK -1 = fail

## I_WagoSysCanOpen.GetEmcy (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetEmcy | DINT |  |
| Input | eRemove | eCanFlagReset | 1 read and remove oldest message from list |
| Inout | aMsg | ARRAY [1..8] OF BYTE | EMC message |

Test for new emergency error on any slave in CANopen Manager Mode

Returns: 0 = no emcy message > 0 node id -1 failure

Interface variables Test for new emergency error on any slave in CANopen Manager Mode Returns: 0 = no emcy message > 0 node id -1 failure

## I_WagoSysCanOpen.GetLastNode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetLastNode | DINT |

Return number of configured node IDs on bus in CANopen Manager Mode or -1 if error

Interface variables Return number of configured node IDs on bus in CANopen Manager Mode or -1 if error

## I_WagoSysCanOpen.GetNodeDiag (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetNodeDiag | DWORD |
| Input | udiNodeId | UDINT |

Get node diagnostic bits in CANopen Manager Mode

Bitmask for return

16#0000 no slave diag entry 16#0001 node configuration: assigned slave 16#0002 node assigned and configured 16#0004 node configuration mismatch 16#0008 node diagnostic: emergency event active 16#0010 node state operational 16#0020 node is set to stopped 16#0040 node is set to preoperational 16#0080 inconsistent cDCF 16#0100 mismatch cDFC and slave`s object dictionary 16#0200 identity error >= 16#FFFF error in get node diag

Interface variables Get node diagnostic bits in CANopen Manager Mode Bitmask for return 16#0000 no slave diag entry 16#0001 node configuration: assigned slave 16#0002 node assigned and configured 16#0004 node configuration mismatch 16#0008 node diagnostic: emergency event active 16#0010 node state operational 16#0020 node is set to stopped 16#0040 node is set to preoperational 16#0080 inconsistent cDCF 16#0100 mismatch cDFC and slave`s object dictionary 16#0200 identity error >= 16#FFFF error in get node diag

## I_WagoSysCanOpen.GetNodeEmcy (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetNodeEmcy | eCanFnReturn |  |
| Input | udiNodeId | UDINT | node Id |
| eRemove | eCanFlagReset | clear message |
| Inout | aMsg | ARRAY [1..8] OF BYTE |  |

Test for Emcy message from node in CANopen Manager Mode

Returns: 0 = no emcy message 1 = message present -1 failure

Interface variables Test for Emcy message from node in CANopen Manager Mode Returns: 0 = no emcy message 1 = message present -1 failure

## I_WagoSysCanOpen.GetNodeId (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetNodeId | DINT |

Get own node Id of can device

Interface variables Get own node Id of can device

## I_WagoSysCanOpen.GetTimestamp (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetTimestamp | eCanFnReturn |
| Inout | typTimestamp | typCanTimestamp |

Get last timestamp

Returns: 0 = OK -1 = Fail

Interface variables Get last timestamp Returns: 0 = OK -1 = Fail

## I_WagoSysCanOpen.GuardError (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GuardError | DINT |

Test for guarding error on any slave (only tests own node in slave mode)

Returns: node Id of node with guarding error 0: no error -1 failure

Interface variables Test for guarding error on any slave (only tests own node in slave mode) Returns: node Id of node with guarding error 0: no error -1 failure

## I_WagoSysCanOpen.GuardErrorNode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GuardErrorNode | eCanFnReturn |
| Input | udiNodeId | UDINT |

Test for guarding error message from slave in CANopen Manager Mode

Returns: 0 = no guarding error message 1 = guarding error message from slave -1 failure

Interface variables Test for guarding error message from slave in CANopen Manager Mode Returns: 0 = no guarding error message 1 = guarding error message from slave -1 failure

## I_WagoSysCanOpen.SdoAdd (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SdoAdd | eCanFnReturn |  |
| Input | udiIndex | UDINT | 16#2000 spezial SDO no subindex size max 1536 byte |
| udiEntrys | UDINT | requested subindexes |
| udiBytes | UDINT | datalen in bytes of 1 subindex |
| udiSDOType | UDINT | data type |
| udiOffset | UDINT | position in parameter data (8192 Bytes) |

Function is called to add a User SDO

Returns: 0 = OK -1 = fail

Interface variables Function is called to add a User SDO Returns: 0 = OK -1 = fail

## I_WagoSysCanOpen.SdoReadAsync (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SdoReadAsync | DINT |  |
| Input | udiNodeId | UDINT | node id |
| udiIndex | UDINT | sdo index |
| udiSubindex | UDINT | sdo subindex |
| udiBytes | UDINT | pData size |
| udiTimeout | UDINT | timeout in ms |
| udiChannel | UDINT | channel number for parallel transfers (0...15) |
| pData | POINTER TO BYTE | sdo data |

Read CANopen SDOs without blocking process

< 0 Error Codes from eCanFnReturn

0.. udiBytes Call finished / bytes received

> 16#10000 SDO abort code

Interface variables Read CANopen SDOs without blocking process Returns < 0 Error Codes from eCanFnReturn 0.. udiBytes Call finished / bytes received > 16#10000 SDO abort code

## I_WagoSysCanOpen.SdoReadData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SdoReadData | eCanFnReturn |  |
| Input | udiIndex | UDINT | index |
| udiSubindex | UDINT | subindex |
| udiBytes | UDINT | datalen |
| pData | POINTER TO BYTE | sdo data |

Read from CANopen process data and parameter data SDOs

Returns: 0 = OK -1 = Fail

Interface variables Read from CANopen process data and parameter data SDOs Returns: 0 = OK -1 = Fail

## I_WagoSysCanOpen.SdoReadSync (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SdoReadSync | DINT |  |
| Input | udiNodeId | UDINT | node id |
| udiIndex | UDINT | index |
| udiSubindex | UDINT | subindex |
| udiBytes | UDINT | pData size |
| udiTimeout | UDINT | timeout in ms |
| pData | POINTER TO BYTE | sdo data |

Read CANopen SDOs with blocking process

Interface variables Read CANopen SDOs with blocking process Returns 0 Call finished < 0 Error Codes from eCanFnReturn > 16#10000 SDO abort code

## I_WagoSysCanOpen.SdoWriteAsync (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SdoWriteAsync | DINT |  |
| Input | udiNodeId | UDINT | node id |
| udiIndex | UDINT | sdo index |
| udiSubindex | UDINT | sdo subindex |
| udiBytes | UDINT | sdo bytes |
| udiTimeout | UDINT | timeout in ms |
| udiChannel | UDINT | channel number for parallel transfers (0...15) |
| pData | POINTER TO BYTE | sdo data |

Send CANopen SDOs without blocking process

Interface variables Send CANopen SDOs without blocking process Returns 0 // call finished < 0 // Error Codes from eCanFnReturn > 16#10000 // SDO abort code

## I_WagoSysCanOpen.SdoWriteData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SdoWriteData | eCanFnReturn |  |
| Input | udiIndex | UDINT | sdo index |
| udiSubindex | UDINT | sdo subindex |
| udiBytes | UDINT | sdo bytes |
| pData | POINTER TO BYTE | sdo data |

Write to CANopen process data and parameter data SDOs

Returns: 0 = OK -1 = fail

Interface variables Write to CANopen process data and parameter data SDOs Returns: 0 = OK -1 = fail

## I_WagoSysCanOpen.SdoWriteSync (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SdoWriteSync | DINT |  |
| Input | udiNodeId | UDINT | node id |
| udiIndex | UDINT | sdo index |
| udiSubindex | UDINT | sdo subindex |
| udiBytes | UDINT | sdo bytes |
| udiTimeout | UDINT | timeout in ms |
| pData | POINTER TO BYTE | sdo data |

Read CANopen SDOs with blocking process

< 0 Error Codes from eCanFnReturn > 16#10000 SDO abort code

Interface variables Read CANopen SDOs with blocking process Returns 0 Call finished < 0 Error Codes from eCanFnReturn > 16#10000 SDO abort code

## I_WagoSysCanOpen.SendEmcy (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SendEmcy | DINT |  |
| Input | dwCode | DWORD | EMC error code |
| dwRegister | DWORD | register 1001 |
| aMfsCode | ARRAY [1..5] OF BYTE | manufacture spec. error field |

Send emc message in CANopen Manager Mode

Returns: 0 = OK -1 = fail -2 = inhibit time not expired

Interface variables Send emc message in CANopen Manager Mode Returns: 0 = OK -1 = fail -2 = inhibit time not expired

## I_WagoSysCanOpen.SendTimestamp (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SendTimestamp | eCanFnReturn |
| Input | typTimestamp | typCanTimestamp |

Send timestamp

If wDay = 0 and dwTime = 0 then system time (in UTC) is used

Returns: 0 = OK -1 = fail

Interface variables Send timestamp If wDay = 0 and dwTime = 0 then system time (in UTC) is used Returns: 0 = OK -1 = fail

## eCanFlagReset (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CanNoReset | 0 | same als FALSE |
| CanDoReset | 1 | same as TRUE |

Replacement for BOOL as UDINT

InOut: Replacement for BOOL as UDINT

## eCanOpenState (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CanStopNode | 16#4 | stop node |
| CanStartNode | 16#5 | start node |
| CanResetNode | 16#6 | reset node |
| CanResetCom | 16#7 | reset communication |
| CanPreop | 16#7F | pre-operational |

Codes for change state of can devices (CiA 302_2)

InOut: Codes for change state of can devices (CiA 302_2)

### Interfaces


## I_WagoSysCanBase (ITF)


```
VAR_GLOBAL
      FbCom1 : WagoSysSerialInterface_Internal_Targetspecific IMPLEMENTS I_WagoSysComBase;
      FbCom2 : WagoSysSerialInterface_Internal_Targetspecific IMPLEMENTS I_WagoSysComBase;
END_VAR
```

```
FbMyComfortSerialInterface.OpenAndConfigure(FbCom1, 9600, 8, eTTYParity.None, ... );
```

Intended usage:

For each avalilable COM subdevice, a unique global FB will be provided via PLC configuration. These FBs implement the behaviour of the different hardware types of serial interfaces.

All these FBs implement this common interface I WagoSysComBase, which is defined in this libraray.

When a serial interface is used by other libraries, that libraries expect this interface for identifying the hardware:

Attention: There is no means implemented for preventing the application from directly using the methods of this interface in an uncontrolled manner.

Intended usage: For each avalilable COM subdevice, a unique global FB will be provided via PLC configuration. These FBs implement the behaviour of the different hardware types of serial interfaces. All these FBs implement this common interface I WagoSysComBase, which is defined in this libraray. When a serial interface is used by other libraries, that libraries expect this interface for identifying the hardware: Attention: There is no means implemented for preventing the application from directly using the methods of this interface in an uncontrolled manner. - I_WagoSysCanBase.CloseLayer2 (METH) - I_WagoSysCanBase.GetBusInfo (METH) - I_WagoSysCanBase.GetCanMode (METH) - I_WagoSysCanBase.GetDeviceInfo (METH) - I_WagoSysCanBase.GetFrame (METH) - I_WagoSysCanBase.GetFrameBuffer (METH) - I_WagoSysCanBase.GetFrameCounter (METH) - I_WagoSysCanBase.LibVersion (METH) - I_WagoSysCanBase.OpenLayer2 (METH) - I_WagoSysCanBase.RegisterAll (METH) - I_WagoSysCanBase.RegisterId (METH) - I_WagoSysCanBase.ResetLayer2 (METH) - I_WagoSysCanBase.SendFrame (METH) - I_WagoSysCanBase.SetCanLed (METH) - I_WagoSysCanBase.SetDeviceInfo (METH)

## I_WagoSysCanOpen (ITF)


- I_WagoSysCanOpen.ChangeState (METH) - I_WagoSysCanOpen.GetEmcy (METH) - I_WagoSysCanOpen.GetLastNode (METH) - I_WagoSysCanOpen.GetNodeDiag (METH) - I_WagoSysCanOpen.GetNodeEmcy (METH) - I_WagoSysCanOpen.GetNodeId (METH) - I_WagoSysCanOpen.GetTimestamp (METH) - I_WagoSysCanOpen.GuardError (METH) - I_WagoSysCanOpen.GuardErrorNode (METH) - I_WagoSysCanOpen.SdoAdd (METH) - I_WagoSysCanOpen.SdoReadAsync (METH) - I_WagoSysCanOpen.SdoReadData (METH) - I_WagoSysCanOpen.SdoReadSync (METH) - I_WagoSysCanOpen.SdoWriteAsync (METH) - I_WagoSysCanOpen.SdoWriteData (METH) - I_WagoSysCanOpen.SdoWriteSync (METH) - I_WagoSysCanOpen.SendEmcy (METH) - I_WagoSysCanOpen.SendTimestamp (METH)

### Internal Components


## eCanInternalState (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CanStateInit | 16#0 | no initialization |
| CanStateResetRequest | 16#1 | reset has been requested |
| CanStateBaudrateTest | 16#4 | baudrate test running |
| CanStateMasterReset | 16#40 | after successful initialization |
| CanStateSlaveStopped | 16#41 | slave mode: stopped |
| CanStateSlavePreop | 16#42 | slave mode: preoperational |
| CanStateSlaveOp | 16#43 | slave mode: operational |
| CanStatePreNetInit | 16#60 | states of the configuration procedure |
| CanStateNtwReset | 16#61 | reset communication all nodes |
| CanStateNtwWait | 16#62 | wait state |
| CanStateBootConf | 16#64 | bootup configuration mode |
| CanStateBootMissing | 16#70 | network has been scanned but there are missing mandatory nodes |
| CanStateClear | 16#80 | configuration matches |
| CanStateFatalError | 16#90 | serious configuration mismatch or bus off |
| CanStateRun | 16#A0 | network is set to operational |
| CanStateStop | 16#C0 | network is set to stopped by request |
| CanStatePreop | 16#E0 | network is set to preop. by request |

Errorinfo bits if CanState > 16#80:

bit 0 = 1: optional/unexpected node error

bit 1 = 1: mandatory node error

bit 2 = 1: at least one slave is operational

bit 3 = 1: the CANopen Manager is operational

Possible internal status of CAN Layer2 stack

CanStateInit := 16#00 no initialization

CanStateRun := 16#A0 network is operational

CanStateFatalError := 16#90 bus off

InOut: Errorinfo bits if CanState > 16#80: bit 0 = 1: optional/unexpected node error bit 1 = 1: mandatory node error bit 2 = 1: at least one slave is operational bit 3 = 1: the CANopen Manager is operational Possible internal status of CAN Layer2 stack CanStateInit := 16#00 no initialization CanStateRun := 16#A0 network is operational CanStateFatalError := 16#90 bus off

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 28.01.2024 | 1.0.2.1 | u010663 | Compiled SP16.3 |
| 08.01.2019 | 1.0.2.0 | u015842 | Properties: free placeholder added |
| 05.07.2018 | 1.0.1.7 | u013939 | update documentation |
| 25.04.2018 | 1.0.1.6 | u010545 | update documentation |
| 13.09.2017 | 1.0.1.5 | u010663 | I_WagoSysCanBase added EXTENDS __SYSTEM.IQueryInterface |
| 19.04.2016 | 1.0.1.4 | AWü / WAGO | update documentation |
| 08.04.2016 | 1.0.1.3 | AWü / WAGO | update documentation |
| 30.09.2015 | 1.0.1.2 | WAGO/ u010663 | Placeholder Attribute added |
| 29.09.2015 | 1.0.1.1 | AWü / WAGO | NoPlaceholder Attribute added |
| 22.09.2015 | 1.0.1.0 | AWü / WAGO | change in SDO Transfer from .udiTaskId to .udiChannel |
| 17.09.2015 |  |  | change in typeCanBusInfo |
| 09.07.2015 | 1.0.0.2 | AWü / WAGO | minor changes in documentation / extra errorcodes |
| 19.06.2015 | 1.0.0.1 | AWü / WAGO | minor changes in documentation |
| 01.06.2015 | 1.0.0.1 | AWü / WAGO | update documentation / merge with WagoTypesCan_Internal |
| 09.03.2015 | 1.0.0.0 | AWü / WAGO | update documentation / Change to 1.0.0.0 |
| 16.01.2015 | 0.0.0.7 | AWü / WAGO | update documentation / added SDO Returns to eCanFnReturn |
| 21.11.2014 | 0.0.0.6 | AWü / WAGO | major update / change var definitions |
| . |  |  | added extras for KBus CAN Gateway and multiport internal can |
| . |  |  | changed error code returns / removes layer2 error defines |
| 04.09.2014 | 0.0.0.5 | AWü / WAGO | added documentation and type eCanFlagResetmore device info types |
| 18.07.2014 | 0.0.0.4 | AWü / WAGO | more device info types |
| 17.07.2014 | 0.0.0.3 | AWü / WAGO | minor changes in project information |
| 24.06.2014 | 0.0.0.2 | RE | DocFormat = reStructuredText |
| 27.05.2014 | 0.0.0.1 | AWü / WAGO | initial version derived from WagoTypesCom |

WagoTypesCan

### Other Components


## Can LED ¶


## Device


- eCanDeviceError (ENUM) - eCanFlagRegister (ENUM) - eCanFlagReset (ENUM) - eCanFnReturn (ENUM) - eCanMode (ENUM) - typCanBusInfo (STRUCT) - typCanDeviceInfo (STRUCT)

## eCanDeviceError (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CanDeviceOK | 0 | standard return |
| CanDeviceIsLocked | -1 | device in in use |
| CanDeviceInvalidMode | -2 | invalid operation mode requested |
| CanDeviceInvalidPort | -3 | invalid operation port requested |
| CanDeviceInvalidBaudrate | -4 | invalid baudrate requested |
| CanDeviceInvalidInterface | -5 | invalid interface or port requested |
| CanDeviceNotReady | -6 | device not ready |

Return values for CAN device open / close / reset

InOut: Return values for CAN device open / close / reset

## eCanFlagRegister (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CanClearId | 0 | same als FALSE |
| CanRegisterId | 1 | same as TRUE |

Replacement for BOOL as UDINT

InOut: Replacement for BOOL as UDINT

## eCanFnReturn (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| CanFnWorking | 2 | function is still working (no error) |
| CanFnData | 1 | function has new data |
| CanFnOk | 0 | standard return |
| CanFnError | -1 | unspecific error |
| CanNoIdx | -2 | no free index in register or no index in unregister |
| CanTimeout | -3 | timeout on layer2 operation |
| CanNoData | -4 | no data in read operation |
| CanTxOverflow | -5 | data was not transmitted because tx overflow |
| CanNotReady | -6 | funktion not ready (error) |
| CanSDOWaiting | -7 | SDO call waiting |
| CanSDOTimeout | -8 | SDO call timeout |
| CanSDOErrorLen | -9 | Data array to small in SDO read |

Return values for CAN operations

InOut: Return values for CAN operations

## eCanLedMode (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| LedAuto | 0 | handle LED by CANopen / CANLayer2 stack |
| LedOff | 1 | unconfigured off |
| LedConfig | 2 | configuration running red 50ms - green 50ms |
| LedConfigError | 3 | configuration fault red 200ms - green 200ms |
| LedStopped | 4 | stopped / init OK green 200ms - off 800ms |
| LedPreOp | 5 | preoperational / no error green 200ms - off 200ms |
| LedPreOpError1 | 6 | preopertional / warning level 1 * (red 200ms - off 200ms) - 2 * (green 200ms - off 200ms) |
| LedPreOpError2 | 7 | preopertional / guard error 2 * (red 200ms - off 200ms) - 2 * (green 200ms - off 200ms) |
| LedPreOpError3 | 8 | preopertional / sync error 3 * (red 200ms - off 200ms) - 2 * (green 200ms - off 200ms) |
| LedOperational | 9 | operational / no error green |
| LedOpError1 | 10 | opertional / warning level 1 * (red 200ms - green 200ms) - green 800ms |
| LedOpError2 | 11 | opertional / guard error 2 * (red 200ms - green 200ms) - green 800ms |
| LedOpError3 | 12 | opertional / sync error 3 * (red 200ms - green 200ms) - green 800ms |
| LedError | 13 | bus off red |
| LedFatalError | 14 | fatal error red 200ms - off 200ms |

Values for SetCanLed

InOut: Values for SetCanLed

## eCanMode (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| None | 0 | CAN not used |
| CanMaster | 1 | CANopen Master |
| CanSlave | 2 | CANopen Local Device (Slave) |
| CanLayer2 | 3 | CAN Layer2 Device |
| CanKBusGateway | 4 | CAN Gateway on KBus |

Operational modes for CAN Device

InOut: Operational modes for CAN Device

## typCanBusInfo (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| wInternalState | WORD | eCanInternalState / internal status of CAN stack |
| wBusDiag | WORD | Bus diagnostic bits |
| uiRxL2Overflows | UINT | Rx CAN Layer2 overflow counter |
| uiTxL2Overflows | UINT | Tx CAN Layer2 overflow counter |
| uiTxL2Timeouts | UINT | Tx CAN Layer2 Timeout counter |
| uiRxOverflows | UINT | Rx overflow counter |
| uiMsgTimeouts | UINT | Msg Timeout counter |
| uiBusOffs | UINT | Bus off counter |
| uiBusWarnings | UINT | Bus warning counter |
| uiBitErrors | UINT | Bus bit error counter |

Return values for GetCanErrorInfo

Bus diagnostic bits

16#01 software overrun (lp-rx-queue)

16#40 software overrun (hp-rx-queue)

16#02 CAN interface: overrun

16#04 CAN interface: bus off

16#08 CAN interface: error-status-bit set

16#10 CAN interface: error-status-bit reset

16#20 lp-tx-queue full

16#80 hp-tx-queue full

16#100 Guarding or Heartbeat error as slave

16#200 Sync error as slave

InOut: Return values for GetCanErrorInfo Bus diagnostic bits 16#01 software overrun (lp-rx-queue) 16#40 software overrun (hp-rx-queue) 16#02 CAN interface: overrun 16#04 CAN interface: bus off 16#08 CAN interface: error-status-bit set 16#10 CAN interface: error-status-bit reset 16#20 lp-tx-queue full 16#80 hp-tx-queue full 16#100 Guarding or Heartbeat error as slave 16#200 Sync error as slave

## typCanDeviceInfo (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| udiDeviceLock | UINT | device is in use |
| udiDeviceMode | UINT | eCanMode as UDINT |
| udiInitMode | UINT | 0:not initialised 1: init OK |
| udiInterface | UINT | interface used |
| udiBaudrate | UDINT | actual baudrate used |
| dwFlags | DWORD | extra flags i.e. mapped or transparent Mode |
| udiBusNr | UDINT | reserved for future use |
| dwiExtraInfo | DWORD | reserved for future use |

Info of CAN Device

InOut: Info of CAN Device

## typCanTimestamp (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| dwTime | UDINT | ms after midnight |
| wDay | UINT | days FROM 1.January 1984 |
| wFlags | WORD | number of received timestamp messages after last read |