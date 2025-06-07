# WagoSysCan_Internal_PFC v1.0.1.6 (WAGO) - Complete Documentation


### Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | creationDateTime | date | 30.01.2024, 11:57:41 |
| companyName | string | WAGO |
| libraryFile | string | WagoSysCan_Internal_PFC.library |
| productName | string | e!COCKPIT |
| contentFile | string | doc.clean.json |
| ProjectInformation | IsEndUserLibrary | bool | False |
| ProjectInformation | Released | bool | False |
| ProjectInformation | LastModificationDateTime | 30.01.2024, 11:57:41 |
| ProjectInformation | LibraryCategories | library-category-list | Intern\|CANbus; WAGO Internal\|Feature\|Fieldbus\|CAN |
| ProjectInformation | Author | string | AWü / WAGO |
| ProjectInformation | Company | string | WAGO |
| ProjectInformation | CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |
| ProjectInformation | Copyright | string | © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. |
| ProjectInformation | DefaultNamespace | string | CanCfg |
| ProjectInformation | Description | string | See: Description |
| ProjectInformation | DocFormat | string | reStructuredText |
| ProjectInformation | LanguageModelAttribute | string | qualified-access-only |
| ProjectInformation | Placeholder | string | WagoSysCan_Internal_PFC |
| ProjectInformation | Project | string | WagoSysCan_Internal_PFC |
| ProjectInformation | Title | string | WagoSysCan_Internal_PFC |
| ProjectInformation | Version | version | 1.0.1.6 |

### Library Information


| LinkAllContent: False Optional: False | QualifiedOnly: False | SystemLibrary: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False | SystemLibrary: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False | SystemLibrary: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False | SystemLibrary: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCan Library Identification : Placeholder: WagoTypesCan Default Resolution: WagoTypesCan, * (WAGO) Namespace: WagoTypesCan Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties :

### Function Blocks


This is the fundamental FB of this library.

Each open FB represents a physical serial interface.

Multiple FBs may share one physical serial interface, but in that case they must not be open simultaneously, i.e. if it is opened by one application, it cannot be opened once more until the firts open() is close()d again.

In normal operation, the serial interfaces do not have to be closed again, as they will be used throughout the runtime of the machine. When encountering situations such as online-change, however, the used interfaces have to be closed() at FB_exit and re-opened again, as otherwise OS resources might stay blocked.

- Initialize (Method) This is the fundamental FB of this library. Each open FB represents a physical serial interface. Multiple FBs may share one physical serial interface, but in that case they must not be open simultaneously, i.e. if it is opened by one application, it cannot be opened once more until the firts open() is close()d again. In normal operation, the serial interfaces do not have to be closed again, as they will be used throughout the runtime of the machine. When encountering situations such as online-change, however, the used interfaces have to be closed() at FB_exit and re-opened again, as otherwise OS resources might stay blocked. - CloseLayer2 (Method) - FB_init (Method) - GetBusInfo (Method) - GetCanMode (Method) - GetDeviceInfo (Method) - GetFrame (Method) - GetFrameBuffer (Method) - GetFrameCounter (Method) - LibVersion (Method) - OpenLayer2 (Method) - RegisterAll (Method) - RegisterId (Method) - ResetLayer2 (Method) - SendFrame (Method) - SetCanLed (Method) - SetDeviceInfo (Method) - ChangeState (Method) - FB_init (Method) - GetEmcy (Method) - GetLastNode (Method) - GetNodeDiag (Method) - GetNodeEmcy (Method) - GetNodeId (Method) - GetTimestamp (Method) - GuardError (Method) - GuardErrorNode (Method) - SdoAdd (Method) - SdoReadAsync (Method) - SdoReadData (Method) - SdoReadSync (Method) - SdoWriteAsync (Method) - SdoWriteData (Method) - SdoWriteSync (Method) - SendEmcy (Method) - SendTimestamp (Method)

