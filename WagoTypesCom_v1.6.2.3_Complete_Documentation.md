# WagoTypesCom v1.6.2.3 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesCom
- **Version:** 1.6.2.3
- **Categories:** WAGO Internal|Feature|Common|Com; WAGO FunctionalView|Connectivity|Serial; WAGO LayerView|Types and Interfaces; Application
- **Author:** WAGO / u013972
- **Placeholder:** WagoTypesCom

### Description ¶


This document is automatically generated.

Type Definitions for Serial Interfaces

This document is automatically generated. Type Definitions for Serial Interfaces

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Functions - Methods I_ComSniffer.RxData (METH) - I_ComSniffer.TxData (METH) - I_SupportComSniffer.RegisterSniffer (METH) - I_SupportComSniffer.UnregisterSniffer (METH) - I_WagoSysComBase.AttachExclusively (METH) - I_WagoSysComBase.ClearBuffers (METH) - I_WagoSysComBase.Close (METH) - I_WagoSysComBase.Configure (METH) - I_WagoSysComBase.Cyclic (METH) - I_WagoSysComBase.Finish (METH) - ... and 12 more Interfaces - I_ComSniffer (ITF) - I_SupportComSniffer (ITF) - I_WagoSysComBase (ITF) - I_WagoSysDmx (ITF) Program Organization Base Components - I_WagoSysComBase.DeferredResult (PROP) - I_WagoSysComBase.IsOpen (PROP) - I_WagoSysComBase.IsTransmitterEmpty (PROP) - I_WagoSysComBase.Name (PROP) Main Interfaces Other Components - 20 Hardware Lines - 29 Types - 30 Exclusive Usage - 40 Administration - Connection Parameters - I_ComSniffer - I_WagoSysDmx.dwSwVersion (PROP) - Miscellaneous - eTTYHandshake (ENUM) - eTTYLineID (ENUM) - ... and 3 more

### Indices and tables ¶


Based on WagoTypesCom.library, last modified 29.05.2024, 19:51:53. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesCom.library, last modified 29.05.2024, 19:51:53. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesCom Library Documentation


| Company: | WAGO |
| Title: | WagoTypesCom |
| Version: | 1.6.2.3 |
| Categories: | WAGO Internal\|Feature\|Common\|Com; WAGO FunctionalView\|Connectivity\|Serial; WAGO LayerView\|Types and Interfaces; Application |
| Author: | WAGO / u013972 |
| Placeholder: | WagoTypesCom |

### Description


This document is automatically generated.

Type Definitions for Serial Interfaces

This document is automatically generated. Type Definitions for Serial Interfaces

### Contents:


- 20 Program Organization Units I_ComSniffer - I_WagoSysComBase (ITF) - I_WagoSysDmx (ITF) 29 Types - Connection Parameters - Miscellaneous FuGetVersionHistory (FUN)

### Indices and tables


Based on WagoTypesCom.library, last modified 29.05.2024, 19:51:53. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesCom.library, last modified 29.05.2024, 19:51:53. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesCom.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:51:53 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:51:53 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesCom |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesCom |
| DefaultNamespace |  |
| Version | version | 1.6.2.3 |
| Title | string | WagoTypesCom |
| LibraryCategories | library-category-list | WAGO Internal\|Feature\|Common\|Com; WAGO FunctionalView\|Connectivity\|Serial; WAGO LayerView\|Types and Interfaces; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties :

### Functions


## FuGetVersionHistory (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FuGetVersionHistory | DWORD |

| date | version | author | change |
| 28.02.2024 | 1.6.2.3 | u010663 | compiled SP16.3 |
| 07.03.2023 | 1.6.2.2 | u010545 | update comments |
| 01.03.2023 | 1.6.2.1 | u010545 | expansion of eTTYPhysicalLayer -> no continous send / I_WagoDataExchangeModule |
| 14.12.2021 | 1.6.2.0 | u010545 | expansion of I_WagoSysDmx |
| 17.08.2021 | 1.6.1.3 | u010545 | parity mark / space added |
| 07.12.2020 | 1.6.1.2 | u010545 | I_ComSniffer modified |
| 24.11.2020 | 1.6.1.1 | u010545 | I_ComSniffer added |
| 08.01.2019 | 1.6.1.0 | u015842 | Properties: free placeholder added |
| 02.05.2017 | 1.6.0.0 | WAGO / u013972 | Add Interfaces form WagoTypesCom_Internal |
| 23.09.2015 | 1.5.1.0 | WAGO / u013972 | Add Placeholder Property |
| 03.07.2015 | 1.5.0.0 | WAGO / u013972 | Release Version |

WagoTypesCom.library

Interface variables WagoTypesCom.library

### Methods


