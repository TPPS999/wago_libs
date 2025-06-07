# WagoSysSocket_Internal_PFC v1.0.5.9

## Overview
WAGO PLC library providing WagoSysSocket_Internal_PFC functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbMulticastListener_internal
**Methods:**

#### ConfigureKeepAliveTransmission
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EINVAL Invalid Parameters ENOSYS This Feature is not supported by the target ============= ====================================================================================== |

#### LeaveGroup
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for communication. ENOSYS the function is not supported. EBADF the FB was not open ============= ====================================================================================== |

#### OpenAndJoin
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for communication. EACCES the socket could not be created by other reasons EINVAL invalid argument ENFILE The system limit on the total number of open sockets has been reached. EADDRINUSE The given address / port combination is already in use. EBUSY The socket is already bound to an address. EPROTOTYPE The given protocol type ('eProto') is not supported. (RAW and UDP only , not TCP) EADDRNOTAVAIL A nonexistent interface was requested or the requested address was not local. ============= ====================================================================================== |

#### Close
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success EBADF The socket FB was not open ============= ====================================================================================== |

#### ReJoinGroup
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for communication. ENOSYS the function is not supported. EBADF the FB was not open ============= ====================================================================================== |

### FbSocket_GenericConnection
**Methods:**

#### InitNewConnection
#### ServerClose
#### initialize_only
#### protActiveClose
#### protGetOpState
#### protGetConnectionClientPort
#### protGetConnectionAddr
### Initialize_FbSocket_GenericConnection
### FbDatagramServer_internal
**Methods:**

#### AttachSingleServerApplication
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success EMFILE the number of server application instances exceeds its limit. (with 'M', not 'N') EINVAL Null-Pointer EACCES the initalization of the server application FB responded a failure ============= ====================================================================================== |

#### OpenAndListen
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for communication. EACCES the socket could not be created by other reasons EINVAL invalid argument, e.g. malformed adress ENFILE The system limit on the total number of open sockets has been reached. EADDRINUSE The given address / port combination is already in use. EBUSY The socket is already bound to an address. EADDRNOTAVAIL A nonexistent interface was requested or the requested address was not local. ============= ====================================================================================== |

#### Close
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success EBADF The socket FB was not open EACCES Unexpected problems at closing the linstening socket ============= ====================================================================================== |

#### AttachServerApplication
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success EMFILE the number of server application instances exceeds its limit. (with 'M', not 'N') EINVAL Null-Pointer EACCES the initalization of the server application FB responded a failure ============= ====================================================================================== |

### FbSocket_UdpInstanceSlot
**Methods:**

#### protWrite
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for new communication. EBADF socket is not open (This schould be a programming error.) EBUSY Actual data is ignored because there is previous data to be written. EMSGSIZE data chunk is too large (esp.: size limit for UDP) EPIPE the stream was closed on serverside EACCES other problem while writing data ============= ====================================================================================== |

#### protActiveClose
#### Read
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for new communication. EBADF socket is not open EWOULDBLOCK the requested amount of data could not be read EACCES other problem while receiving data ENODATA No data EPIPE connection closed from server side ============= ====================================================================================== |

#### protGetWritecapacity
#### protAttachWriteBuffer
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for communication. EINVAL Invalid parameters (size beyond plausibility). EFBIG New buffer is too small for data which is already contained in the previous buffer. ============= ====================================================================================== |

### Initialize_FbSocket_UdpInstanceSlot
### FbSocketClient_internal
**Methods:**

#### finish
#### initialize
#### CloseConnection
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success EBADF The socket FB was not open ============= ====================================================================================== |

