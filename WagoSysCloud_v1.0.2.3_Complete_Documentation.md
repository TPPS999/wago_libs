# WagoSysCloud v1.0.2.3 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoSysCloud
- **Version:** 1.0.2.3
- **Categories:** WAGO Internal; WAGO Internal|Common
- **Namespace:** WagoSysCloud
- **Author:** WAGO / u014791
- **Placeholder:** WagoSysCloud

### Description ¶


This document is automatically generated.

Library project template with all possible element types, docu and a sample project structure

This document is automatically generated. Library project template with all possible element types, docu and a sample project structure

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Function Blocks FbAgentBusReciever (FB) - FbAgentBusTransmitter (FB) - FbDatagramServer_internal_copy (FB) Functions Methods - FbAgentBusReciever.NotifyReceivedData (METH) - FbAgentBusReciever.QueryReadyForReceiveData (METH) - FbAgentBusReciever.QueryReceiveBufferLocation (METH) - FbAgentBusTransmitter.FB_Exit (METH) - FbDatagramServer_internal_copy.OpenAndListen (METH) Function Groups Internal Components Global Variable Lists - GVL (GVL) - Status (GVL) - VersionHistory (GVL) Other Components - 10 AgentBus - 29 Types - 80 Status - ErrorInformationCloud (STRUCT) - Param (PARAMS) - eConnectionId (ENUM) - eStatus (ENUM) - notifications

### Indices and tables ¶


Based on WagoSysCloud.library, last modified 05.11.2024, 23:35:44. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysCloud.library, last modified 05.11.2024, 23:35:44. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoSysCloud Library Documentation


| Company: | WAGO |
| Title: | WagoSysCloud |
| Version: | 1.0.2.3 |
| Categories: | WAGO Internal; WAGO Internal\|Common |
| Namespace: | WagoSysCloud |
| Author: | WAGO / u014791 |
| Placeholder: | WagoSysCloud |

### Description


This document is automatically generated.

Library project template with all possible element types, docu and a sample project structure

This document is automatically generated. Library project template with all possible element types, docu and a sample project structure

### Contents:


- 29 Types ErrorInformationCloud (STRUCT) - eConnectionId (ENUM) 80 Status - Status (GVL) - eStatus (ENUM) 90 Internal - 10 AgentBus - 20 Functions GVL (GVL) Param (PARAMS) VersionHistory (GVL)

### Indices and tables


Based on WagoSysCloud.library, last modified 05.11.2024, 23:35:44. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoSysCloud.library, last modified 05.11.2024, 23:35:44. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoSysCloud.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 05.11.2024, 23:35:44 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 05.11.2024, 23:35:44 |
| Description | string | See: Description |
| DocFormat | reStructuredText |
| Author | WAGO / u014791 |
| AutoResolveUnbound | bool | True |
| LanguageModelAttribute | string | qualified-access-only |
| Company | WAGO |
| Placeholder | WagoSysCloud |
| SourceLibrary | bool | False |
| Project | string | WagoSysCloud |
| DefaultNamespace | WagoSysCloud |
| Version | version | 1.0.2.3 |
| Title | string | WagoSysCloud |
| Released | bool | False |
| LibraryCategories | library-category-list | WAGO Internal; WAGO Internal\|Common |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |
| IsEndUserLibrary | bool | False |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: True | SystemLibrary: False | Optional: False |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: True | Optional: False |

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