## I_ComSniffer.RxData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | RxData | BOOL |  |
| Input | pRxBuffer | POINTER TO BYTE | Where the received data |
| udiRxNBytes | UDINT | how many received data |

## I_ComSniffer.TxData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | TxData | BOOL |  |
| Input | pTxBuffer | POINTER TO BYTE | Where the transmit data |
| udiTxNBytes | UDINT | how many transmit data |

## I_SupportComSniffer.RegisterSniffer (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | RegisterSniffer | BOOL |
| Input | IComSniffer | I_ComSniffer |

## I_SupportComSniffer.UnregisterSniffer (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | UnregisterSniffer | BOOL |
| Input | IComSniffer | I_ComSniffer |

## I_WagoSysComBase.AttachExclusively (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | AttachExclusively | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | address of the instance which wants to use the device exclusively |

| result codes |
| 0 | success, exclusive usage is granted |
| EBUSY | Usage is not granted. The device has been attached to another user already |
| EINVAL | Null instance is passed. (Null denotes a detached device) |

Tries to get grant of exclusive acces to the device.

Note (1): This mechanism provides a means for cooperatively using specific devices. However, It does not implement mechanisms for enforcing that policy.

Note (2): It seems suitable to pass the address of the attached high-level-FB as unique identification tag for the client which uses the device. The device, however does not use any knowledge about those high-level-FBs, so virtually any unique number may be passed here.

Interface variables Tries to get grant of exclusive acces to the device. Note (1): This mechanism provides a means for cooperatively using specific devices. However, It does not implement mechanisms for enforcing that policy. Note (2): It seems suitable to pass the address of the attached high-level-FB as unique identification tag for the client which uses the device. The device, however does not use any knowledge about those high-level-FBs, so virtually any unique number may be passed here.

## I_WagoSysComBase.ClearBuffers (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ClearBuffers | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |

| result codes |
| 0 | Success or ‘No Buffers to clear’ |
| EWOULDBLOCK | ClearBuffers requires multiple cycles. Poll ‘DeferredResult’ for a final result. |
| ENOSYS | This operation is not supported by this device. |
| EBUSY | The device is already in use by another client. |
| EACCESS | Other Problems while accessing the serial port (error). |

Clears all internal receive or send buffers of the device.

Interface variables Clears all internal receive or send buffers of the device.

## I_WagoSysComBase.Close (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Close | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |

| result codes |
| 0 | Success, ready for communication. |
| EBUSY | The device is already in use by another client |
| EBADF | The FB was not open |
| EACCES | Close() fails for other reasons |
| EWOULDBLOCK | Close() requires multiple cycles. Poll ‘DeferredResult’ for a final result. |

Closes the connection and detaches the FB from the serial interface.

Interface variables Closes the connection and detaches the FB from the serial interface.

## I_WagoSysComBase.Configure (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Configure | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | unique identification of the caller |
| udiBaudrate | UDINT | Baudrate (9600 = 9k6) |
| usiDataBits | USINT | Number of bits per frame (5..8) |
| eParity | eTTYParity | Parity |
| eStopbits | eTTYStopBits | Number of stop-bits, see note (1) |
| eHandshake | eTTYHandshake | Type of handshake (XON/XOFF, etc) |
| ePhysical | eTTYPhysicalLayer | RS232, RS422, RS485, etc |
| uiSystemBufferSize | UINT | Size of system buffer (important for ‘read’). |

| result codes |
| 0 | Success |
| ENOSYS | This operation is not supported by this device, because it operates with fixed settings. |
| EBUSY | The device is already in use by another client. |
| ENOPROTOOPT | Configuration options not available for this device. |
| EINVAL | Invalid parameters. |
| EBUSY | The device was open at the time of the call. |
| EACCES | Other Error when opening the device. |
| EWOULDBLOCK | Configure requires multiple cycles. Poll ‘DeferredResult’ for a final result. |

Configures a serial FB before opening it

This method is meant to be called when the device is not open. The settings will not take immediate effect, but they will be applied to the interface with the following Open() call.

Note(1): When setting up the number of stop-bits, unusual situations might occur, such as 1.5 stop bits, which is often seen with 5-bit-frames.

Note(2): At a variety of serial interfaces the stop-bit setting affects only the transmitter, while the receiver uniformly requires 1 stop bit and tolerates more, regardless of the setting. This is, however, not the case for synchronous operation, where bit positions of adjacent frames are synchronized.

This method returns one of the following result codes:

Note: This method may be used to try if several settings are allowed for a device without actually opening the device with these settings.

