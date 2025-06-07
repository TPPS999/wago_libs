# WagoSysSocket_Internal_PFC v1.0.5.9 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysSocket_Internal_PFC
- **Version:** 1.0.5.9
- **Categories:** WAGO Internal|Target|PFC; WAGO Internal|Feature|Network|Common; Application; WAGO LayerView|Sys; WAGO Internal|Target
- **Namespace:** WagoSysSocket_internal
- **Author:** WAGO / u013972
- **Placeholder:** WagoSysSocketInternal

### Description ¶


This document is automatically generated.

Handling network communication on internet layer and on transport layer.

This document is automatically generated. Handling network communication on internet layer and on transport layer.

### Contents: ¶


Contents: - Project Information - Library Information - Function Blocks FbDatagramServer_internal (FB) - FbMulticastListener_internal (FB) - FbSocketClient_internal (FB) - FbSocket_GenericConnection (FB) - FbSocket_TcpInstanceSlot (FB) - FbSocket_UdpInstanceSlot (FB) - FbTcpServer_internal (FB) - TcpInstanceWriteBuffer (FB) - UdpInstanceWriteBuffer (FB) Functions - GetIpAddressOfInterface (FUN) - SinglePing (FUN) - _ApplyKeepAliveParameters (FUN) - _TransposeKeepAliveResults (FUN) Methods - FbDatagramServer_internal.AttachServerApplication (METH) - FbDatagramServer_internal.AttachSingleServerApplication (METH) - FbDatagramServer_internal.Close (METH) - FbDatagramServer_internal.CyclicRun (METH) - FbDatagramServer_internal.OpenAndListen (METH) - FbDatagramServer_internal.finish (METH) - FbDatagramServer_internal.initialize (METH) - FbMulticastListener_internal.Close (METH) - FbMulticastListener_internal.ConfigureKeepAliveTransmission (METH) - FbMulticastListener_internal.LeaveGroup (METH) - ... and 55 more Program Organization Function Groups - 21 Auxiliary Functions - Singular Functions Main Interfaces - 10 Main Interface - 10 Main Interface - 10 Main Interface Internal Components - 02_for internal framework - 02_for internal framework - 02_for internal framework - 90 Internal - 90 internal - 90 internal - FbDatagramServer_internal.HasOpenSocket (PROP) - FbSocketClient_internal.OpState (PROP) - FbSocketClient_internal.OwnPort (PROP) - FbTcpServer_internal.HasOpenSocket (PROP) - ... and 1 more Global Variable Lists - LibraryResult (GVL) - ResultItems (GVL) - VersionHistory (GVL) Other Components - 01_from Application - 01_from Application - 01_from Application - 10 Main - 20 Administration - 20 administrative - 20 administrative - 20 advanced - 30 properties - 40 administrative - ... and 4 more

### Indices and tables ¶


Based on WagoSysSocket_Internal_PFC.library, last modified 20.09.2024, 21:05:25. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysSocket_Internal_PFC.library, last modified 20.09.2024, 21:05:25. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysSocket_Internal_PFC.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 20.09.2024, 21:05:25 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 20.09.2024, 21:05:25 |
| Description | string | See: Description |
| Copyright | © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u013972 |
| DefaultNamespace | WagoSysSocket_internal |
| Placeholder | WagoSysSocketInternal |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoSysSocket_Internal_PFC |
| Version | version | 1.0.5.9 |
| Title | string | WagoSysSocket_Internal_PFC |
| LibraryCategories | library-category-list | WAGO Internal\|Target\|PFC; WAGO Internal\|Feature\|Network\|Common; Application; WAGO LayerView\|Sys; WAGO Internal\|Target |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. CmpErrors2 Interfaces Library Identification : Name: CmpErrors2 Interfaces Version: newest Company: System Namespace: CmpErrors Library Properties : SysSocket Library Identification : Placeholder: SysSocket Default Resolution: SysSocket, * (System) Namespace: SysSocket Library Properties : SysTime Library Identification : Placeholder: SysTime Default Resolution: SysTime, * (System) Namespace: SysTime Library Properties : SysTypes2 Interfaces Library Identification : Name: SysTypes2 Interfaces Version: newest Company: System Namespace: SysTypes Library Properties : WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : Library Parameter : Parameter: RES_LOG_MAX_FILESIZE = 2000 Parameter: RES_LOG_MAX_FILES = 1 Parameter: RES_LOG_MAX_ENTRIES = 200 Parameter: RES_LOG_NAME = ‘WagoAppResultLogger’ WagoSysPlainMem Library Identification : Placeholder: WagoSysPlainMem Default Resolution: WagoSysPlainMem, * (WAGO) Namespace: WagoSysPlainMem Library Properties : WagoSysString Library Identification : Placeholder: WagoSysString Default Resolution: WagoSysString, * (WAGO) Namespace: WagoSysString Library Properties : WagoSysTypedefs_Pointer Library Identification : Placeholder: WagoSysTypedefs_Pointer Default Resolution: WagoSysTypedefs_Pointer, * (WAGO) Namespace: WAGOWagoTypesPointer Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoSysVirtualBuffer Library Identification : Placeholder: WagoSysVirtualBuffer Default Resolution: WagoSysVirtualBuffer, * (WAGO) Namespace: WagoSysVirtualBuffer Library Properties : WagoTypesCommon Library Identification : Placeholder: WagoTypesCommon Default Resolution: WagoTypesCommon, * (WAGO) Namespace: WagoTypes Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties : WagoTypesSocket Library Identification : Placeholder: WagoTypesSocket Default Resolution: WagoTypesSocket, * (WAGO) Namespace: WagoTypesSocket Library Properties :

### Function Blocks


## FbDatagramServer_internal (FB)


This FB provides a framework for building Server structures within the application.

This FB provides a framework for building Server structures within the application. - 10 Main Interface FbDatagramServer_internal.AttachServerApplication (METH) - FbDatagramServer_internal.AttachSingleServerApplication (METH) - FbDatagramServer_internal.Close (METH) - FbDatagramServer_internal.OpenAndListen (METH) 20 administrative - FbDatagramServer_internal.finish (METH) - FbDatagramServer_internal.initialize (METH) 90 internal - FbDatagramServer_internal.CyclicRun (METH) - FbDatagramServer_internal.HasOpenSocket (PROP)

## FbMulticastListener_internal (FB)


A UDP-Server (sic!) which is able to join an IGMP-Group

(See at that point for interface-variables)

A UDP-Server (sic!) which is able to join an IGMP-Group (See at that point for interface-variables) - 10 Main Interface FbMulticastListener_internal.Close (METH) - FbMulticastListener_internal.ConfigureKeepAliveTransmission (METH) - FbMulticastListener_internal.LeaveGroup (METH) - FbMulticastListener_internal.OpenAndJoin (METH) - FbMulticastListener_internal.ReJoinGroup (METH) 20 Administration - FbMulticastListener_internal.finish (METH) - FbMulticastListener_internal.initialize (METH)

## FbSocketClient_internal (FB)


This FB is used to implement the client role of a socket connection.

This FB handles TCP connections as well as UDP transmissions. If a UDP transmitter does not expect any response, this FB produces a slight overhead by reserving a receiver port number which is never used.

Unlike the socket server FB, the client role is not purely event driven, but the client is supposed to act initiatively and there is no need to handle multiple connections for one service at the client side. Thus, there is in the first place no need to derive other FBs from this one.

The FB is used very similarly like file FBs.

The main difference in behaviour is that a considerable latency (even in terms of PLC cycles) or even complete failure is to be expected regularly for each action, depending on the health and connection circumstances of the corresponding server.

Thus, it must be waited if the socket FB is ready for transmitting new data (unless you derive your own client which handles data buffering) and it should be checked regularly if new response data has been arrived, which could occcur at random points in time.

This FB is used to implement the client role of a socket connection. This FB handles TCP connections as well as UDP transmissions. If a UDP transmitter does not expect any response, this FB produces a slight overhead by reserving a receiver port number which is never used. Unlike the socket server FB, the client role is not purely event driven, but the client is supposed to act initiatively and there is no need to handle multiple connections for one service at the client side. Thus, there is in the first place no need to derive other FBs from this one. The FB is used very similarly like file FBs. The main difference in behaviour is that a considerable latency (even in terms of PLC cycles) or even complete failure is to be expected regularly for each action, depending on the health and connection circumstances of the corresponding server. Thus, it must be waited if the socket FB is ready for transmitting new data (unless you derive your own client which handles data buffering) and it should be checked regularly if new response data has been arrived, which could occcur at random points in time. - 10 Main FbSocketClient_internal.CheckConnection (METH) - FbSocketClient_internal.CloseConnection (METH) - FbSocketClient_internal.OpenAndConnect (METH) - FbSocketClient_internal.Read (METH) - FbSocketClient_internal.Write (METH) 20 advanced - FbSocketClient_internal.Block (METH) - FbSocketClient_internal.CalmWatchdog (METH) - FbSocketClient_internal.ConfigureKeepAliveTransmission (METH) - FbSocketClient_internal.ReadWithHeader (METH) 30 properties - FbSocketClient_internal.OpState (PROP) - FbSocketClient_internal.OwnPort (PROP) 40 administrative - FbSocketClient_internal.finish (METH) - FbSocketClient_internal.initialize (METH)

## FbSocket_GenericConnection (FB)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | xConnected | BOOL |  |
| _handle | rts_iec_handle | from accept()^ |
| _ClientAddress | SysSocket.SOCKADDRESS | for general reply |

Interface variables - 01_from Application FbSocket_GenericConnection.protActiveClose (METH) - FbSocket_GenericConnection.protGetConnectionAddr (METH) - FbSocket_GenericConnection.protGetConnectionClientPort (METH) - FbSocket_GenericConnection.protGetOpState (METH) 02_for internal framework - FbSocket_GenericConnection.CalmWatchdog (METH) - FbSocket_GenericConnection.InitNewConnection (METH) - FbSocket_GenericConnection.Initialize_FbSocket_GenericConnection (METH) - FbSocket_GenericConnection.ServerClose (METH) - FbSocket_GenericConnection.getIdleTime (METH) - FbSocket_GenericConnection.initialize_only (METH)

## FbSocket_TcpInstanceSlot (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Input | xConnected | BOOL |  | FbSocket_GenericConnection |
| _handle | rts_iec_handle | from accept()^ | FbSocket_GenericConnection |
| _ClientAddress | SysSocket.SOCKADDRESS | for general reply | FbSocket_GenericConnection |

Interface variables - 01_from Application FbSocket_TcpInstanceSlot.protAttachWriteBuffer (METH) - FbSocket_TcpInstanceSlot.protGetConnectionProtocol (METH) - FbSocket_TcpInstanceSlot.protGetWriteCapacity (METH) - FbSocket_TcpInstanceSlot.protWrite (METH) 02_for internal framework - FbSocket_TcpInstanceSlot.InitNewConnection (METH) - FbSocket_TcpInstanceSlot.Initialize_FbSocket_TcpInstanceSlot (METH) - FbSocket_TcpInstanceSlot.ProcessPendingWritedata (METH) - FbSocket_TcpInstanceSlot.Read (METH)

## FbSocket_UdpInstanceSlot (FB)


| Scope | Name | Type | Comment | Inherited from |
| --- | --- | --- | --- | --- |
| Input | xConnected | BOOL |  | FbSocket_GenericConnection |
| _handle | rts_iec_handle | from accept()^ | FbSocket_GenericConnection |
| _ClientAddress | SysSocket.SOCKADDRESS | for general reply | FbSocket_GenericConnection |

Interface variables - 01_from Application FbSocket_UdpInstanceSlot.protActiveClose (METH) - FbSocket_UdpInstanceSlot.protAttachWriteBuffer (METH) - FbSocket_UdpInstanceSlot.protGetWritecapacity (METH) - FbSocket_UdpInstanceSlot.protWrite (METH) 02_for internal framework - FbSocket_UdpInstanceSlot.InitNewConnection (METH) - FbSocket_UdpInstanceSlot.Initialize_FbSocket_UdpInstanceSlot (METH) - FbSocket_UdpInstanceSlot.ProcessPendingWritedata (METH) - FbSocket_UdpInstanceSlot.Read (METH)

## FbTcpServer_internal (FB)