### Functions


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuChangeState | eCanFnReturn |  |
| Input | udiNodeId | UDINT | NodeId of device |
| Input | eState | eCanOpenState | state to set |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuCloseLayer2 | eCanDeviceError |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuGetBusInfo | eCanFnReturn |  |
| Input | eResetflags | eCanFlagReset | reset error counters |
| Inout | typBusInfo | typCanBusInfo |  |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetCanMode | eCanMode |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuGetDeviceInfo | eCanFnReturn |  |
| Inout | typCanInfo | typCanDeviceInfo | device info struct |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuGetEmcy | DINT |  |
| Input | eRemove | eCanFlagReset | 1 read and remove oldest message from list |
| Inout | aMsg | ARRAY [1..8] OF BYTE | info of message |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuGetFrame | DINT |  |
| Input | udiTimeout | UDINT | Timeout in ms |
| Inout | dwId | DWORD | CAN Id (updated id RegisterAll(1) was set) |
| Inout | aMsg | ARRAY [1..8] OF BYTE | message buffer |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuGetFrameBuffer | DINT |  |
| Input | dwID | DWORD | CAN Id |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuGetFrameCounter | DINT |  |
| Input | dwId | DWORD | CAN Id |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetLastNode | DINT |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetNodeDiag | DWORD |
| Input | udiNodeId | UDINT |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuGetNodeEmcy | eCanFnReturn |  |
| Input | udiNodeId | UDINT | node Id |
| Input | eRemove | eCanFlagReset | clear message |
| Inout | aMsg | ARRAY [1..8] OF BYTE |  |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetNodeId | DINT |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetTimestamp | eCanFnReturn |
| Inout | typTimestamp | typCanTimestamp |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGuardError | DINT |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGuardErrorNode | eCanFnReturn |
| Input | udiNodeId | UDINT |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuLibVersion | UDINT |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuOpenLayer2 | eCanDeviceError |  |
| Input | udiBaudrate | UDINT | baudrate in baud valid is 100baud…1Mbaud 0 = auto (if supported) |
| Input | dwFlags | DWORD | reserved for future use |
| Input | udiBusNr | UDINT | reserved for future use |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuRegisterAll | eCanFnReturn |
| Input | eRegflag | eCanFlagRegister |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuRegisterId | eCanFnReturn |  |
| Input | eRegflag | eCanFlagRegister | register or unregister |
| Input | dwId | DWORD | CAN Id + 16#80000000 if 29Bit Id |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuResetLayer2 | eCanDeviceError |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSdoAdd | eCanFnReturn |  |
| Input | udiIndex | UDINT | 16#2000 spezial SDO no subindex size max 1536 byte |
| Input | udiEntrys | UDINT | requested subindexes |
| Input | udiBytes | UDINT | datalen in bytes of 1 subindex |
| Input | udiSDOType | UDINT | data type |
| Input | udiOffset | UDINT | position in parameter data (8192 Bytes) |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSdoReadAsync | DINT |  |
| Input | udiNodeId | UDINT | node id |
| Input | udiIndex | UDINT | sdo index |
| Input | udiSubindex | UDINT | sdo subindex |
| Input | udiBytes | UDINT | sdo bytes (0 = all) |
| Input | udiTimeout | UDINT | timeout in ms |
| Input | udiChannel | UDINT | channel number for parallel transfers (0…15) |
| Input | pData | POINTER TO BYTE | sdo data |

| Returnvalue | Description |
| < 0 | // Error Codes from eCanFnReturn |
| 0 | // call finished / bytes received |
| > 16#10000 | // SDO abort code |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSdoReadData | eCanFnReturn |  |
| Input | udiIndex | UDINT | index |
| Input | udiSubindex | UDINT | subindex |
| Input | udiBytes | UDINT | datalen |
| Input | pData | POINTER TO BYTE | sdo data |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSdoReadSync | DINT |  |
| Input | udiNodeId | UDINT | node id |
| Input | udiIndex | UDINT | sdo index |
| Input | udiSubindex | UDINT | sdo subindex |
| Input | udiBytes | UDINT | sdo bytes |
| Input | udiTimeout | UDINT | timeout in ms |
| Input | pData | POINTER TO BYTE | sdo data |

| Returnvalue | Description |
| 0 | // Call finished |
| < 0 | // Error Codes from eCanFnReturn |
| > 16#10000 | // SDO abort code |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSdoWriteAsync | DINT |  |
| Input | udiNodeId | UDINT | node id |
| Input | udiIndex | UDINT | sdo index |
| Input | udiSubindex | UDINT | sdo subindex |
| Input | udiBytes | UDINT | sdo bytes |
| Input | udiTimeout | UDINT | timeout in ms |
| Input | udiChannel | UDINT | channel number for parallel transfers (0…15) |
| Input | pData | POINTER TO BYTE | sdo data |

| Returnvalue | Description |
| < 0 | // Error Codes from eCanFnReturn |
| 0 | // Call finished |
| > 16#10000 | // SDO abort code |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSdoWriteData | DINT |  |
| Input | udiIndex | UDINT | sdo index |
| Input | udiSubindex | UDINT | sdo index |
| Input | udiBytes | UDINT | sdo bytes |
| Input | pData | POINTER TO BYTE | sdo data |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSdoWriteSync | DINT |  |
| Input | udiNodeId | UDINT | node id |
| Input | udiIndex | UDINT | sdo index |
| Input | udiSubindex | UDINT | sdo subindex |
| Input | udiBytes | UDINT | sdo bytes |
| Input | udiTimeout | UDINT | timeout in ms |
| Input | pData | POINTER TO BYTE | sdo data |

| Returnvalue | Description |
| 0 | // Call finished |
| < 0 | // Error Codes from eCanFnReturn |
| > 16#10000 | // SDO abort code |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSendEmcy | DINT |  |
| Input | dwCode | DWORD | EMC error code |
| Input | dwRegister | DWORD | register 1001 |
| Input | aMfsCode | ARRAY [1..5] OF BYTE | manufacture spec. error field |

| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FuSendFrame | DINT |  |
| Input | dwId | DWORD | CAN Id + 16#80000000 if 29Bit Adress |
| Input | dwDlc | DWORD | CAN Dlc or 16#10 for RTR Call |
| Input | udiTimeout | UDINT | timeout in ms (not used in layer2 device) |
| Input | aMsg | ARRAY [1..8] OF BYTE | message |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuSendTimestamp | eCanFnReturn |
| Input | typTimestamp | typCanTimestamp |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuSetCanLed | eCanFnReturn |
| Input | eMode | eCanLedMode |

| Scope | Name | Type |
| --- | --- | --- |
| Return | FuSetDeviceInfo | eCanFnReturn |
| Inout | typCanInfo | typCanDeviceInfo |

Change state of CANopen device or master (valid only for own node in slave mode) Returns: 0 = OK -1 = fail

Close CAN Layer2 Device Returns: 0 = OK -1 = fail

Fill CAN Bus info struct Returns: 0: OK -1: no active CAN device

Get CAN device operational mode Returns: 0: not used 1:CANopen Master 2:CANopen Local Device 3:CAN Layer2 Device

Fill CAN device info struct Returns: 0 = OK

Test for new emergency error on any slave in CANopen Manager Mode Returns: 0 = no emcy message > 0 node id -1 failure

Get layer2 frame from registered Id Returns: Dlc of message, 16#10 for RTR call or eCanL2ErrorCode

Get number of frames in buffer from registered Id Returns: number of frames in buffer (maximum 8) + 0x1000 if buffer overflow -1 for error -2 id no index entry

Get layer2 frame counter for registered Id Returns: 16 Bit frame counter -1 for error -2 id no index entry

return number of configured node Ids on bus in CANopen Manager Mode or -1 if error

get node diagnostic bits in CANopen Manager Mode

Test for Emcy message from node in CANopen Manager Mode Returns: 0 = no emcy message 1 = message present -1 failure

get own node Id of can device

Get last timestamp Returns: 0 = OK -1 = fail

Test for guarding error on any slave (only tests own node in slave mode) Returns: node Id of node with guarding error 0: no error -1 failure

Test for guarding error message from slave in CANopen Manager Mode Returns: 0 = no guarding error message 1 = guarding error message from slave -1 = failure

return version of library interface in firmware

Open CAN connection in layer2 mode Returns: 0 = OK -1 = fail -3 invalid port -4 invalid baudrate -6 not ready(error)

Register or unregister all Ids for layer2 rx Returns: 0 = OK -1 = fail Warning: all incoming messages must be handled by the application

Register or unregister id for layer2 rx Returns: 0 = OK -1 = device fail -2 = no free index in register or no index in unregister

Reset and restart CAN communication in layer2 mode Returns: 0 = OK -1 = fail

Function is called to add a User SDO Returns: 0 = OK -1 = fail

read CANopen SDOs without blocking process

read CANopen from process data and parameter data sdos Returns: 0 = OK -1 = fail

read CANopen SDOs with blocking process

send CANopen SDOs without blocking process

write to CANopen process data and parameter data sdos Returns: 0 = OK -1 = fail

read CANopen SDOs with blocking process

send emc message Returns: 0 = OK -1 = Error -2 = inhibit time not expired

Send layer2 frame Returns: 0: OK -1: no active CAN device -5: bus 0ff or buffer full

Send timestamp wDay = 0 then system time is used Returns: 0 = OK -1 = fail

Set CAN LED Returns: 0 = OK -1 = fail

Set/Reset DeviceLock in CAN device info struct Returns: 0