Interface variables Configures a serial FB before opening it This method is meant to be called when the device is not open. The settings will not take immediate effect, but they will be applied to the interface with the following Open() call. Note(1): When setting up the number of stop-bits, unusual situations might occur, such as 1.5 stop bits, which is often seen with 5-bit-frames. Note(2): At a variety of serial interfaces the stop-bit setting affects only the transmitter, while the receiver uniformly requires 1 stop bit and tolerates more, regardless of the setting. This is, however, not the case for synchronous operation, where bit positions of adjacent frames are synchronized. This method returns one of the following result codes: Note: This method may be used to try if several settings are allowed for a device without actually opening the device with these settings.

## I_WagoSysComBase.Cyclic (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Cyclic | eResultCode |

| Result Codes |
| 0 = OK | Regular cyclic processing |
| ENOSYS | No cyclic processing necessary, further calls may be omitted |
| ENOTRECOVERABLE | Unrecoverable Error. Further operation of the port is not possible. |
| (other) | fatal error conditions of the port which cannot be handled otherwise. |

Provides a hook for cyclic processing of the instance.

The instance, which open()s a serial port, is expected to provide a cyclic call of this method unless otherwise noted. These calls continue until the serial port is close()d again. Before open() and after close(), the serial port cannot expect to get any cyclic calls, but it must tolerate it.

Ports without cyclic processing:

When a serial port does not require or inplement cyclic processing, it might silently ignore these calls. It is recommended, however, to return ENOSYS in this case. This will save processor performance, as the opening instance is allowed to NOT issue further cyclic calls, after one of them returns with ENOSYS.

Note(1): The property DeferredResult normally relies on cyclic processing.

Note(2): Unexpected Cyclic()-calls must be tolerated anytime.

Error Codes:

In regular cases, the Cyclic call must return 0=OK or ENOSYS , as described above.

Exceptional conditions which are not recoverable and which will prevent the port from further regular operation might be indicated by ENOTRECOVERABLE . By this means, the calling fb has a chance to detect fatal conditions at an early point in time. (If that is not required, this feedback may also be just ignored.) Once a port returns ENOTRECOVERABLE , it cannot expect to get further Cyclic() calls.

Other result codes are reserved for signalling error conditions, which could not be handled otherwise. Those conditions are, however, currently not specified, nor is the way, Application-FBs are expected to react on them. (Default is: treat as ‘OK’.)

Serial ports must not return other codes unless they are uniformly specified in future versions.

Interface variables Provides a hook for cyclic processing of the instance. The instance, which open()s a serial port, is expected to provide a cyclic call of this method unless otherwise noted. These calls continue until the serial port is close()d again. Before open() and after close(), the serial port cannot expect to get any cyclic calls, but it must tolerate it. Ports without cyclic processing: When a serial port does not require or inplement cyclic processing, it might silently ignore these calls. It is recommended, however, to return ENOSYS in this case. This will save processor performance, as the opening instance is allowed to NOT issue further cyclic calls, after one of them returns with ENOSYS. Note(1): The property DeferredResult normally relies on cyclic processing. Note(2): Unexpected Cyclic()-calls must be tolerated anytime. Error Codes: In regular cases, the Cyclic call must return 0=OK or ENOSYS , as described above. Exceptional conditions which are not recoverable and which will prevent the port from further regular operation might be indicated by ENOTRECOVERABLE . By this means, the calling fb has a chance to detect fatal conditions at an early point in time. (If that is not required, this feedback may also be just ignored.) Once a port returns ENOTRECOVERABLE , it cannot expect to get further Cyclic() calls. Other result codes are reserved for signalling error conditions, which could not be handled otherwise. Those conditions are, however, currently not specified, nor is the way, Application-FBs are expected to react on them. (Default is: treat as ‘OK’.) Serial ports must not return other codes unless they are uniformly specified in future versions.

## I_WagoSysComBase.Finish (METH)


Perform all settings to ensure that this FB will not require any resources from now on

Perform all settings to ensure that this FB will not require any resources from now on

## I_WagoSysComBase.ForceDetachment (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ForceDetachment | eResultCode |

| result codes |
| 0 | success (this operation does not fail) |

Forces detachment of the device.

This is used for initialization or for recovery from crashed client FBs which still hold a zombie lock to the device, which could not be released otherwise. This method is not intended for regular usage.

Interface variables Forces detachment of the device. This is used for initialization or for recovery from crashed client FBs which still hold a zombie lock to the device, which could not be released otherwise. This method is not intended for regular usage.

## I_WagoSysComBase.GetErrorObject (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetErrorObject | eResultCode |  |
| Input | xAcknowledge | BOOL | when TRUE, the error condition is acknowledged with call |
| pBuffer | POINTER TO BYTE | points to the buffer for the error object ADR(oError) |
| udiBufferSize | UDINT | size of the error object SizeOf(oError) |

