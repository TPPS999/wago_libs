# WagoAppCom v1.7.1.2

## Overview
WAGO PLC library providing WagoAppCom functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbDataExchangeMode
This FB supports the data exchange mode for modules 652 and 1652

### FbSerialinterface_WithStatusOutputs
This is a convenience wrapper for :ref:`FbSerialInterface` which does not require to use properties but instead delivers the complete status via output variables.

**Description:**
This FB is intended to be a substitute for :ref:`FbSerialInterface` in graphical languages, where conditional use of properties might turn out to be not too feasible. Thus, the main properties are mapped to additional output variables here. When using textual languages, however, the advantage of this FB over its parent is only marginal. In these cases we recommend using :ref:`FbSerialInterface` instead because the interface of the base class is simpler.

**Methods:**

#### ResetErrors
This clears all error indicators.

This method *ResetErrors()* clears the accumulated error conditions. After doing so the property *ErrorCondition* yields 'OK' until further error conditions newly arise.

#### Write
This writes data to the serial port.

Before sending data, the application SHOULD check if the FB is ready to accept the data. This is done by evaluating 'nReadyForWrite'. Note, that it is a regular prodcedure to write more data than indicated by nReadyForWrite. In that case the location of the data will be used as temporary buffer and MUST NOT be altered until the transmission is completed. There is virtually no sensible limit ( < 2 Gigabyte) for the amout of data which could be passed in this manner. If 'nReadyForWrite' yields a negative number, however, the FB is strictly not ready to accept further transmission data at all. This condition will be lifted again when all pending data is finally transmitted. Note(1): Asynchronous waiting would be pointless here, because in that case the application would have to poll for the termination of the asynchronous job. This is functionally equivalent to polling nReadyForWrite, which is much more efficient. Note(2): When passing more data than indicated by 'nReadyForWrite', the serial FB just buffers the *pointer* to the data but not the data itself. This mechanism allows for a nearly unlimited amount of transmit data to be buffered. This situation is indicated by *nReadyForWrite

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EBADF The FB is not open EINVAL Invalid parameters. EWOULDBLOCK FB is busy with previous data and would block ENOTCONN The FB represents a removable device which has been disconnected during operation ============= ====================================================================================== Note(4): For determining if the data chunk has been sent, the properties *IsTransmitterEmpty* or *nBytesInTxBuffer* may be used. |

#### Read
This reads data from the serial port.

The input 'udiRxBufferSize' denotes the maximum number of expected bytes. This is typically the size of a buffer variable within the application. The read() method will not transfer more data than indicated here. If more data is physically received than is to be read with one call of this function, the remaining data bytes stay in the internal buffer until the next *read()*. The output 'udiRxNBytes' indicates the number of actually transferred data. This might be less than the maximum number (which is a regular situation). If no data is received at all this method returns ENODATA. Note: Asynchronous waiting until a number of bytes is finally received would be pointless here, because in that case the application would have to poll for the termination of the asynchronous job in that case. This is functionally equivalent to polling nReceiveDataArrived - which is much more efficient. If a framing error or a parity error is detected, this condition will be signalled by EBADMSG. Nevertheless, the potentially corrupted data is transferred without any change.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EBADF The FB is not open EINVAL Invalid parameters. ENOTCONN The FB represents a removable device which has been disconnected during operation ENODATA No new data has arrived yet (regular condition) or data is ignored EBADMSG Data integrity is severed (Framing Error or Parity Error) ============= =================================================================================== |

#### Close
This closes the connection and detaches the FB.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The FB was not open ENOTTY The serial Interface was attached exclusively to a different FB EWOULDBLOCK Potentially successful operation, but final result needs some more cycles ============= ====================================================================================== |

#### OpenAndConfigure
This attaches an FB to a serial port at runtime.