```
////////////////////////////////////////////////////////////////////
// declare what the new server should do
////////////////////////////////////////////////////////////////////

FUNCTION_BLOCK FbMyOwnServer EXTENDS FbSocketServerApplicationBase

  METHOD NotifyAttachment [...]
    InitializeEverything();
    NotifyAttachment := OK;

  METHOD NotifyNewConnection [...]
    If xAnythingStrange THEN ActiveClose(); END_IF
    NotifyNewConnection := OK;

  METHOD NotifyReceivedData [...]
    DoProcessingOf(pData, uiDataSize);
    If xAppropriate THEN Write(pAnswer,uiSizeOfAnswer); END_IF;
    NotifyReceivedData := OK;

  METHOD NotifyClose [...]
    CleanUp();
    NotifyClose := OK;

////////////////////////////////////////////////////////////////////
// provide at least instance of the Application Server application
// and one of the generic server
////////////////////////////////////////////////////////////////////


VAR_GLOBAL
  MyOwnServers  : ARRAY[0..4] OF FbMyOwnServer;
  MyFrameServer : FBSocketServer;
END_VAR

////////////////////////////////////////////////////////////////////
// The incorporation of the server into the application is just this:
//
// - initialize all servers
// - open the service on port 8080 (e.g.)
// - and let it run
////////////////////////////////////////////////////////////////////

PROGRAM PLC_PRG

  IF xInitializationCycle THEN

      MyFrameServer.AttachServerApplication(ADR(MyOwnServers[0]));
      MyFrameServer.AttachServerApplication(ADR(MyOwnServers[1]));
      MyFrameServer.AttachServerApplication(ADR(MyOwnServers[2]));
      MyFrameServer.AttachServerApplication(ADR(MyOwnServers[3]));
      MyFrameServer.AttachServerApplication(ADR(MyOwnServers[4]));

      MyFrameServer.OpenAndListen("Localhost", 8080, SocketProtocol_TCP);
  END_IF


  MyFrameServer();   // runs all instances of attached MyOwnServers
```

This FB provides a framework for building Server structures within the application.

For this purpose, the application derives own extentions from ‘FbSocketServerApplicationBase’ , which is able to respond approptiatelly to a connection start and to incoming data.

Then, a number of instances of these derived FBs are attached to the generic FbSocketServer, which listens to a certain port and distributes the incoming connections to the derived ServerApplication instances. Note: this technique allows for handling multiple clients simultaneously without needing true multitasking.

The ApplicationSevers were notified from the FbSocketServer with the following events:

They use the following services

Typical Usage:

This FB provides a framework for building Server structures within the application. For this purpose, the application derives own extentions from ‘FbSocketServerApplicationBase’ , which is able to respond approptiatelly to a connection start and to incoming data. Then, a number of instances of these derived FBs are attached to the generic FbSocketServer, which listens to a certain port and distributes the incoming connections to the derived ServerApplication instances. Note: this technique allows for handling multiple clients simultaneously without needing true multitasking. The ApplicationSevers were notified from the FbSocketServer with the following events: - new incoming connection - new incoming data - closure of the connection - cyclic call (‘service’) They use the following services - incorporating the complete connection data (client identity, etc.) - write data to the peer - send keep-alive packets - poll the current status of the connection - close the connection actively Typical Usage: - 10 Main Interface FbTcpServer_internal.AttachServerApplication (METH) - FbTcpServer_internal.Close (METH) - FbTcpServer_internal.ConfigureKeepAliveTransmission (METH) - FbTcpServer_internal.OpenAndListen (METH) 20 administrative - FbTcpServer_internal.finish (METH) - FbTcpServer_internal.initialize (METH) 90 internal - FbTcpServer_internal.CyclicRun (METH) - FbTcpServer_internal.HasOpenSocket (PROP)

## TcpInstanceWriteBuffer (FB)


- TcpInstanceWriteBuffer.initialize (METH) - TcpInstanceWriteBuffer.protProcessData (METH)

## UdpInstanceWriteBuffer (FB)


- UdpInstanceWriteBuffer.CyclicService (METH) - UdpInstanceWriteBuffer.FillIn (METH) - UdpInstanceWriteBuffer.availableSpace (PROP) - UdpInstanceWriteBuffer.initialize (METH) - UdpInstanceWriteBuffer.protProcessData (METH)

### Functions


## GetIpAddressOfInterface (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | GetIpAddressOfInterface | eResultCode |  |
| Input | psDeviceName | POINTER TO BYTE | Name of the device / interface, e.g. ‘br1’, ‘eth0’, ... |
| psTargetName | POINTER TO BYTE | Description of the target, if Interface name has wildcards (ignored otherwise) |
| pResultBuffer | POINTER TO BYTE | space for the resulting IP-Address of the interface in network-byte-order |
| udiBufferSize | UDINT | size of the result buffer (at least 4, might be more for future IPv6) |
| Output | udiResultSize | UDINT | Actually used size of the result. ( 4 for ipV4, 16 for ipV6, 0 on error) |

| result codes |
| 0 | successful operation |
| ENOENT | the device/interface name is unknown |
| EOVERFLOW | the given buffer space was too small for the result |
| EBADRQC | invalid request code: use of wildcards is not supported. |
| ENOSYS | the desired functionality is not supported at all |
| EINVAL | invalid arguments (e.g. nullpointer for buffer) |
| EACCES | other errors while resolving the device name |

Retrieves the ip address of an internal device or interface from its name

For regular use, only the device name is passed (e.g. ‘eth0’ or ‘br1’) while any target name is ignored for computation.