| result codes |
| 0 | success, error object is retrieved (either OK or NOR) |
| ENOSYS | the COM-interface does not support Error Objects, output is invalid. |
| EFBIG | the buffer size was too small |

retrieves the actual error cause from the hardware inerface and displays it at its output.

The next call would return either an ‘OK’-Object or the next error Object in a series. When FALSE, the same Error object is displayed with each call until the hardware component decides to remove it for any reason.

When a hardware component does not support error objects, this call returns ENOSYS, and the error Object at the Output is invalid.

Interface variables retrieves the actual error cause from the hardware inerface and displays it at its output. xAcknowledge: When TRUE, the error is acknowledged with this call. The next call would return either an ‘OK’-Object or the next error Object in a series. When FALSE, the same Error object is displayed with each call until the hardware component decides to remove it for any reason. When a hardware component does not support error objects, this call returns ENOSYS, and the error Object at the Output is invalid.

## I_WagoSysComBase.GetLineState (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetLineState | BOOL |  |
| Input | eLineID | eTTYLineID | which line; |

retrieves the state of hardware lines, if available.

If no line states are available, this method returns always TRUE.

Interface variables retrieves the state of hardware lines, if available. If no line states are available, this method returns always TRUE.

## I_WagoSysComBase.Initialize (METH)


Perform all settings which are necessary bring the FB into a well-defined (but not necessary operative) state.

Perform all settings which are necessary bring the FB into a well-defined (but not necessary operative) state.

## I_WagoSysComBase.IsLineAvailable (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | IsLineAvailable | BOOL |  |
| Input | eLineID | eTTYLineID | which line; |

checks if the driver and the protocol supports manipulation of a hardware line.

If no extra hardware lines are available, this call returns FALSE. Note: hardware handhake cannot be configured in this case either. If hardware handhake is configured, some lines are not available for manipulation and this call returns FALSE for them. If lines are available and no hardware handshake is configured, the call returns TRUE.

Interface variables checks if the driver and the protocol supports manipulation of a hardware line. If no extra hardware lines are available, this call returns FALSE. Note: hardware handhake cannot be configured in this case either. If hardware handhake is configured, some lines are not available for manipulation and this call returns FALSE for them. If lines are available and no hardware handshake is configured, the call returns TRUE.

## I_WagoSysComBase.Open (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Open | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | unique identification of the caller |

| result codes |
| 0 | Success, ready for communication. |
| EBUSY | The device is already in use by another client |
| ENOPROTOOPT | Configuration options not available for this device (e.g. hardware handshake) |
| EWOULDBLOCK | Open requires multiple cycles. Poll ‘DeferredResult’ for a final result. |
| EALREADY | The Fb is already open |
| EACCES | Other Error when opening the device |

Attaches an FB to a serial port at runtime.

The device is opened with the previously set settings. The device performs the following actions on this call:

This method returns one of the following result codes:

Interface variables Attaches an FB to a serial port at runtime. The device is opened with the previously set settings. The device performs the following actions on this call: - it configures its hardware with the settings which are previously sent with Configure() if the device does not operate on fixed settings. - it switches on the receiver in order to accept data from the line This method returns one of the following result codes:

## I_WagoSysComBase.Read (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Read | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | unique identification of the caller |
| pRxBuffer | POINTER TO BYTE | Location of receive buffer. |
| udiRxBufferSize | UDINT | Size of the receive buffer. |
| Output | udiRxNBytes | UDINT | Number of transferred bytes. |

| result codes |
| 0 | Success. |
| EBUSY | The device is already in use by another client. |
| EBADF | The FB is not open (error). |
| EINVAL | Invalid parameters (error). |
| EBADMSG | Integrity of data is severed (Parity-Error or Frame-Error). |
| EACCESS | Other Problems while accessing the serial port. |

Reads data from the serial port.

A description of the location and the size of the data area is fed into the method.

When no bytes or less bytes than the buffer size are received, the number of transferred bytes is returned via the output udiRxNBytes, but no error status is raised because of the lack of data.

When exactly the amount of requested data is read, udiRxNBytes denotes exactly that size, but there is no hint if more data could be expected with a consecutive read.

This method returns one of the following result codes:

Interface variables Reads data from the serial port. A description of the location and the size of the data area is fed into the method. When no bytes or less bytes than the buffer size are received, the number of transferred bytes is returned via the output udiRxNBytes, but no error status is raised because of the lack of data. When exactly the amount of requested data is read, udiRxNBytes denotes exactly that size, but there is no hint if more data could be expected with a consecutive read. This method returns one of the following result codes:

## I_WagoSysComBase.ReleaseExclusivity (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ReleaseExclusivity | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | address of the instance which reseases its exclusivity |