#### CheckConnection
#### OpenAndConnect
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EACCES Permission to create a socket of the specified type and/or protocol is denied. EINVAL Unknown protocol or malformed address ENFILE The system limit on the total number of open sockets has been reached. EPROTONOSUPPORT The desired protocol is not supported. ECONNREFUSED No-one listening on the remote address. EHOSTUNREACH Target Host is not reachable ENOPROTOOPT Protocol option 'sOwnInterface' not applicable ETIME Timeout while attempting connection. EAGAIN No response from server received yet. (That may take longer time) EIO Unspecific =============== ====================================================================================== Note(1): This FB does not support hopping between different port numbers, as occasionally used by UDP connections. For that purpose, another FB type has to be used. Note (2): We did not specify any optional flags yet. In contrast to lowlevel system calls, we would implement flags as binary inputs rather than packed 32-bits. Note (3) There are many possible causes for ETIME. One is that the server may be too busy to accept new connections. For IP sockets the timeout may be very long when syncookies are enabled on the server. |

#### Block
#### CalmWatchdog
#### Read
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for new communication. EBADF socket is not open EWOULDBLOCK the requested amount of data could not be read EACCES other problem while receiving data ENODATA No data EPIPE connection closed from server side ============= ====================================================================================== |

#### ReadWithHeader
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for new communication. EBADF socket is not open ENOSYS this function is not supported by the hardware EWOULDBLOCK the requested amount of data could not be read EMSGSIZE requested data size is too large (esp.: size limit for UDP) EACCES other problem while receiving data ============= ====================================================================================== |

#### Write
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for new communication. EINPROGRESS success, data are pending to be written EBADF socket is not open EBUSY Actual data is ignored because there is previous data to be written. EMSGSIZE data chunk is too large (esp.: size limit for UDP) EPIPE the stream was closed on server side EACCES other problem while writing data ============= ====================================================================================== |

#### ConfigureKeepAliveTransmission
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EINVAL Invalid Parameters. ENOSYS This Feature is not supported by the target. EWOULDBLOCK No Connection was established. Settings will be applied later. EACCES Other Error from OS layer. ============= ====================================================================================== |

### FbSocket_TcpInstanceSlot
**Methods:**

#### protAttachWriteBuffer
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for communication. EINVAL Invalid parameters (size beyond plausibility). EFBIG New buffer is too small for data which is already contained in the previous buffer. ============= ====================================================================================== |

#### protWrite
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for new communication. EBADF socket is not open (This schould be a programming error.) EBUSY Actual data is ignored because there is previous data to be written. EMSGSIZE data chunk is too large (esp.: size limit for UDP) EPIPE the stream was closed on serverside EACCES other problem while writing data ============= ====================================================================================== |

#### protGetConnectionProtocol
#### protGetWriteCapacity
#### Read
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for new communication. EBADF socket is not open EWOULDBLOCK the requested amount of data could not be read EACCES other problem while receiving data ENODATA No data EPIPE connection closed from server side ============= ====================================================================================== |

### Initialize_FbSocket_TcpInstanceSlot
### FbTcpServer_internal
**Methods:**

#### ConfigureKeepAliveTransmission
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EINVAL Invalid Parameters ENOSYS This Feature is not supported by the target ============= ====================================================================================== |

#### AttachServerApplication
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success EMFILE the number of server application instances exceeds its limit. (with 'M', not 'N') EINVAL Null-Pointer EACCES the initalization of the server application FB responded a failure ============= ====================================================================================== |

#### Close
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success EBADF The socket FB was not open EACCES Unexpected problems at closing the linstening socket ============= ====================================================================================== |

#### OpenAndListen
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for communication. EACCES the socket could not be created by other reasons EINVAL invalid argument ENFILE The system limit on the total number of open sockets has been reached. EADDRINUSE The given address / port combination is already in use. EBUSY The socket is already bound to an address. EADDRNOTAVAIL A nonexistent interface was requested or the requested address was not local. ============= ====================================================================================== |

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbMulticastListener_internal: FbMulticastListener_internal;
END_VAR

// Basic function block usage
fbFbMulticastListener_internal(
    // Configure inputs as needed
);

// Check status
IF fbFbMulticastListener_internal.xValid THEN
    // Operation successful
END_IF

IF fbFbMulticastListener_internal.xError THEN
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