Interface variables Change state of CANopen device or master (valid only for own node in slave mode) Returns: 0 = OK -1 = fail Interface variables Close CAN Layer2 Device Returns: 0 = OK -1 = fail Interface variables Fill CAN Bus info struct Returns: 0: OK -1: no active CAN device Interface variables Get CAN device operational mode Returns: 0: not used 1:CANopen Master 2:CANopen Local Device 3:CAN Layer2 Device Interface variables Fill CAN device info struct Returns: 0 = OK Interface variables Test for new emergency error on any slave in CANopen Manager Mode Returns: 0 = no emcy message > 0 node id -1 failure Interface variables Get layer2 frame from registered Id Returns: Dlc of message, 16#10 for RTR call or eCanL2ErrorCode Interface variables Get number of frames in buffer from registered Id Returns: number of frames in buffer (maximum 8) + 0x1000 if buffer overflow -1 for error -2 id no index entry Interface variables Get layer2 frame counter for registered Id Returns: 16 Bit frame counter -1 for error -2 id no index entry Interface variables return number of configured node Ids on bus in CANopen Manager Mode or -1 if error Interface variables get node diagnostic bits in CANopen Manager Mode Interface variables Test for Emcy message from node in CANopen Manager Mode Returns: 0 = no emcy message 1 = message present -1 failure Interface variables get own node Id of can device Interface variables Get last timestamp Returns: 0 = OK -1 = fail Interface variables Test for guarding error on any slave (only tests own node in slave mode) Returns: node Id of node with guarding error 0: no error -1 failure Interface variables Test for guarding error message from slave in CANopen Manager Mode Returns: 0 = no guarding error message 1 = guarding error message from slave -1 = failure Interface variables return version of library interface in firmware Interface variables Open CAN connection in layer2 mode Returns: 0 = OK -1 = fail -3 invalid port -4 invalid baudrate -6 not ready(error) Interface variables Register or unregister all Ids for layer2 rx Returns: 0 = OK -1 = fail Warning: all incoming messages must be handled by the application Interface variables Register or unregister id for layer2 rx Returns: 0 = OK -1 = device fail -2 = no free index in register or no index in unregister Interface variables Reset and restart CAN communication in layer2 mode Returns: 0 = OK -1 = fail Interface variables Function is called to add a User SDO Returns: 0 = OK -1 = fail Interface variables read CANopen SDOs without blocking process Interface variables read CANopen from process data and parameter data sdos Returns: 0 = OK -1 = fail Interface variables read CANopen SDOs with blocking process Interface variables send CANopen SDOs without blocking process Interface variables write to CANopen process data and parameter data sdos Returns: 0 = OK -1 = fail Interface variables read CANopen SDOs with blocking process Interface variables send emc message Returns: 0 = OK -1 = Error -2 = inhibit time not expired Interface variables Send layer2 frame Returns: 0: OK -1: no active CAN device -5: bus 0ff or buffer full Interface variables Send timestamp wDay = 0 then system time is used Returns: 0 = OK -1 = fail Interface variables Set CAN LED Returns: 0 = OK -1 = fail Interface variables Set/Reset DeviceLock in CAN device info struct Returns: 0

### Methods


## CANRemoteDevice.Initialize (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Initialize | BOOL |
| Input | wModuleType | WORD |
| Input | dwInstance | DWORD |
| Input | pConnector | POINTER TO DWORD |

## FbCanInterface.CloseLayer2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | CloseLayer2 | eCanDeviceError |

Close CAN Layer2 Device Returns: 0 = OK -1 = fail -6 not ready

Interface variables Close CAN Layer2 Device Returns: 0 = OK -1 = fail -6 not ready

## FbCanInterface.FB_init (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FB_init | BOOL |  |
| Input | bInitRetains | BOOL |  |
| Input | bInCopyCode | BOOL |  |
| Input | udiLogicalNumber | UDINT | 0 for internal CAN |

## FbCanInterface.GetBusInfo (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetBusInfo | eCanFnReturn |  |
| Input | eResetflags | eCanFlagReset | reset error counters |
| Inout | typBusInfo | WagoTypesCan.typCanBusInfo | CAN info struct |

Get CAN status struct Returns: 0: OK -1: no active CAN device

Interface variables Get CAN status struct Returns: 0: OK -1: no active CAN device

## FbCanInterface.GetCanMode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetCanMode | eCanMode |

Get CAN device operational mode Returns: 0: not used 1:CANopen Master 2:CANopen Local Device 3:CAN Layer2 Device 4:KBus CAN Gateway

Interface variables Get CAN device operational mode Returns: 0: not used 1:CANopen Master 2:CANopen Local Device 3:CAN Layer2 Device 4:KBus CAN Gateway

## FbCanInterface.GetDeviceInfo (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetDeviceInfo | eCanFnReturn |  |
| Inout | typCanInfo | typCanDeviceInfo | device info struct |

Fill CAN device info struct Returns: 0

Interface variables Fill CAN device info struct Returns: 0

## FbCanInterface.GetFrame (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetFrame | DINT |  |
| Input | udiTimeout | UDINT | timeout in ms |
| Inout | dwId | DWORD | CAN Id (updated id RegisterAll(1) was set) |
| Inout | aMsg | ARRAY [1..8] OF BYTE | message buffer |

Get layer2 frame from registered Id Returns: Dlc of message, 16#10 for RTR call or eCanL2ErrorCode

Interface variables Get layer2 frame from registered Id Returns: Dlc of message, 16#10 for RTR call or eCanL2ErrorCode

## FbCanInterface.GetFrameBuffer (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetFrameBuffer | DINT |  |
| Input | dwId | DWORD | CAN Id (ignored if RegisterAll(1) was set) |

Get number of frames in buffer from registered Id Returns: number of frames in buffer (maximum 8) + 0x1000 if buffer overflow or -1 if error -2 if no index entry

Interface variables Get number of frames in buffer from registered Id Returns: number of frames in buffer (maximum 8) + 0x1000 if buffer overflow or -1 if error -2 if no index entry