| result codes |
| 0 | success, the device is detached again |
| EBUSY | Usage has not been granted to this FB. It is in use by another FB |
| EINVAL | Null instance is passed. (Null denotes a detached device) |

Releases the device from exclusive usage.

Interface variables Releases the device from exclusive usage.

## I_WagoSysComBase.SetLineState (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SetLineState | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | unique identification of the caller |
| eLineID | eTTYLineID | which line; |
| xState | BOOL | to which state? TRUE = active |

| result codes |
| 0 | success, ready for communication. |
| ENOSYS | This interface does not support control of hardware lines |
| EBUSY | the device is already in use by another client |
| ENOTCONN | The FB represents a revovable device which has been disconnected during operation (very unlikely) |
| EINVAL | Invalid line ID for output |
| EPROTONOSUPPORT | Device is configured for RS485 protocol |
| EBADF | Not open |
| EACCES | Could not set the line |

allows control of the hardware lines to the application

Regularly, these lines are controlled by hardware handshake internally. Nevertheless, when no hardware handshake is involved, the serial lines might be used for very individual purposes.

In the latter case, these hardware wires can be manipulated directly with this functions to desired levels, according to the need of the actual application. This allows to implement some exotic handshake schemes which are not foreseen at the time of the creation of this library.

Interface variables allows control of the hardware lines to the application Regularly, these lines are controlled by hardware handshake internally. Nevertheless, when no hardware handshake is involved, the serial lines might be used for very individual purposes. In the latter case, these hardware wires can be manipulated directly with this functions to desired levels, according to the need of the actual application. This allows to implement some exotic handshake schemes which are not foreseen at the time of the creation of this library.

## I_WagoSysComBase.TestExclusivity (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | TestExclusivity | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | address of the instance which wants to use the device exclusively |

| result codes |
| 0 | success, exclusive usage is granted |
| EUNATCH | the device is not attached at all |
| EBUSY | Usage is not granted. The device has been attached to another FB already |

Tests if an FB has been granted exclusive usage of the device without trying to attach it

Interface variables Tests if an FB has been granted exclusive usage of the device without trying to attach it

## I_WagoSysComBase.Write (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Write | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |
| pTxBuffer | POINTER TO BYTE | Location of write data. |
| udiTxNBytes | UDINT | Number of bytes to be written. |
| Output | udiTxNBytesTransferred | UDINT | Nuimber of transferred bytes. |

| result codes |
| 0 | Success, ready for communication. |
| EBUSY | The device is already in use by another client. |
| EBADF | The FB is not open. |
| EINVAL | Invalid parameters. |
| EWOULDBLOCK | FB is busy with previous data and would block. |

Writes data to the serial port.

The first two arguments describe the loaction and the amount of data to be sent. Note: it is formally ok, to pass ‘no’ bytes for write. In that case, simply nothing happens.

Via udiTxNBytesTransferred a feedback is given, how many bytes are actually transferred to the firmware layer. If this is less than th erequested amount, write() returns with EWOULDBLOCK, which is a regular state. In that case, sending of the remaining data has to be tried again later.

This method returns the following result codes:

Interface variables Writes data to the serial port. The first two arguments describe the loaction and the amount of data to be sent. Note: it is formally ok, to pass ‘no’ bytes for write. In that case, simply nothing happens. Via udiTxNBytesTransferred a feedback is given, how many bytes are actually transferred to the firmware layer. If this is less than th erequested amount, write() returns with EWOULDBLOCK, which is a regular state. In that case, sending of the remaining data has to be tried again later. This method returns the following result codes:

## I_WagoSysDmx.diDmxStartAddress (PROP)


-1 –> use terminal settings otherwise allowed range 0..65535

-1 –> use terminal settings otherwise allowed range 0..65535

### Interfaces


## I_ComSniffer (ITF)


- I_ComSniffer.RxData (METH) - I_ComSniffer.TxData (METH)

## I_SupportComSniffer (ITF)


- I_SupportComSniffer.RegisterSniffer (METH) - I_SupportComSniffer.UnregisterSniffer (METH)

## I_WagoSysComBase (ITF)


```
VAR_GLOBAL
      FbCom1 : WagoSysSerialInterface_Internal_Targetspecific IMPLEMENTS I_WagoSysComBase;
      FbCom2 : WagoSysSerialInterface_Internal_Targetspecific IMPLEMENTS I_WagoSysComBase;
END_VAR
```

```
FbMyComfortSerialInterface.OpenAndConfigure(FbCom1, 9600, 8, eTTYParity.None, ... );
```

CDS-Interface for serial interfaces.

Instances which implements this interface are used as inputs for higher-level FBs, e.g. in WagoAppCom. These instances are not intended to be controlled directly, but they are rather meant to be controlled exclusively from the higher-level FBs.

Intended usage:

