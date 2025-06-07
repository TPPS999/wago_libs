# WagoAppSocket v1.7.9.3

## Overview
WAGO PLC library providing WagoAppSocket functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbUdpTransmitterExt
This is a UDP-Transmitter with *cpt*-type interface. In contrast to the FbUDPTransmitter, the transmission port can also be defined for this function block.

**Description:**
This FB sends UDP packets to a UDP-Receiver. The address and port number of the target are given by the inputs ``sServername`` and ``wPort``. The port number of the transmission port on the local device is given by the input ``wOwnPort``. The location and size of the packet contents are given by ``udiTxNBytes`` and ``pTxData``. The rising slope of ``xTxTrigger`` initiates the sending process.

### FbWakeOnLAN
This function block transmits a Wake On LAN command

### FbBroadcastReceiver
This is a Broadcast and Multicast-Receiver with *cpt*-type interface.

**Description:**
After the input ``xOpen`` is set ``TRUE``, this FB listens for incoming UDP packet at ``sNetName`` on the given port ``wPort``. While ``xOpen`` stays ``TRUE``, any changes of the NetName or the port number are ignored until ``xOpen`` returns to ``FALSE`` again. When a packet is received, the output ``xPacketReceived`` will be set for one cycle and the contents of the packet will be transferred to the memory location which is declared by ``pRxBuffer`` and ``udiRxBufferSize``. The output ``udiRxNBytes`` indicates the number of bytes in that packet. This number should be less than ``udiRxBufferSize``. It could also be 0 for empty packets. Previous data will be overwritten in the receive buffer. If overwriting is not wanted, the application could either hold ``xRxEnable`` at ``FALSE``, which prevents the FB from fetching new data, while still keeping it listening. Alternatively, ``pRxBuffer`` could be set to a different location after the previous data were received, so the new data will be written to a different location. If the received packet is larger than the declared buffer space, ``udiRxNBytes`` still reflects the size of the received packet, but it is ensured that no more data is written to the buffer as indicated by ``udiRxBufferSize``. Excess data will be lost. This situation is indicated by ``xRxOverflow``. The outputs ``sClientIP`` and ``wClientPort`` indicate the identity of the client. These could be used as address information if answers to the received packets are to be sent.

### FbBroadcaster
This is a FB for broadcasting and multicast messages with *cpt*-type interface.

**Description:**
This FB sends UDP packets to a broadcast address. The net address and port number of the target are given by the inputs ``sNetname`` and ``wPort``. The location and size of the packet contents are given by ``udiTxNBytes`` and ``pTxData``. The rising slope of ``xTxTrigger`` initiates the sending process.

### FbUdpTransmitter
This is a UDP-Transmitter with *cpt*-type interface.

**Description:**
This FB sends UDP packets to a UDP-Receiver. The address and port number of the target are given by the inputs ``sServername`` and ``wPort``. The location and size of the packet contents are given by ``udiTxNBytes`` and ``pTxData``. The rising slope of ``xTxTrigger`` initiates the sending process.

### FbUdpReceiver
This is a UDP-Receiver with *cpt*-type interface.

**Description:**
After the input ``xOpen`` is set ``TRUE``, this FB listens for incoming UDP packet on the given port ``wPort``. While ``xOpen`` stays ``TRUE``, any changes of the port number are ignored until ``xOpen`` returns to ``FALSE`` again. When a packet is received, the output ``xPacketReceived`` will be set for one cycle and the contents of the packet will be transferred to the memory location which is declared by ``pRxBuffer`` and ``udiRxBufferSize``. The output ``udiRxNBytes`` indicates the number of bytes in that packet. This number should be less than ``udiRxBufferSize``. It could also be 0 for empty packets. Previous data will be overwritten in the receive buffer. If overwriting is not wanted, the application could either hold ``xRxEnable`` at ``FALSE``, which prevents the FB from fetching new data, while still keeping it listening. Alternatively, ``pRxBuffer`` could be set to a different location after the previous data were received, so the new data will be written to a different location. If the received packet is larger than the declared buffer space, ``udiRxNBytes`` still reflects the size of the received packet, but it is ensured that no more data is written to the buffer as indicated by ``udiRxBufferSize``. Excess data will be lost. This situation is indicated by ``xRxOverflow``. The outputs ``sClientIP`` and ``wClientPort`` indicate the identity of the client. These could be used as address information if answers to the received packets are to be sent. N.B.: This udp receiver has no sending functionality. It is intended to be used in combination with :ref:`FbUdpTransmitter`. If sending is required, both parts could be composed into higher-level blocks, as it is already done in :ref:`FbUdpStreamClient`, :ref:`FbUdpPacketClient`, or :ref:`FbUdpPacketServer`.

### FbUdpPacketServer
This is a UDP-Server with *cpt*-type interface.

