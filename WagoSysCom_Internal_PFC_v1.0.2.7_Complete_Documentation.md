# WagoSysCom_Internal_PFC v1.0.2.7 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysCom_Internal_PFC
- **Version:** 1.0.2.7
- **Categories:** WAGO Internal|Target|PFC; WAGO Internal|Feature|Common|Com
- **Namespace:** WagoSysCom_Internal
- **Author:** WAGO / u013972

### Description ¶


This document is automatically generated.

Target specific library for the onboard serial interface (COM1 on PFC)

This document is automatically generated. Target specific library for the onboard serial interface (COM1 on PFC)

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks FbSerialInterface_internal (FB) - doc10_general (FB) Methods - FbSerialInterface_internal.AttachExclusively (METH) - FbSerialInterface_internal.ClearBuffers (METH) - FbSerialInterface_internal.Close (METH) - FbSerialInterface_internal.Configure (METH) - FbSerialInterface_internal.Cyclic (METH) - FbSerialInterface_internal.Finish (METH) - FbSerialInterface_internal.ForceDetachment (METH) - FbSerialInterface_internal.GetErrorObject (METH) - FbSerialInterface_internal.GetLineState (METH) - FbSerialInterface_internal.Initialize (METH) - ... and 9 more Program Organization Base Components Main Interfaces Internal Components - FbSerialInterface_internal.DeferredResult (PROP) - FbSerialInterface_internal.IsTransmitterEmpty (PROP) - FbSerialInterface_internal.Name (PROP) - FbSerialInterface_internal.isOpen (PROP) - WagoSysCom_Internal_PFC Library Documentation Global Variable Lists Other Components - 20 Hardware Lines - 20 I_SupportComSniffer - 30 Exclusive Use - 40 Administration - ParameterList (PARAMS)

### Indices and tables ¶


Based on WagoSysCom_Internal_PFC.library, last modified 29.05.2024, 19:51:57. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysCom_Internal_PFC.library, last modified 29.05.2024, 19:51:57. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## 10 Documentation ¶


### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysCom_Internal_PFC.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:51:57 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:51:57 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| DefaultNamespace | WagoSysCom_Internal |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysCom_Internal_PFC |
| NoPlaceholder |  |
| Version | version | 1.0.2.7 |
| Title | string | WagoSysCom_Internal_PFC |
| LibraryCategories | library-category-list | WAGO Internal\|Target\|PFC; WAGO Internal\|Feature\|Common\|Com |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CmpErrors2 Interfaces Library Identification : Name: CmpErrors2 Interfaces Version: newest Company: System Namespace: CmpErrors Library Properties : Standard Library Identification : Placeholder: Standard Default Resolution: Standard, * (System) Namespace: Standard Library Properties : SysCom Library Identification : Placeholder: SysCom Default Resolution: SysCom, * (System) Namespace: SysCom Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysPlainMem Library Identification : Placeholder: WagoSysPlainMem Default Resolution: WagoSysPlainMem, * (WAGO) Namespace: WagoSysPlainMem Library Properties : WagoSysTypedefs_Internal_32Bit Library Identification : Placeholder: WagoSysTypedefsInternal Default Resolution: WagoSysTypedefs_Internal_32Bit, * (WAGO) Namespace: WagoTypesInternal Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCom Library Identification : Placeholder: WagoTypesCom Default Resolution: WagoTypesCom, * (WAGO) Namespace: WagoTypesCom Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : Library Parameter : Parameter: MAX_STRING_LENGTH = 255 Parameter: MAX_WSTRING_LENGTH = 255

### Function Blocks


## FbSerialInterface_internal (FB)


This is the fundamental FB of this library and contains the interface to the pyhsical serial interface.

Each open FB represents one physical serial interface according to ‘I_WagoSysComBase’.

Please Note : This FB is meant to be accessed by application-level FBs from WagoAppCom.library. Under normal circumstances it should not be used directly.

Multiple application FBs may share one physical serial interface FB, but in that case they must not be open simultaneously. I.e. if an FbSerialInterface_internal is opened by one application, it cannot be opened once more by another application FB until the first ‘open()’ is ‘close()’d again.

