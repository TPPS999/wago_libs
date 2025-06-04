# WagoSysCom_Internal_PFC Library v1.0.2.7

## Overview
Target-specific internal communication library for handling physical serial interfaces on WAGO PFC controllers.

**Key Features:**
- Implementation of I_WagoSysComBase interface for PFC hardware
- Serial communication interface management
- TSC (Target System Code) integration
- Exclusive device access control
- Hardware line state monitoring and control

**Important Note:** This library provides low-level internal functions that are not intended for direct use by application programs. Instead, use higher-level libraries like WagoAppCom that take references to instances of I_WagoSysComBase as input parameters.

## Core Function Block

### FbSerialInterface_internal
Main function block implementing the I_WagoSysComBase interface for physical serial communication.

**Purpose:**
- Provides interface to physical serial interfaces on PFC controllers
- Implements complete serial communication functionality
- Supports exclusive device access management
- Handles hardware line state control

**Usage Pattern:**
- Each instance represents one physical serial interface
- Multiple application FBs may share one physical interface
- Only one application can open the interface at a time
- Proper close() required before another application can open()

## Methods

### Device Management

#### Initialize()
Initialize FbSerialInterface_internal at FB_Init.
- Initializes member variables and properties to initial state
- Called automatically during FB initialization

#### Open()
Attaches an application FB to a serial port at runtime.

**Behavior:**
- Configures hardware with settings from Configure()
- Switches on receiver to accept data
- Completes immediately (no deferred execution)

**Result Codes:**
- `0` - Success
- `EBUSY` - FB busy with another client
- `EALREADY` - COM port already open
- `EACCES` - Problem opening system COM port
- `ENOPROTOOPT` - Requested option/physical layer not available

#### Close()
Closes connection and detaches FB from serial interface.

**Result Codes:**
- `0` - Success
- `EBUSY` - FB busy with another client
- `EACCES` - Problem closing system COM port
- `EBADF` - COM port was not open

#### Configure()
Configures serial FB before opening.

**Notes:**
- Must be called before Open()
- Settings applied on next Open() call
- Can test settings without opening device
- Completes immediately (no deferred execution)

**Limitations:**
- `eStopbits`: 'None' and 'OneDotFive' not supported

**Result Codes:**
- `0` - Success
- `EBUSY` - FB busy with another client
- `EALREADY` - COM port already open
- `ENOPROTOOPT` - Requested option not available

#### Finish()
Detach and close serial interface before destruction.
- Called before FB_Exit
- No return value

### Data Transfer

#### Read()
Reads data from the serial port.

**Parameters:**
- `pDest` - Receive buffer location
- `udiRxBufferSize` - Maximum bytes to process
- `udiRxNBytes` - Actual bytes transferred (output)

**Behavior:**
- Stores incoming data in receive buffer
- Excess bytes remain in system buffer for next read
- Typical calls return fewer bytes than requested

**Result Codes:**
- `0` - Success
- `EBUSY` - FB busy with another client
- `EINVAL` - Invalid buffer arguments
- `EBADMSG` - Data integrity error (parity/frame error)
- `EACCES` - Problem reading from COM port
- `EBADF` - COM port not open

#### Write()
Writes data to the serial port.

**Parameters:**
- `pTxBuffer` - Data location to send
- `udiTxNBytes` - Number of bytes to send
- `udiTxNBytesTransferred` - Actual bytes transferred (output)

**Behavior:**
- Transfers data to system layer
- May not send all bytes at once
- Remaining bytes should be resent in consecutive calls

**Result Codes:**
- `0` - Success
- `EBUSY` - FB busy with another client
- `EINVAL` - Invalid buffer arguments
- `EACCES` - Problem accessing COM port
- `EBADF` - COM port not open
- `EWOULDBLOCK` - Not all data sent (retry needed)

### Buffer Management

#### ClearBuffers()
Clears all internal receive and send buffers.

**Result Codes:**
- `0` - Success
- `EBUSY` - FB busy with another client
- `EACCES` - Problem accessing COM port
- `EBADF` - COM port not open

### Exclusive Access Control

#### AttachExclusively()
Tries to get exclusive access to the device.

**Parameters:**
- `RequestorID` - Unique identifier (typically FB address)