When a baudrate of '0' is passed to the FB, an apropriate default baudrate is taken, which is dependant on the specific hardware. Note (1): Normally, the FB is opened at the very beginning of the program and typically does not change its configuration afterwards. By applying OpenAndConfigure() consecutively, however, the settings of *the same* interface may be changed without closing it. Note(2): When setting up the number of stop-bits, unusual situations might occur, such as 1.5 stop bits, which is often seen with 5-bit-frames. These settings are not valid for each configuration. Details depend on the specific hardware. Note(3): For a variety of serial interfaces (

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. ENOTTY The addressed SI does not exist or is already attached to another FB ENOTCONN The addressed SI is a removable device which is not connected right now. ENOPROTOOPT Configuration options not available for this device (e.g. hardware handshake) EINVAL Invalid parameters EBUSY Double open() with different device names (close previous device first) EAGAIN The device is busy with other blocking operation, e.g. clearBuffers() EWOULDBLOCK Potentially successful operation, but final result needs some more cycles. ============= ====================================================================================== |

### FbSerialInterface_Write_mod
This writes data bytes to a serial interface.

**Description:**
This Fb implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModelWagoExecute>` for the process of writing a number of bytes to a serial interface.

**Status Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EBADF The FB is not open EINVAL Invalid parameters. ============= ====================================================================================== |

### FbSerialInterface_Read_mod
This reads data bytes from a serial interface.

**Description:**
This Fb implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModelWagoExecute>` for the process of reading a number of bytes from a serial interface.

### FbSerialInterface_Open_mod
This opens a serial connection.

**Description:**
This Fb implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModelWagoExecute>` for the process of opening a serial channel. For operation, an instance of :ref:`FbSerialInterface` has to be declared and assigned to the in-out variable 'Connection'. When using the corresponding FBs 'Close_mod(FB)', 'Read_mod(FB)', or 'Write_mod(FB)', all these Fbs MUST be connected to the same instance of FbSerialInterface (which may be regarded as a kind of 'handle' for these FBs).

### FbSerialInterface_Close_mod
This closes a serial connection.

**Description:**
This Fb implements the behaviour model :ref:`'WagoExecute' <FbBehaviourModelWagoExecute>` for closing a serial channel.

### FbSerialInterface
This is the fundamental FB of this library.

**Description:**
Each open FB represents a physical serial interface ('SI'). Multiple FBs may share one physical serial interface, but in that case they must not be open simultaneously, i.e. if the SI is opened by one application, it cannot be opened once more until the first open() has been close()d again. In normal operation, the serial interfaces do not have to be closed again, as they will be used throughout the runtime of the machine. When encountering situations such as online-change, however, the used interfaces have to be closed() and re-opened again, as otherwise OS resources might stay blocked.

**Methods:**

#### ResetErrors
This clears all error indicators.

This method *ResetErrors()* clears the accumulated error conditions. After doing so the property *ErrorCondition* yields 'OK' until further error conditions newly arise.

#### Read
This reads data from the serial port.

The input 'udiRxBufferSize' denotes the maximum number of expected bytes. This is typically the size of a buffer variable within the application. The read() method will not transfer more data than indicated here. If more data is physically received than is to be read with one call of this function, the remaining data bytes stay in the internal buffer until the next *read()*. The output 'udiRxNBytes' indicates the number of actually transferred data. This might be less than the maximum number (which is a regular situation). If no data is received at all this method returns ENODATA. Note: Asynchronous waiting until a number of bytes is finally received would be pointless here, because in that case the application would have to poll for the termination of the asynchronous job in that case. This is functionally equivalent to polling nReceiveDataArrived - which is much more efficient. If a framing error or a parity error is detected, this condition will be signalled by EBADMSG. Nevertheless, the potentially corrupted data is transferred without any change.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EBADF The FB is not open EINVAL Invalid parameters. ENOTCONN The FB represents a removable device which has been disconnected during operation ENODATA No new data has arrived yet (regular condition) or data is ignored EBADMSG Data integrity is severed (Framing Error or Parity Error) ============= =================================================================================== |

#### AttachWriteBuffer
This attaches an external Buffer to the FB.

This method can be applied at any time, even when the FB is not attached to a serial interface. By default, each serial FB might have a small built-in buffer which handles most standard situations but is small enough to not waste system memory. In certain situations, when high transmission rate (e.g. 115.2 kBaud) is combined with large cycle times (e.g. 250ms), or when large chunks of write data are generated, it is advisable to have buffers significantly larger than the standard. If applied while in full operation, the previously written data were copied into the new buffer, if that one is big enough. If the new buffer is not big enough, data is lost. If NULL-pointers are appilied together with zero size, the external buffer is detached. Possible Data remaining in that buffer is silently discarded.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EINVAL Invalid parameters (size beyond plausibility). EFBIG New buffer is too small for data which is already contained in the previous buffer. ============= ==================================================================================== |

#### Write
This writes data to the serial port.

Before sending data, the application SHOULD check if the FB is ready to accept the data. This is done by evaluating 'nReadyForWrite'. Note, that it is a regular prodcedure to write more data than indicated by nReadyForWrite. In that case the location of the data will be used as temporary buffer and MUST NOT be altered until the transmission is completed. There is virtually no sensible limit ( < 2 Gigabyte) for the amout of data which could be passed in this manner. If 'nReadyForWrite' yields a negative number, however, the FB is strictly not ready to accept further transmission data at all. This condition will be lifted again when all pending data is finally transmitted. Note(1): Asynchronous waiting would be pointless here, because in that case the application would have to poll for the termination of the asynchronous job. This is functionally equivalent to polling nReadyForWrite, which is much more efficient. Note(2): When passing more data than indicated by 'nReadyForWrite', the serial FB just buffers the *pointer* to the data but not the data itself. This mechanism allows for a nearly unlimited amount of transmit data to be buffered. This situation is indicated by *nReadyForWrite

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EBADF The FB is not open EINVAL Invalid parameters. EWOULDBLOCK FB is busy with previous data and would block ENOTCONN The FB represents a removable device which has been disconnected during operation ============= ====================================================================================== Note(4): For determining if the data chunk has been sent, the properties *IsTransmitterEmpty* or *nBytesInTxBuffer* may be used. |

#### IgnoreIncomingData
This clears RX buffer and ignores further data.

This method instructs the FB to clear the receive Buffer and to ignore all incoming data until regular operation is resumed. (ResumeOperation()) Note: this is intended for fault recovery. Data which is received inbetween is positively lost. The result code yields information whether data has come in during the 'ignore'-phase.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | No inbound data since last call. ENOLINK Since the last call new data was received and positively discarded. EDOTDOT Not detectable if data loss has occurred. ============= ==================================================================== |

#### ClearRxBuffer
This discards all received data up to this point in time.

This is mainly used for recovery from a messed up status in the application.

#### Close
This closes the connection and detaches the FB.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The FB was not open ENOTTY The serial Interface was attached exclusively to a different FB EWOULDBLOCK Potentially successful operation, but final result needs some more cycles ============= ====================================================================================== |

#### IsTransmitterEmpty
This function indicates that all data has been sent.

``TRUE`` is returned if all data has left the scope of the FB and the hardware does not indicate otherwise that there is still data to be sent. ``FALSE`` is returned otherwise. If this function is not supported by the hardware but the result would depend on the hardware, or if any other errors occur which would affect the operation result, then the ``xDefaultValue`` is returned.

#### GetErrorObject
This retrieves the error object from the hardware interface.

If the underlying objects for serial interfaces support error objects, this method delivers these objects to the application. .. note:: The capability of a specific interface ('COM-object') to deliver error objects may be tested by simply calling this method. A result code 0

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, error object is retrieved (either OK or NOK) ENOSYS The COM-interface does not support Error Objects; output is invalid. EBADF No COM-object is attached to this FB EFBIG The COM object implements a different FBErrorFormat ============= ===================================================================== |

#### finish
This tears down the internal structures of FbSerialInterface.

This method is important when own FBs are derived from the base FB. In that case the derived FB should call ``SUPER^.finish()`` during its own finish() method. In other cases (especially when the FB is instantiated directly) this method should not be used. (Treat as if declared PROTECTED, although technically PUBLIC)

#### initialize
This initializes the internal structures of the FbSerialInterface.

This method is important when own FBs are derived from the base FB. In that case the derived FB should call ``SUPER^.initialize()`` during its own initialization. In other cases (especially when the FB is instantiated directly) this method should not be used. (Treat as if declared PROTECTED, although technically PUBLIC)

#### AttachReadBuffer
This attaches external Buffer to the FB.

This method can be applied at any time, even when the FB is not attached to a serial interface. By default, each serial FB has a small built-in buffer which handles most standard situations but is small enough to not waste system memory. In certain situations, when high transmission rate (e.g. 115.2 kBaud) is combined with large cycle times (e.g. 250ms), or when large chunks of write data are generated, it is advisable to have buffers significantly larger than standard. This is provided by this method. If applied while in full operation, the previously received data were copied into the new buffer, if that one is big enough. If the new buffer is not big enough, data is lost. If NULL-pointers are applied together with zero size, the external buffer is detached. Possible Data remaining in that buffer is silently discarded.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EINVAL Invalid parameters (size beyond plausibility). EFBIG New buffer is too small for data which is already contained in the previous buffer. ============= ====================================================================================== |

#### ClearTxBuffer
This discards all data which is scheduled for transmission.

#### IsLineAvailable
This checks if an output line may be directly manipulated.

This method checks if the driver and the protocol supports manipulation of an output line. If no extra hardware lines are available, this call returns FALSE. Note: hardware handhake cannot be configured in this case either. If hardware handhake is configured, some lines are not available for manipulation and this call returns FALSE for them. If lines are available and no hardware handshake is configured, the call returns TRUE.

#### OpenAndConfigure
This attaches an FB to a serial port at runtime.

When a baudrate of '0' is passed to the FB, an apropriate default baudrate is taken, which is dependant on the specific hardware. Note (1): Normally, the FB is opened at the very beginning of the program and typically does not change its configuration afterwards. By applying OpenAndConfigure() consecutively, however, the settings of *the same* interface may be changed without closing it. Note(2): When setting up the number of stop-bits, unusual situations might occur, such as 1.5 stop bits, which is often seen with 5-bit-frames. These settings are not valid for each configuration. Details depend on the specific hardware. Note(3): For a variety of serial interfaces (

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. ENOTTY The addressed SI does not exist or is already attached to another FB ENOTCONN The addressed SI is a removable device which is not connected right now. ENOPROTOOPT Configuration options not available for this device (e.g. hardware handshake) EINVAL Invalid parameters EBUSY Double open() with different device names (close previous device first) EAGAIN The device is busy with other blocking operation, e.g. clearBuffers() EWOULDBLOCK Potentially successful operation, but final result needs some more cycles. ============= ====================================================================================== |

#### SetBusyState
This announces that no more receive data is welcome.

This method tells the handshake mechanism that the FB does not want to receive data and applies the appropriate handshake mechanisms for that case - even if the receive buffer would otherwise be ready to accept more data. This method is intended for the higher level application to try to stop the data flow from the sender when it is clear that the application temporarily cannot handle any more the data. This behaviour is intended to improve latency between sender and recipient. If in spite of this new data arrives during this state, this is not an error and it will be processed regardless of the busy state. But the data is likely to stay in the buffer until the application gets ready for new data again. By applying ResumeOperation() normal Operation will be resumed.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EBADF The FB was not open EUNATCH No protocol (handhake) suitable for busy state is configured. ============= ============================================================= |

#### GetLineState
This retrieves the state of input lines, if available.

This method returns TRUE if the input line is active and FALSE if otherwise. If the hardware does not permit querying of the hardware line, this method always returns TRUE.

#### SetLineState
This sets an output line directly to active or passive state.

Under normal circumstances, output lines are controlled by hardware handshake internally. Nevertheless, when no hardware handshake is involved, the serial lines might be used for individual purposes. In the latter case, these hardware wires can be manipulated directly with this method to desired levels, according to the need of the actual application. This allows to implement also rather exotic handshake schemes.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. ENOSYS This interface does not support control of hardware lines EBADF The FB is not open EPROTONOSUPPORT The configured protocol does not allow for manipulating output lines EACCES Other problem while attempting to manipulate an output line ================ ================================================================================= |

#### ResumeOperation
This turns on the Receiver after interruption.

This method instructs the FB to resume normal operation after having turned the RX off or having entered a busy state. It revokes the effect of IgnoreRxData() and SetBusyState().

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EBADF The FB was not open, so normal operation cannot take place. ENOTCONN The hardware is not connected, so normal operation cannot take place. ============= ====================================================================================== |

## Compact Function Blocks

### FbSerialInterface_cpt
This is a serial communication FB with *cpt*-type interface for use in graphical languages. (For textual languages we recommend :ref:`FbSerialInterface` instead.)

**Description:**
This FB implements the behaviour of the model :ref:`'WagoCommunicator' <FbBehaviourModel_WagoCommunicator>`. The Fb is divided into three submodules: - Channel control - Transmitter (TX) - Receiver (RX)

**Methods:**

#### initialize
This initializes the internal structures of the FbSerialInterface.

This method is important when own FBs are derived from the base FB. In that case the derived FB should call ``SUPER^.initialize()`` during its own initialization. In other cases (especially when the FB is instantiated directly) this method should not be used. (Treat as if declared PROTECTED, although technically PUBLIC)

#### finish
This tears down the internal structures of FbSerialInterface.

This method is important when own FBs are derived from the base FB. In that case the derived FB should call ``SUPER^.finish()`` during its own finish() method. In other cases (especially when the FB is instantiated directly) this method should not be used. (Treat as if declared PROTECTED, although technically PUBLIC)

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbDataExchangeMode: FbDataExchangeMode;
END_VAR

// Basic function block usage
fbFbDataExchangeMode(
    // Configure inputs as needed
);

// Check status
IF fbFbDataExchangeMode.xValid THEN
    // Operation successful
END_IF

IF fbFbDataExchangeMode.xError THEN
    // Handle error
END_IF
```

## Best Practices

### Error Handling
```iec
IF fbInstance.xError THEN
    CASE fbInstance.eStatus OF
        // Handle specific error codes
    END_CASE
END_IF
```

### Performance Considerations
- Use appropriate polling intervals
- Handle communication errors gracefully
- Consider device response times
- Test thoroughly in target environment

## Important Notes

- This documentation was automatically generated from XML specification
- Always refer to official WAGO documentation for complete details
- Test thoroughly in your specific application environment
- Check library compatibility with your PLC hardware