This is the fundamental FB of this library and contains the interface to the pyhsical serial interface. Each open FB represents one physical serial interface according to ‘I_WagoSysComBase’. Please Note : This FB is meant to be accessed by application-level FBs from WagoAppCom.library. Under normal circumstances it should not be used directly. Multiple application FBs may share one physical serial interface FB, but in that case they must not be open simultaneously. I.e. if an FbSerialInterface_internal is opened by one application, it cannot be opened once more by another application FB until the first ‘open()’ is ‘close()’d again. - 10 I_WagoSysComBase 10 Main Interface FbSerialInterface_internal.ClearBuffers (METH) - FbSerialInterface_internal.Close (METH) - FbSerialInterface_internal.Configure (METH) - FbSerialInterface_internal.DeferredResult (PROP) - FbSerialInterface_internal.IsTransmitterEmpty (PROP) - FbSerialInterface_internal.Open (METH) - FbSerialInterface_internal.Read (METH) - FbSerialInterface_internal.Write (METH) - FbSerialInterface_internal.isOpen (PROP) 20 Hardware Lines - FbSerialInterface_internal.GetLineState (METH) - FbSerialInterface_internal.IsLineAvailable (METH) - FbSerialInterface_internal.SetLineState (METH) 30 Exclusive Use - FbSerialInterface_internal.AttachExclusively (METH) - FbSerialInterface_internal.ForceDetachment (METH) - FbSerialInterface_internal.ReleaseExclusivity (METH) - FbSerialInterface_internal.TestExclusivity (METH) 40 Administration - FbSerialInterface_internal.Cyclic (METH) - FbSerialInterface_internal.Finish (METH) - FbSerialInterface_internal.GetErrorObject (METH) - FbSerialInterface_internal.Initialize (METH) - FbSerialInterface_internal.Name (PROP) 20 I_SupportComSniffer - FbSerialInterface_internal.RegisterSniffer (METH) - FbSerialInterface_internal.UnregisterSniffer (METH)

## doc10_general (FB)


This library provides target specific internal functions and TSC-functions for handling the internal COM (physical) interfaces of PFC. Mainly it provides the FB ‘FbSerialInterface_internal’ which implements the interface ‘I_WagoSysComBase’.

Please note: The components of that interface are not meant to be used directly by application programs.

Instead, there exist more high-level libraries, e.g. WagoAppCom, which take references to instances of I_WagoSysComBase or FbSerialInterface_internal as input parameter and then provide appropriate functionality at application-level. Those libraries are also capable of handling other implementations of this software interface, e.g. those for K-Bus hardware. Under normal circumstances, the functions and methods which are described in this document should only be used in libraries, never in applications.

Please refer to the specification of I_WagoSysComBase in WagoTypesCom_Internal.library for a more comprehensive description of the functionality of that interface.

Note(2): Additionally this library also contains code for mediating between firmware compontents (TSC) and the formal ‘I_WagoSysComBase’-Implementation. These functions are visible only in the original source code and are otherwise hidden in the public documentation, because the interfaces of these non-public parts may change without further notice.

For detailed information about data types which are used in this internal library, please refer to the type definitions given in WagoTypesCom.library and WagoTypesCommon.library .

This library provides target specific internal functions and TSC-functions for handling the internal COM (physical) interfaces of PFC. Mainly it provides the FB ‘FbSerialInterface_internal’ which implements the interface ‘I_WagoSysComBase’. Please note: The components of that interface are not meant to be used directly by application programs. Instead, there exist more high-level libraries, e.g. WagoAppCom, which take references to instances of I_WagoSysComBase or FbSerialInterface_internal as input parameter and then provide appropriate functionality at application-level. Those libraries are also capable of handling other implementations of this software interface, e.g. those for K-Bus hardware. Under normal circumstances, the functions and methods which are described in this document should only be used in libraries, never in applications. Please refer to the specification of I_WagoSysComBase in WagoTypesCom_Internal.library for a more comprehensive description of the functionality of that interface. Note(2): Additionally this library also contains code for mediating between firmware compontents (TSC) and the formal ‘I_WagoSysComBase’-Implementation. These functions are visible only in the original source code and are otherwise hidden in the public documentation, because the interfaces of these non-public parts may change without further notice. For detailed information about data types which are used in this internal library, please refer to the type definitions given in WagoTypesCom.library and WagoTypesCommon.library .

### Methods


## FbSerialInterface_internal.AttachExclusively (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | AttachExclusively | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | Address of the instance |