**Notes:**
- Provides cooperative device usage mechanism
- Does not enforce policy, only tracks usage
- Pass unique number (e.g., FB address) as identifier

**Result Codes:**
- `0` - Success, exclusive use granted
- `EBUSY` - Device already attached to another user
- `EINVAL` - Null instance passed

#### TestExclusivity()
Check if exclusive usage has been granted.

**Parameters:**
- `RequestorID` - Identifier to check

**Result Codes:**
- `0` - Success, device free for exclusive attachment
- `EUNATCH` - Device not attached
- `EBUSY` - Exclusive use cannot be granted

#### ReleaseExclusivity()
Releases device from exclusive usage.

**Parameters:**
- `RequestorID` - Identifier releasing exclusivity

**Result Codes:**
- `0` - Success, device detached
- `EBUSY` - Use not granted to this FB
- `EINVAL` - Null instance passed

#### ForceDetachment()
Forces detachment of the device.

**Purpose:**
- Emergency recovery from crashed client FBs
- Initialization purposes
- Not for regular use

**Result Codes:**
- `0` - Success (operation does not fail)

### Hardware Line Control

#### SetLineState()
Allows direct control of hardware lines.

**Purpose:**
- Control hardware lines when no hardware handshake used
- Implement custom handshake schemes
- Direct line manipulation for special applications

**Result Codes:**
- `0` - Success
- `ENOSYS` - Functionality not supported
- `EBUSY` - FB busy with another client
- `EINVAL` - Invalid line ID
- `EPROTONOSUPPORT` - Device configured for RS485
- `EBADF` - Bad handle to serial port
- `EACCES` - Could not set line

#### GetLineState()
Retrieve the state of hardware lines.

**Returns:**
- `TRUE` - Line shows active level (+3..+15V for RS232)
- `FALSE` - Line shows passive level (-3..-15V for RS232)
- `TRUE` - If level cannot be retrieved

#### IsLineAvailable()
Checks if manipulation of hardware line is possible.

**Behavior:**
- Returns FALSE if no extra hardware lines available
- Returns FALSE if hardware handshake configured
- Returns TRUE if lines available and no handshake configured

### Utility Methods

#### Cyclic()
Cyclic processing of the FB.

**Implementation:**
- Not implemented for this FB
- No deferred operations require cyclic processing

**Result Codes:**
- `ENOSYS` - No cyclic processing necessary

#### GetErrorObject()
Obtains error cause from hardware interface.

**Implementation:**
- Not implemented (COM1 does not produce error objects)
- Returns ENOSYS
- Result buffer remains unchanged

### Sniffer Support

#### RegisterSniffer()
Register communication sniffer interface.

#### UnregisterSniffer()
Unregister communication sniffer interface.

## Properties

### Name
**Type:** STRING (Read-only)
- Returns the name/identifier of the serial interface

### isOpen
**Type:** BOOL (Read-only)
- Returns TRUE if the interface is currently open
- Returns FALSE if the interface is closed

### OSNumber
**Type:** UINT (Read-only)
- Returns the operating system number of the interface

### IsTransmitterEmpty
**Type:** BOOL (Read-only)
- Returns TRUE if the transmitter buffer is empty
- Returns FALSE if data is pending transmission

### DeferredResult
**Type:** Result code (Read-only)
- Returns result of deferred operations
- Not used in this implementation (no deferred operations)

## Usage Examples

### Basic Interface Setup
```iec
VAR
    fbSerial: FbSerialInterface_internal;
    config: typSerialConfig;
    result: WAGO_RESULT;
END_VAR

// Initialize FB
fbSerial.Initialize();

// Configure interface
config.eBaudrate := COM_9600;
config.eParity := COM_EVEN;
config.eStopbits := COM_1_STOPBIT;
config.eDataBits := COM_8_DATABITS;
config.eHandshake := COM_NO_HANDSHAKE;

result := fbSerial.Configure(config);

// Open interface
IF result = 0 THEN
    result := fbSerial.Open();
END_IF
```