For each avalilable COM subdevice, a unique global FB will be provided via PLC configuration. These FBs implement the behaviour of the different hardware types of serial interfaces.

All these FBs implement this common interface I WagoSysComBase, which is defined in this libraray.

When a serial interface is used by other libraries, these libraries expect this interface for identifying the hardware:

Attention: There is no means implemented for preventing the application from directly using the methods of this interface in an uncontrolled manner.

CDS-Interface for serial interfaces. Instances which implements this interface are used as inputs for higher-level FBs, e.g. in WagoAppCom. These instances are not intended to be controlled directly, but they are rather meant to be controlled exclusively from the higher-level FBs. Intended usage: For each avalilable COM subdevice, a unique global FB will be provided via PLC configuration. These FBs implement the behaviour of the different hardware types of serial interfaces. All these FBs implement this common interface I WagoSysComBase, which is defined in this libraray. When a serial interface is used by other libraries, these libraries expect this interface for identifying the hardware: Attention: There is no means implemented for preventing the application from directly using the methods of this interface in an uncontrolled manner. - 10 Main Interface I_WagoSysComBase.ClearBuffers (METH) - I_WagoSysComBase.Close (METH) - I_WagoSysComBase.Configure (METH) - I_WagoSysComBase.DeferredResult (PROP) - I_WagoSysComBase.IsOpen (PROP) - I_WagoSysComBase.IsTransmitterEmpty (PROP) - I_WagoSysComBase.Open (METH) - I_WagoSysComBase.Read (METH) - I_WagoSysComBase.Write (METH) 20 Hardware Lines - I_WagoSysComBase.GetLineState (METH) - I_WagoSysComBase.IsLineAvailable (METH) - I_WagoSysComBase.SetLineState (METH) 30 Exclusive Usage - I_WagoSysComBase.AttachExclusively (METH) - I_WagoSysComBase.ForceDetachment (METH) - I_WagoSysComBase.ReleaseExclusivity (METH) - I_WagoSysComBase.TestExclusivity (METH) 40 Administration - I_WagoSysComBase.Cyclic (METH) - I_WagoSysComBase.Finish (METH) - I_WagoSysComBase.GetErrorObject (METH) - I_WagoSysComBase.Initialize (METH) - I_WagoSysComBase.Name (PROP)

## I_WagoSysDmx (ITF)


For serial modules that support DMX like 750-652

For serial modules that support DMX like 750-652 - I_WagoSysDmx.diDmxStartAddress (PROP) - I_WagoSysDmx.dwSwVersion (PROP)

### Program Organization


## 20 Program Organization Units


- I_ComSniffer I_ComSniffer (ITF) I_ComSniffer.RxData (METH) - I_ComSniffer.TxData (METH) I_SupportComSniffer (ITF) - I_SupportComSniffer.RegisterSniffer (METH) - I_SupportComSniffer.UnregisterSniffer (METH) I_WagoSysComBase (ITF) - 10 Main Interface I_WagoSysComBase.ClearBuffers (METH) - I_WagoSysComBase.Close (METH) - I_WagoSysComBase.Configure (METH) - I_WagoSysComBase.DeferredResult (PROP) - I_WagoSysComBase.IsOpen (PROP) - I_WagoSysComBase.IsTransmitterEmpty (PROP) - I_WagoSysComBase.Open (METH) - I_WagoSysComBase.Read (METH) - I_WagoSysComBase.Write (METH) 20 Hardware Lines - I_WagoSysComBase.GetLineState (METH) - I_WagoSysComBase.IsLineAvailable (METH) - I_WagoSysComBase.SetLineState (METH) 30 Exclusive Usage - I_WagoSysComBase.AttachExclusively (METH) - I_WagoSysComBase.ForceDetachment (METH) - I_WagoSysComBase.ReleaseExclusivity (METH) - I_WagoSysComBase.TestExclusivity (METH) 40 Administration - I_WagoSysComBase.Cyclic (METH) - I_WagoSysComBase.Finish (METH) - I_WagoSysComBase.GetErrorObject (METH) - I_WagoSysComBase.Initialize (METH) - I_WagoSysComBase.Name (PROP) I_WagoSysDmx (ITF) - I_WagoSysDmx.diDmxStartAddress (PROP) - I_WagoSysDmx.dwSwVersion (PROP)

### Base Components


## I_WagoSysComBase.DeferredResult (PROP)


| result codes |
| 0 | Ok: the channel is operative. |
| EAGAIN | Open() or ClearBuffers() is pending, no feedback so far (no error). |
| ENOPROTOOPT | configuration options not available for this device (e.g. hardware handshake, error). |
| EBADF | The FB is not open (error). |
| EINVAL | Invalid parameters (error). |
| EBUSY | Open failed because the FB was open for another client. |
| EACCESS | Other Problems while accessing the serial port (error). |