| result codes |
| 0 | Success, exclusive use has been granted. |
| EBUSY | Exclusive use has been refused. The device has already been attached to another user. |
| EINVAL | Null instance has been passed. (Null denotes a detached device) |

Tries to get exclusive access to the device.

Note (1): This mechanism provides a means for cooperatively using specific devices. However, It does not implement mechanisms for enforcing that policy.

Note (2): It seems suitable to pass the address of the attached high-level-FB as the unique identification tag for the client which uses the device. The device, however, does not have any knowledge about these high-level-FBs, so virtually any unique number may be passed here.

Note (3): “RequestorID” corresponds to the address of the instance which should use the device exclusively.

Interface variables Tries to get exclusive access to the device. Note (1): This mechanism provides a means for cooperatively using specific devices. However, It does not implement mechanisms for enforcing that policy. Note (2): It seems suitable to pass the address of the attached high-level-FB as the unique identification tag for the client which uses the device. The device, however, does not have any knowledge about these high-level-FBs, so virtually any unique number may be passed here. Note (3): “RequestorID” corresponds to the address of the instance which should use the device exclusively.

## FbSerialInterface_internal.ClearBuffers (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ClearBuffers | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |

| Result Codes |
| 0 | Success |
| EBUSY | The FB is busy with another client. |
| EACCES | There was a problem while opening the system com port. |
| EBADF | The com-port was not open. |

Clears all internal receive or send buffers of the device.

Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method, in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.

Interface variables Clears all internal receive or send buffers of the device. Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method, in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.

## FbSerialInterface_internal.Close (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Close | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |

| Result Codes |
| 0 | Success |
| EBUSY | The FB is busy with another client. |
| EACCES | There was a problem while closing the system com-port. |
| EBADF | The com-port was not open. |

Closes the connection and detaches the FB from the serial interface.

Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method, in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.

Interface variables Closes the connection and detaches the FB from the serial interface. Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method, in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.

## FbSerialInterface_internal.Configure (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Configure | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |
| udiBaudrate | UDINT | Baudrate (9600 = 9k6) |
| usiDataBits | USINT | Number of Bits per frame (5..8) |
| eParity | eTTYParity | Parity |
| eStopbits | eTTYStopBits | Number of Stop-Bits (see Note 1) |
| eHandshake | eTTYHandshake | Type of handshake (XON/XOFF, etc) |
| ePhysical | eTTYPhysicalLayer | RS232, RS422, RS485, etc |
| uiSystemBufferSize | UINT | Size of system buffer (important for ‘read’) |

| Result Codes |
| 0 | Success |
| EBUSY | The FB is busy with another client. |
| EALREADY | The com-port is already open. |
| ENOPROTOOPT | The requested option or physical layer (e.g. ‘RS-xyz’) is not available. |

Configures a serial FB before opening it.

This method is intended to be called before opening the device. The settings will thus not take immediate effect, but they will be applied to the device with the following Open() call.

Note(1): For eStopbits the settings ‘None’ (for synchronous operation) and ‘OneDotFive’ (1.5 stop bits, as common for teletypewriters) are not supported and will result in ENOPROTOOPT.

This method returns the following result codes:

Note(2): Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method, in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.

Note (3): This method may be used to try if several settings are allowed for a device without actually opening the device with these settings.

Interface variables Configures a serial FB before opening it. This method is intended to be called before opening the device. The settings will thus not take immediate effect, but they will be applied to the device with the following Open() call. Note(1): For eStopbits the settings ‘None’ (for synchronous operation) and ‘OneDotFive’ (1.5 stop bits, as common for teletypewriters) are not supported and will result in ENOPROTOOPT. This method returns the following result codes: Note(2): Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method, in this implementation it will complete its job immediately and it will not return EWOULDBLOCK. Note (3): This method may be used to try if several settings are allowed for a device without actually opening the device with these settings.

## FbSerialInterface_internal.Cyclic (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Cyclic | eResultCode |

| Result Code |
| ENOSYS | No cyclic processing necessary, further calls may be omitted. |

Cyclic processing of this FB.

This method is not implemented.

In general, this method is intended for carrying out cyclic operation of the connected instance. Cyclic operation would be necessary, if one or more operations were deferred for future completion (such as Open(), etc.). Then this deferred execution is carried out by this cyclic call.