Optional functionality : In some special cases, the device name is ambiguous. In that cases the device name may contain an wildcard ‘br*’ and for resolution of the correct device ip address additional information is required(e.g. the target address, which is passed via ‘psTargetName’. (Please note that this usage of wildcrad is not necessarily supported by the target PLC, which would return EBADRQC in that case)

Result : The resulting IP-address is written into a buffer location which is indicated by pResultBuffer. Although for conventional ip-V4-systems a fixed buffersize of 4 bytes is used, future developments (such as iv-V6) may require more space (which would be 16 bytes in that case).

Interface variables Retrieves the ip address of an internal device or interface from its name For regular use, only the device name is passed (e.g. ‘eth0’ or ‘br1’) while any target name is ignored for computation. Optional functionality : In some special cases, the device name is ambiguous. In that cases the device name may contain an wildcard ‘br*’ and for resolution of the correct device ip address additional information is required(e.g. the target address, which is passed via ‘psTargetName’. (Please note that this usage of wildcrad is not necessarily supported by the target PLC, which would return EBADRQC in that case) Result : The resulting IP-address is written into a buffer location which is indicated by pResultBuffer. Although for conventional ip-V4-systems a fixed buffersize of 4 bytes is used, future developments (such as iv-V6) may require more space (which would be 16 bytes in that case).

## SinglePing (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | SinglePing | eResultCode |  |
| Input | sAddress | STRING | address of the target device |
| tTimeout | TIME | aftwer which time we assume non-existence (default minimum 5ms) |
| Output | tResponseTime | TIME |  |

| Result codes |
| 0 | regular response |
| EINVAL | the address is malformed |
| ETIMEDOUT | no response within the given timeout |
| ENETUNREACH | the target net address could not be reached (active error response from networkstack) |

sets up s single Ping.

Interface variables sets up s single Ping.

## _ApplyKeepAliveParameters (FUN)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | _ApplyKeepAliveParameters | eResultCode |  |
| Input | handle | SysTypes.RTS_IEC_HANDLE | to which socket should the result be applied to? |
| pPara | POINTER TO typKeepAliveParameter |  |

## _TransposeKeepAliveResults (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | _TransposeKeepAliveResults | eResultCode |
| Input | iecResult | DWORD |

### Methods


## FbDatagramServer_internal.AttachServerApplication (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | AttachServerApplication | eResultCode |
| Input | pInstance | POINTER TO FbSocketServer_ApplicationBase |

| result codes |
| 0 | success |
| EMFILE | the number of server application instances exceeds its limit. (with ‘M’, not ‘N’) |
| EINVAL | Null-Pointer |
| EACCES | the initalization of the server application FB responded a failure |

Attaches a new Server FB to the Server Socket

When an instance of the server application FB is attached to the socket server FB, it can be used for an new incoming connection. Calling this server application FB will then be handled by the socket server FB, which might handle multiple server application FBs.

Note: New server application FBs may be added/attached while the socket server FB is already open.

Interface variables Attaches a new Server FB to the Server Socket When an instance of the server application FB is attached to the socket server FB, it can be used for an new incoming connection. Calling this server application FB will then be handled by the socket server FB, which might handle multiple server application FBs. Note: New server application FBs may be added/attached while the socket server FB is already open.

## FbDatagramServer_internal.AttachSingleServerApplication (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | AttachSingleServerApplication | eResultCode |
| Input | pInstance | POINTER TO FbSocketServer_ApplicationBase |

| result codes |
| 0 | success |
| EMFILE | the number of server application instances exceeds its limit. (with ‘M’, not ‘N’) |
| EINVAL | Null-Pointer |
| EACCES | the initalization of the server application FB responded a failure |

Attaches a new Server FB to the Server Socket

When an instance of the server application FB is attached to the socket server FB, it can be used for an new incoming connection. Calling this server application FB will then be handled by the socket server FB, which might handle multiple server application FBs.

Note: New server application FBs may be added/attached while the socket server FB is already open.

Interface variables Attaches a new Server FB to the Server Socket When an instance of the server application FB is attached to the socket server FB, it can be used for an new incoming connection. Calling this server application FB will then be handled by the socket server FB, which might handle multiple server application FBs. Note: New server application FBs may be added/attached while the socket server FB is already open.

## FbDatagramServer_internal.Close (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Close | eResultCode |

| result codes |
| 0 | success |
| EBADF | The socket FB was not open |
| EACCES | Unexpected problems at closing the linstening socket |

Closes the Server socket and closes all attached server FBs

Interface variables Closes the Server socket and closes all attached server FBs

## FbDatagramServer_internal.CyclicRun (METH) ¶


## FbDatagramServer_internal.OpenAndListen (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | OpenAndListen | eResultCode |  |
| Input | sAddress | STRING | local address of the network plug |
| uiPort | UINT | port number of the service (0=RAW) |
| tTimeout | TIME | tolerated inactivity |

| result codes |
| 0 | success, ready for communication. |
| EACCES | the socket could not be created by other reasons |
| EINVAL | invalid argument, e.g. malformed adress |
| ENFILE | The system limit on the total number of open sockets has been reached. |
| EADDRINUSE | The given address / port combination is already in use. |
| EBUSY | The socket is already bound to an address. |
| EADDRNOTAVAIL | A nonexistent interface was requested or the requested address was not local. |

Opens a Server socket and listens for incoming packets.

After this call is done, the FbServerSocket dispatches incoming data to the attached server application FBs.

sAddress defines the local network interface which is attached to this service. It can be identified either by the IP-Address, (‘192.168.8.15’), or by the device name (‘ETH0’), or by just an interface number (‘#0’). If nothing is declared, the default interface is taken.

uiPort identifies the port number under which this service should be advertised.

eType specifies, if it is a TCP-Socket, a UDP-Socket or a RAW connection.

uiBacklog specifies the maximum length to which the queue of pending connections for the socket may grow beyond the number of server instances. If a connection request arrives when all attached server instances are busy and the queue is full, the client will receive an error with an indication of ECONNREFUSED or, if the underlying protocol supports retransmission, the request may be ignored so that a later reattempt at connection succeeds.

Interface variables Opens a Server socket and listens for incoming packets. After this call is done, the FbServerSocket dispatches incoming data to the attached server application FBs. sAddress defines the local network interface which is attached to this service. It can be identified either by the IP-Address, (‘192.168.8.15’), or by the device name (‘ETH0’), or by just an interface number (‘#0’). If nothing is declared, the default interface is taken. uiPort identifies the port number under which this service should be advertised. eType specifies, if it is a TCP-Socket, a UDP-Socket or a RAW connection. uiBacklog specifies the maximum length to which the queue of pending connections for the socket may grow beyond the number of server instances. If a connection request arrives when all attached server instances are busy and the queue is full, the client will receive an error with an indication of ECONNREFUSED or, if the underlying protocol supports retransmission, the request may be ignored so that a later reattempt at connection succeeds.

## FbDatagramServer_internal.finish (METH) ¶


## FbDatagramServer_internal.initialize (METH) ¶


## FbMulticastListener_internal.Close (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Close | eResultCode |

| result codes |
| 0 | success |
| EBADF | The socket FB was not open |

Closes the Server socket.

If Multicast was selected, IGMP messages for leaving the group were sent before.

Interface variables Closes the Server socket. If Multicast was selected, IGMP messages for leaving the group were sent before.

## FbMulticastListener_internal.ConfigureKeepAliveTransmission (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ConfigureKeepAliveTransmission | eResultCode |  |
| Input | xEnable | BOOL | Switch keepalive mechanism on |
| tMaxIdleTime | TIME | Maximum time of inactivity before first keep-alive packet is sent. |
| tInterval | TIME | Interval between two successive KA-Packets if no reply is received |
| udiProbes | UDINT | Number of KA transmissions before declaring the connection ‘dead’ |

| result codes |
| 0 | Success, ready for communication. |
| EINVAL | Invalid Parameters |
| ENOSYS | This Feature is not supported by the target |

This method configures the autonomous sending of keep alive (‘KA’) packets.

When the keep-alive (KA) feature is turned on, the client socket checks periodically if the server is still reachable by sending empty packets and expecting acknowledge packets.

The purpose of this is to ensure for the client that the server is still reachable.

Thus, after a maximum idle time after complete inactivity (no transmission nor reception of any packets), a special keep-alive-packet is sent (which contains no data, but is acknowledged by TCP). Unless that KA-packet is acknowledged, it is retransmitted after a given interval .

When the prefifined number of probes is exceeded without acknowledgement, the connection is considered to be broken and the socket status is set to ETIMEDOUT.

Nevertheless, more packets could be tried to be sent in spite of that situation (as the socket is still open) and whith the first sign of life from the peer the connection will be considered ‘alive’ again.

The input udiProbes is interpreted as follows: 0=give up without KA-Packet, 1=give up after ‘Interval’ is elapsed after first KA-packet.

This configuration has to be done only once per inctance, as it will persist after opening or closing the FB.

Note: This feature is controversially disputed (see RFC 1122) and not useful in every situation.

Interface variables This method configures the autonomous sending of keep alive (‘KA’) packets. When the keep-alive (KA) feature is turned on, the client socket checks periodically if the server is still reachable by sending empty packets and expecting acknowledge packets. The purpose of this is to ensure for the client that the server is still reachable. Thus, after a maximum idle time after complete inactivity (no transmission nor reception of any packets), a special keep-alive-packet is sent (which contains no data, but is acknowledged by TCP). Unless that KA-packet is acknowledged, it is retransmitted after a given interval . When the prefifined number of probes is exceeded without acknowledgement, the connection is considered to be broken and the socket status is set to ETIMEDOUT. Nevertheless, more packets could be tried to be sent in spite of that situation (as the socket is still open) and whith the first sign of life from the peer the connection will be considered ‘alive’ again. The input udiProbes is interpreted as follows: 0=give up without KA-Packet, 1=give up after ‘Interval’ is elapsed after first KA-packet. This configuration has to be done only once per inctance, as it will persist after opening or closing the FB. Note: This feature is controversially disputed (see RFC 1122) and not useful in every situation.

## FbMulticastListener_internal.LeaveGroup (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | LeaveGroup | eResultCode |

| result codes |
| 0 | success, ready for communication. |
| ENOSYS | the function is not supported. |
| EBADF | the FB was not open |

Leaves a Multicast Group without closing the FB.

Interface variables Leaves a Multicast Group without closing the FB.

## FbMulticastListener_internal.OpenAndJoin (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | OpenAndJoin | eResultCode |  |
| Input | sAddress | IPAddressString | local address OF the network plug |
| uiPort | UINT | port number of the service (0=RAW) |
| usiVersion | USINT | 0 = broadcast, 1..3 = IGMP-V1..3 |
| sGroupAddress | IPAddressString | The group or network, which is listened to |
| sSource | STRING | Designated data producer (‘’ = any) |

| result codes |
| 0 | success, ready for communication. |
| EACCES | the socket could not be created by other reasons |
| EINVAL | invalid argument |
| ENFILE | The system limit on the total number of open sockets has been reached. |
| EADDRINUSE | The given address / port combination is already in use. |
| EBUSY | The socket is already bound to an address. |
| EPROTOTYPE | The given protocol type (‘eProto’) is not supported. (RAW and UDP only , not TCP) |
| EADDRNOTAVAIL | A nonexistent interface was requested or the requested address was not local. |

Opens a Server socket and listens for incoming packets.

After this call is done, the FbServerSocket dispatches incoming data to the attached server application FBs.

sAddress defines the local network interface which is attached to this service. It can be identified either by the IP-Address, (‘192.168.8.15’), or by the device name (‘ETH0’), or by just an interface number (‘#0’). If nothing is declared, the default interface is taken.

uiPort identifies the port number under which this service should be advertised.

usiVersion specifies the underlying protocol version. 0 means, the FB listens to a common broadcast or unicast, while the numbers 1..3 identify the different versions of IGMP.

sGroupAddress specifies the multicast address, the FB listens to. Note: This is neither the clients, nor the producers IP address. It would be e.g. ‘192.168.0.255’ for a broadcast listener an a class C local net or e.g. ‘224.1.2.3’ for a multicast listener. When ‘’ is applied, the FB listens to the broadcast address of the specified local network interface. When the same string as ‘sAddress’ is applied, the FB listens on regular unicast datagrams. When Multicast is selected, the FB actively registers to the group address specified here.

sSource specifies if datagrams are accepted only from one well-defined producer. (‘’ = accept from any producer) If multiple producers are accepted, the addresses are separeted by ‘,’. Note: Although IGMP-v3 allows the specification of an unlimited list of producers, this feature is restricted here, to a short list of 80 chars size, which is sufficient to contain 5 different IPv4 addresses. (not yet implemented)

Interface variables Opens a Server socket and listens for incoming packets. After this call is done, the FbServerSocket dispatches incoming data to the attached server application FBs. sAddress defines the local network interface which is attached to this service. It can be identified either by the IP-Address, (‘192.168.8.15’), or by the device name (‘ETH0’), or by just an interface number (‘#0’). If nothing is declared, the default interface is taken. uiPort identifies the port number under which this service should be advertised. usiVersion specifies the underlying protocol version. 0 means, the FB listens to a common broadcast or unicast, while the numbers 1..3 identify the different versions of IGMP. sGroupAddress specifies the multicast address, the FB listens to. Note: This is neither the clients, nor the producers IP address. It would be e.g. ‘192.168.0.255’ for a broadcast listener an a class C local net or e.g. ‘224.1.2.3’ for a multicast listener. When ‘’ is applied, the FB listens to the broadcast address of the specified local network interface. When the same string as ‘sAddress’ is applied, the FB listens on regular unicast datagrams. When Multicast is selected, the FB actively registers to the group address specified here. sSource specifies if datagrams are accepted only from one well-defined producer. (‘’ = accept from any producer) If multiple producers are accepted, the addresses are separeted by ‘,’. Note: Although IGMP-v3 allows the specification of an unlimited list of producers, this feature is restricted here, to a short list of 80 chars size, which is sufficient to contain 5 different IPv4 addresses. (not yet implemented)

## FbMulticastListener_internal.ReJoinGroup (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ReJoinGroup | eResultCode |

| result codes |
| 0 | success, ready for communication. |
| ENOSYS | the function is not supported. |
| EBADF | the FB was not open |

Re-Joins a Multicast group with the parameter from ‘open’.

This function repeats the joining process to a group, which has already done with open. This might be necessary, when the integrity of the data path is in doubt.

Interface variables Re-Joins a Multicast group with the parameter from ‘open’. This function repeats the joining process to a group, which has already done with open. This might be necessary, when the integrity of the data path is in doubt.

## FbMulticastListener_internal.finish (METH) ¶


## FbMulticastListener_internal.initialize (METH) ¶


## FbSocketClient_internal.Block (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Block | eResultCode |
| Input | eScheduledOP | eSocketOpState |

Prepares for asynchronous scheduling.

This method informs the fb that some asynchronous operation is to come and other operations than the scheduled are to be rejected. This prevents from writing and reading when the FB is busy with asynchronous issues. The blocking state will be lifted automatically when the open() or close() methods are finished.

Interface variables Prepares for asynchronous scheduling. This method informs the fb that some asynchronous operation is to come and other operations than the scheduled are to be rejected. This prevents from writing and reading when the FB is busy with asynchronous issues. The blocking state will be lifted automatically when the open() or close() methods are finished.

## FbSocketClient_internal.CalmWatchdog (METH)


Acknowledges that the channel is still in use.

Acknowledges that the channel is still in use.

## FbSocketClient_internal.CheckConnection (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | CheckConnection | eSocketOpState |

checks the connection state of a socket and returns the result.

Interface variables checks the connection state of a socket and returns the result.

## FbSocketClient_internal.CloseConnection (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | CloseConnection | eResultCode |

| result codes |
| 0 | success |
| EBADF | The socket FB was not open |

closes the connection from client side

Interface variables closes the connection from client side

## FbSocketClient_internal.ConfigureKeepAliveTransmission (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ConfigureKeepAliveTransmission | eResultCode |  |
| Input | xEnable | BOOL | Switch keepalive mechanism on |
| tMaxIdleTime | TIME | Maximum time of inactivity before first keep-alive packet is sent. |
| tInterval | TIME | Interval between two successive KA-Packets if no reply is received |
| udiProbes | UDINT | Number of KA transmissions before declaring the connection ‘dead’ |

| result codes |
| 0 | Success, ready for communication. |
| EINVAL | Invalid Parameters. |
| ENOSYS | This Feature is not supported by the target. |
| EWOULDBLOCK | No Connection was established. Settings will be applied later. |
| EACCES | Other Error from OS layer. |

Configures keep alive (‘KA’) operation.

This method configures the autonomous sending of keep alive (‘KA’) packets.

When the keep-alive (KA) feature is turned on, the client socket checks periodically if the server is still reachable by sending empty packets and expecting acknowledge packets.

The purpose of this is to ensure for the client that the server is still reachable.

Thus, after a maximum idle time after complete inactivity (no transmission nor reception of any packets), a special keep-alive-packet is sent (which contains no data, but is acknowledged by TCP). Unless that KA-packet is acknowledged, it is retransmitted after a given interval .

When the prefifined number of probes is exceeded without acknowledgement, the connection is considered to be broken and the socket status is set to ETIMEDOUT.

Nevertheless, more packets could be tried to be sent in spite of that situation (as the socket is still open) and whith the first sign of life from the peer the connection will be considered ‘alive’ again.

The input udiProbes is interpreted as follows: 0=give up without KA-Packet, 1=give up after ‘Interval’ is elapsed after first KA-packet.

This configuration has to be done only once per inctance, as it will persist after opening or closing the FB.

Note: This feature is controversially disputed (see RFC 1122) and not useful in every situation.

Interface variables Configures keep alive (‘KA’) operation. This method configures the autonomous sending of keep alive (‘KA’) packets. When the keep-alive (KA) feature is turned on, the client socket checks periodically if the server is still reachable by sending empty packets and expecting acknowledge packets. The purpose of this is to ensure for the client that the server is still reachable. Thus, after a maximum idle time after complete inactivity (no transmission nor reception of any packets), a special keep-alive-packet is sent (which contains no data, but is acknowledged by TCP). Unless that KA-packet is acknowledged, it is retransmitted after a given interval . When the prefifined number of probes is exceeded without acknowledgement, the connection is considered to be broken and the socket status is set to ETIMEDOUT. Nevertheless, more packets could be tried to be sent in spite of that situation (as the socket is still open) and whith the first sign of life from the peer the connection will be considered ‘alive’ again. The input udiProbes is interpreted as follows: 0=give up without KA-Packet, 1=give up after ‘Interval’ is elapsed after first KA-packet. This configuration has to be done only once per inctance, as it will persist after opening or closing the FB. Note: This feature is controversially disputed (see RFC 1122) and not useful in every situation.

## FbSocketClient_internal.OpenAndConnect (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | OpenAndConnect | eResultCode |  |
| Input | sAddress | IPAddressString | provides the Address of the desired endpoint. |
| uiPort | UINT | port number |
| eType | eSocketProtocol | Raw or UDP or TCP |
| xAllowBroadcast | BOOL | Allows Broadcast or Multicast rsp. |
| sOwnInterface | STRING | Specifies which logical device to use (Normally ‘’) |
| tTimeout | TIME | Timeout for connection |

| result codes |
| 0 | Success, ready for communication. |
| EACCES | Permission to create a socket of the specified type and/or protocol is denied. |
| EINVAL | Unknown protocol or malformed address |
| ENFILE | The system limit on the total number of open sockets has been reached. |
| EPROTONOSUPPORT | The desired protocol is not supported. |
| ECONNREFUSED | No-one listening on the remote address. |
| EHOSTUNREACH | Target Host is not reachable |
| ENOPROTOOPT | Protocol option ‘sOwnInterface’ not applicable |
| ETIME | Timeout while attempting connection. |
| EAGAIN | No response from server received yet. (That may take longer time) |
| EIO | Unspecific |

Opens a new client connection and connects to the server

When TCP is selected as protocol, this method also tries to establish a TCP-connection to the server, which is pointless in the other cases.

The OpenAndConnect() call returns direcly without necessarily waiting for the server to respond (equivalent to O_NONBLOCK). In most cases, the connection has not been established yet, so the call returns with EAGAIN, which does not mean failure, but “Try Again”. Before sending data to the socket, the application should use IsReadyForWrite or State for determining if the server has answered inbetween.

Note: the tTimeout does not mean that the call will wait for a maximum of this time, but after this time the socket FB gives up and transits to the “Closed” state.

Write Buffer: In order to optimize the data flow, the client FB may be provided by externally allocated buffer space for the write queue. The inputs pWriteBuffer and udiWriteBufferSize hold the parameters of that external buffer.

Providing an external buffer space is, hovwever, not mandatory. When a null-pointer is passed to the input, the client FB simply operates with minimal internal buffering so the application would have to wait between adjecent write()s.

Broadcast and Multicast: Regularly, the socket client FB is operated on point-to-point connections. When broadcast transmission or mulicast transmission is required, this has to be explicitelly enabled by the xAllowBroadcast -flag in the OpenAndConnect call, in order to prevent erroneous broadcasting due to errors in the target addrest.

For broadcasts and multicasts there are special target addresses to be used (e.g. 224.0.0.0/4 for multicast). While for broadcast operation, no further speacuial means are required (beside setting some options in the socket stack), multicast operation requires configuration of the involved routers via IGMP in one of its three versions. To the sender of multicasts (i.e. this FB) this process is completelly hidden. Beside the special target address the sender is completely unaware about how many and which receivers are listening to the messages - it simply sends the packets to the primary router.

The potential receivers of multicast (not broadcast!) messages have to play an active role now. They have to register to the involved routers via IGMP. This is, however, beyond the scope of this client FB, as the recipients of multicast messages act formally as servers (i.e. they receive spontaneous transmissions which are not direct responses to own transmissions).

Note: There are function blocks ‘FbMulticastReceiver’, which are especially designed for using Broadcast and Multicast connections.

sOwnInterface: This parameter is used for specifying which interface is to be used. The same naming conventions apply as for the host-IP of server sockets. If it is not possible to honor the specified sOwnInterface , then ENOPROTOOPT is returned.

Note(1): This FB does not support hopping between different port numbers, as occasionally used by UDP connections. For that purpose, another FB type has to be used.

Note (2): We did not specify any optional flags yet. In contrast to lowlevel system calls, we would implement flags as binary inputs rather than packed 32-bits.

Note (3) There are many possible causes for ETIME. One is that the server may be too busy to accept new connections. For IP sockets the timeout may be very long when syncookies are enabled on the server.

Interface variables Opens a new client connection and connects to the server When TCP is selected as protocol, this method also tries to establish a TCP-connection to the server, which is pointless in the other cases. The OpenAndConnect() call returns direcly without necessarily waiting for the server to respond (equivalent to O_NONBLOCK). In most cases, the connection has not been established yet, so the call returns with EAGAIN, which does not mean failure, but “Try Again”. Before sending data to the socket, the application should use IsReadyForWrite or State for determining if the server has answered inbetween. Note: the tTimeout does not mean that the call will wait for a maximum of this time, but after this time the socket FB gives up and transits to the “Closed” state. Write Buffer: In order to optimize the data flow, the client FB may be provided by externally allocated buffer space for the write queue. The inputs pWriteBuffer and udiWriteBufferSize hold the parameters of that external buffer. Providing an external buffer space is, hovwever, not mandatory. When a null-pointer is passed to the input, the client FB simply operates with minimal internal buffering so the application would have to wait between adjecent write()s. Broadcast and Multicast: Regularly, the socket client FB is operated on point-to-point connections. When broadcast transmission or mulicast transmission is required, this has to be explicitelly enabled by the xAllowBroadcast -flag in the OpenAndConnect call, in order to prevent erroneous broadcasting due to errors in the target addrest. For broadcasts and multicasts there are special target addresses to be used (e.g. 224.0.0.0/4 for multicast). While for broadcast operation, no further speacuial means are required (beside setting some options in the socket stack), multicast operation requires configuration of the involved routers via IGMP in one of its three versions. To the sender of multicasts (i.e. this FB) this process is completelly hidden. Beside the special target address the sender is completely unaware about how many and which receivers are listening to the messages - it simply sends the packets to the primary router. The potential receivers of multicast (not broadcast!) messages have to play an active role now. They have to register to the involved routers via IGMP. This is, however, beyond the scope of this client FB, as the recipients of multicast messages act formally as servers (i.e. they receive spontaneous transmissions which are not direct responses to own transmissions). Note: There are function blocks ‘FbMulticastReceiver’, which are especially designed for using Broadcast and Multicast connections. sOwnInterface: This parameter is used for specifying which interface is to be used. The same naming conventions apply as for the host-IP of server sockets. If it is not possible to honor the specified sOwnInterface , then ENOPROTOOPT is returned. - If an empty string (‘’) is passed (the default and regular case), then the OS decides itself via the routing table which interface to use. - This option is mainly used for broadcast- or multicast transmissions, where the usage of the routing table might be ambiguous. Note(1): This FB does not support hopping between different port numbers, as occasionally used by UDP connections. For that purpose, another FB type has to be used. Note (2): We did not specify any optional flags yet. In contrast to lowlevel system calls, we would implement flags as binary inputs rather than packed 32-bits. Note (3) There are many possible causes for ETIME. One is that the server may be too busy to accept new connections. For IP sockets the timeout may be very long when syncookies are enabled on the server.

## FbSocketClient_internal.Read (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Read | eResultCode |  |
| Input | pReadBuffer | POINTER TO BYTE | The location of the databuffer to transfer the data to |
| udiSize | UDINT | Number of bytes to be read |
| Output | udiResNRead | UDINT | Response, how many data are actualy transferred |

| result codes |
| 0 | success, ready for new communication. |
| EBADF | socket is not open |
| EWOULDBLOCK | the requested amount of data could not be read |
| EACCES | other problem while receiving data |
| ENODATA | No data |
| EPIPE | connection closed from server side |

Reads a number of bytes from the stream / datagram

Interface variables Reads a number of bytes from the stream / datagram

## FbSocketClient_internal.ReadWithHeader (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ReadWithHeader | eResultCode |

| FbSocketClient.ReadWithHeader (FUN) - Interface |
| Name | Access | Type | Semantics |
| pTarget | IN | POINTER TO BYTE | The location of the databuffer |
| udiNData | IN | UDINT | Number of bytes to be read |
| pHeader | IN | POINTER TO BYTE | Location of the header buffer |
| uiHeaderSize | IN | UINT | Size of the Header buffer |
| (none) | Return | eResultCode | success (=0) or error cause |

| result codes |
| 0 | success, ready for new communication. |
| EBADF | socket is not open |
| ENOSYS | this function is not supported by the hardware |
| EWOULDBLOCK | the requested amount of data could not be read |
| EMSGSIZE | requested data size is too large (esp.: size limit for UDP) |
| EACCES | other problem while receiving data |

Delivers payload and header (not implemented yet)

Reads a number of bytes from the stream / datagram and also provides header data

( Not Implemented Yet )

In contrast to the conventional read, this one provides the full IP-header information of the received packet. Note: the size of the header is no given explicitelly, as it is implicitelly part of the header data itself. If there is more header data than buffer space available, the rest of the header is silently discarded.

Interface variables Delivers payload and header (not implemented yet) Reads a number of bytes from the stream / datagram and also provides header data ( Not Implemented Yet ) In contrast to the conventional read, this one provides the full IP-header information of the received packet. Note: the size of the header is no given explicitelly, as it is implicitelly part of the header data itself. If there is more header data than buffer space available, the rest of the header is silently discarded.

## FbSocketClient_internal.Write (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Write | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | The location of the data |
| udiTxBufferSize | UDINT | Number of bytes to send |
| Output | udiTxNBytes | UDINT | Response, how many data are actualy transferred |

| result codes |
| 0 | success, ready for new communication. |
| EINPROGRESS | success, data are pending to be written |
| EBADF | socket is not open |
| EBUSY | Actual data is ignored because there is previous data to be written. |
| EMSGSIZE | data chunk is too large (esp.: size limit for UDP) |
| EPIPE | the stream was closed on server side |
| EACCES | other problem while writing data |

Writes data to a client socket

Note(1): before writing data, it should be checked, that the socket is ready for accepting data.

Note(2): The write() call returns immediatelly without checking that the data is actually written. Before new data is written, it must be ensured that the previous data has been processed completely by checking IsReadyForWrite.

Application Note on Data Buffering:

Buffering data is a well known standard problem when large chunks of data are to be sent over a slow connection and the producer (sender) of the data must not be blocked during the transmission process. In order to cope with envisaged standard data sizes, each instance of the client FBs may be provided with appropriate buffer space on opening the connection.

When unexpectedly larger chunks of data are to be sent, a bunch of established techniques - e.g. providing asynchronous execution of the transmission process or dynamically increase of transmission buffers - are be helpful at the first glance, but they all will not solve this ultimatively, because it all comes down to the point that the data has to be buffered somewhere and the total buffer size on real systems has hard limits.

Considering the fact that even with infinite buffer space the client typically has to wait an undefined long time for the answer from the server anyway, it would not hurt much, if the client has to wait during the sending process between several writes. The total sum of wait time is thus not significantly increased, but just chopped into smaller portions.

Consequently, before potentially ending up with out-of-buffer conditions the client FB is temporariliy precented from producing more send data when it is clear that the produced data cannot be delivered anywhere at that time.

To save resources, the memory portion, which is passed to the write() method, is used as write buffer itself. Thus, this memory must not be altered until the method IsReadyForWrite() returns TRUE. During that time, the production of new data should be stopped. This procedure allows for processing of virtually unlimited data sizes (as long as it can be passed through the write() interface) without any chance of encountering a buffer-full condition.

Note (3): For appropriate handling of small chunks of data, a minimum sizeof internal buffer space is provided inside the FB, so for small data portions the function IsReadyForWrite() returns immedially TRUE.

Note (4): In parallel, the result code of write() tells direcly, if the passed data space may be re-used again (‘OK’) or not (‘EINPROGRESS’).

Note (5): By calling CancelWrite() the usage of passed data space by the client-FB is stopped immediatelly. This might be used in case of ‘emergency’, when the data space has to be released quickly, e.g. in FB_Exit.

Note (6): The implementation of IsReadyForWrite() does not depend on internals of the firmware socket-stack. It is a mere administration function for internal data handling of the client FB.

Interface variables Writes data to a client socket Note(1): before writing data, it should be checked, that the socket is ready for accepting data. Note(2): The write() call returns immediatelly without checking that the data is actually written. Before new data is written, it must be ensured that the previous data has been processed completely by checking IsReadyForWrite. Application Note on Data Buffering: Buffering data is a well known standard problem when large chunks of data are to be sent over a slow connection and the producer (sender) of the data must not be blocked during the transmission process. In order to cope with envisaged standard data sizes, each instance of the client FBs may be provided with appropriate buffer space on opening the connection. When unexpectedly larger chunks of data are to be sent, a bunch of established techniques - e.g. providing asynchronous execution of the transmission process or dynamically increase of transmission buffers - are be helpful at the first glance, but they all will not solve this ultimatively, because it all comes down to the point that the data has to be buffered somewhere and the total buffer size on real systems has hard limits. Considering the fact that even with infinite buffer space the client typically has to wait an undefined long time for the answer from the server anyway, it would not hurt much, if the client has to wait during the sending process between several writes. The total sum of wait time is thus not significantly increased, but just chopped into smaller portions. Consequently, before potentially ending up with out-of-buffer conditions the client FB is temporariliy precented from producing more send data when it is clear that the produced data cannot be delivered anywhere at that time. To save resources, the memory portion, which is passed to the write() method, is used as write buffer itself. Thus, this memory must not be altered until the method IsReadyForWrite() returns TRUE. During that time, the production of new data should be stopped. This procedure allows for processing of virtually unlimited data sizes (as long as it can be passed through the write() interface) without any chance of encountering a buffer-full condition. Note (3): For appropriate handling of small chunks of data, a minimum sizeof internal buffer space is provided inside the FB, so for small data portions the function IsReadyForWrite() returns immedially TRUE. Note (4): In parallel, the result code of write() tells direcly, if the passed data space may be re-used again (‘OK’) or not (‘EINPROGRESS’). Note (5): By calling CancelWrite() the usage of passed data space by the client-FB is stopped immediatelly. This might be used in case of ‘emergency’, when the data space has to be released quickly, e.g. in FB_Exit. Note (6): The implementation of IsReadyForWrite() does not depend on internals of the firmware socket-stack. It is a mere administration function for internal data handling of the client FB.

## FbSocketClient_internal.finish (METH)


Cleans up FbSocketClient_internal.

Cleans up FbSocketClient_internal.

## FbSocketClient_internal.initialize (METH)


Initializes FbSocketClient_internal.

Initializes FbSocketClient_internal.

## FbSocket_GenericConnection.CalmWatchdog (METH) ¶


## FbSocket_GenericConnection.InitNewConnection (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | NewHandle | rts_iec_handle | from accept()^ |
| pAddress | POINTER TO SysSocket.SOCKADDRESS |  |

initializes the new member variables of GenericConnection, but not the parent, i.e. the framepointer is untouched.

Interface variables initializes the new member variables of GenericConnection, but not the parent, i.e. the framepointer is untouched.

## FbSocket_GenericConnection.Initialize_FbSocket_GenericConnection (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | pNewInstance | POINTER TO FbSocketServer_ApplicationBase |

## FbSocket_GenericConnection.ServerClose (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ServerClose | eResultCode |  |
| Input | eReason | eResultCode | why the connection was closed from the server side |

close the connection from the server side and notify the server instance about that

Interface variables close the connection from the server side and notify the server instance about that

## FbSocket_GenericConnection.getIdleTime (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getIdleTime | TIME |

## FbSocket_GenericConnection.initialize_only (METH)


initialize the new member variables, but leave the inherited members as they are.

initialize the new member variables, but leave the inherited members as they are.

## FbSocket_GenericConnection.protActiveClose (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | protActiveClose | eResultCode |

| FbSocketServer_MethodsForApplication.ActiveClose(FUN) - Interface |
| Name | Access | Type | Semantics |
| (none) | Return | eResultCode | success (=0) or error cause |

| Reason codes |
| 0 | regular closure |
| ECONNREFUSED | the application does not want to communicate with THAT client. |
| ECONNABORTED | a special error condition in processing causes a termination of the connection |
| EPIPE | the client has closed this connection |
| ETIMEDOUT | connection was idle for too long |

The argument Reason takes information to the framework why the application server closes the connection:

As a return result code, we do not expect other than ‘OK’.

Interface variables The argument Reason takes information to the framework why the application server closes the connection: As a return result code, we do not expect other than ‘OK’.

## FbSocket_GenericConnection.protGetConnectionAddr (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | protGetConnectionAddr | IpAddressString |

Asks the frame Server FB about the client’s identity

(May not be implemented for all protocols, returns empty string if information is not available.)

Interface variables Asks the frame Server FB about the client’s identity (May not be implemented for all protocols, returns empty string if information is not available.)

## FbSocket_GenericConnection.protGetConnectionClientPort (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | protGetConnectionClientPort | WORD |

Asks the frame Server FB about the client’s local port number

(May not be implemented for all protocols, returns zero if information is not available.)

Interface variables Asks the frame Server FB about the client’s local port number (May not be implemented for all protocols, returns zero if information is not available.)

## FbSocket_GenericConnection.protGetOpState (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | protGetOpState | eSocketOpState |

This asks the framework about the actual connection state of this instance.

Note: regularly, most ‘notify...()’-methods were either called only for attached and connected server instances or they signalize themself a disabled connection state so this state query is redundant for these cases.

But when derived instances are extended not only to react on notifications but also to external stimuli, it is convenient to have this status without the need to carefully trace the notifications.

Interface variables This asks the framework about the actual connection state of this instance. Note: regularly, most ‘notify...()’-methods were either called only for attached and connected server instances or they signalize themself a disabled connection state so this state query is redundant for these cases. But when derived instances are extended not only to react on notifications but also to external stimuli, it is convenient to have this status without the need to carefully trace the notifications.

## FbSocket_TcpInstanceSlot.InitNewConnection (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | NewHandle | rts_iec_handle | from accept()^ |
| pAddress | POINTER TO SysSocket.SOCKADDRESS |  |

## FbSocket_TcpInstanceSlot.Initialize_FbSocket_TcpInstanceSlot (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | pNewInstance | POINTER TO FbSocketServer_ApplicationBase |

## FbSocket_TcpInstanceSlot.ProcessPendingWritedata (METH)


## FbSocket_TcpInstanceSlot.Read (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Read | eResultCode |  |
| Input | pReadBuffer | POINTER TO BYTE | The location of the databuffer to transfer the data to |
| udiSize | UDINT | Number of bytes to be read |
| Output | udiResNRead | UDINT | Response, how many data are actualy transferred |

| ** Read (FUN) - Interface** |
| Name | Access | Type | Semantics |
| pReadBuffer | IN | POINTER TO BYTE | The location of the databuffer to transfer the data to |
| udiNData | IN | UDINT | Number of bytes to be read |
| pResNRead | OUT | UDINT | Response, how many data are actualy transferred |
| (none) | Return | eResultCode | success (=0) or error cause |

| result codes |
| 0 | success, ready for new communication. |
| EBADF | socket is not open |
| EWOULDBLOCK | the requested amount of data could not be read |
| EACCES | other problem while receiving data |
| ENODATA | No data |
| EPIPE | connection closed from server side |

Reads a number of bytes from the stream / datagram

Interface variables Reads a number of bytes from the stream / datagram

## FbSocket_TcpInstanceSlot.protAttachWriteBuffer (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | protAttachWriteBuffer | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | Location of external buffer space |
| udiTxBufferSize | UDINT | Size of the external buffer |

| FbSerialInterface.AttachExternalWriteBuffer (FUN) - Interface |
| Name | Access | Type | Semantics |
| pTxBuffer | IN | POINTER TO BYTE | Location of external buffer space for receiving |
| udiTxBufferSize | IN | UDINT | Size of the external receive buffer |
| (none) | Return | eResultCode | success (=0) or error cause |

| result codes |
| 0 | success, ready for communication. |
| EINVAL | Invalid parameters (size beyond plausibility). |
| EFBIG | New buffer is too small for data which is already contained in the previous buffer. |

Attaches external Buffers to the SI-FB

This method can be applied any time, even when the FB is not attached to a serial interface.

By default, each serial FB might have a small built-in buffer which handles most standard situations but is small enough to not waste system memory. In certain situations, when high transmission rate (e.g. 115k2) is combined with large cycle times (e.g. 250ms), or when large chunks of write data are generated, it is advisable to have buffers significantly larger than standard.

This is provided by this method.

If applied while in full operation, the previously received data were copied into the new buffer, if that one is big enough. If the new buffer is not big enough, data is lost.

If NULL-pointers are appilied or the buffer sizes are smaller than the internal buffers, then the internal buffer of the FB is used and the external buffer is silently ignored.

This method returns the following result codes:

Interface variables Attaches external Buffers to the SI-FB This method can be applied any time, even when the FB is not attached to a serial interface. By default, each serial FB might have a small built-in buffer which handles most standard situations but is small enough to not waste system memory. In certain situations, when high transmission rate (e.g. 115k2) is combined with large cycle times (e.g. 250ms), or when large chunks of write data are generated, it is advisable to have buffers significantly larger than standard. This is provided by this method. If applied while in full operation, the previously received data were copied into the new buffer, if that one is big enough. If the new buffer is not big enough, data is lost. If NULL-pointers are appilied or the buffer sizes are smaller than the internal buffers, then the internal buffer of the FB is used and the external buffer is silently ignored. This method returns the following result codes:

## FbSocket_TcpInstanceSlot.protGetConnectionProtocol (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | protGetConnectionProtocol | eSocketProtocol |

Asks the frame Server FB about the protocol type of the server

Interface variables Asks the frame Server FB about the protocol type of the server

## FbSocket_TcpInstanceSlot.protGetWriteCapacity (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | protGetWriteCapacity | DINT |

Asks the frame Server FB how many bytes of write data it can process at the moment.

If the frame server responds 0, you have to wait until the value increases. If it reports otherwise a too low value, you may have a problem.

Interface variables Asks the frame Server FB how many bytes of write data it can process at the moment. If the frame server responds 0, you have to wait until the value increases. If it reports otherwise a too low value, you may have a problem.

## FbSocket_TcpInstanceSlot.protWrite (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | protWrite | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | The location of the data |
| udiTxBufferSize | UDINT | Number of bytes to send |

| FbSocketServer_MethodsForApplication.Write (FUN) - Interface |
| Name | Access | Type | Semantics |
| pTxBuffer | IN | POINTER TO BYTE | The location of the data |
| udiTxBufferSize | IN | UDINT | Number of bytes to send |
| (none) | Return | eResultCode | success (=0) or error cause |

| result codes |
| 0 | success, ready for new communication. |
| EBADF | socket is not open (This schould be a programming error.) |
| EBUSY | Actual data is ignored because there is previous data to be written. |
| EMSGSIZE | data chunk is too large (esp.: size limit for UDP) |
| EPIPE | the stream was closed on serverside |
| EACCES | other problem while writing data |

Writes data from the Server to the Client.

Interface variables Writes data from the Server to the Client.

## FbSocket_UdpInstanceSlot.InitNewConnection (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Input | NewHandle | rts_iec_handle | from accept()^ |
| pAddress | POINTER TO SysSocket.SOCKADDRESS |  |

## FbSocket_UdpInstanceSlot.Initialize_FbSocket_UdpInstanceSlot (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | pNewInstance | POINTER TO FbSocketServer_ApplicationBase |

## FbSocket_UdpInstanceSlot.ProcessPendingWritedata (METH)


## FbSocket_UdpInstanceSlot.Read (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | Read | eResultCode |  |
| Input | handle | SysTypes.RTS_IEC_HANDLE | handle of the listening socket. |
| pReadBuffer | POINTER TO BYTE | The location of the databuffer to transfer the data to |
| udiSize | UDINT | Number of bytes to be read |
| Output | udiResNRead | UDINT | Response, how many data are actualy transferred |

| ** Read (FUN) - Interface** |
| Name | Access | Type | Semantics |
| pReadBuffer | IN | POINTER TO BYTE | The location of the databuffer to transfer the data to |
| udiNData | IN | UDINT | Number of bytes to be read |
| pResNRead | OUT | UDINT | Response, how many data are actualy transferred |
| (none) | Return | eResultCode | success (=0) or error cause |

| result codes |
| 0 | success, ready for new communication. |
| EBADF | socket is not open |
| EWOULDBLOCK | the requested amount of data could not be read |
| EACCES | other problem while receiving data |
| ENODATA | No data |
| EPIPE | connection closed from server side |

Reads a number of bytes from the stream / datagram

Interface variables Reads a number of bytes from the stream / datagram

## FbSocket_UdpInstanceSlot.protActiveClose (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | protActiveClose | eResultCode |

| FbSocketServer_MethodsForApplication.ActiveClose(FUN) - Interface |
| Name | Access | Type | Semantics |
| Reason | IN | eResultCode | why the server closes the connection |
| (none) | Return | eResultCode | success (=0) or error cause |

| Reason codes |
| 0 | regular closure |
| ECONNREFUSED | the application does not want to communicate with THAT client. |
| ECONNABORTED | a special error condition in processing causes a termination of the connection |
| EPIPE | the client has obviously closed the connection |
| ETIMEDOUT | connection was idle for too long |

The argument Reason takes information to the framework why the application server closes the connection:

As a return result code, we do not expect other than ‘OK’.

Interface variables The argument Reason takes information to the framework why the application server closes the connection: As a return result code, we do not expect other than ‘OK’.

## FbSocket_UdpInstanceSlot.protAttachWriteBuffer (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | protAttachWriteBuffer | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | Location of external buffer space |
| udiTxBufferSize | UDINT | Size of the external buffer |

| FbSerialInterface.AttachExternalWriteBuffer (FUN) - Interface |
| Name | Access | Type | Semantics |
| pTxBuffer | IN | POINTER TO BYTE | Location of external buffer space for receiving |
| udiTxBufferSize | IN | UDINT | Size of the external receive buffer |
| (none) | Return | eResultCode | success (=0) or error cause |

| result codes |
| 0 | success, ready for communication. |
| EINVAL | Invalid parameters (size beyond plausibility). |
| EFBIG | New buffer is too small for data which is already contained in the previous buffer. |

Attaches external Buffers to the SI-FB

This method can be applied any time, even when the FB is not attached to a serial interface.

By default, each serial FB might have a small built-in buffer which handles most standard situations but is small enough to not waste system memory. In certain situations, when high transmission rate (e.g. 115k2) is combined with large cycle times (e.g. 250ms), or when large chunks of write data are generated, it is advisable to have buffers significantly larger than standard.

This is provided by this method.

If applied while in full operation, the previously received data were copied into the new buffer, if that one is big enough. If the new buffer is not big enough, data is lost.

If NULL-pointers are appilied or the buffer sizes are smaller than the internal buffers, then the internal buffer of the FB is used and the external buffer is silently ignored.

This method returns the following result codes:

Interface variables Attaches external Buffers to the SI-FB This method can be applied any time, even when the FB is not attached to a serial interface. By default, each serial FB might have a small built-in buffer which handles most standard situations but is small enough to not waste system memory. In certain situations, when high transmission rate (e.g. 115k2) is combined with large cycle times (e.g. 250ms), or when large chunks of write data are generated, it is advisable to have buffers significantly larger than standard. This is provided by this method. If applied while in full operation, the previously received data were copied into the new buffer, if that one is big enough. If the new buffer is not big enough, data is lost. If NULL-pointers are appilied or the buffer sizes are smaller than the internal buffers, then the internal buffer of the FB is used and the external buffer is silently ignored. This method returns the following result codes:

## FbSocket_UdpInstanceSlot.protGetWritecapacity (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | protGetWritecapacity | DINT |

Asks the frame Server FB how many bytes of write data it can process at the moment.

If the frame server responds 0, you have to wait until the value increases. If it reports otherwise a too low value, you may have a problem.

Interface variables Asks the frame Server FB how many bytes of write data it can process at the moment. If the frame server responds 0, you have to wait until the value increases. If it reports otherwise a too low value, you may have a problem.

## FbSocket_UdpInstanceSlot.protWrite (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | protWrite | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | The location of the data |
| udiTxBufferSize | UDINT | Number of bytes to send |

| FbSocketServer_MethodsForApplication.Write (FUN) - Interface |
| Name | Access | Type | Semantics |
| pTxBuffer | IN | POINTER TO BYTE | The location of the data |
| udiTxBufferSize | IN | UDINT | Number of bytes to send |
| (none) | Return | eResultCode | success (=0) or error cause |

| result codes |
| 0 | success, ready for new communication. |
| EBADF | socket is not open (This schould be a programming error.) |
| EBUSY | Actual data is ignored because there is previous data to be written. |
| EMSGSIZE | data chunk is too large (esp.: size limit for UDP) |
| EPIPE | the stream was closed on serverside |
| EACCES | other problem while writing data |

Writes data from the Server to the Client.

Attn: The Data in the databuffer must not be altered until we have the acknowledge that it has finally been sent.

Interface variables Writes data from the Server to the Client. Attn: The Data in the databuffer must not be altered until we have the acknowledge that it has finally been sent.

## FbTcpServer_internal.AttachServerApplication (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | AttachServerApplication | eResultCode |  |
| Input | pInstance | POINTER TO FbSocketServer_ApplicationBase | one instance of the server application fb |

| result codes |
| 0 | success |
| EMFILE | the number of server application instances exceeds its limit. (with ‘M’, not ‘N’) |
| EINVAL | Null-Pointer |
| EACCES | the initalization of the server application FB responded a failure |

Attaches a new Server FB to the Server Socket

When an instance of the server application FB is attached to the socket server FB, it can be used for an new incoming connection. Calling this server application FB will then be handled by the socket server FB, which might handle multiple server application FBs.

Note: New server application FBs may be added/attached while the socket server FB is already open.

Interface variables Attaches a new Server FB to the Server Socket When an instance of the server application FB is attached to the socket server FB, it can be used for an new incoming connection. Calling this server application FB will then be handled by the socket server FB, which might handle multiple server application FBs. Note: New server application FBs may be added/attached while the socket server FB is already open.

## FbTcpServer_internal.Close (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | Close | eResultCode |

| result codes |
| 0 | success |
| EBADF | The socket FB was not open |
| EACCES | Unexpected problems at closing the linstening socket |

Closes the Server socket and closes all attached server FBs

Interface variables Closes the Server socket and closes all attached server FBs

## FbTcpServer_internal.ConfigureKeepAliveTransmission (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ConfigureKeepAliveTransmission | eResultCode |  |
| Input | xEnable | BOOL | Switch keepalive mechanism on |
| tMaxIdleTime | TIME | Maximum time of inactivity before first keep-alive packet is sent. |
| tInterval | TIME | Interval between two successive KA-Packets if no reply is received |
| udiProbes | UDINT | Number of KA transmissions before declaring the connection ‘dead’ |
| xApplyToAll | BOOL | on TRUE: apply Keepalive also to existing connections |

| result codes |
| 0 | Success, ready for communication. |
| EINVAL | Invalid Parameters |
| ENOSYS | This Feature is not supported by the target |

This method configures the autonomous sending of keep alive (‘KA’) packets.

When the keep-alive (KA) feature is turned on, the client socket checks periodically if the server is still reachable by sending empty packets and expecting acknowledge packets.

The purpose of this is to ensure for the client that the server is still reachable.

Thus, after a maximum idle time after complete inactivity (no transmission nor reception of any packets), a special keep-alive-packet is sent (which contains no data, but is acknowledged by TCP). Unless that KA-packet is acknowledged, it is retransmitted after a given interval .

When the prefifined number of probes is exceeded without acknowledgement, the connection is considered to be broken and the socket status is set to ETIMEDOUT.

Nevertheless, more packets could be tried to be sent in spite of that situation (as the socket is still open) and whith the first sign of life from the peer the connection will be considered ‘alive’ again.

The input udiProbes is interpreted as follows: 0=give up without KA-Packet, 1=give up after ‘Interval’ is elapsed after first KA-packet.

This configuration has to be done only once per inctance, as it will persist after opening or closing the FB.

Note: This feature is controversially disputed (see RFC 1122) and not useful in every situation.

Interface variables This method configures the autonomous sending of keep alive (‘KA’) packets. When the keep-alive (KA) feature is turned on, the client socket checks periodically if the server is still reachable by sending empty packets and expecting acknowledge packets. The purpose of this is to ensure for the client that the server is still reachable. Thus, after a maximum idle time after complete inactivity (no transmission nor reception of any packets), a special keep-alive-packet is sent (which contains no data, but is acknowledged by TCP). Unless that KA-packet is acknowledged, it is retransmitted after a given interval . When the prefifined number of probes is exceeded without acknowledgement, the connection is considered to be broken and the socket status is set to ETIMEDOUT. Nevertheless, more packets could be tried to be sent in spite of that situation (as the socket is still open) and whith the first sign of life from the peer the connection will be considered ‘alive’ again. The input udiProbes is interpreted as follows: 0=give up without KA-Packet, 1=give up after ‘Interval’ is elapsed after first KA-packet. This configuration has to be done only once per inctance, as it will persist after opening or closing the FB. Note: This feature is controversially disputed (see RFC 1122) and not useful in every situation.

## FbTcpServer_internal.CyclicRun (METH) ¶


## FbTcpServer_internal.OpenAndListen (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | OpenAndListen | eResultCode |  |
| Input | sAddress | IPAddressString | local address of the network plug |
| uiPort | UINT | port number of the service |
| uiBacklog | UINT | The maximum length to which the queue of pending connections may grow |
| tTimeout | TIME | tolerated inactivity |

| result codes |
| 0 | success, ready for communication. |
| EACCES | the socket could not be created by other reasons |
| EINVAL | invalid argument |
| ENFILE | The system limit on the total number of open sockets has been reached. |
| EADDRINUSE | The given address / port combination is already in use. |
| EBUSY | The socket is already bound to an address. |
| EADDRNOTAVAIL | A nonexistent interface was requested or the requested address was not local. |

Opens a Server socket and listens for incoming packets.

After this call is done, the FbServerSocket dispatches incoming data to the attached server application FBs.

sAddress defines the local network interface which is attached to this service. It can be identified either by the IP-Address, (‘192.168.8.15’), or by the device name (‘ETH0’), or by just an interface number (‘#0’). If nothing is declared, the default interface is taken.

uiPort identifies the port number under which this service should be advertised.

eType specifies, if it is a TCP-Socket, a UDP-Socket or a RAW connection.

uiBacklog specifies the maximum length to which the queue of pending connections for the socket may grow beyond the number of server instances. If a connection request arrives when all attached server instances are busy and the queue is full, the client will receive an error with an indication of ECONNREFUSED or, if the underlying protocol supports retransmission, the request may be ignored so that a later reattempt at connection succeeds.

Interface variables Opens a Server socket and listens for incoming packets. After this call is done, the FbServerSocket dispatches incoming data to the attached server application FBs. sAddress defines the local network interface which is attached to this service. It can be identified either by the IP-Address, (‘192.168.8.15’), or by the device name (‘ETH0’), or by just an interface number (‘#0’). If nothing is declared, the default interface is taken. uiPort identifies the port number under which this service should be advertised. eType specifies, if it is a TCP-Socket, a UDP-Socket or a RAW connection. uiBacklog specifies the maximum length to which the queue of pending connections for the socket may grow beyond the number of server instances. If a connection request arrives when all attached server instances are busy and the queue is full, the client will receive an error with an indication of ECONNREFUSED or, if the underlying protocol supports retransmission, the request may be ignored so that a later reattempt at connection succeeds.

## FbTcpServer_internal.finish (METH) ¶


## FbTcpServer_internal.initialize (METH) ¶


## TcpInstanceWriteBuffer.initialize (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | pSlot | POINTER TO FbSocket_TcpInstanceSlot |

## TcpInstanceWriteBuffer.protProcessData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | protProcessData | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | where the data-to-process is located |
| udiTxNBytes | UDINT | how much data to process |
| Output | udiTxNBytesTransferred | UDINT | this much data was actually processed |

| result codes |
| 0 | all data successfully processed |
| EWOULDBLOCK | not all data could be processed, but no further errors |
| others: | specific error messages |

This method is to be overwritten by a real processing routine.

For re-implementations there are two requirements:

a) the method must return OK when all data is processed and EWOULDBLOCK when not all data could be processed because of temporarily blocking of the data stream but no other error occurred. All other result codes indicate serious specific processing errors that will be passed to the caller.

Interface variables This method is to be overwritten by a real processing routine. For re-implementations there are two requirements: a) the method must return OK when all data is processed and EWOULDBLOCK when not all data could be processed because of temporarily blocking of the data stream but no other error occurred. All other result codes indicate serious specific processing errors that will be passed to the caller. 1. the number of processed data must be less or equal to the size of the passed data chunk.

## UdpInstanceWriteBuffer.CyclicService (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | CyclicService | eResultCode |

## UdpInstanceWriteBuffer.FillIn (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | FillIn | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | where the data is |
| udiTxBufferSize | UDINT | how much data |

| result codes |
| 0 | complete success |
| EINVAL | invalid call parameters (null-pointer or size>2G) |
| EBUSY | new data cannot be accepted. |
| EACCES | processing returned with EINVAL or EBUSY or FIFO is not operational |
| ENOSYS | There is no method ‘protProcessDataOut’ specified. |
| others: | specific error messages |

Tries to process an amount of data.

Interface variables Tries to process an amount of data.

## UdpInstanceWriteBuffer.availableSpace (PROP) ¶


## UdpInstanceWriteBuffer.initialize (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Input | pSlot | POINTER TO FbSocket_UdpInstanceSlot |

## UdpInstanceWriteBuffer.protProcessData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | protProcessData | eResultCode |  |
| Input | pTxBuffer | POINTER TO BYTE | where the data-to-process is located |
| udiTxBufferSize | UDINT | how much data to process |
| Output | udiTxNBytes | UDINT | this much data was actually processed |

| result codes |
| 0 | all data successfully processed |
| EWOULDBLOCK | not all data could be processed, but no further errors |
| others: | specific error messages |

This method is to be overwritten by a real processing routine.

For re-implementations there are two requirements:

a) the method must return OK when all data is processed and EWOULDBLOCK when not all data could be processed because of temporarily blocking of the data stream but no other error occurred. All other result codes indicate serious specific processing errors that will be passed to the caller.

Interface variables This method is to be overwritten by a real processing routine. For re-implementations there are two requirements: a) the method must return OK when all data is processed and EWOULDBLOCK when not all data could be processed because of temporarily blocking of the data stream but no other error occurred. All other result codes indicate serious specific processing errors that will be passed to the caller. 1. the number of processed data must be less or equal to the size of the passed data chunk.

### Program Organization


## 20 Program Organization Units


- Client-FBs FbMulticastListener_internal (FB) 10 Main Interface FbMulticastListener_internal.Close (METH) - FbMulticastListener_internal.ConfigureKeepAliveTransmission (METH) - FbMulticastListener_internal.LeaveGroup (METH) - FbMulticastListener_internal.OpenAndJoin (METH) - FbMulticastListener_internal.ReJoinGroup (METH) 20 Administration - FbMulticastListener_internal.finish (METH) - FbMulticastListener_internal.initialize (METH) FbSocketClient_internal (FB) - 10 Main FbSocketClient_internal.CheckConnection (METH) - FbSocketClient_internal.CloseConnection (METH) - FbSocketClient_internal.OpenAndConnect (METH) - FbSocketClient_internal.Read (METH) - FbSocketClient_internal.Write (METH) 20 advanced - FbSocketClient_internal.Block (METH) - FbSocketClient_internal.CalmWatchdog (METH) - FbSocketClient_internal.ConfigureKeepAliveTransmission (METH) - FbSocketClient_internal.ReadWithHeader (METH) 30 properties - FbSocketClient_internal.OpState (PROP) - FbSocketClient_internal.OwnPort (PROP) 40 administrative - FbSocketClient_internal.finish (METH) - FbSocketClient_internal.initialize (METH) Server-FBs - 90 private FbSocket_GenericConnection (FB) 01_from Application FbSocket_GenericConnection.protActiveClose (METH) - FbSocket_GenericConnection.protGetConnectionAddr (METH) - FbSocket_GenericConnection.protGetConnectionClientPort (METH) - FbSocket_GenericConnection.protGetOpState (METH) 02_for internal framework - FbSocket_GenericConnection.CalmWatchdog (METH) - FbSocket_GenericConnection.InitNewConnection (METH) - FbSocket_GenericConnection.Initialize_FbSocket_GenericConnection (METH) - FbSocket_GenericConnection.ServerClose (METH) - FbSocket_GenericConnection.getIdleTime (METH) - FbSocket_GenericConnection.initialize_only (METH) FbSocket_TcpInstanceSlot (FB) - 01_from Application FbSocket_TcpInstanceSlot.protAttachWriteBuffer (METH) - FbSocket_TcpInstanceSlot.protGetConnectionProtocol (METH) - FbSocket_TcpInstanceSlot.protGetWriteCapacity (METH) - FbSocket_TcpInstanceSlot.protWrite (METH) 02_for internal framework - FbSocket_TcpInstanceSlot.InitNewConnection (METH) - FbSocket_TcpInstanceSlot.Initialize_FbSocket_TcpInstanceSlot (METH) - FbSocket_TcpInstanceSlot.ProcessPendingWritedata (METH) - FbSocket_TcpInstanceSlot.Read (METH) FbSocket_UdpInstanceSlot (FB) - 01_from Application FbSocket_UdpInstanceSlot.protActiveClose (METH) - FbSocket_UdpInstanceSlot.protAttachWriteBuffer (METH) - FbSocket_UdpInstanceSlot.protGetWritecapacity (METH) - FbSocket_UdpInstanceSlot.protWrite (METH) 02_for internal framework - FbSocket_UdpInstanceSlot.InitNewConnection (METH) - FbSocket_UdpInstanceSlot.Initialize_FbSocket_UdpInstanceSlot (METH) - FbSocket_UdpInstanceSlot.ProcessPendingWritedata (METH) - FbSocket_UdpInstanceSlot.Read (METH) TcpInstanceWriteBuffer (FB) - TcpInstanceWriteBuffer.initialize (METH) - TcpInstanceWriteBuffer.protProcessData (METH) UdpInstanceWriteBuffer (FB) - UdpInstanceWriteBuffer.CyclicService (METH) - UdpInstanceWriteBuffer.FillIn (METH) - UdpInstanceWriteBuffer.availableSpace (PROP) - UdpInstanceWriteBuffer.initialize (METH) - UdpInstanceWriteBuffer.protProcessData (METH) FbDatagramServer_internal (FB) - 10 Main Interface FbDatagramServer_internal.AttachServerApplication (METH) - FbDatagramServer_internal.AttachSingleServerApplication (METH) - FbDatagramServer_internal.Close (METH) - FbDatagramServer_internal.OpenAndListen (METH) 20 administrative - FbDatagramServer_internal.finish (METH) - FbDatagramServer_internal.initialize (METH) 90 internal - FbDatagramServer_internal.CyclicRun (METH) - FbDatagramServer_internal.HasOpenSocket (PROP) FbTcpServer_internal (FB) - 10 Main Interface FbTcpServer_internal.AttachServerApplication (METH) - FbTcpServer_internal.Close (METH) - FbTcpServer_internal.ConfigureKeepAliveTransmission (METH) - FbTcpServer_internal.OpenAndListen (METH) 20 administrative - FbTcpServer_internal.finish (METH) - FbTcpServer_internal.initialize (METH) 90 internal - FbTcpServer_internal.CyclicRun (METH) - FbTcpServer_internal.HasOpenSocket (PROP) Singular Functions - SinglePing (FUN)

### Function Groups


## 21 Auxiliary Functions


- GetIpAddressOfInterface (FUN)

## Singular Functions ¶


### Main Interfaces


## 10 Main Interface


- FbMulticastListener_internal.Close (METH) - FbMulticastListener_internal.ConfigureKeepAliveTransmission (METH) - FbMulticastListener_internal.LeaveGroup (METH) - FbMulticastListener_internal.OpenAndJoin (METH) - FbMulticastListener_internal.ReJoinGroup (METH)

## 10 Main Interface


- FbDatagramServer_internal.AttachServerApplication (METH) - FbDatagramServer_internal.AttachSingleServerApplication (METH) - FbDatagramServer_internal.Close (METH) - FbDatagramServer_internal.OpenAndListen (METH)

## 10 Main Interface


- FbTcpServer_internal.AttachServerApplication (METH) - FbTcpServer_internal.Close (METH) - FbTcpServer_internal.ConfigureKeepAliveTransmission (METH) - FbTcpServer_internal.OpenAndListen (METH)

### Internal Components


## 02_for internal framework


- FbSocket_TcpInstanceSlot.InitNewConnection (METH) - FbSocket_TcpInstanceSlot.Initialize_FbSocket_TcpInstanceSlot (METH) - FbSocket_TcpInstanceSlot.ProcessPendingWritedata (METH) - FbSocket_TcpInstanceSlot.Read (METH)

## 02_for internal framework


- FbSocket_UdpInstanceSlot.InitNewConnection (METH) - FbSocket_UdpInstanceSlot.Initialize_FbSocket_UdpInstanceSlot (METH) - FbSocket_UdpInstanceSlot.ProcessPendingWritedata (METH) - FbSocket_UdpInstanceSlot.Read (METH)

## 02_for internal framework


- FbSocket_GenericConnection.CalmWatchdog (METH) - FbSocket_GenericConnection.InitNewConnection (METH) - FbSocket_GenericConnection.Initialize_FbSocket_GenericConnection (METH) - FbSocket_GenericConnection.ServerClose (METH) - FbSocket_GenericConnection.getIdleTime (METH) - FbSocket_GenericConnection.initialize_only (METH)

## 90 Internal


- _ApplyKeepAliveParameters (FUN) - _TransposeKeepAliveResults (FUN)

## 90 internal


- FbTcpServer_internal.CyclicRun (METH) - FbTcpServer_internal.HasOpenSocket (PROP)

## 90 internal


- FbDatagramServer_internal.CyclicRun (METH) - FbDatagramServer_internal.HasOpenSocket (PROP)

## FbDatagramServer_internal.HasOpenSocket (PROP) ¶


## FbSocketClient_internal.OpState (PROP)


Internal operational status.

Internal operational status.

## FbSocketClient_internal.OwnPort (PROP) ¶


## FbTcpServer_internal.HasOpenSocket (PROP) ¶


## WagoSysSocket_Internal_PFC Library Documentation


| Company: | WAGO |
| Title: | WagoSysSocket_Internal_PFC |
| Version: | 1.0.5.9 |
| Categories: | WAGO Internal\|Target\|PFC; WAGO Internal\|Feature\|Network\|Common; Application; WAGO LayerView\|Sys; WAGO Internal\|Target |
| Namespace: | WagoSysSocket_internal |
| Author: | WAGO / u013972 |
| Placeholder: | WagoSysSocketInternal |

### Description


This document is automatically generated.

Handling network communication on internet layer and on transport layer.

This document is automatically generated. Handling network communication on internet layer and on transport layer.

### Contents:


- 20 Program Organization Units Client-FBs - Server-FBs - Singular Functions 21 Auxiliary Functions - GetIpAddressOfInterface (FUN) 90 Internal - _ApplyKeepAliveParameters (FUN) - _TransposeKeepAliveResults (FUN) LibraryResult (GVL) ParameterList (PARAMS) ResultItems (GVL) VersionHistory (GVL)

### Indices and tables


Based on WagoSysSocket_Internal_PFC.library, last modified 20.09.2024, 21:05:25. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysSocket_Internal_PFC.library, last modified 20.09.2024, 21:05:25. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Global Variable Lists


## LibraryResult (GVL)


| Name | Type |
| --- | --- |
| Factory | FbResultFactory |

```
VAR
  eMyResult : eResultCode;  // result code whic is to be investigated
  oError    : FbResult;     // result object for use in highe levels.
END_VAR;

eMyResult := myFunction(...);
Namespace.LibraryResult.Factory.SetResult(eMyResult, oError);
```

Factory for standard result objects

Use this to translate result codes from this library into standard result objects.

where ‘Namespace’ denotes the namespace which is used for including the specific library and ‘myFunction()’ is an example for a general function from this library.

Factory for standard result objects Use this to translate result codes from this library into standard result objects. Usage: where ‘Namespace’ denotes the namespace which is used for including the specific library and ‘myFunction()’ is an example for a general function from this library.

## ResultItems (GVL)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Constant | ERROR | ARRAY [0..30] OF typResultItem | [STRUCT(ID := OK, Severity := eSeverity.none, Text := ‘OK’), STRUCT(ID := EAGAIN, Severity := eSeverity.info, Text := ‘No response from server received yet. (That may take a while.).’), STRUCT(ID := EINPROGRESS, Severity := eSeverity.info, Text := ‘Success, data transfer or other activity is pending or expected soon.’), STRUCT(ID := EWOULDBLOCK, Severity := eSeverity.info, Text := ‘The Connection is not yet established. Configuring is deferred.’), STRUCT(ID := ENODATA, Severity := eSeverity.info, Text := ‘No data is available (not an error).’), STRUCT(ID := ETIMEDOUT, Severity := eSeverity.info, Text := ‘Connetion was idle for too long or Ping required too much time.’), STRUCT(ID := EINVAL, Severity := eSeverity.error, Text := ‘Invalid arument or unknown protocol or malformed address.’), STRUCT(ID := ENFILE, Severity := eSeverity.error, Text := ‘The system limit on the total number of open sockets has been reached.’), STRUCT(ID := EMFILE, Severity := eSeverity.error, Text := ‘The number of server application instances exceeds its limit.’), STRUCT(ID := EPROTONOSUPPORT, Severity := eSeverity.error, Text := ‘The desired protocol is not supported.’), STRUCT(ID := ENOPROTOOPT, Severity := eSeverity.error, Text := ‘Protocol option “sOwnInterface” or “RawSocket” not applicable.’), STRUCT(ID := EPROTOTYPE, Severity := eSeverity.error, Text := ‘The given protocol type (eProto) is not supported. (RAW and UDP only)’), STRUCT(ID := ECONNREFUSED, Severity := eSeverity.error, Text := ‘On remote address the connection was refused or no-one listens.’), STRUCT(ID := ENETUNREACH, Severity := eSeverity.error, Text := ‘Target network or address is unreachable.’), STRUCT(ID := ETIME, Severity := eSeverity.error, Text := ‘Timeout while attempting connection.’), STRUCT(ID := EBADF, Severity := eSeverity.error, Text := ‘Socket is not open.’), STRUCT(ID := EBUSY, Severity := eSeverity.error, Text := ‘Resource conlict, FB already bound to an address or otherwise busy.’), STRUCT(ID := EMSGSIZE, Severity := eSeverity.error, Text := ‘Data chunk is too large (esp.: size limit for UDP).’), STRUCT(ID := EPIPE, Severity := eSeverity.error, Text := ‘The stream was closed on server side.’), STRUCT(ID := EADDRINUSE, Severity := eSeverity.error, Text := ‘The given address / port combination is already in use.’), STRUCT(ID := EADDRNOTAVAIL, Severity := eSeverity.error, Text := ‘A nonexistent interface or nonlocal address was requested.’), STRUCT(ID := EFBIG, Severity := eSeverity.error, Text := ‘The already contained data is too big for new buffer size.’), STRUCT(ID := EFAULT, Severity := eSeverity.error, Text := ‘Bad address or bad reference to parameters or values.’), STRUCT(ID := ECONNREFUSED, Severity := eSeverity.error, Text := ‘On remote address the connection was refused or no-one listens.’), STRUCT(ID := ECONNABORTED, Severity := eSeverity.error, Text := ‘A special error condition causes the connection to terminate.’), STRUCT(ID := ENOSYS, Severity := eSeverity.error, Text := ‘This feature is not supported by the target.’), STRUCT(ID := EACCES, Severity := eSeverity.error, Text := ‘General problem with processing he socket.’), STRUCT(ID := EIO, Severity := eSeverity.error, Text := ‘Unspecified internal errors from OS layer.’), STRUCT(ID := ENOENT, Severity := eSeverity.error, Text := ‘the device/interface name is unknown.’), STRUCT(ID := EOVERFLOW, Severity := eSeverity.error, Text := ‘the given buffer space was too small for the result.’), STRUCT(ID := EBADRQC, Severity := eSeverity.error, Text := ‘invalid request code: use of wildcards is not supported.’)] |

Standard result items specific for this library

Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library Note: This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| date | version | author | change |
| 11.07.2024 | 1.0.5.9 | WAGO / u0103719 | update library version (context: build server,compile file) |
| 24.10.2023 | 1.0.5.8 | WAGO / u010663 | 64-Bit adjustment ->SysTypes2Interfaces |
| 14.03.2023 | 1.0.5.7 | WAGO / u010663 | Remove license info |
| 31.01.2023 | 1.0.5.6 | WAGO / u013972 | Fix problems in simulation |
| 15.04.2022 | 1.0.5.5 | WAGO / u013972 | Fix double close of udp sockets |
| 03.02.2022 | 1.0.5.4 | WAGO / u010663 | New parameter TCP_USER_TIMEOUT |
| 15.04.2021 | 1.0.5.3 | WAGO / u016760 | Revert to blocking |
| 08.01.2019 | 1.0.5.1 | u015842 | Properties: copyright added |
| 02.07.2018 | 1.0.5.0 | WAGO / u013972 | For FbSocketClient_internal() the source port can be set |
| 18.04.2018 | 1.0.4.4 | WAGO / u013972 | Resolve documentation errors |
| 01.02.2018 | 1.0.4.3 | WAGO / u013972 | Change SysSocket.SysSockConnect() against SysSocket23.SysSockConnect() in FbSocketClient_internal.OpenAndConnect() |
| 11.04.2016 | 1.0.4.2 | WAGO / u013972 | Set flag SOCKET_MSG_DONTWAIT |
| 11.04.2016 | 1.0.4.1 | WAGO / u013972 | FbSocketClient_internal.OpenAndConnect() use a default port |
| 04.03.2016 | 1.0.3.0 | WAGO / u013972 | Replace WagoAppErrorBase with WagoSysErrorBase and WagoTypesErrorBase |
| 29.09.2015 | 1.0.2.0 | u013972 | Workaround for C0351-Bug, Resolve libraries with placeholders |
| 06.03.2015 | 1.0.0.0 | RE | Release Version |

WagoSysSocket_Internal_PFC

WagoSysSocket_Internal_PFC

### Other Components


## 01_from Application


- FbSocket_GenericConnection.protActiveClose (METH) - FbSocket_GenericConnection.protGetConnectionAddr (METH) - FbSocket_GenericConnection.protGetConnectionClientPort (METH) - FbSocket_GenericConnection.protGetOpState (METH)

## 01_from Application


- FbSocket_TcpInstanceSlot.protAttachWriteBuffer (METH) - FbSocket_TcpInstanceSlot.protGetConnectionProtocol (METH) - FbSocket_TcpInstanceSlot.protGetWriteCapacity (METH) - FbSocket_TcpInstanceSlot.protWrite (METH)

## 01_from Application


- FbSocket_UdpInstanceSlot.protActiveClose (METH) - FbSocket_UdpInstanceSlot.protAttachWriteBuffer (METH) - FbSocket_UdpInstanceSlot.protGetWritecapacity (METH) - FbSocket_UdpInstanceSlot.protWrite (METH)

## 10 Main


- FbSocketClient_internal.CheckConnection (METH) - FbSocketClient_internal.CloseConnection (METH) - FbSocketClient_internal.OpenAndConnect (METH) - FbSocketClient_internal.Read (METH) - FbSocketClient_internal.Write (METH)

## 20 Administration


- FbMulticastListener_internal.finish (METH) - FbMulticastListener_internal.initialize (METH)

## 20 administrative


- FbDatagramServer_internal.finish (METH) - FbDatagramServer_internal.initialize (METH)

## 20 administrative


- FbTcpServer_internal.finish (METH) - FbTcpServer_internal.initialize (METH)

## 20 advanced


- FbSocketClient_internal.Block (METH) - FbSocketClient_internal.CalmWatchdog (METH) - FbSocketClient_internal.ConfigureKeepAliveTransmission (METH) - FbSocketClient_internal.ReadWithHeader (METH)

## 30 properties


- FbSocketClient_internal.OpState (PROP) - FbSocketClient_internal.OwnPort (PROP)

## 40 administrative


- FbSocketClient_internal.finish (METH) - FbSocketClient_internal.initialize (METH)

## 90 private


These FBs are used for implementation only. They are in no case meant as public interface for the library

These FBs are used for implementation only. They are in no case meant as public interface for the library - FbSocket_GenericConnection (FB) 01_from Application FbSocket_GenericConnection.protActiveClose (METH) - FbSocket_GenericConnection.protGetConnectionAddr (METH) - FbSocket_GenericConnection.protGetConnectionClientPort (METH) - FbSocket_GenericConnection.protGetOpState (METH) 02_for internal framework - FbSocket_GenericConnection.CalmWatchdog (METH) - FbSocket_GenericConnection.InitNewConnection (METH) - FbSocket_GenericConnection.Initialize_FbSocket_GenericConnection (METH) - FbSocket_GenericConnection.ServerClose (METH) - FbSocket_GenericConnection.getIdleTime (METH) - FbSocket_GenericConnection.initialize_only (METH) FbSocket_TcpInstanceSlot (FB) - 01_from Application FbSocket_TcpInstanceSlot.protAttachWriteBuffer (METH) - FbSocket_TcpInstanceSlot.protGetConnectionProtocol (METH) - FbSocket_TcpInstanceSlot.protGetWriteCapacity (METH) - FbSocket_TcpInstanceSlot.protWrite (METH) 02_for internal framework - FbSocket_TcpInstanceSlot.InitNewConnection (METH) - FbSocket_TcpInstanceSlot.Initialize_FbSocket_TcpInstanceSlot (METH) - FbSocket_TcpInstanceSlot.ProcessPendingWritedata (METH) - FbSocket_TcpInstanceSlot.Read (METH) FbSocket_UdpInstanceSlot (FB) - 01_from Application FbSocket_UdpInstanceSlot.protActiveClose (METH) - FbSocket_UdpInstanceSlot.protAttachWriteBuffer (METH) - FbSocket_UdpInstanceSlot.protGetWritecapacity (METH) - FbSocket_UdpInstanceSlot.protWrite (METH) 02_for internal framework - FbSocket_UdpInstanceSlot.InitNewConnection (METH) - FbSocket_UdpInstanceSlot.Initialize_FbSocket_UdpInstanceSlot (METH) - FbSocket_UdpInstanceSlot.ProcessPendingWritedata (METH) - FbSocket_UdpInstanceSlot.Read (METH) TcpInstanceWriteBuffer (FB) - TcpInstanceWriteBuffer.initialize (METH) - TcpInstanceWriteBuffer.protProcessData (METH) UdpInstanceWriteBuffer (FB) - UdpInstanceWriteBuffer.CyclicService (METH) - UdpInstanceWriteBuffer.FillIn (METH) - UdpInstanceWriteBuffer.availableSpace (PROP) - UdpInstanceWriteBuffer.initialize (METH) - UdpInstanceWriteBuffer.protProcessData (METH)

## Client-FBs


- FbMulticastListener_internal (FB) 10 Main Interface FbMulticastListener_internal.Close (METH) - FbMulticastListener_internal.ConfigureKeepAliveTransmission (METH) - FbMulticastListener_internal.LeaveGroup (METH) - FbMulticastListener_internal.OpenAndJoin (METH) - FbMulticastListener_internal.ReJoinGroup (METH) 20 Administration - FbMulticastListener_internal.finish (METH) - FbMulticastListener_internal.initialize (METH) FbSocketClient_internal (FB) - 10 Main FbSocketClient_internal.CheckConnection (METH) - FbSocketClient_internal.CloseConnection (METH) - FbSocketClient_internal.OpenAndConnect (METH) - FbSocketClient_internal.Read (METH) - FbSocketClient_internal.Write (METH) 20 advanced - FbSocketClient_internal.Block (METH) - FbSocketClient_internal.CalmWatchdog (METH) - FbSocketClient_internal.ConfigureKeepAliveTransmission (METH) - FbSocketClient_internal.ReadWithHeader (METH) 30 properties - FbSocketClient_internal.OpState (PROP) - FbSocketClient_internal.OwnPort (PROP) 40 administrative - FbSocketClient_internal.finish (METH) - FbSocketClient_internal.initialize (METH)

## ParameterList (PARAMS)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | cuiNInstanceListSize | UINT | 20 | This many instances a server can serve simultaneously |
| TCP_USER_TIMEOUT | DINT | 10000 | 10s |

## Server-FBs


- 90 private FbSocket_GenericConnection (FB) 01_from Application FbSocket_GenericConnection.protActiveClose (METH) - FbSocket_GenericConnection.protGetConnectionAddr (METH) - FbSocket_GenericConnection.protGetConnectionClientPort (METH) - FbSocket_GenericConnection.protGetOpState (METH) 02_for internal framework - FbSocket_GenericConnection.CalmWatchdog (METH) - FbSocket_GenericConnection.InitNewConnection (METH) - FbSocket_GenericConnection.Initialize_FbSocket_GenericConnection (METH) - FbSocket_GenericConnection.ServerClose (METH) - FbSocket_GenericConnection.getIdleTime (METH) - FbSocket_GenericConnection.initialize_only (METH) FbSocket_TcpInstanceSlot (FB) - 01_from Application FbSocket_TcpInstanceSlot.protAttachWriteBuffer (METH) - FbSocket_TcpInstanceSlot.protGetConnectionProtocol (METH) - FbSocket_TcpInstanceSlot.protGetWriteCapacity (METH) - FbSocket_TcpInstanceSlot.protWrite (METH) 02_for internal framework - FbSocket_TcpInstanceSlot.InitNewConnection (METH) - FbSocket_TcpInstanceSlot.Initialize_FbSocket_TcpInstanceSlot (METH) - FbSocket_TcpInstanceSlot.ProcessPendingWritedata (METH) - FbSocket_TcpInstanceSlot.Read (METH) FbSocket_UdpInstanceSlot (FB) - 01_from Application FbSocket_UdpInstanceSlot.protActiveClose (METH) - FbSocket_UdpInstanceSlot.protAttachWriteBuffer (METH) - FbSocket_UdpInstanceSlot.protGetWritecapacity (METH) - FbSocket_UdpInstanceSlot.protWrite (METH) 02_for internal framework - FbSocket_UdpInstanceSlot.InitNewConnection (METH) - FbSocket_UdpInstanceSlot.Initialize_FbSocket_UdpInstanceSlot (METH) - FbSocket_UdpInstanceSlot.ProcessPendingWritedata (METH) - FbSocket_UdpInstanceSlot.Read (METH) TcpInstanceWriteBuffer (FB) - TcpInstanceWriteBuffer.initialize (METH) - TcpInstanceWriteBuffer.protProcessData (METH) UdpInstanceWriteBuffer (FB) - UdpInstanceWriteBuffer.CyclicService (METH) - UdpInstanceWriteBuffer.FillIn (METH) - UdpInstanceWriteBuffer.availableSpace (PROP) - UdpInstanceWriteBuffer.initialize (METH) - UdpInstanceWriteBuffer.protProcessData (METH) FbDatagramServer_internal (FB) - 10 Main Interface FbDatagramServer_internal.AttachServerApplication (METH) - FbDatagramServer_internal.AttachSingleServerApplication (METH) - FbDatagramServer_internal.Close (METH) - FbDatagramServer_internal.OpenAndListen (METH) 20 administrative - FbDatagramServer_internal.finish (METH) - FbDatagramServer_internal.initialize (METH) 90 internal - FbDatagramServer_internal.CyclicRun (METH) - FbDatagramServer_internal.HasOpenSocket (PROP) FbTcpServer_internal (FB) - 10 Main Interface FbTcpServer_internal.AttachServerApplication (METH) - FbTcpServer_internal.Close (METH) - FbTcpServer_internal.ConfigureKeepAliveTransmission (METH) - FbTcpServer_internal.OpenAndListen (METH) 20 administrative - FbTcpServer_internal.finish (METH) - FbTcpServer_internal.initialize (METH) 90 internal - FbTcpServer_internal.CyclicRun (METH) - FbTcpServer_internal.HasOpenSocket (PROP)