This is a dictionary of all referenced libraries and their name spaces. Analyzation Library Identification : Placeholder: Analyzation Default Resolution: Analyzation, 3.5.2.0 (System) Namespace: Analyzation Library Properties : Library Parameter : Parameter: TABLE_UPPER_BOUND = 15 Parameter: STRING_LENGTH_ADDRESS = 20 Parameter: STRING_LENGTH_EXP = 255 Parameter: STRING_LENGTH_COMMENT = 255 Parameter: TABLE_SHOW_VALID_ITEMS = FALSE Parameter: STRING_LENGTH_OUTSTRING = 255 CAA FB Factory Library Identification : Placeholder: CAA FB Factory Default Resolution: CAA FB Factory, * (CAA Technical Workgroup) Namespace: FBF Library Properties : CAA Types Extern Library Identification : Placeholder: CAA Types Default Resolution: CAA Types Extern, * (CAA Technical Workgroup) Namespace: CAA Library Properties : IecSfc Library Identification : Placeholder: IecSfc Default Resolution: IecSfc, 3.4.2.0 (System) Namespace: IecSfc Library Properties : SysSocket Library Identification : Name: SysSocket Version: newest Company: System Namespace: SysSocket Library Properties : WagoAppJSON Library Identification : Placeholder: WagoAppJSON Default Resolution: WagoAppJSON, * (WAGO) Namespace: WagoAppJSON Library Properties : Library Parameter : Parameter: JSON_REPLACE_STRING = ‘#Parameter’ Parameter: SIZE_JSON_POINTER = 255 Parameter: JSON_SKIP_STRING = ‘##’ Parameter: JSON_ADVANCED_CHUNK_SIZE_IMPORT = 50000 Parameter: MAX_ARRAY_ELEMENTS_CUSTOM = 7 Parameter: JSON_MAX_STRING = 2000 Parameter: JSON_ADVANCED_CHUNK_SIZE_EXPORT = 50000 Parameter: MAX_JSON_FILE_SIZE = 6000 Parameter: JSON_POINTER_RESULT = 255 Parameter: JSON_MAX_DATA_LENGTH = 65535 Parameter: MAX_SINGLE_KEY_VALUE_LENGTH = 255 Parameter: JSON_NAME_ARRAY_BY_INDEX_SAX = FALSE Parameter: JSON_SAX_UTF8_ENABLED = FALSE Parameter: JSON_MAX_PARAMETER_STRING = 80 Parameter: JSON_MAX_TOKEN_COUNT = 100 Parameter: JSON_SAX_CHUNK_SIZE = 10000 Parameter: JSON_MAX_STRING_SAX = 2000 Parameter: JSON_MAX_ARRAY_SIZE = 170 Parameter: JSON_MAX_STRING_RESULT = 80 WagoSysErrorBase Library Identification : Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase Library Properties : WagoSysFileDir Library Identification : Placeholder: WagoSysFileDir Default Resolution: WagoSysFileDir, * (WAGO) Namespace: WagoSysFileDir Library Properties : WagoSysSocket_Internal_PFC Library Identification : Placeholder: WagoSysSocketInternal Default Resolution: WagoSysSocket_Internal_PFC, * (WAGO) Namespace: WagoSysSocket_internal Library Properties : Library Parameter : Parameter: TCP_USER_TIMEOUT = 10000 Parameter: CUININSTANCELISTSIZE = 20 WagoSysString Library Identification : Placeholder: WagoSysString Default Resolution: WagoSysString, * (WAGO) Namespace: WagoSysString Library Properties : WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesErrorBase Library Identification : Placeholder: WagoTypesErrorBase Default Resolution: WagoTypesErrorBase, * (WAGO) Namespace: WagoTypesErrorBase Library Properties : WagoTypesSocket Library Identification : Placeholder: WagoTypesSocket Default Resolution: WagoTypesSocket, * (WAGO) Namespace: WagoTypesSocket Library Properties :

### Function Blocks


## FbAgentBusReciever (FB)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Input | sAddress | STRING |  |
| wPort | WORD |  |
| pRxBuffer | POINTER TO BYTE |  |
| udiRxBufferSize | UDINT |  |
| xRxEnable | BOOL |  |
| xOpen | BOOL |  |
| Output | xPackedReceived | BOOL |  |
| udiNumberOfReceivedBytes | UDINT |  |
| sClientIpAddress | IpAddressString |  |
| xReadyToRecieve | BOOL | FALSE |

Interface variables - notifications FbAgentBusReciever.NotifyReceivedData (METH) - FbAgentBusReciever.QueryReadyForReceiveData (METH) - FbAgentBusReciever.QueryReceiveBufferLocation (METH)

## FbAgentBusTransmitter (FB)


| Scope | Name | Type | Initial |
| --- | --- | --- | --- |
| Input | pTxData | POINTER TO ARRAY [0..(gMAX_UDP_SIZE - 1)] OF BYTE |  |
| dwNumberOfTxBytes | DWORD |  |
| eConnection | eConnectionId |  |
| Inout | xTxTrigger | BOOL |  |
| Output | xBusy | BOOL | FALSE |
| xError | BOOL | FALSE |
| oStatus | WagoSysErrorBase.FbResult |  |

Interface variables - FbAgentBusTransmitter.FB_Exit (METH)