As this FbSerialInterface_internal does not defer anything there is no need for cyclic operation.

Interface variables Cyclic processing of this FB. This method is not implemented. In general, this method is intended for carrying out cyclic operation of the connected instance. Cyclic operation would be necessary, if one or more operations were deferred for future completion (such as Open(), etc.). Then this deferred execution is carried out by this cyclic call. As this FbSerialInterface_internal does not defer anything there is no need for cyclic operation.

## FbSerialInterface_internal.Finish (METH)


Detach and close a serial interface.

This method is called before destruction (FB_Exit) It has no return value.

Detach and close a serial interface. This method is called before destruction (FB_Exit) It has no return value.

## FbSerialInterface_internal.ForceDetachment (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ForceDetachment | eResultCode |

| result codes |
| 0 | Success (this operation does not fail) |

Forces detachment of the device.

This is used for initialization or for recovery from crashed client FBs which still hold a lock on the device, which could not be released. This method is meant for emergency recovery rather than for regular use.

Interface variables Forces detachment of the device. This is used for initialization or for recovery from crashed client FBs which still hold a lock on the device, which could not be released. This method is meant for emergency recovery rather than for regular use.

## FbSerialInterface_internal.GetErrorObject (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetErrorObject | eResultCode |  |
| Input | xAcknowledge | BOOL | Auto-acknowledge the error object. |
| pBuffer | POINTER TO BYTE | Location of result buffer for the error object. |
| udiBufferSize | UDINT | Size of the result buffer. |

Obtains error cause from hardware interface.

As COM1 does not produce any error objects, this method is not implemented and returns ENOSYS. The result buffer which is indicated by ‘pBuffer’ remains unchanged.

Interface variables Obtains error cause from hardware interface. As COM1 does not produce any error objects, this method is not implemented and returns ENOSYS. The result buffer which is indicated by ‘pBuffer’ remains unchanged.

## FbSerialInterface_internal.GetLineState (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetLineState | BOOL |  |
| Input | eLineID | eTTYLineID | Line to be obtained. |

Retrieve the state of hardware lines, if available.

This method yields TRUE if the addressed hardware line shows an ‘active’ physical level (+3..+15V for RS232) and FALSE if it shows a ‘passive’ physical level (-3..-15V for RS232). If the level cannot be retrieved, TRUE is returned.

Interface variables Retrieve the state of hardware lines, if available. This method yields TRUE if the addressed hardware line shows an ‘active’ physical level (+3..+15V for RS232) and FALSE if it shows a ‘passive’ physical level (-3..-15V for RS232). If the level cannot be retrieved, TRUE is returned.

## FbSerialInterface_internal.Initialize (METH)


Initialize FbSerialInterface_internal at Fb_Init().

This method initalizes member variables and properties of the FB ‘FbSerialInterface_internal’ to an initial state.

Initialize FbSerialInterface_internal at Fb_Init(). This method initalizes member variables and properties of the FB ‘FbSerialInterface_internal’ to an initial state.

## FbSerialInterface_internal.IsLineAvailable (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | IsLineAvailable | BOOL |  |
| Input | eLineID | eTTYLineID | Hardware line to check for manipulation. |

Checks if manipulation of a hardware line is possible.

This method checks whether the driver and protocol support manipulation of the hardware line.

If no extra hardware lines are available, this call returns FALSE. Note: hardware handshake cannot be configured in this case either. If hardware handshake is configured, some lines are not available for manipulation and this call returns FALSE for them. If lines are available and no hardware handshake is configured, the call returns TRUE.

Interface variables Checks if manipulation of a hardware line is possible. This method checks whether the driver and protocol support manipulation of the hardware line. If no extra hardware lines are available, this call returns FALSE. Note: hardware handshake cannot be configured in this case either. If hardware handshake is configured, some lines are not available for manipulation and this call returns FALSE for them. If lines are available and no hardware handshake is configured, the call returns TRUE.

## FbSerialInterface_internal.Open (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Open | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |

| Result Codes |
| 0 | Success |
| EBUSY | The FB is busy with another client. |
| EALREADY | The com-port is already open. |
| EACCES | There was a problem while opening the system com-port. |
| ENOPROTOOPT | The requested option or physical layer (RS-xyz) is not available. |

Attaches an application FB to a serial port at runtime.