## FbCanInterface.GetFrameCounter (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetFrameCounter | DINT |  |
| Input | dwId | DWORD | CAN Id (ignored if RegisterAll(1) was set) |

Get layer2 frame counter for registered Id Returns: 16 bit frame counter or -1 if error -2 if no index entry

Interface variables Get layer2 frame counter for registered Id Returns: 16 bit frame counter or -1 if error -2 if no index entry

## FbCanInterface.LibVersion (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | LibVersion | UDINT |

return version of library interface in firmware

Interface variables return version of library interface in firmware

## FbCanInterface.OpenLayer2 (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | OpenLayer2 | eCanDeviceError |  |
| Input | udiBaudrate | UDINT | baudrate in baud valid 100 baud … 1Mbaud 0 = auto (if supported) |
| Input | dwFlags | DWORD | reserved for future use |
| Input | udiBusNr | UDINT | reserved for future use |

Open CAN connection in layer2 mode Returns: 0 = OK -1 = fail -3 invalid port -4 invalid baudrate -6 not ready(error)

Interface variables Open CAN connection in layer2 mode Returns: 0 = OK -1 = fail -3 invalid port -4 invalid baudrate -6 not ready(error)

## FbCanInterface.RegisterAll (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | RegisterAll | eCanFnReturn |
| Input | eRegflag | eCanFlagRegister |

Register or unregister all Ids for layer2 rx Returns: 0 = OK -1 = fail Warning: all incoming messages must be handled by the application

Interface variables Register or unregister all Ids for layer2 rx Returns: 0 = OK -1 = fail Warning: all incoming messages must be handled by the application

## FbCanInterface.RegisterId (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | RegisterId | eCanFnReturn |  |
| Input | eRegflag | eCanFlagRegister | register or unregister |
| Input | dwId | DWORD | CAN Id + 16#80000000 if 29Bit Id |

Register or unregister id for layer2 rx Returns: 0 = OK -1 = device fail -2 = no free index in register or no index in unregister

Interface variables Register or unregister id for layer2 rx Returns: 0 = OK -1 = device fail -2 = no free index in register or no index in unregister

## FbCanInterface.ResetLayer2 (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ResetLayer2 | eCanDeviceError |

Reset and restart CAN communication in layer2 mode Returns: 0 = OK -1 = fail -6 not ready

Interface variables Reset and restart CAN communication in layer2 mode Returns: 0 = OK -1 = fail -6 not ready

## FbCanInterface.SendFrame (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SendFrame | eCanFnReturn |  |
| Input | dwId | DWORD | CAN Id + 16#80000000 if 29Bit Adress |
| Input | dwDlc | DWORD | CAN Dlc or 16#10 for RTR Call |
| Input | udiTimeout | UDINT | timeout in ms (not used in layer2 device) |
| Input | aMsg | ARRAY [1..8] OF BYTE | Message |

Send layer2 frame Returns: 0: OK -1: no active CAN device -5: bus 0ff or buffer full

Interface variables Send layer2 frame Returns: 0: OK -1: no active CAN device -5: bus 0ff or buffer full

## FbCanInterface.SetCanLed (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetCanLed | eCanFnReturn |
| Input | eMode | eCanLedMode |

Set CAN LED Returns: 0 = OK -1 = fail

Interface variables Set CAN LED Returns: 0 = OK -1 = fail

## FbCanInterface.SetDeviceInfo (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetDeviceInfo | eCanFnReturn |
| Inout | typCanInfo | typCanDeviceInfo |

Set/Reset DeviceLock in CAN device info struct Returns: 0

Interface variables Set/Reset DeviceLock in CAN device info struct Returns: 0

## FbCanOpenInterface.ChangeState (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ChangeState | eCanFnReturn |  |
| Input | udiNodeId | UDINT | Node Id of device |
| Input | eState | eCanOpenState | state to set |

Change state of CANopen device or master (valid only for own node in slave mode) Returns: 0 = OK -1 = fail

Interface variables Change state of CANopen device or master (valid only for own node in slave mode) Returns: 0 = OK -1 = fail

## FbCanOpenInterface.FB_init (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FB_init | BOOL |  |
| Input | bInitRetains | BOOL |  |
| Input | bInCopyCode | BOOL |  |
| Input | udiLogicalNumber | UDINT | 0 for internal CAN |

## FbCanOpenInterface.GetEmcy (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetEmcy | DINT |  |
| Input | eRemove | eCanFlagReset | 1 read and remove oldest message from list |
| Inout | aMsg | ARRAY [1..8] OF BYTE | info of message |

Test for new emergency error on any slave in CANopen Manager Mode Returns: 0 = no emcy message > 0 node id -1 failure

Interface variables Test for new emergency error on any slave in CANopen Manager Mode Returns: 0 = no emcy message > 0 node id -1 failure

## FbCanOpenInterface.GetLastNode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetLastNode | DINT |

return number of configured node Ids on bus in CANopen Manager Mode -1 = failure