## FbDatagramServer_internal_copy (FB)


FUNCTION_BLOCK INTERNAL FbDatagramServer_internal_copy EXTENDS WagoSysSocket_internal.FbDatagramServer_internal

FUNCTION_BLOCK INTERNAL FbDatagramServer_internal_copy EXTENDS WagoSysSocket_internal.FbDatagramServer_internal - FbDatagramServer_internal_copy.OpenAndListen (METH)

### Functions


## ASCII_TO_CHAR (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | ASCII_TO_CHAR | STRING |
| Input | bAsciiByte | BYTE |

### Methods


## FbAgentBusReciever.NotifyReceivedData (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | NotifyReceivedData | WagoTypes.eResultCode |  |
| Input | pData | POINTER TO BYTE | points to the received data |
| udiDataSize | UDINT | number of data in this chunk |
| pHeader | POINTER TO BYTE | points to the header, 0 if not available |

## FbAgentBusReciever.QueryReadyForReceiveData (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | QueryReadyForReceiveData | UDINT |

## FbAgentBusReciever.QueryReceiveBufferLocation (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | QueryReceiveBufferLocation | POINTER TO BYTE |

## FbAgentBusTransmitter.FB_Exit (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | FB_Exit | BOOL |
| Input | bInCopyCode | BOOL |

## FbDatagramServer_internal_copy.OpenAndListen (METH)


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

### Function Groups


## 20 Functions ¶


- ASCII_TO_CHAR (FUN)

### Internal Components


## 90 Internal


- 10 AgentBus FbAgentBusReciever (FB) notifications FbAgentBusReciever.NotifyReceivedData (METH) - FbAgentBusReciever.QueryReadyForReceiveData (METH) - FbAgentBusReciever.QueryReceiveBufferLocation (METH) FbAgentBusTransmitter (FB) - FbAgentBusTransmitter.FB_Exit (METH) FbDatagramServer_internal_copy (FB) - FbDatagramServer_internal_copy.OpenAndListen (METH) 20 Functions - ASCII_TO_CHAR (FUN)

### Global Variable Lists


## GVL (GVL)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | gMAX_UDP_SIZE | DWORD | 65507 | Maximal size for the internal udp communication to the dataagent (65535 - 20 (IP Header) - 8 (UDP Header) = 65507) |

## Status (GVL)


| Scope | Name | Type |
| --- | --- | --- |
| Constant | StatusCloud | ARRAY [0..39] OF WagoTypesErrorBase.typResultItem |

| Value | Level | Description |
| --- | --- | --- |
| eStatus.OK | WagoTypesErrorBase.eSeverity.info | ‘OK’ |
| eStatus.Status_ReadError | WagoTypesErrorBase.eSeverity.error | ‘Read error to read status information’ |
| eStatus.Status_InterprationError | WagoTypesErrorBase.eSeverity.error | ‘Error in the Interpretation of the status informations’ |

Standard result items specific for this library

This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library.

Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

Standard result items specific for this library This is a general mapping of result codes to short standard texts which are appropriate to the usage of these codes in this library. Typially, each unit (function, method, or function block) in this library uses only a subset of these codes. Please, refer to the documentation of the specific unit for the set of codes which is actualy used and for a detailed explanation of the meaning of a result code in the specifc context.

## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| Date | Version | Author | Change |
| 24.05.2024 | 1.0.2.2 | WAGO / u014791 | Fix plaholder for WagoSysSocketInternal |
| 24.05.2024 | 1.0.2.2 | WAGO / u014791 | Add categories for WagoSysCloud |
| 16.04.2024 | 1.0.2.1 | WAGO / u014791 | FbAgentBusReciever add output xReadyToRecieve |

Version of library WagoAppSparkplug

Release Notes:

Version of library WagoAppSparkplug Release Notes:

### Other Components


## 10 AgentBus


- FbAgentBusReciever (FB) notifications FbAgentBusReciever.NotifyReceivedData (METH) - FbAgentBusReciever.QueryReadyForReceiveData (METH) - FbAgentBusReciever.QueryReceiveBufferLocation (METH) FbAgentBusTransmitter (FB) - FbAgentBusTransmitter.FB_Exit (METH) FbDatagramServer_internal_copy (FB) - FbDatagramServer_internal_copy.OpenAndListen (METH)