The device is opened with the settings which are previously set by Configure(). The device performs the following actions on this call:

Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method, in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.

This method returns the following result codes:

Interface variables Attaches an application FB to a serial port at runtime. The device is opened with the settings which are previously set by Configure(). The device performs the following actions on this call: - It configures the hardware with the settings which are previously sent with Configure(). - It switches on the receiver in order to accept data from the line. Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method, in this implementation it will complete its job immediately and it will not return EWOULDBLOCK. This method returns the following result codes:

## FbSerialInterface_internal.Read (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Read | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |
| pRxBuffer | POINTER TO BYTE | Location of the receive buffer |
| udiRxBufferSize | UDINT | Size of the receive buffer |
| Output | udiRxNBytes | UDINT | Number of transferred bytes |

| Result Codes |
| 0 | Success |
| EBUSY | The FB is busy with another client. |
| EINVAL | Invalid arguments for buffer size or location (programming error) |
| EBADMSG | Integrity of data is severed (Parity-Error or Frame-Error). |
| EACCES | There was a problem while reading from the system com_port. |
| EBADF | The com-port was not open. |

Reads data from the serial port.

This method stores incoming data at the location which is given by pDest (‘receive buffer’). The input ‘udiRxBufferSize’ denote the size of the receive buffer, i.e. the maximum number of bytes which are allowed to be processed.

If more bytes than this number have come in through the serial line, the excessive bytes will remain in the internal system buffer and will be transferred with one of the following read() calls.

The output ‘udiRxNBytes’ represents the number of bytes which are actually transferred. When read() is called periodically, the typical situation is that ‘udiRxNBytes’ is less than ‘udiRxBufferSize’ or even zero.

When exactly the amount of requested data is read, ‘udiRxNBytes’ denotes exactly that size, but there is no hint has to whether more data could be expected with a consecutive read or not.

Interface variables Reads data from the serial port. This method stores incoming data at the location which is given by pDest (‘receive buffer’). The input ‘udiRxBufferSize’ denote the size of the receive buffer, i.e. the maximum number of bytes which are allowed to be processed. If more bytes than this number have come in through the serial line, the excessive bytes will remain in the internal system buffer and will be transferred with one of the following read() calls. The output ‘udiRxNBytes’ represents the number of bytes which are actually transferred. When read() is called periodically, the typical situation is that ‘udiRxNBytes’ is less than ‘udiRxBufferSize’ or even zero. When exactly the amount of requested data is read, ‘udiRxNBytes’ denotes exactly that size, but there is no hint has to whether more data could be expected with a consecutive read or not.

## FbSerialInterface_internal.RegisterSniffer (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | RegisterSniffer | BOOL |
| Input | IComSniffer | WagoTypesCom.I_ComSniffer |

## FbSerialInterface_internal.ReleaseExclusivity (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ReleaseExclusivity | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | Address of the instance |

| result codes |
| 0 | Success, the device has been detached. |
| EBUSY | Use has not been granted to this FB. It is in use by another FB. |
| EINVAL | Null instance is passed. (Null denotes a detached device) |

Releases the device from exclusive usage.

This method is intended to release the exclusivity which has been assigned with AttachExclusively() .

Note (1): “RequestorID” corresponds to the address of the instance which releases its exclusivity.

Interface variables Releases the device from exclusive usage. This method is intended to release the exclusivity which has been assigned with AttachExclusively() . Note (1): “RequestorID” corresponds to the address of the instance which releases its exclusivity.

## FbSerialInterface_internal.SetLineState (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SetLineState | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |
| eLineID | eTTYLineID | Line whose state is to be set. |
| xState | BOOL | TRUE = active, FALSE = inactive |

| Result Codes |
| 0 | Success |
| ENOSYS | The functionality is not supported. |
| EBUSY | The FB is busy with another client. |
| EINVAL | Invalid line ID for output |
| EPROTONOSUPPORT | Device is configured for RS485 protocol. |
| EBADF | Bad handle to serial port |
| EACCES | Could not set the line. |

Allows control of the hardware lines by the application

Normally, these lines are controlled by hardware handshake internally. Nevertheless, when no hardware handshake is involved, the serial lines might be used for very individual purposes.

In the latter case, these hardware wires can be manipulated directly with this functions to desired levels, according to the need of the actual application. This allows the implementation of some exotic handshake schemes which were not foreseen at the time of the creation of this library.