Interface variables return number of configured node Ids on bus in CANopen Manager Mode -1 = failure

## FbCanOpenInterface.GetNodeDiag (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetNodeDiag | DWORD |
| Input | udiNodeId | UDINT |

get node diagnostic bits in CANopen Manager Mode -1 = failure

Interface variables get node diagnostic bits in CANopen Manager Mode -1 = failure

## FbCanOpenInterface.GetNodeEmcy (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetNodeEmcy | eCanFnReturn |  |
| Input | udiNodeId | UDINT | node id |
| Input | eRemove | eCanFlagReset | clear message |
| Inout | aMsg | ARRAY [1..8] OF BYTE |  |

Test for Emcy message from node in CANopen Manager Mode Returns: 0 = no emcy message 1 = message present -1 failure

Interface variables Test for Emcy message from node in CANopen Manager Mode Returns: 0 = no emcy message 1 = message present -1 failure

## FbCanOpenInterface.GetNodeId (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetNodeId | DINT |

get own node Id of can device -1 = failure

Interface variables get own node Id of can device -1 = failure

## FbCanOpenInterface.GetTimestamp (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetTimestamp | eCanFnReturn |
| Inout | typTimestamp | typCanTimestamp |

Get last timestamp Returns: 0 = OK -1 = fail

Interface variables Get last timestamp Returns: 0 = OK -1 = fail

## FbCanOpenInterface.GuardError (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GuardError | DINT |

Test for guarding error on any slave (only tests own node in slave mode) Returns: node Id of node with guarding error 0: no error -1 failure

Interface variables Test for guarding error on any slave (only tests own node in slave mode) Returns: node Id of node with guarding error 0: no error -1 failure

## FbCanOpenInterface.GuardErrorNode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GuardErrorNode | eCanFnReturn |
| Input | udiNodeId | UDINT |

Test for guarding error message from slave in CANopen Manager Mode Returns: 0 = no guarding error message node Id = = guarding error message from slave -1 failure

Interface variables Test for guarding error message from slave in CANopen Manager Mode Returns: 0 = no guarding error message node Id = = guarding error message from slave -1 failure

## FbCanOpenInterface.SdoAdd (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SdoAdd | eCanFnReturn |  |
| Input | udiIndex | UDINT | 16#2000 spezial SDO no subindex size max 1536 byte |
| Input | udiEntrys | UDINT | requested subindexes |
| Input | udiBytes | UDINT | datalen in bytes of 1 subindex |
| Input | udiSDOType | UDINT | data type |
| Input | udiOffset | UDINT | position in parameter data (8192 Bytes) |

Function is called to add a user SDO Returns: 0 = OK -1 = fail

Interface variables Function is called to add a user SDO Returns: 0 = OK -1 = fail

## FbCanOpenInterface.SdoReadAsync (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | SdoReadAsync | DINT |  |  |
| Input | udiNodeId | UDINT |  | Node id |
| Input | udiIndex | UDINT |  | sdo index |
| Input | udiSubindex | UDINT |  | sdo subindex |
| Input | udiBytes | UDINT |  | sdo bytes (0 = all) |
| Input | udiTimeout | UDINT |  | timeout in ms |
| Input | udiChannel | UDINT | 1 | channel number for parallel transfers (0…15) |
| Input | pData | POINTER TO BYTE |  | sdo data |

| Returnvalue | Description |
| < 0 | // Error Codes from eCanFnReturn |
| 0..udiBytes | // call finished / bytes received |
| > 16#10000 | // SDO abort code |

read CANopen SDOs without blocking process

Interface variables Function read CANopen SDOs without blocking process

## FbCanOpenInterface.SdoReadData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SdoReadData | eCanFnReturn |  |
| Input | udiIndex | UDINT | index |
| Input | udiSubindex | UDINT | subindex |
| Input | udiBytes | UDINT | datalen |
| Input | pData | POINTER TO BYTE | sdo data |

read CANopen from process data and parameter data sdos Returns: 0 = OK -1 = Fail

Interface variables read CANopen from process data and parameter data sdos Returns: 0 = OK -1 = Fail

## FbCanOpenInterface.SdoReadSync (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SdoReadSync | DINT |  |
| Input | udiNodeId | UDINT | node id |
| Input | udiIndex | UDINT | sdo index |
| Input | udiSubindex | UDINT | sdo subindex |
| Input | udiBytes | UDINT | sdo bytes |
| Input | udiTimeout | UDINT | timeout in ms |
| Input | pData | POINTER TO BYTE | sdo data |

| Returnvalue | Description |
| < 0 | // Error Codes from eCanFnReturn |
| 0..udiBytes | // call finished / bytes received |
| > 16#10000 | // SDO abort code |

read CANopen SDOs with blocking process

Interface variables read CANopen SDOs with blocking process

