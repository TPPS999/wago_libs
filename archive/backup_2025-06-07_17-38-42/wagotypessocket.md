# WagoTypesSocket v1.5.3.1

## Overview
WAGO PLC library providing WagoTypesSocket functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbSocketServer_MethodsForApplication
This is a set of Methods and variables, which are intended to be used by FbSocketServerApplicationBase. Server classes could uses these methods from parent class.

**Description:**
These functions do directly call corresponding functionalities in the FbSocketServer, which the derived application server is attached to. In that derived FB, however, one does not want to have to deal with pointers to embedding classes, so this job is done at this place without the user having to do anything.

**Methods:**

#### protSetResponseHeader
This information may be ignored for certain RAW protocol implementations. It will certainly be ignored for TCP and UDP.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for new communication. ENOSYS header data will be ignored for current protocol type ============= ====================================================================================== |

#### protGetConnectionClientPort
(May not be implemented for all protocols, returns zero if information is not available.)

#### protGetConnectionAddr
(May not be implemented for all protocols, returns empty string if information is not available.)

#### protGetConnectionProtocol
This asks the frame Server FB about the protocol type of the server.

#### protGetOpState
Note: regularly, most 'notify...()'-methods were either called only for attached and connected server instances or they signalize themself a disabled connection state so this state query is redundant for these cases. But when derived instances are extended not only to react on notifications but also to external stimuli, it is convenient to have this status without the need to carefully trace the notifications.

#### protAttachWriteBuffer
With this call, the serving FB may tell the framework about internal buffers on the serving FB side for write data. This may accelerate the transfer if lots of small write() calls are expected. The server framework will collect this data in that buffer until it is finally sent. Note: Although this space is provided from the application FB, the application must not make any assumptions about the internal structure of this space. This data space is used in a proprietary way by the framework.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for communication. EINVAL Invalid parameters (size beyond plausibility). EFBIG New buffer is too small for data which is already contained in the previous buffer. ============= ====================================================================================== |

#### protWrite
Attn: The Data in the databuffer must not be altered until we have the acknowledge that it has finally been sent.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for new communication. EBADF socket is not open (This schould be a programming error.) EINPROGRESS success, data are pending to be written EBUSY Actual data is ignored because there is previous data to be written. EMSGSIZE data chunk is too large (esp.: size limit for UDP) EPIPE the stream was closed on serverside EACCES other problem while writing data ============= ====================================================================================== |

#### protActiveClose
#### protSendStandardKeepAlive
#### protGetWriteCapacity
If the frame server responds 0, no data can be buffered, so that the memory space which is passed with the write()-call will be logically locked until the data is finally processed. If it reports -1, then previously passed data space is still occupied.

### FbSocketServer_ApplicationBase
This is the base object for establishing a network server.

**Description:**
This is a base class for deriving one's own servers. It must not be used directly, but always as a parent class. One or more instances of that child class may be created and all attached to one server FB (FbTcpServer, see: WagoAppSocket). Each Child represents one possible simultaneous connection. These child objects hold the mere application specific functionality while framework operations, such as opening sockets, receiving packets, etc. are handled by the FbTcpServer. *Context:* That other server FB will notify these instances if a new connection from a new client is accepted or if new data is received for this instance. In these cases the NotifyXYZ() methods were called from the framework. The application is supposed to implement appropriate specific reactions to these events. The applications may use the suite of methods which are declared elsewhere as

**Methods:**

#### QueryReceiveBufferLocation
This method queries the internal buffer location of the child server.

By this method the framework asks the implementation about the location of its receive buffer. If the implementation does not provide a receive buffer, 0 is to be returned. This information allows the framework to directly pass data to the serving FB instead of performing multiple copy operations.

#### NotifyDetachment
This method notifies about detachment from a server framework.

This is called when the application base is detached from the server framework. (This normally happens only during the destruction of the framework and not in regular operation.) This method is supposed to respond with standardized result codes.

#### NotifyService
This method provides a periodic call

This method will be called periodically from the framework in each cycle. Any procedure which is not driven by events but which needs cyclic processing should be placed here. This method is supposed to respond with standardized result codes.

#### QueryReadyForReceiveData
This method queries the maximum size of the data to be received.

Tells the framework if the FB is ready to receive data and how many bytes it can accept in one chunk. This method must be implemented by the application, as otherwise the application will not get any data. While the application is occupied with other business, it should return '0'.

#### NotifyAttachment
This method notifies about attachment to a server framework.

This method informs the application that it has been attached to the server framework. It may be used to cause initialization of the application FB. This method is supposed to respond with standardized result codes.

**Result Codes:**
| Code | Description |
|------|-------------|
| OK | (=0) General acknowledge other Reserved for future specification ============= ====================================================================================== |

#### NotifyClose
This method notifies about closure of a connection.

This method notifies the application that the client or the framework has closed the connection. It is supposed to return '0'. No other result codes are specified yet.

#### NotifyReceivedData
This method notifies that new data was received.

This method passes received data to the application. When receiving RAW data or UDP data, the header information is also passed to the application, if available. Note: although the length of the IP-header is implicitly contained in the header itself, the difference between data and header pointer gives another hint about the size of the header. For TCP connections, a NULL-Pointer is delivered here. Note (2): Before passing data, the frame will already have asked the application with QueryReadyForReceiveData() about its ability to accept data, so the application is strongly expected to be able to handle the passed data. If it cannot, the data will be lost. Note(3): The server application may also be notified that no bytes were received - this is a general standard for notifying the server that the client is still alive. This method is supposed to respond with standardized result codes.

#### NotifyNewConnection
This method notifies that a new connection was accepted.

This method is called from the framework when a new connection is accepted by this host. This method is supposed to respond with standardized result codes.

## Data Types

### eSocketProtocol
Enumeration type.

This enumeration denotes different protocols which can be used on a socket FB.

### eSocketOpState
Enumeration type.

``eSocketOpState`` represents the operation state of a socket FB.

This state is intended to be presented publicly to the user of the FB as well as to be used for internal purposes. The States have the following meaning:

### typKeepAliveParameter
Structure type.

This structure holds parameters for the Keep-Alive ('KA') functionality.

This structure contains the parameters which are used for the

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbSocketServer_MethodsForApplication: FbSocketServer_MethodsForApplication;
END_VAR

// Basic function block usage
fbFbSocketServer_MethodsForApplication(
    // Configure inputs as needed
);

// Check status
IF fbFbSocketServer_MethodsForApplication.xValid THEN
    // Operation successful
END_IF

IF fbFbSocketServer_MethodsForApplication.xError THEN
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