**Description:**
This FB listens to incoming UDP packets at the given port ``wPort`` and provides means for sending back answers to the originator of the packet. After the input ``xOpen`` is set ``TRUE``, this FB listens for incoming UDP packets on the given port ``wPort``. While ``xOpen`` stays ``TRUE``, any changes of the port number are ignored until ``xOpen`` returns to FALSE again. *Receiver:* The FB is able to receive one packet per cycle. The packet contents will be transferred to the memory location which is given by ``pRxBuffer`` and ``udiRxBufferSize``. These values may vary from cycle to cycle. The output ``xPacketReceived`` indicates the presence of an incoming packet for the duration of one cycle. (If it is ``TRUE`` for two cycles, e.g., two packets were received.) ``udiRxNBytes`` reflects the size of the packet. Previous data in the receive buffer will be overwritten. If overwriting is not wanted, the application could either hold ``xRxEnable`` at ``FALSE``, which prevents the FB from fetching new data, while still keeping it listening. Alternatively, ``pRxBuffer`` could be set to a different location after the previous data were received, so the new data will be written to a different location. If the received packet is larger than the declared buffer space, ``udiRxNBytes`` still reflects the size of the received packet, but it is ensured that no more data is written to the buffer as indicated by ``udiRxBufferSize``. Excess data will be lost. This situation is indicated by ``xRxOverflow``. The outputs ``sClientIP`` and ``wClientPort`` indicate the identity of the client. *Transmitter:* As soon as a UDP packet has been recieved, it is possible to send one or more reply packets to the originator of the incoming packet. This part of the FB is according to the behaviour model :ref:`WagoTrigger <FbBehaviourModel_Socket_Trigger>` and behaves similar to the :ref:`FbUdpTransmitter` - with the difference that we need no explicite coordinates for the destination of the transmission, because this information is already provided by the incoming request packet. ``pTxData`` and ``udiTxNBytes`` define the location and size of the packet to transmit. By applying a rising slope to ``xTxTrigger``, the transmission is started. When the FB has finished transmitting, it indicates this by resetting ``xTxTrigger`` again.

### FbUdpStreamClient
This is a UDP-client with *cpt*-type interface for STREAM context.