## FbCanOpenInterface.SdoWriteAsync (METH)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Return | SdoWriteAsync | DINT |  |  |
| Input | udiNodeId | UDINT |  | Node id |
| Input | udiIndex | UDINT |  | sdo index |
| Input | udiSubindex | UDINT |  | sdo dubindex |
| Input | udiBytes | UDINT |  | sdo bytes |
| Input | udiTimeout | UDINT |  | timeout in ms |
| Input | udiChannel | UDINT | 1 | channel number for parallel transfers (0…15) |
| Input | pData | POINTER TO BYTE |  | sdo data |

| Returnvalue | Description |
| < 0 | // Error Codes from eCanFnReturn |
| 0 | // call finished |
| > 16#10000 | // SDO abort code |

send CANopen SDOs without blocking process

Interface variables send CANopen SDOs without blocking process

## FbCanOpenInterface.SdoWriteData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SdoWriteData | eCanFnReturn |  |
| Input | udiIndex | UDINT | sdo index |
| Input | udiSubindex | UDINT | sdo subindex |
| Input | udiBytes | UDINT | sdo bytes |
| Input | pData | POINTER TO BYTE | sdo data |

write to CANopen process data and parameter data sdos Returns: 0 = OK -1 = fail

Interface variables write to CANopen process data and parameter data sdos Returns: 0 = OK -1 = fail

## FbCanOpenInterface.SdoWriteSync (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SdoWriteSync | DINT |  |
| Input | udiNodeId | UDINT | node id |
| Input | udiIndex | UDINT | sdo index |
| Input | udiSubindex | UDINT | sdo subindex |
| Input | udiBytes | UDINT | sdo bytes |
| Input | udiTimeout | UDINT | timeout in ms |
| Input | pData | POINTER TO BYTE | sdo data |

| Returnvalue | Description |
| 0 | // call finished |
| < 0 | // Error Codes from eCanFnReturn |
| > 16#10000 | // SDO abort code |

write CANopen SDOs with blocking process

Interface variables write CANopen SDOs with blocking process

## FbCanOpenInterface.SendEmcy (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SendEmcy | DINT |  |
| Input | dwCode | DWORD | EMC error code |
| Input | dwRegister | DWORD | register 1001 |
| Input | aMfsCode | ARRAY [1..5] OF BYTE | manufacture spec. error field |

send emc message Returns: 0 = OK -1 = Error -2 = inhibit time not expired

Interface variables send emc message Returns: 0 = OK -1 = Error -2 = inhibit time not expired

## FbCanOpenInterface.SendTimestamp (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SendTimestamp | eCanFnReturn |
| Input | typTimestamp | typCanTimestamp |

Send timestamp if wDay = 0 and time = 0 system then time is used Returns: 0 = OK -1 = fail

Interface variables Send timestamp if wDay = 0 and time = 0 system then time is used Returns: 0 = OK -1 = fail

### Function Groups


- FuChangeState (Function) - FuCloseLayer2 (Function) - FuGetBusInfo (Function) - FuGetCanMode (Function) - FuGetDeviceInfo (Function) - FuGetEmcy (Function) - FuGetFrame (Function) - FuGetFrameBuffer (Function) - FuGetFrameCounter (Function) - FuGetLastNode (Function) - FuGetNodeDiag (Function) - FuGetNodeEmcy (Function) - FuGetNodeId (Function) - FuGetTimestamp (Function) - FuGuardError (Function) - FuGuardErrorNode (Function) - FuLibVersion (Function) - FuOpenLayer2 (Function) - FuRegisterAll (Function) - FuRegisterId (Function) - FuResetLayer2 (Function) - FuSdoAdd (Function) - FuSdoReadAsync (Function) - FuSdoReadData (Function) - FuSdoReadSync (Function) - FuSdoWriteAsync (Function) - FuSdoWriteData (Function) - FuSdoWriteSync (Function) - FuSendEmcy (Function) - FuSendFrame (Function) - FuSendTimestamp (Function) - FuSetCanLed (Function) - FuSetDeviceInfo (Function)

### Internal Components


## 90 Internal


- CANRemoteDevice (FunctionBlock) Initialize (Method) Functions - FuChangeState (Function) - FuCloseLayer2 (Function) - FuGetBusInfo (Function) - FuGetCanMode (Function) - FuGetDeviceInfo (Function) - FuGetEmcy (Function) - FuGetFrame (Function) - FuGetFrameBuffer (Function) - FuGetFrameCounter (Function) - FuGetLastNode (Function) - FuGetNodeDiag (Function) - FuGetNodeEmcy (Function) - FuGetNodeId (Function) - FuGetTimestamp (Function) - FuGuardError (Function) - FuGuardErrorNode (Function) - FuLibVersion (Function) - FuOpenLayer2 (Function) - FuRegisterAll (Function) - FuRegisterId (Function) - FuResetLayer2 (Function) - FuSdoAdd (Function) - FuSdoReadAsync (Function) - FuSdoReadData (Function) - FuSdoReadSync (Function) - FuSdoWriteAsync (Function) - FuSdoWriteData (Function) - FuSdoWriteSync (Function) - FuSendEmcy (Function) - FuSendFrame (Function) - FuSendTimestamp (Function) - FuSetCanLed (Function) - FuSetDeviceInfo (Function)