## 29 Types


- ErrorInformationCloud (STRUCT) - eConnectionId (ENUM)

## 80 Status ¶


- Status (GVL) - eStatus (ENUM)

## ErrorInformationCloud (STRUCT)


| Name | Type |
| --- | --- |
| ID | INT |
| Description | STRING(255) |
| Hint | STRING(255) |

| ErrorId | Description |
| 1 | PLC application is using wrong function block |
| 3 | PLC application is sending variables not supported by WAGO Protocol version |
| 5 | Received unhealthy packet (data loss) |
| 6 | PLC application is using wrong library version |
| 7 | Multi Cloud Connectivity license not existent |
| 8 | Sparkplug license not existing |
| 9 | Fallback to RAM cache due to SD card faults |
| 10 | Mosquitto error message |
| 11 | The connection was refused. |
| 12 | The connection was lost. |
| 13 | Keepalive Timeout. |
| 14 | Lookup error. |
| 15 | A TLS error occurred. |

ErrorInformationCloud includes the error information about the Cloud Connectivity. These error messages must be corrected one after the other by the customer.

InOut: ErrorInformationCloud includes the error information about the Cloud Connectivity. These error messages must be corrected one after the other by the customer.

## Param (PARAMS)


| Scope | Name | Type | Initial | Comment |
| --- | --- | --- | --- | --- |
| Constant | gMAX_PAYLOAD_SIZE_PUBLISH | DWORD | 65237 | Parameter of the maximal payload size for publish instances (DataProtocol: NativeMQTT) - max 65237 Bytes (Parameter applies to both connections) |
| gMAX_PAYLOAD_SIZE_SUBSCRIBE | DWORD | 65237 | Parameter of the maximal payload size for subscribe instances (DataProtocol: NativeMQTT) - max 65237 Bytes (Parameter applies to both connections) |
| gCONNECTION_1_PORT1 | WORD | 14118 |  |
| gCONNECTION_1_PORT2 | WORD | 14119 |  |
| gCONNECTION_1_PORT3 | WORD | 14120 |  |
| gCONNECTION_2_PORT1 | WORD | 14121 |  |
| gCONNECTION_2_PORT2 | WORD | 14122 |  |
| gCONNECTION_2_PORT3 | WORD | 14123 |  |

## eConnectionId (ENUM)


| Name | Initial |
| --- | --- |
| Connection1 | 1 |
| Connection2 | 2 |

## eStatus (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| OK | 0 | all is well |
| Status_ReadError | 238 | Init := 201, CollectionLogger_RegistrateCollection := 202, CollectionLogger_NoCollections := 204, CollectionLogger_FalseCollectionCount := 205, CollectionLogger_NoVariableDescriptions := 206, CollectionLogger_NoVariable := 207, CollectionLogger_NoPublishInterval := 208, CollectionLogger_NoSampleInterval := 209, CollectionLogger_VariablesCount := 210, CommandConfigurator_NoCmdDescriptions := 211, CommandConfigurator_CommandCounts := 212, FalseNumRequestParameter := 213, FalseNumResponseParameter := 214, CommandListener_NoCommandRequest := 215, CommandResponder_NoCommandResponse := 216, RegistrationMessage := 217, RegMsgFactory_NullPointer := 218, CmdRequestDecoder_MagicId := 219, CmdRequestDecoder_MessageSize := 220, CmdRequestDecoder_Version := 221, CmdRequestDecoder_NullPointer := 222, CmdRegMsgFactory_NullPointer := 223, CmdResponseMsgFactory_NullPointer := 224, SampleMsg_Overflow := 225, SampleMsg_NullPointer := 226, MsgListener_UnknownSender := 227, MsgListener_NoPacket := 228, MsgListener_NullPointer := 229, AgentBusRx_NullPointer := 230, AgentBusTx_NullPointer := 231, Publish_dwSizeFalse := 232, Publish_sTopicFalse := 233, Publish_eQoS := 234, PublishMessageFactory_NullPointer := 235, Subscribe_FalseParameter := 236, CommandConfiguratorMaxLimit := 237, |
| Status_InterprationError | 239 |  |

## notifications


- FbAgentBusReciever.NotifyReceivedData (METH) - FbAgentBusReciever.QueryReadyForReceiveData (METH) - FbAgentBusReciever.QueryReceiveBufferLocation (METH)