Interface variables Allows control of the hardware lines by the application Normally, these lines are controlled by hardware handshake internally. Nevertheless, when no hardware handshake is involved, the serial lines might be used for very individual purposes. In the latter case, these hardware wires can be manipulated directly with this functions to desired levels, according to the need of the actual application. This allows the implementation of some exotic handshake schemes which were not foreseen at the time of the creation of this library.

## FbSerialInterface_internal.TestExclusivity (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | TestExclusivity | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | Address of the instance |

| result codes |
| 0 | Success, the device is free and may be attached exclusively. |
| EUNATCH | The device is not attached. |
| EBUSY | Exclusive use can not be granted. The device is already attached to another FB. |

Check if exclusive usage has been granted.

This method tests if an FB has been granted exclusive use of the device, but without trying to attach it.

Note (1): “RequestorID” corresponds to the address of the instance which wants to use the device exclusively.

Interface variables Check if exclusive usage has been granted. This method tests if an FB has been granted exclusive use of the device, but without trying to attach it. Note (1): “RequestorID” corresponds to the address of the instance which wants to use the device exclusively.

## FbSerialInterface_internal.UnregisterSniffer (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | UnregisterSniffer | BOOL |
| Input | IComSniffer | WagoTypesCom.I_ComSniffer |

## FbSerialInterface_internal.Write (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Write | eResultCode |  |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |
| pTxBuffer | POINTER TO BYTE | Location of write data |
| udiTxNBytes | UDINT | Number of bytes to be written. |
| Output | udiTxNBytesTransferred | UDINT | Number of transferred bytes |

| Result Codes |
| 0 | Success |
| EBUSY | The FB is busy with another client. |
| EINVAL | Invalid arguments for buffer size or location (programming error) |
| EACCES | There was a problem while opening the system com_port. |
| EBADF | The com-port was not open. |
| EWOULDBLOCK | Not all data could be sent at once. |

Writes data to the serial port.

The inputs ‘pTxBuffer’ and ‘udiTxNBytes’ denote the location and the size of the data to be sent. Note: it is formally ok, to pass 0 bytes for write. In that case, simply nothing happens.

Via ‘udiTxNBytesTransferred’ a feedback is given, how many bytes are actually transferred to the system layer. If this is less than the requested amount, write() returns with EWOULDBLOCK. This is not an error, but a regular state: The remaining bytes should be re-sent later with consecutive write() calls until all bytes are successfully sent.

Interface variables Writes data to the serial port. The inputs ‘pTxBuffer’ and ‘udiTxNBytes’ denote the location and the size of the data to be sent. Note: it is formally ok, to pass 0 bytes for write. In that case, simply nothing happens. Via ‘udiTxNBytesTransferred’ a feedback is given, how many bytes are actually transferred to the system layer. If this is less than the requested amount, write() returns with EWOULDBLOCK. This is not an error, but a regular state: The remaining bytes should be re-sent later with consecutive write() calls until all bytes are successfully sent.

### Program Organization


## 20 Program Organization Units


- FbSerialInterface_internal (FB) 10 I_WagoSysComBase 10 Main Interface FbSerialInterface_internal.ClearBuffers (METH) - FbSerialInterface_internal.Close (METH) - FbSerialInterface_internal.Configure (METH) - FbSerialInterface_internal.DeferredResult (PROP) - FbSerialInterface_internal.IsTransmitterEmpty (PROP) - FbSerialInterface_internal.Open (METH) - FbSerialInterface_internal.Read (METH) - FbSerialInterface_internal.Write (METH) - FbSerialInterface_internal.isOpen (PROP) 20 Hardware Lines - FbSerialInterface_internal.GetLineState (METH) - FbSerialInterface_internal.IsLineAvailable (METH) - FbSerialInterface_internal.SetLineState (METH) 30 Exclusive Use - FbSerialInterface_internal.AttachExclusively (METH) - FbSerialInterface_internal.ForceDetachment (METH) - FbSerialInterface_internal.ReleaseExclusivity (METH) - FbSerialInterface_internal.TestExclusivity (METH) 40 Administration - FbSerialInterface_internal.Cyclic (METH) - FbSerialInterface_internal.Finish (METH) - FbSerialInterface_internal.GetErrorObject (METH) - FbSerialInterface_internal.Initialize (METH) - FbSerialInterface_internal.Name (PROP) 20 I_SupportComSniffer - FbSerialInterface_internal.RegisterSniffer (METH) - FbSerialInterface_internal.UnregisterSniffer (METH)