## WagoSysCan_Internal_PFC Library Documentation


WagoSysCan_Internal_PFC

Intern|CANbus; WAGO Internal|Feature|Fieldbus|CAN

WagoSysCan_Internal_PFC

This document is automatically generated.

target specific CAN library for PFC

Based on WagoSysCan_Internal_PFC.library, last modified 30.01.2024, 11:57:41. LibDoc 4.1.1.0

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

Company WAGO Title WagoSysCan_Internal_PFC Version 1.0.1.6 Categories Intern|CANbus; WAGO Internal|Feature|Fieldbus|CAN Namespace CanCfg Author AWü / WAGO Placeholder WagoSysCan_Internal_PFC This document is automatically generated. target specific CAN library for PFC - 20 Programm Organisation Units FbCanInterface (FunctionBlock) - FbCanOpenInterface (FunctionBlock) 90 Internal - CANRemoteDevice (FunctionBlock) - Functions VersionHistory (GVL) - File and Project Information - Library Reference Based on WagoSysCan_Internal_PFC.library, last modified 30.01.2024, 11:57:41. LibDoc 4.1.1.0 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 23.10.2023 | 1.0.1.6 | u010663 | 64-Bit adjustment ->SysTypes2Interfaces |
| 08.01.2019 | 1.0.1.5 | u015842 | Properties: copyright added |
| 25.04.2018 | 1.0.1.4 | u010545 | update documentation |
| 18.05.2015 | 1.0.1.3 | AWü / WAGO | removed typos |
| 30.09.2015 | 1.0.1.2 | AWü / WAGO | Placeholder for WagoTypesCan |
| 29.09.2015 | 1.0.1.1 | AWü / WAGO | Placeholder for WagoTypesCan |
| 22.09.2015 | 1.0.1.0 | AWü / WAGO | change in SDO Transfer from .udiTAskId to .udiChannel |
| 17.09.2015 |  |  | minor changes in documenation / change in WagoTypesCan |
| 09.07.2015 | 1.0.0.2 | AWü / WAGO | minor changes in documenation / change in WagoTypesCan |
| 19.06.2015 | 1.0.0.1 | AWü / WAGO | minor changes in documenation |
| 01.06.2015 | 1.0.0.1 | AWü / WAGO | use merged WagoTypesCan / update documentation |
| 09.03.2015 | 1.0.0.0 | AWü / WAGO | change to version 1.0.0.0 / update documentation |
| 19.01.2015 | 0.0.0.11 | AWü / WAGO | minor changes / update documentation |
| 21.11.2014 | 0.0.0.10 | AWü / WAGO | major update / change var definitions / added extras for KBus CAN Gateway and multiport internal can |
| 18.09.2014 | 0.0.0.9 | AWü / WAGO | change to WagoTypesCommon |
| 04.09.2014 | 0.0.0.8 | AWü / WAGO | added documentation and changes in definitions |
| 23.08.2014 | 0.0.0.7 | AWü / WAGO | added timestamp functions |
| 18.07.2014 | 0.0.0.6 | AWü / WAGO | added device lock an info function |
| 17.07.2014 | 0.0.0.5 | AWü / WAGO | port of function frames compleated (ToDo: function internal) |
| 24.06.2014 | 0.0.0.4 | RE | DocFormat = reStructuredText |
| 27.05.2014 | 0.0.0.3 | AWü / WAGO | ported from WagoSysCom_Internal_PFC |

WagoSysCan_Internal_PFC

WagoSysCan_Internal_PFC

### Other Components


## 20 Programm Organisation Units


- FbCanInterface (FunctionBlock) CloseLayer2 (Method) - FB_init (Method) - GetBusInfo (Method) - GetCanMode (Method) - GetDeviceInfo (Method) - GetFrame (Method) - GetFrameBuffer (Method) - GetFrameCounter (Method) - LibVersion (Method) - OpenLayer2 (Method) - RegisterAll (Method) - RegisterId (Method) - ResetLayer2 (Method) - SendFrame (Method) - SetCanLed (Method) - SetDeviceInfo (Method) FbCanOpenInterface (FunctionBlock) - ChangeState (Method) - FB_init (Method) - GetEmcy (Method) - GetLastNode (Method) - GetNodeDiag (Method) - GetNodeEmcy (Method) - GetNodeId (Method) - GetTimestamp (Method) - GuardError (Method) - GuardErrorNode (Method) - SdoAdd (Method) - SdoReadAsync (Method) - SdoReadData (Method) - SdoReadSync (Method) - SdoWriteAsync (Method) - SdoWriteData (Method) - SdoWriteSync (Method) - SendEmcy (Method) - SendTimestamp (Method)