**Description:**
This FB acts as stream-oriented client for UDP-connections. Reading and writing to the FB follow the pattern of :ref:`WagoAppCommunicator <FbBehaviourModel_WagoAppCommunicator>`, while its function scope is based on the FB :ref:`FbSocketClient` which are both described in other places in this library. This FB is composed of three separated sub-modules: Channel: Controls the opening and closing of an associated communication channel. Transmitter (``Tx``): Controls the transmission of data. The Transmitter part is only active while the *Channel*-Part is an open state. Otherwise the transmitter is not called. Receiver (``Rx``): Receives spontaneously incoming data and presents it to the application. Like the *transmitter*, it is called only as long as the *channel* is open. *Channel:* The communication channel is opened by assigning the target address and the target port to the inputs ``sServerName`` and ``wPort``. and then setting ``xOpen`` to ``TRUE``. On the rising edge of the input ``xOpen`` the channel is opened. Unless an error occurs, the channel stays open while ``xOpen`` is kept ``TRUE``. This status is indicated by the output ``xIsOpen``, which is ``TRUE`` while the channel is operative. When ``xOpen`` returns to ``FALSE``, the channel is closed again after pending communication is finished. *Transmitter:* For transmitting data, the input ``pTxBuffer`` is to be set to the address of the data block and the input ``udiTxNBytes`` has to carry the size of the data block. Setting ``xTxTrigger`` to ``TRUE`` initiates the transmission of the data. By setting ``xTxTrigger`` to ``FALSE`` again the transmitter indicates the completion of the transmitting process. .. note :: The application MUST NOT reset ``xTxTrigger`` to ``FALSE``, because in that case the FB itself has no means to signal the completion of the process. .. note:: In this context 'completion' does not mean that the data has actually been sent physically. Instead, it indicates that the data is delivered out of the FB and new data may now be processed. *Receiver:* The inputs ``pRxBuffer`` and ``udiRxBufferSize`` have to be fed with the location and the size of raw buffer space for received data. (E.g.: :: pRxBuffer:

### FbUdpPacketClient
This is a UDP-client with *cpt*-type interface.

**Description:**
This FB is used to send UDP packets to a server and pass corresponding response packets to the application. It behaves like :ref:`FbUdpTransmitter`, from which it is derived and extended by a receiver unit. *Transmitter:* At the rising slope if ``xTxTrigger`` the UDP packet is sent. Like in in WagoSimpleUdpTransmitter, destination address and destination port are given by ``sServerName`` and ``wPort``, while the packet content is defined by ``udiTxNBytes`` and ``pTxBuffer`` rsp. *xBusy* is kept TRUE while the transmission process is still not completed. After sending is completed, the FB re-sets ``xBusy`` and ``xTxTrigger`` back to FALSE. *Receiver:* After the first transmission is performed this FB listens to packets coming from the addressed server at the given port number. The output ``xListeningForResponse`` indicates the point in time when the FB starts and keeps listening to packets. The FB is able to receive one packet per cycle. The packet contents will be transferred to the memory location which is given by *pRxBuffer* and ``udiRxBufferSize``. These values may vary from cycle to cycle. The output ``xPacketReceived`` indicates the presence of an incoming packet for the duration of one cycle. (If it is TRUE for two cycles, two packets were received.) ``udiRxNBytes`` reflects the size of the packet. If the received packet is larger than the declared buffer space, ``udiRxPacketSize`` still reflects the size of the received packet, but it is ensured that no more data is written to the buffer as indicated by ``udiRxBufferSize``. Excess data will be lost. This situation is indicated by ``xRxOverflow``. The output ``udiRxPacketCounter`` counts how many packets were received since the last transmission. If a new packet is received, previous data will be overwritten in the receive buffer. If overwriting is not wanted, the application could either hold ``xRxEnable`` FALSE, which prevents the FB from fetching new data, while still keeping it listening. Alternatively, ``pRxBuffer`` could be set to a different location after the previous data were received, so the new data will be written to a different location.

### FbBehaviourModel_Socket_Trigger
This is the base class for behaviour model WagoAppTrigger with Specifica for 'Socket'.

**Description:**
This base model is completely identical to 'WagoAppTrigger' with the only difference that the trigger variable is named slightly differently here.

### FbBehaviourModel_Socket_ChannelledTrigger
### FbTcpServerMulticonnect
This is a *cpt*-version of a TCP-multi-connect server.

**Description:**
This server FB is capable of maintaining connections to multiple clients simultaneously and passing the requests to one single acceptor. *Overview:* This FB inherits all functionality from :ref:`FbTcpServer_Multiconnect_base` and provides its complete set of functionality for handling multiple connections. Additionaly it implements a public variable interface which is similar to :ref:`FbBehaviourmodel_WagoAppChannel`. Like its parent :ref:`FbTcpServer_Multiconnect_base`, this server FB does not represent its multiple connections by multiple instances of ``FbSocketServer_ApplicationBase``, (as done with the :ref:`FbTcpServer`), but instead just one single instance of the child object is required - which itself is an extension of :ref:`FbSocketServer_ApplicationBase`: :: FUNCTION_BLOCK MyModbusServer EXTENDS FbTcpServer_Multiconnect_base METHOD NotifyReceivedData(pData,udiDataSize,pHeader): eResultCode // // In thes method the child object represents most of the specific reaction to client data // *General:* Via the overloaded method :ref:`NotifyReceivedData() <FbSocketServer_ApplicationBase.NotifyReceivedData>` the child server will be notified about data beeing sent to it. If it turns out that for a processing step more data is required which is expected to arrive in following packets, the data which is received so far can be postponed via the method :ref:`protUnread`<FbTcpServer_Multiconnect_base.protUnread>`. When the same client sends more data, the postponed data is merged with the new data and presented together as 'new data' in the expectation that we have now sufficient data for a processing step. If not, this merged new data can again be postponed until even more data arrives from the client. The methods from the base :ref:`FbSocketServer_ApplicationBase` (e.g. ``protWrite()``) apply to the client which is the originator of the actual data. Thus, no handling of the identity of the client is necessary if a respone packet is to be sent from within the method ``NotifyReceivedData()``. If - in contrast to the beforesaid without a preceeding request - a packet is to be sent sponaneously to a specific client, the method ``protSelectClient()`` has to be called before in order to tell the FB where to send the unrequested packet. Attention (1): the ``protUnread()`` mechanism requires a certain amount of internal buffer, which is allocated statically when the FB is opened. The total size of the buffer memory is defined via the constant ``udiMultiConnect_UnreadBufferSize`` from the ``ParameterList``. Attention (2): In order to avoid deadlocks, received packets are only then processed if the FB is capable to buffer one response packet. If too much internal buffer is occupied, further processing is postponed until the transmitter buffers are empty again. *Usage:* For using a multiconnect server within an application, from this base class an application specific child is derived. :: FUNCTION_BLOCK MyMulticonnectServer EXTENDS FbTcpServer_Multiconnect_cpt SUPER^(); Attention (3): The child FB MUST call ``SUPER^();`` in its body. Attention (4): Unlike in non-graphical server classes, the two query methods ``QueryReadyForReceiveData()`` and ``QueryReceiveBufferLocation()`` MUST NOT be implemented by the user, because the information provided by these methods is already provided by input variables and thus the queries are decleared FINAL internally (and are hidden.) The application specific functionality of the child FB is represented in the overloaded *Notify*-methods. In the simplest case, just *NotifyReceivedData()* is to be implemented: :: METHOD NotifyReceivedData : eResultCode VAR_INPUT pData : POINTER TO BYTE; // Points to the received data udiDataSize : UDINT; // Number of data in this chunk pHeader : POINTER TO BYTE; // (will be ignored) END_VAR sResponseString :

**Methods:**

#### protInitializeResultFactory
This method initializes the result factory.

Use this in derived FBs for initializing the inherited structure: :: METHOD FB_Init : BOOL initialize(); METHOD initialize : // own initialization SUPER^.initialize();

#### protOnClose
This method performs final actions on closing.

This method is meant to be re-implemented by the child FB if the child requires special actions on closing the server. If such a functionality is not needed, this method may be left unimplemented. Although this method delivers an error code for formal reasons, it is not supposed to produce anything else than OK. Currently, the error code is silently ignored.

#### protOnOpen
This method is called before opening - e.g. for fetching interface variables.

This method is meant to be re-implemented by the child FB if the child requires special actions on opening the server. If such a functionality is not needed, this method may be left unimplemented. If this method returns an error code other than ``OK``, opening fails.

#### NotifyClose
This method notifies that a connection is closed.

This method notifies the application that the client or the framework has closed the connection. It is supposed to return '0'. No other result codes are specified yet. *Please note:* In a contextual sense this method is a PROTECTED one, because it is intended for exclusive use from the framework and it is intended to be overwritten by the child class if this functionality is needed. In contrast to the semantics, this method had to be declared PUBLIC for technical reasons, because of the calling structure of the underlying framework. Nevertheless: it

#### NotifyNewConnection
This method notifies that a new connection was accepted.

This method is called from the framework when a new connection is accepted by this host. This method is supposed to respond with standardized result codes.

### FbTcpServerSingleConnect
This is a TCP-server with *cpt*-type interface.

**Description:**
This server FB handles incoming connections in a sequential manner. It listens to incoming connections after ``xOpen`` is set to ``TRUE``. The port number ``wPort`` has to be set up before or simultaneously with opening; subsequent changes while ``xOpen`` is ``TRUE`` have no effect. After a client has established a connection the ``xConnected``-output of the server-FB is set to ``TRUE``. The outputs ``sClient`` and ``wClientPort`` then represent the identity of the connected client. The data stream from the client is passed to the application via the the receiver part of the FB (``pRxBuffer``, ``udiBufferSize``, ``udiRxIndex``). Via the transmitter part (``xTxTrigger``, ``pTxBuffer``, ``udiTxNBytes``), data is sent from the application back to the client. Both parts behave according to the specifications of the ``Wago-Communicator`` scheme. The input ``xDisconnect`` provides a means for the application to disconnect the connection from server side. This process may be a regular part of the protocol (e.g. HTTP), but it may also be used to deny the service if the client is unwanted or behaves in a unwanted manner. A ``TRUE`` level causes the actual connection to be disconnected. .. note:: If this input is held ``TRUE`` permanently, all incoming connections were disconnected immediately.

**Status Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for new communication. EMSGSIZE Incoming data chunk was larger than allowed. ============= ====================================================================================== |

### FbTcpServer_Multiconnect_base
This is the base class for a TCP-Server which can handle multiple connections.

**Description:**
This server is able to maintain connections with several clients simultaneously. In contrast to the general FbTcpServer this is not represented by several instances of FbSocketServer_ApplicationBase but the several connections are handled via a single child of this FB: :: FUNCTION_BLOCK MyModbusServer EXTENDS FbTcpServer_Multiconnect_base METHOD NotifyReceivedData(pData,udiDataSize,pHeader): eResultCode // // In this method the child object implements the reaction to client data. // Via ``NotifyReceivedData()`` the child server is notified about received data. If it turns out that for a processing step more data is required which is expected to come in in following packets, the data which is received so far can be postponed via the method ``protUnread()``. When the same client sends more data, the postponed data is merged with the new data and presented together as 'new data' in the expectation that we have now sufficient data for a processing step. If not, this merged new data can again be postponed until even more data arrives from the client. The methods from the base ``FbSocketServer_ApplicationBase`` (e.g. ``protWrite()``) apply to that client which is the originator of the actual data. Thus, no handling of the identity of the client is necessary if a respone packet is to be sent from within the method ``NotifyReceivedData()``. If - in contrast to the beforesaid without a preceeding request - a packet is to be sent sponaneously to a specific client, the method ``protSelectClient()`` has to be called previously in order to tell the FB where to send the unrequested packet. Attention (1): the ``protUnread()`` mechanism requires a certain amount of internal buffer, which is allocated statically when the FB is opened. The total size of the buffer memory is defined via the constant ``udiMultiConnect_UnreadBufferSize`` from the ``ParameterList``. Attention (2): In order to avoid deadlocks, received packets were only then processed if the FB is capable to buffer one response packet. If too much internal buffer is occupied, further processing is postponed until the transmitter buffers are empty again. *Usage:* For using a multiconnect server within an application, from this base class an application specific child is derived. :: FUNCTION_BLOCK MyMulticonnectServer EXTENDS FbTcpServer_Multiconnect_base SUPER^();

**Methods:**

#### protWriteToAll
This method writes data from Server to all connected Clients.

This method writes data from Server to all connected Clients. If ``xWithNotifySelection`` is true, the method ``NotifySelection()`` will be called for each client.

**Result Codes:**
| Code | Description |
|------|-------------|
| OK | Success, ready for new communication. EUNSPECIFIC Error while writing data to the clients ============= ===================================================================== |

#### NotifySelection
Notifies the child that connection was selected externally.

This Method is called automatically, when *SelectClient()* has been called. As it is a memeber of the FB, all protected methods may be used within this method, while these have restrictions when called from outside.

#### CalculateBufferDistribution
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success. ENOSPC Parameters do not allow a single client E2BIG Resources do not match minimum requirements for a single client ENOMEM Resources do not fit minimum number of clients EINVAL Invalid or unplausible resource figures ECHRNG Minimum number of Clients cannot be granted. ============= ====================================================================================== |

#### SetSlotAddress
#### TriggerPostponedProcessing
This method triggers processing of unread bytes.

If called, the unread data of the selected client are re-scheduled for processing.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF No active client was selected. ============= ====================================================================================== |

#### ClearUnreadBuffer
This method clears the unread-Buffer of the actual client.

This might be necessary if the data could not be processed for some semantical reason.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF No active client was selected. ============= ====================================================================================== |

#### SelectClient
This method selects a client for spontaneous transmission.

This method is used when the server has to perform operations to a client (write, close, etc) which are spontaneous, i.e. not a reaction to a previous data transmission from the client. For this case, a successful call of *SelectClient()* triggers *NotifySelection()*, where all protected methods (e.g. protWrite()) are available. If the input *sAddress* is empty, the most recently processed client is used for selection. If that client is not connected any more, ENOENT is returend. If the input *wPort* is zero, the first client in the list is taken, which matches the Address, while the port identification is neglected.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success ENOENT The desired client is not connected. ============= ====================================================================================== |

#### protUnread
This method postpones read data for later use.

This method is used when the child object detects that the incoming data contains incomplete logical frames. In that case the application may refuse to process the incomplete data by applying this method from within :ref:`NotifyReceivedData() <FbSocketServer_ApplicationBase.NotifyReceivedData>`. The incomplete data will be stored within the server framework and when the next packet arrives a new attempt will be made to process the old data together with the new one. When the data pointer of ``protUnRead()`` is not equal to the data pointer of ``NotifyReceivedData()`` (i.e. some of the data has been processed), then ``NotifyReceivedData()`` is called again afterwards with the reduced amount of data. This repeats until all data was either accepted or rejected.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EINVAL Data location or size does not match with last read. ENOMEM The server has too less buffer space, data will be lost. EBADF Unread() was not associated to any connection. ============= ====================================================================================== |

#### getNumberOfClientsLimit
This method returns the maximum number of simultaneously connected clients.

This is the limit which is given as overall result from the parameters of all concerned libraries. It does not reflect actual settings directly.

#### getNumberOfConnectedClients
This method returns the number of actually connected clients.

#### ConfigureKeepAliveTransmission
This method configures the transmission of keep-alive packets.

When the keep-alive (KA) feature is turned on, the client socket checks periodically if the server is still reachable by sending empty packets and expecting acknowledge packets. This is to enable the server to make sure that the client is still reachable. After a maximum idle time following complete inactivity (no transmission nor reception of any packets), a special keep-alive-packet is sent (which contains no data, but is acknowledged by TCP). If that KA-packet is not acknowledged, it is retransmitted after a given *interval*. If the predefined number of attempts is exceeded without acknowledgement, the connection is considered to be broken and the socket status is set to ETIMEDOUT. Nevertheless, more packets could be tried to be sent (as the socket is still open) and with the first sign of life from the peer the connection will be considered 'alive' again. The input

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EINVAL Invalid Parameters. ENOSYS This Feature is not supported by the target. ============= ====================================================================================== |

#### Initialize
This method initializes FbTcpServer_Multiconnect_base.

Called automatically with FB_Init().

#### Finish
This method releases FbTcpServer_Multiconnect_base.

Called automatically with FB_Exit().

#### Close
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success EBADF The socket FB was not open. ============= ====================================================================================== |

#### OpenAndListen_base
After this call is done, the FbServerSocket dispatches incoming data to the attached server application FBs. *sAddress* defines the local network interface which is attached to this service. It can be identified by the IP-Address, ('192.168.8.15'). If nothing is declared, the default interface device is taken. *uiPort* identifies the port number under which this service should be advertised. *tTimeout:* When no traffic passes the connection for a longer time, the connection will be closed automatically. A value of T#0s disables this feature. *pBuffer*, *udiBufferSize*: For bookkeeping of actual connections, a certain amount of internal buffer space is required. The exact amount depends on the expected sizes of the requests and the expected number of simultaneous connections.

**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | Success, ready for communication. EACCES The socket could not be created for some other reason. EINVAL Invalid arguments ENFILE The system limit on the total number of open sockets has been reached. EADDRINUSE The given address / port combination is already in use. EBUSY The socket is already bound to an address. EADDRNOTAVAIL A nonexistent interface was requested or the requested address was not local. ENOSPC Parameters do not allow a single client E2BIG Resources do not match minimum requirements for a single client ENOMEM Resources do not fit minimum number of clients ECHRNG Minimum number of Clients cannot be granted. ============= ====================================================================================== |

### FbPing
This is a Ping FB with *cpt*-type interface.

**Description:**
This FB provides the functionality of :ref:`FbPing_base` while implementing the behaviour model :ref:`WagoAppEnable <FbBehaviourModel_WagoAppEnable>` in order to form a *cpt*-interface. (Both of them are described below in detail.) While ``xEnable`` is ``TRUE``, ``FbPing`` continuously issues probe packets to the addressed target ``sAddress`` and calculates transmission statistics. The inputs were sampled at the rising edge of ``xEnable``. Any changes during a started ping-process will have no effect. The outputs ``xValid``, ``xBusy``, ``xError``, and ``oStatus`` signal the processing status according to the WagoAppEnable model. The other outputs represents the response statistics for the time since ``xEnable`` was set. .. note :: For technical reasons the minimum response time is indicated as at least 1ms or larger, although the internally measured time could be in the range of microseconds. .. note:: The type of packet which is used for probing (native ICMP-echoes or ARP) depends on firmware implementations and is beyond the scope of this library. In modern systems it is more likely that ARP-packets are used. Please consult the firmware reference if this should be an issue.

### FbTcpClient
This is a TCP-client with *cpt*-type interface.

**Description:**
This FB acts as client for TCP/IP-connections. It implements the behaviour model :ref:`WagoAppCommunicator <FbBehaviourModel_WagoAppCommunicator>`, based on the functionality of the FB :ref:`FbSocketClient` which is described below in this library. The communication channel is opened by assigning the target address and the target port to the inputs ``sServerName`` and ``wPort``. and then setting ``xOpen`` to ``TRUE``. .. note:: Befor ``xOpen`` is setting to ``True`` the FB must signal with ``xIsIdle``, that the FB is ready to open the communication channel. At the rising edge of ``xOpen`` the keep-alive (KA) feature can turned on or off and the given parameter will be set. If the keep-alive feature is turned on with ``xKeepAlive_Enable``, the client socket checks periodically if the server is still reachable by sending empty packets and expecting acknowledge packets. The purpose of this is to ensure for the client that the server is still reachable. Thus, after ``tKeepAlive_MaxIdleTime`` after complete inactivity (no transmission nor reception of any packets), a special keep-alive-packet is sent (which contains no data, but is acknowledged by TCP). Unless that KA-packet is acknowledged, it is retransmitted after ``tKeepAlive_Interval``. When the number of ``udiKeepAlive_Probes`` is exceeded without acknowledgement, the connection is considered to be broken and the socket status is set to ETIMEDOUT. .. note:: If ``tKeepAlive_MaxIdleTime`` is higher as ``tKeepAlive_Interval`` then ``tKeepAlive_MaxIdleTime`` is used as interval

### FbDatagramReceiver
This is a client for receiving multicast and broadcast datagrams.

**Description:**
The interface of ``FbDatagramReceiver`` is prepared for sending IGMP-packets for multicast. If the capability of handling multicast or broadcast is not used, this FB behaves very similar to the more simple :ref:`FbDatagramServer`.

**Methods:**

#### ConfigureKeepAliveTransmission
This method configures transmission of keep-alive packets.

#### Close
This method closes the Server socket.

#### ReJoinGroup
This method re-joins a multicast group.

#### LeaveGroup
This method leaves a multicast group without closing.

#### OpenAndJoin
This method opens a socket and listens for incoming packets.

``sAddress``: defines the local network interface which is attached to this service. It can be identified by the IP-Address, ('192.168.8.15'). If nothing is declared, the default interface device is taken. ``uiPort``: identifies the port number under which this service should be advertised. ``usiVersion``: specifies the underlying protocol version. 0 means, the FB listens to a common broadcast or unicast, while the numbers 1..3 identify the different versions of IGMP. ``sGroupAddress``: specifies the multicast address, the FB listens to. Be aware that this is neither the clients, nor the producers IP address. It would be for example '192.168.0.255' for a broadcast listener in a class C local net or for another example '224.1.2.3' for a multicast listener. When '' is applied, the FB listens to the broadcast address of the specified local network interface. When the same string as 'sAddress' is applied, the FB listens on regular unicast datagrams. When Multicast is selected, the FB actively registers to the group address specified here. ``sSource``: specifies if datagrams are accepted only from one well-defined producer. (''

#### Initialize
This method initializes FbDatagramReceiver

#### Finish
This method finishes FbDatagramReceiver and release resources.

### FbDatagramServer
This is a server FB for UDP packets (datagrams).

**Description:**
The ``FbDatagramServer`` is quite similar to the TCP-Server. But, in contrast to the latter, this server works connection-less. As a consequence, no different instances for multiple connections are attached, but the FB itself is derived from :ref:`FbSocketServer_ApplicationBase`. Thus, the application has to deal with only one single server FB. It is completely method driven.

**Methods:**

#### Finish
#### Initialize
#### Close
This method closes the Server socket and closes all attached server FBs.

#### OpenAndListen
This method opens a Server socket and listens for incoming packets.

After this call is done, the FbServerSocket dispatches incoming data to the attached server application FBs. ``sAddress``: defines the local network interface which is attached to this service. It can be identified by the IP-Address, ('192.168.8.15'). If nothing is declared, the default interface is taken. ``uiPort``: identifies the port number under which this service should be advertised (0

### FbPing_base
This FB sends a series of pings to a destination and waits for the response.

**Description:**
The Fb is started with the method :ref:`Start() <FbPing_base.Start>` which is the only relevant method in this FB. The operational parameters (such as destination address, number of trials, timeout) are passed as arguments of this start()-method. .. note:: As indicated in the interface summary, there are several methods and properties inherited from the fundamental behaviour model. These have no use here and should be ignored. They *should not* be used in any application code. During the main run, statistics about the ping response is gathered and provided at the output. The others were counted as 'failed', but do not contribute to average calculations. The sequence of PINGs may be interrupted by setting the ``xAbort`` input to ``TRUE``. .. note:: The type of packet which is used for probing (native ICMP-echoes or ARP) depends on firmware implementations and is beyond the scope of this library. In modern systems it is more likely that ARP-packets are used. Please consult the firmware reference if this should be an issue.

**Methods:**

#### protsetupResultFactory
This Method sets upt the details of the result catory. It is typically called in initialization code, e.g. :: protSetupResultFactory(ADR('Name of the FB or the Instance'), ADR(ERROR_ARRAY), SIZEOF(ERROR_ARRAY)); *Caveat:* This initialization cannot always be performed in FB_Init(), because the order of initialization is unclear in several situations. A most safe way would be the following snipped : :: IF IsNotInitalized() THEN protSetupResultFactory(ADR('Name of the FB or the Instance'), ADR(ERROR_ARRAY), SIZEOF(ERROR_ARRAY)); END_IF

#### Start
This method starts the execution of :ref:`FbPing`. It is the only relevant method in the interface of FbPing.

The method ``start()`` carries all relevant parameters for the core process of PING and defers the core functionality of PING to an asynchronous context. It returns immediately afterwards although the ping process itself might not yet be completed. The termination of the PING process is indicated by the standard output flags of Fb_Async_Base - i.e. ``xTerminated``. .. note:: Timeout values below a critical value (5ms) will be silently clamped to the critical value (5ms). This is to avoid unreasonably short timout values. Under normal circumstances, this minimum limit does not affect the use of this Fb.

### FbSocketClient
This FB implements the client role of a socket connection. It handles TCP connections as well as UDP transmissions.

**Description:**
This FB is completely method driven. The most prominent methods are :ref:`OpenAndConnect() <FbSocketClient.OpenAndConnect>`, :ref:`Write() <FbSocketClient.Write>`, :ref:`Read() <FbSocketClient.Read>`, and :ref:`Close() <FbSocketClient.Close>`. Details of the functionality are provided at the place of the description of the methods and properties.

**Methods:**

#### CheckConnectionHealth
Cancels pending write data.

This method peeks if data could be accessed from the socket but does not actually fetch the data. If the connection is found to be broken EPIPE is returned and the connection is closed actively. In any other case (data present or not) OK is returned. This method is intended for probing if the keepalive mechanism has detected a broken connection. If keepalive is configured, it will be called automatically so no extra call from teh user is necessary. Attention: If there has been data received before the connection broke and which is not read yet by the user, the connection is considered OK until the pending data is read.

#### ClearStatusObject
This method erases all error- and status-information from the FB.

#### protsetupResultFactory
This Method sets upt the details of the result catory. It is typically called in initialization code, e.g. :: protSetupResultFactory(ADR('Name of the FB or the Instance'), ADR(ERROR_ARRAY), SIZEOF(ERROR_ARRAY)); *Caveat:* This initialization cannot always be performed in FB_Init(), because the order of initialization is unclear in several situations. A most safe way would be the following snipped : :: IF IsNotInitalized() THEN protSetupResultFactory(ADR('Name of the FB or the Instance'), ADR(ERROR_ARRAY), SIZEOF(ERROR_ARRAY)); END_IF

#### Initialize
This initializes all internal components of ``FbSocketClient``.

Use this in derived FBs for initializing the inherited structure: :: METHOD FB_Init : BOOL initialize(); METHOD initialize : // own initialization SUPER^.initialize();

#### Write
Writes data to a client socket.

#### Finish
This finishes the operation of all internal components of ``FbSocketClient``.

Use this in derived FBs for finishing the inherited structure: :: METHOD FB_Exit : BOOL finish(); METHOD finish : // own finishing code SUPER^.finish();

#### Close
Closes the connection from client side.

#### OpenAndConnect
This method opens a new client conection and establishes a TCP-connection to the addressed server, if TCP is selected as protocol.

The ``OpenAndConnect()`` call returns direcly without necessarily waiting for the server to respond (equivalent to the option ``O_NONBLOCK``). In most cases, the connection has not been established yet, so the call returns with EAGAIN, which does not mean failure, but 'Try Again'. Before sending data to the socket, the application should use :ref:`IsReadyForWrite <FbSocketClient.IsReadyForWrite>` or :ref:`State <FbSocketClient.State>` for determining if the server has answered in between. Timeout: The parameter `tTimeout`` denotes the time after which the FB stops all activities for opening the socket and transits to the 'closed' state if the connection is not established until then. If the firmware detects other reasons for considering the connection as 'failed' (including other firmware timeouts), the FB might also give up earlier. If the firmware manages to establish the connection finally after the FB has decided to time out, this connection will automatically be closed again. Write Buffer: In order to optimize the data flow, the client FB may be provided with externally allocated buffer space for the write queue. The inputs ``pWriteBuffer`` and ``udiWriteBufferSize`` hold the parameters of that external buffer. Providing an external buffer space is, however, not mandatory. When a null-pointer is passed to the input, the client FB simply operates with minimal internal buffering so the application would have to wait between adjacent write operations. Broadcast and Multicast: Under normal circumstances, the socket client FB is operated on point-to-point connections. When broadcast transmission or mulicast transmission is required, this has to be explicitly enabled by the ``xAllowBroadcast``-flag in the OpenAndConnect call. For broadcasts and multicasts there are special target addresses to be used (e.g. 224.0.0.0/4 for multicast). .. note:: While for broadcast operation no special means other than the ones mentioned before are required, multicast operation requires configuration of the involved routers via IGMP. To the sender of multicasts (i.e. this FB) this process is completly hidden. It is just triggered by using a multicast address and setting xAllowBroadcast. Apart from the special target address the sender is completely unaware about how many and which receivers are listening to the messages - it simply sends the packets to the primary router. The potential receivers of multicast (not broadcast!) messages have to play an active role now. They have to register to the involved routers via IGMP. This is, however, beyond the scope of this client FB, as the recipients of multicast messages act formally as servers (i.e. they receive spontaneous transmissions which are not direct responses to their own transmissions). .. note:: There is as special function block :ref:`FbDatagramReceiver`, which has an interface especially designed for receiving packets from Unicast, Broadcast and Multicast connections. sOwnInterface: This parameter is used for specifying which interface is to be used. The same naming conventions apply as for the host-IP of server sockets. If it is not possible to honor the specified ``sOwnInterface``, then ENOPROTOOPT is returned. If an empty string ('') is passed (the default and normal case), then the OS decides itself via the routing table which interface to use. This option is mainly used for broadcast- or multicast transmissions, where the use of the routing table might be ambiguous.

#### Read
Reads a number of bytes.

A number of bytes are read from the socket. The input 'udiRxBufferSize' denotes the maximum number of bytes which can be accepted. This is normally the buffer size. The output 'udiRxNBytes' denotes, how many bytes are really read. If at least one or more bytes are successfully read, the method returns 'OK'. If no bytes could be read, the call returns ENODATA in normal cases or an error code in case of an error.

#### ConfigureKeepAliveTransmission
This method configures the autonomous sending of keep-alive ('KA') packets.

When the keep-alive (KA) feature is turned on, the client socket checks periodically if the server is still reachable by sending empty packets and expecting acknowledge packets. Thus, after a maximum idle time following complete inactivity (no transmission nor reception of any packets), a special keep-alive-packet is sent which contains no data, but which is acknowledged by TCP. If that KA-packet is not acknowledged, it is retransmitted after a given *tInterval*. If the predefined number of attempts is exceeded without acknowledgement, the connection is considered broken and the socket status is set to ETIMEDOUT. Nevertheless, more packets could be tried to be sent in spite of that situation (as the socket is still open) and with the first sign of life from the peer the connection will be considered 'alive' again. The input ``udiProbes`` is the number of unresponded KA packets before the KA mechanism gives up and declares the connection 'broken'. In Detail: 0

#### CancelWrite
Cancels pending write data.

This method cancels pending write data which has not yet been transported. This may be used to release data space or to free the stream or pipe for new data if it is clear that the pending data is obsolete now anyway. This is a typically used as an emergency call, e.g. for telling the client-FB that the data space, which is passed to the write call and not processed yet, is not to be accessed any more because the memory has to be released due to FB_Exit or similar issues. .. note:: This does not necessarily stop those parts of the data, which has already been successfully passed via the OS-call send() into the system socket stack already. Nevertheless, a side effect might also be (not strictly defined) that this data would also be be stopped from transmission. What happens to this data in the intermediate state is explicitly undefined.

### FbTcpServer
**Description:**
This FB provides a framework for building Server structures within the application.

**Methods:**

#### ConfigureKeepAliveTransmission
This method configures transmission of keep-alive ('KA') packets.

When the keep-alive (KA) feature is turned on, the client socket checks periodically if the server is still reachable by sending empty packets and expecting acknowledge packets. The purpose of this is to enable the server to ascertain that the client is still reachable. Thus, after a maximum idle time following complete inactivity (no transmission nor reception of any packets), a special keep-alive-packet is sent (which contains no data, but is acknowledged by TCP). If that KA-packet is not acknowledged, it is retransmitted after a given *interval*. If the predefined number of attempts is exceeded without acknowledgement, the connection is considered to be broken and the socket status is set to ETIMEDOUT. Nevertheless, more packets could be tried to be sent in spite of that situation (as the socket is still open) and with the first sign of life from the peer the connection will be considered 'alive' again. The input ``udiProbes`` is interpreted as follows: 0

#### Initialize
This method initializes FbTcpServer.

#### Finish
This method releases all resources of FbTcpServer.

#### AttachServerApplication
This method attaches a new application FB to the server.

When an instance of the server application FB (:ref:`FbSocketServer_ApplicationBase`) is attached to the FbTcpServer, this instance can be used my the FbTcpServer for a new incoming connection. All communication and method calls regarding this instance will then be handled by the FbTcpServer-instance, which may handle multiple instances of the server application FBs. .. note:: New server application FBs may be added/attached while the FbTcpServer is already open.

#### Close
This method closes the server and all attached application FBs.

#### OpenAndListen
This method opens a Server socket and listens for incoming packets.

After this call is done, the FbServerSocket dispatches incoming data to the attached server application FBs. ``sAddress``: defines the local network interface which is attached to this service. It can be identified by the IP-Address, ('192.168.8.15'). If nothing is declared, the default interface device is taken. ``uiPort``: identifies the port number under which this service should be advertised. ``tTimeout``: When no traffic passes the connection for a longer time, the connection will be closed automatically. A value of T#0s disables this feature.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbUdpTransmitterExt: FbUdpTransmitterExt;
END_VAR

// Basic function block usage
fbFbUdpTransmitterExt(
    // Configure inputs as needed
);

// Check status
IF fbFbUdpTransmitterExt.xValid THEN
    // Operation successful
END_IF

IF fbFbUdpTransmitterExt.xError THEN
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