### Base Components


## 10 I_WagoSysComBase


- 10 Main Interface FbSerialInterface_internal.ClearBuffers (METH) - FbSerialInterface_internal.Close (METH) - FbSerialInterface_internal.Configure (METH) - FbSerialInterface_internal.DeferredResult (PROP) - FbSerialInterface_internal.IsTransmitterEmpty (PROP) - FbSerialInterface_internal.Open (METH) - FbSerialInterface_internal.Read (METH) - FbSerialInterface_internal.Write (METH) - FbSerialInterface_internal.isOpen (PROP) 20 Hardware Lines - FbSerialInterface_internal.GetLineState (METH) - FbSerialInterface_internal.IsLineAvailable (METH) - FbSerialInterface_internal.SetLineState (METH) 30 Exclusive Use - FbSerialInterface_internal.AttachExclusively (METH) - FbSerialInterface_internal.ForceDetachment (METH) - FbSerialInterface_internal.ReleaseExclusivity (METH) - FbSerialInterface_internal.TestExclusivity (METH) 40 Administration - FbSerialInterface_internal.Cyclic (METH) - FbSerialInterface_internal.Finish (METH) - FbSerialInterface_internal.GetErrorObject (METH) - FbSerialInterface_internal.Initialize (METH) - FbSerialInterface_internal.Name (PROP)

### Main Interfaces


## 10 Main Interface


This section contains the most prominent and most frequently used parts of the interface.

This section contains the most prominent and most frequently used parts of the interface. - FbSerialInterface_internal.ClearBuffers (METH) - FbSerialInterface_internal.Close (METH) - FbSerialInterface_internal.Configure (METH) - FbSerialInterface_internal.DeferredResult (PROP) - FbSerialInterface_internal.IsTransmitterEmpty (PROP) - FbSerialInterface_internal.Open (METH) - FbSerialInterface_internal.Read (METH) - FbSerialInterface_internal.Write (METH) - FbSerialInterface_internal.isOpen (PROP)

### Internal Components


## FbSerialInterface_internal.DeferredResult (PROP)


| result codes |
| 0 | Ok: the channel is operative. |
| EAGAIN | Open() is pending, no feedback so far. (no error) |
| ENOPROTOOPT | Configuration options not available for this device. (e.g. hardware handshake, error) |
| EBADF | The FB is not open. (error) |
| EINVAL | Invalid parameters. (error) |
| EACCESS | Other Problems while accessing the serial port. (error) |

Status of the channel after deferred method

This property contains a getter to obtain the actual state of a channel: ready or not after potentially deferred methods: Open(), Close(), or Clearbuffers().

Note: As this implementation of ‘I_WagoSysComBase’ does not defer these calls, this getter always returns the direct results which were delivered by those methods and should never return EAGAIN.

Status of the channel after deferred method This property contains a getter to obtain the actual state of a channel: ready or not after potentially deferred methods: Open(), Close(), or Clearbuffers(). Note: As this implementation of ‘I_WagoSysComBase’ does not defer these calls, this getter always returns the direct results which were delivered by those methods and should never return EAGAIN.

## FbSerialInterface_internal.IsTransmitterEmpty (PROP)


| result codes |
| 0 | Transmitter is empty and has no more bytes to send. |
| EINPROGRESS | Transmitter still has bytes to send. |
| ENOSYS | This operation is not supported by the device. |
| EACCES | Internal error while determining the tx state. |

Determines if the transmitter still has bytes to send.

Three different reactions are possible:

If the transmitter is empty, this property delivers 0=OK, if it has bytes to send, it delivers EINPROGRESS. If the device cannot tell anything about its status, it delivers ENOSYS.

Note: In particular cases it may be technically impossible for a device to determine, whether the transmitter still has data to send or not.

Determines if the transmitter still has bytes to send. Three different reactions are possible: If the transmitter is empty, this property delivers 0=OK, if it has bytes to send, it delivers EINPROGRESS. If the device cannot tell anything about its status, it delivers ENOSYS. Note: In particular cases it may be technically impossible for a device to determine, whether the transmitter still has data to send or not.