Status of the channel after deferred open() or clearBuffers().

Status of the channel after deferred open() or clearBuffers().

## I_WagoSysComBase.IsOpen (PROP)


Tells the application if the FB open and ready for operation.

Note: while Open() is still pending but not completed, IsOpen() remains false.

Tells the application if the FB open and ready for operation. Note: while Open() is still pending but not completed, IsOpen() remains false.

## I_WagoSysComBase.IsTransmitterEmpty (PROP)


| result codes |
| 0 | Transmitter is empty and no more bytes to send |
| EINPROGRESS | Transmitter has still bytes to send |
| ENOSYS | This operation is not supported by the device. |
| EACCES | Internal error: it could not be determined if bytes are pending or not |

Determines if the transmitter has still bytes to send or not.

Three different reactions are possible:

If the transmitter is empty, this property delivers 0=OK, if it has bytes to send, it delivers EINPROGRESS. If the device cannot tell anything about its status, it delivers ENOSYS.

Note: In particular cases it may be technically impossible for a device to determine, if the transmitter has sttill data to send or not. In thoses cases this method must return ENOSYS.

Determines if the transmitter has still bytes to send or not. Three different reactions are possible: If the transmitter is empty, this property delivers 0=OK, if it has bytes to send, it delivers EINPROGRESS. If the device cannot tell anything about its status, it delivers ENOSYS. Note: In particular cases it may be technically impossible for a device to determine, if the transmitter has sttill data to send or not. In thoses cases this method must return ENOSYS.

## I_WagoSysComBase.Name (PROP)


returns the name of the connected interface

returns the name of the connected interface

### Main Interfaces


## 10 Main Interface


- I_WagoSysComBase.ClearBuffers (METH) - I_WagoSysComBase.Close (METH) - I_WagoSysComBase.Configure (METH) - I_WagoSysComBase.DeferredResult (PROP) - I_WagoSysComBase.IsOpen (PROP) - I_WagoSysComBase.IsTransmitterEmpty (PROP) - I_WagoSysComBase.Open (METH) - I_WagoSysComBase.Read (METH) - I_WagoSysComBase.Write (METH)

### Other Components


## 20 Hardware Lines


- I_WagoSysComBase.GetLineState (METH) - I_WagoSysComBase.IsLineAvailable (METH) - I_WagoSysComBase.SetLineState (METH)

## 29 Types


- Connection Parameters eTTYHandshake (ENUM) - eTTYParity (ENUM) - eTTYPhysicalLayer (ENUM) - eTTYStopBits (ENUM) Miscellaneous - eTTYLineID (ENUM)

## 30 Exclusive Usage


- I_WagoSysComBase.AttachExclusively (METH) - I_WagoSysComBase.ForceDetachment (METH) - I_WagoSysComBase.ReleaseExclusivity (METH) - I_WagoSysComBase.TestExclusivity (METH)

## 40 Administration


- I_WagoSysComBase.Cyclic (METH) - I_WagoSysComBase.Finish (METH) - I_WagoSysComBase.GetErrorObject (METH) - I_WagoSysComBase.Initialize (METH) - I_WagoSysComBase.Name (PROP)

## Connection Parameters


Types for settings which are typically used for opening or configuring a serial device.

Types for settings which are typically used for opening or configuring a serial device. - eTTYHandshake (ENUM) - eTTYParity (ENUM) - eTTYPhysicalLayer (ENUM) - eTTYStopBits (ENUM)

## I_ComSniffer


- I_ComSniffer (ITF) I_ComSniffer.RxData (METH) - I_ComSniffer.TxData (METH) I_SupportComSniffer (ITF) - I_SupportComSniffer.RegisterSniffer (METH) - I_SupportComSniffer.UnregisterSniffer (METH)

## I_WagoSysDmx.dwSwVersion (PROP)


2 Byte ASCII Example (04) –> 16#3034

2 Byte ASCII Example (04) –> 16#3034

## Miscellaneous ¶


## eTTYHandshake (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| Default | 0 | Use default behaviour of the interface |
| None | 1 | No handshake at all |
| XON_XOFF | 2 | Software handshake |
| Hardware_DTE_RTSCTS | 3 | DTE, listens for: CTS; drives: RTS, DTR. |
| Hardware_DCE_RTSCTS | 4 | DCE, drives: CTS, DSR, DCD, RI; listens on: RTS, |
| Hardware_DTE_DSRDTR | 5 | DTE, listens for: DSR, DCD, RI; drives: RTS, DTR. |
| Hardware_DCE_DSRDTR | 6 | DCE, drives: CTS, DSR, DCD, RI; listens on: DTR. |
| Hardware_RTS_LeadTime | 7 | Specific functionality of 75x-652 and 75x-1652 |

