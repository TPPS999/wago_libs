# WagoSysBSDSocket v1.1.2.3

## Overview
WAGO PLC library providing WagoSysBSDSocket functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Data Types

### eSock_FcntlArg
Enumeration type.

Argument of :ref:`FuSock_Fcntl` *Deviation from POSIX.1-2008:* - For the sake of simple application code this argument structure does not reflect the variable argument list as required by POSIX. Other options than ``O_NONBLOCK`` are not envisaged for this implementation.

### eSock_TcpOptionName
Enumeration type.

### eSock_ShutdownType
Enumeration type.

``eSockShutdownType`` specifies how the shutdown of a socket is performed. It serves as input type of :ref:`FuSock_Shutdown`.

### eSock_FlagsTx
Enumeration type.

Flags for data transmission for use in :ref:`FuSock_Send` and :ref:`FuSock_Sendto`. *Deviation from POSIX.1-2008:* - ``MSG_NOSIGNAL`` is neglected, because no signal handling takes place in codesys. (``MSG_NOSIGNAL`` : Requests not to send the SIGPIPE signal if an attempt to send is made on a stream-oriented socket that is no longer connected. The ``EPIPE`` error is still be returned.) - MSG_EOR is not supported by codesys;

### eSock_FlagsRx
Enumeration type.

Flags for receiving data for use in :ref:`FuSock_Recv` and :ref:`FuSock_Recvfrom`. *Deviation from POSIX:* - MSG_WAITALL is not supported by codesys

### eSock_OptionName
Enumeration type.

Option definitions for use in :ref:`FuSock_Setsockopt` and :ref:`FuSock_Getsockopt`.

Sizes and semantics of the values which are corresponding to the options are quite different for each option and may even vary between implementations: SO_ACCEPTCONN: Non-zero indicates that socket listening is enabled (FuSock_Getsockopt() only, length

### eSock_Level
Enumeration type.

Level definitions for use in :ref:`FuSock_Setsockopt` and :ref:`FuSock_Getsockopt` .. note:: IPPROTO_IPV6 is not supported in some versions of Codesys.

### eSock_FcntlCmd
Enumeration type.

This enumeration summarizes the available commands for :ref:`FuSock_Fcntl`. (Only ``F_SETFL`` available)

### eSock_Protocol
Enumeration type.

This enumeration holds the valid values for the third argument of :ref:`FuSock_Socket`.

### eSock_Type
Enumeration type.

``eSock_Type`` specifies if a socket is UDP, TCP, RAW, for use in :ref:`FuSock_Socket()`.

- SOCK_STREAM: Provides sequenced, reliable, two-way, connection- based byte streams. An out-of-band data transmission mechanism may be supported. - SOCK_DGRAM: Supports datagrams (connectionless, unreliable messages of a fixed maximum length). - SOCK_SEQPACKET: Provides a sequenced, reliable, two-way connection- based data transmission path for datagrams of fixed maximum length; a consumer is required to read an entire packet with each input system call. - SOCK_RAW: Provides raw network protocol access. (Extension to POSIX) - SOCK_RDM: Provides a reliable datagram layer that does not guarantee ordering. (Extension to POSIX) .. note:: SOCK_RAW and SOCK_RDM are not mentioned in POSIX but obviously needed.

## Usage Examples

```iec
// Basic usage example
// Refer to function block documentation for specific usage
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