### Exclusive Access Pattern
```iec
VAR
    fbSerial: FbSerialInterface_internal;
    requestor_id: DINT;
    result: WAGO_RESULT;
END_VAR

// Use FB address as unique identifier
requestor_id := ADR(fbSerial);

// Test if exclusive access possible
result := fbSerial.TestExclusivity(requestor_id);

IF result = 0 THEN
    // Attach exclusively
    result := fbSerial.AttachExclusively(requestor_id);
    
    IF result = 0 THEN
        // Perform exclusive operations
        // ...
        
        // Release when done
        fbSerial.ReleaseExclusivity(requestor_id);
    END_IF
END_IF
```

### Data Communication
```iec
VAR
    fbSerial: FbSerialInterface_internal;
    tx_buffer: ARRAY[0..255] OF BYTE;
    rx_buffer: ARRAY[0..255] OF BYTE;
    tx_count, rx_count: UDINT;
    result: WAGO_RESULT;
END_VAR

// Write data
tx_count := 10; // bytes to send
result := fbSerial.Write(ADR(tx_buffer), tx_count, tx_count);

IF result = EWOULDBLOCK THEN
    // Not all data sent, retry remaining bytes
END_IF

// Read data
result := fbSerial.Read(ADR(rx_buffer), SIZEOF(rx_buffer), rx_count);

IF result = 0 AND rx_count > 0 THEN
    // Process received data
END_IF
```

### Hardware Line Control
```iec
VAR
    fbSerial: FbSerialInterface_internal;
    line_available: BOOL;
    line_state: BOOL;
    result: WAGO_RESULT;
END_VAR

// Check if RTS line is available
line_available := fbSerial.IsLineAvailable(COM_LINE_RTS);

IF line_available THEN
    // Set RTS line high
    result := fbSerial.SetLineState(COM_LINE_RTS, TRUE);
    
    // Read CTS line state
    line_state := fbSerial.GetLineState(COM_LINE_CTS);
END_IF
```

## Error Handling

### Standard Error Codes
- `0` - Success
- `EBUSY` - Resource busy with another client
- `EALREADY` - Operation already performed
- `EACCES` - Access denied or system error
- `EBADF` - Invalid file descriptor/handle
- `EINVAL` - Invalid parameters
- `ENOSYS` - Function not implemented
- `ENOPROTOOPT` - Protocol option not supported
- `EPROTONOSUPPORT` - Protocol not supported
- `EWOULDBLOCK` - Operation would block, retry needed
- `EBADMSG` - Message integrity error
- `EUNATCH` - Device not attached

### Error Handling Pattern
```iec
result := fbSerial.SomeMethod();

CASE result OF
    0:
        // Success
    EBUSY:
        // Handle busy condition
    EACCES:
        // Handle access error
    EINVAL:
        // Handle invalid parameters
    // ... handle other specific errors
ELSE
    // Handle unexpected errors
END_CASE
```

## Best Practices

### Resource Management
- Always call Close() before FB destruction
- Use exclusive access for critical operations
- Check isOpen property before operations
- Handle EWOULDBLOCK in write operations

### Error Handling
- Check result codes for all method calls
- Implement retry logic for EWOULDBLOCK
- Use appropriate error recovery strategies
- Log errors for debugging purposes

### Performance Considerations
- Configure interface once before opening
- Use appropriate buffer sizes for read/write
- Clear buffers when switching protocols
- Monitor transmitter empty state for timing

### Integration with Higher-Level Libraries
- Use WagoAppCom for application-level functionality
- Pass FB references to higher-level libraries
- Avoid direct usage in applications when possible
- Follow cooperative access patterns

## Important Notes

### Design Philosophy
- Internal library for hardware abstraction
- Not intended for direct application use
- Provides foundation for higher-level libraries
- Implements standard I_WagoSysComBase interface

### Hardware Compatibility
- Specific to WAGO PFC controllers
- Supports standard serial communication protocols
- Limited to available hardware interfaces
- Hardware line control depends on interface type

### Thread Safety
- Implements exclusive access mechanism
- Cooperative rather than enforced exclusivity
- Application must follow access protocols
- Single client per open instance

## Version History

| Date | Version | Author | Change |
|------|---------|--------|--------|
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

## Related Libraries
- **WagoTypesCom_Internal** - Interface definitions and base types
- **WagoTypesCom** - Communication type definitions
- **WagoTypesCommon** - Common type definitions
- **WagoAppCom** - Application-level communication functions
- **WagoSysSerial** - Low-level serial communication interface