Configuration parameter for automatic handshake handling.

For hardware handshake, the interface may play the role of a Data Terminal Equipment (DTE) or a Data Communication Equipment (DCE). Not all hardware can be set up to any role. The PFC 750-8202, e.g. provides hardware only for the DCE role, not for DTE.

Furthermode, hardware handhake differenciates between two major sub-modes, involving either the lines (CTS, RTS) in one case, or (DSR, DCD, RI, DTR) in the other case.

InOut: Configuration parameter for automatic handshake handling. For hardware handshake, the interface may play the role of a Data Terminal Equipment (DTE) or a Data Communication Equipment (DCE). Not all hardware can be set up to any role. The PFC 750-8202, e.g. provides hardware only for the DCE role, not for DTE. Furthermode, hardware handhake differenciates between two major sub-modes, involving either the lines (CTS, RTS) in one case, or (DSR, DCD, RI, DTR) in the other case.

## eTTYLineID (ENUM)


| Name | Comment |
| --- | --- |
| LineRTSCTS | Request to Send (DCE input) or Clear to Send (DCE output) |
| LineDTRDSR | Data Terminal Ready (DCE input) or Data Set Ready (DCE output) |
| LineDCD | Data carrier Detect (DCE output, DTE input) |
| LineRI | Ring Indicator (DCE output, DTE input) |

Identifies special hardware lines at the serial port for “manipulation of hardware lines”.

(see: SetLineState(), GetLineState())

The following enumeration identifies, which hardware line is to be manipulated by the appropriate functions (SetLineState(), GetLineState())

Please note, that the same lines have different namings, depending upon if the PLC is in the role of either a DCE or a DTE. In one role a line is an output while in the other role the same line acts as input.

Please note also that not all hardware lines are available on each hardware.

InOut: Identifies special hardware lines at the serial port for “manipulation of hardware lines”. (see: SetLineState(), GetLineState()) The following enumeration identifies, which hardware line is to be manipulated by the appropriate functions (SetLineState(), GetLineState()) Please note, that the same lines have different namings, depending upon if the PLC is in the role of either a DCE or a DTE. In one role a line is an output while in the other role the same line acts as input. Please note also that not all hardware lines are available on each hardware.

## eTTYParity (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| Default | 0 | Use default behaviour of the interface |
| None | 1 | No parity bit |
| Odd | 2 | Odd parity (sum of all data bits and parity bit contents odd) |
| Even | 3 | Even parity (sum of all data bits and parity bit contents is even) |
| Mark | 4 | parity bit always 1 |
| Space | 5 | parity bit always 0 |

Configuration parameter for the parity bit

InOut: Configuration parameter for the parity bit

## eTTYPhysicalLayer (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| Default | 0 | Use default behaviour of the interface |
| RS232 | 1 |  |
| RS422 | 2 |  |
| RS423 | 3 |  |
| RS485_HalfDuplex | 4 |  |
| RS485_FullDuplex | 5 |  |
| DMX_HalfDuplex | 6 |  |
| RS232_No_SC | 11 | disable continous send |
| RS422_No_SC | 12 | disable continous send |
| RS485_HalfDuplex_No_SC | 14 | disable continous send |
| RS485_FullDuplex_No_SC | 15 | disable continous send |

This type denotes different physical configurations.

InOut: This type denotes different physical configurations.

## eTTYStopBits (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| Default | 0 | Use default behaviour of the interface |
| None | 1 | No stop bit, i.e. synchronous operation |
| Minimum | 2 | Minimum possible value (typically 1); |
| One | 3 | Exactly 1 stop bit required |
| OneDotFive | 4 | Exactly 1.5 stop bit (often seen in combination with 5-bit- frames) |
| Two | 5 | Exactly 2 stop bits required |
| Maximum | 255 | Maximum possible value (typically 2) |

Encodes how many stop bits are desired.

Note (1): The values ‘Default’, ‘Minimum’, and ‘Maximum’ do not specify an exact number of stop bits. Instead they advise the physical device to use a setting which is most appropriate, but which may differ between different device types.

Note (2): Not every hardware supports every stop bit setting. E.g. the values ‘None’ (synchronous operation) or ‘OneDotFive’ are available only on certain specialized devices.

InOut: Encodes how many stop bits are desired. Note (1): The values ‘Default’, ‘Minimum’, and ‘Maximum’ do not specify an exact number of stop bits. Instead they advise the physical device to use a setting which is most appropriate, but which may differ between different device types. Note (2): Not every hardware supports every stop bit setting. E.g. the values ‘None’ (synchronous operation) or ‘OneDotFive’ are available only on certain specialized devices.