## FbSerialInterface_internal.Name (PROP)


Returns the name of the connected interface.

In this implementation strings as ‘COM1’..’COM4’ are returned.

Returns the name of the connected interface. In this implementation strings as ‘COM1’..’COM4’ are returned.

## FbSerialInterface_internal.isOpen (PROP)


Tells if the FB is ready for operation.

This property merely contains a getter function to obtain the actual state of a channel connected to an interface: ready for operation or not.

Tells if the FB is ready for operation. This property merely contains a getter function to obtain the actual state of a channel connected to an interface: ready for operation or not.

## WagoSysCom_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysCom_Internal_PFC |
| Version: | 1.0.2.7 |
| Categories: | WAGO Internal\|Target\|PFC; WAGO Internal\|Feature\|Common\|Com |
| Namespace: | WagoSysCom_Internal |
| Author: | WAGO / u013972 |

### Description


This document is automatically generated.

Target specific library for the onboard serial interface (COM1 on PFC)

This document is automatically generated. Target specific library for the onboard serial interface (COM1 on PFC)

### Contents:


- 10 Documentation doc10_general (FB) 20 Program Organization Units - FbSerialInterface_internal (FB) ParameterList (PARAMS) VersionHistory (GVL)

### Indices and tables


Based on WagoSysCom_Internal_PFC.library, last modified 29.05.2024, 19:51:57. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysCom_Internal_PFC.library, last modified 29.05.2024, 19:51:57. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 20.03.2023 | 1.0.2.7 | u013972 | Resolve types by namespace |
| 23.10.2023 | 1.0.2.6 | u010663 | 64-Bit adjustment ->SysTypes2Interfaces |
| 22.06.2023 | 1.0.2.5 | u013972 | Revert publishing symbols of underlying libraries |
| 07.12.2020 | 1.0.2.4 | u010545 | I_ComSniffer modified |
| 24.11.2020 | 1.0.2.3 | u010545 | I_ComSniffer added |
| 08.01.2019 | 1.0.2.2 | u015842 | Properties: copyright added |
| 29.09.2015 | 1.0.1.0 | u013972 | Resolve libraries with placeholder |
| 10.09.2015 | 1.0.0.3 | u013972 | Workaround C0351-Bug |
| 10.09.2015 | 1.0.0.2 | u013972 | Rename Variables in methods Read and Write |
| 26.08.2015 | 1.0.0.2 | u013972 | COM-Numbers more flexible via Parameter List |
| 09.03.2015 | 1.0.0.0 | RE | Release Version |

WagoSysCom_Internal_PFC.library

WagoSysCom_Internal_PFC.library

### Other Components


## 20 Hardware Lines


This section contains methods for direct usage of hardware lines of the physical interface.

This section contains methods for direct usage of hardware lines of the physical interface. - FbSerialInterface_internal.GetLineState (METH) - FbSerialInterface_internal.IsLineAvailable (METH) - FbSerialInterface_internal.SetLineState (METH)

## 20 I_SupportComSniffer


- FbSerialInterface_internal.RegisterSniffer (METH) - FbSerialInterface_internal.UnregisterSniffer (METH)

## 30 Exclusive Use


Here we have methods for ensuring that a FbSerialInterface instance is operated from only one application FB exclusively.

Here we have methods for ensuring that a FbSerialInterface instance is operated from only one application FB exclusively. - FbSerialInterface_internal.AttachExclusively (METH) - FbSerialInterface_internal.ForceDetachment (METH) - FbSerialInterface_internal.ReleaseExclusivity (METH) - FbSerialInterface_internal.TestExclusivity (METH)

## 40 Administration


This section contains administrative functionalities, such as initialization, cyclic operation, etc.

This section contains administrative functionalities, such as initialization, cyclic operation, etc. - FbSerialInterface_internal.Cyclic (METH) - FbSerialInterface_internal.Finish (METH) - FbSerialInterface_internal.GetErrorObject (METH) - FbSerialInterface_internal.Initialize (METH) - FbSerialInterface_internal.Name (PROP)

## ParameterList (PARAMS)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | cudiMaxComNumber | UDINT | 32767 | Highest ordinal number for OS-serial interfaces. (Must be less than 32768) |