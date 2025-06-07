# WagoTypesModbus v1.6.1.2 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesModbus
- **Version:** 1.6.1.2
- **Categories:** WAGO FunctionalView|Connectivity|FieldBus; WAGO LayerView|Types and Interfaces; WAGO Internal|Feature|Fieldbus|Modbus; Application
- **Namespace:** WagoTypesModbus
- **Author:** WAGO / u015658
- **Placeholder:** WagoTypesModbus

### Description ¶


This document is automatically generated.

Modbus specific data types.

This document is automatically generated. Modbus specific data types.

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Functions convert_ip_settings (FUN) - convert_ip_transport_layer (FUN) - convert_serial_physical_layer (FUN) - convert_serial_settings (FUN) Methods - I_MbDataModel.ProcessPdu (METH) - I_MbDataModel.getUnitId (METH) - I_WagoSysModbusDiag.GetChannelErrorCode (METH) - I_WagoSysModbusDiag.GetErrorCode (METH) - I_WagoSysModbusDiag.GetNumberOfChannels (METH) - typIpSettings (STRUCT) - typSerialSettings (STRUCT) Interfaces - I_MbDataModel (ITF) - I_WagoSysModbusDiag (ITF) Program Organization Internal Components Global Variable Lists Other Components - eChannelError (ENUM) - eEvent (ENUM) - eIpTransportLayer (ENUM) - eRemoteSlaveError (ENUM)

### Indices and tables ¶


Based on WagoTypesModbus.library, last modified 29.05.2024, 19:56:19. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesModbus.library, last modified 29.05.2024, 19:56:19. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesModbus Library Documentation


| Company: | WAGO |
| Title: | WagoTypesModbus |
| Version: | 1.6.1.2 |
| Categories: | WAGO FunctionalView\|Connectivity\|FieldBus; WAGO LayerView\|Types and Interfaces; WAGO Internal\|Feature\|Fieldbus\|Modbus; Application |
| Namespace: | WagoTypesModbus |
| Author: | WAGO / u015658 |
| Placeholder: | WagoTypesModbus |

### Description


This document is automatically generated.

Modbus specific data types.

This document is automatically generated. Modbus specific data types.

### Contents:


- 20 Program Organization Units I_MbDataModel (ITF) - I_WagoSysModbusDiag (ITF) - eChannelError (ENUM) - eEvent (ENUM) - eIpTransportLayer (ENUM) - eRemoteSlaveError (ENUM) - typIpSettings (STRUCT) - typSerialSettings (STRUCT) 90 Internal - convert_ip_settings (FUN) - convert_ip_transport_layer (FUN) - convert_serial_physical_layer (FUN) - convert_serial_settings (FUN) VersionHistory (GVL)

### Indices and tables


Based on WagoTypesModbus.library, last modified 29.05.2024, 19:56:19. LibDoc 3.5.16.10

© WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference Based on WagoTypesModbus.library, last modified 29.05.2024, 19:56:19. LibDoc 3.5.16.10 © WAGO GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesModbus.library |
| contentFile | doc.clean.json |
| productName | e!COCKPIT |
| creationDateTime | date | 29.05.2024, 19:56:19 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 29.05.2024, 19:56:19 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO / u015658 |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesModbus |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesModbus |
| DefaultNamespace | WagoTypesModbus |
| Version | version | 1.6.1.2 |
| Title | string | WagoTypesModbus |
| Released | bool | False |
| LibraryCategories | library-category-list | WAGO FunctionalView\|Connectivity\|FieldBus; WAGO LayerView\|Types and Interfaces; WAGO Internal\|Feature\|Fieldbus\|Modbus; Application |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

| LinkAllContent: False Optional: False | QualifiedOnly: False SystemLibrary: False | PublishSymbolsInContainer: True |

| LinkAllContent: False QualifiedOnly: False | SystemLibrary: False | Optional: False |

This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces. WagoSysVersion Library Identification : Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion Library Properties : WagoTypesCom Library Identification : Placeholder: WagoTypesCom Default Resolution: WagoTypesCom, * (WAGO) Namespace: WagoTypesCom Library Properties : WagoTypesSocket Library Identification : Placeholder: WagoTypesSocket Default Resolution: WagoTypesSocket, * (WAGO) Namespace: WagoTypesSocket Library Properties :

### Functions


## convert_ip_settings (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | convert_ip_settings | BOOL |
| Inout | dst | ip_settings |
| Input | src | typIpSettings |

firmware interface

Interface variables firmware interface

## convert_ip_transport_layer (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | convert_ip_transport_layer | BOOL |
| Inout | dst | ip_transport_layer |
| Input | src | eIpTransportLayer |

firmware interface

Interface variables firmware interface

## convert_serial_physical_layer (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | convert_serial_physical_layer | BOOL |
| Inout | dst | serial_physical_layer |
| Input | src | eTTYPhysicalLayer |

firmware interface

Interface variables firmware interface

## convert_serial_settings (FUN)


| Scope | Name | Type |
| --- | --- | --- |
| Return | convert_serial_settings | BOOL |
| Inout | dst | serial_settings |
| Input | src | typSerialSettings |

firmware interface

Interface variables firmware interface

### Methods


## I_MbDataModel.ProcessPdu (METH)


| Scope | Name | Type | Comment |
| --- | --- | --- | --- |
| Return | ProcessPdu | BOOL |  |
| Input | pRxData | POINTER TO BYTE | points to SlaveAddress (Unit-ID) |
| udiRxNBytes | UDINT | quantity without crc |
| pTxBuffer | POINTER TO BYTE |  |
| udiTxSize | UDINT |  |
| Inout | sClientId | IpAddressString |  |
| Output | udiTxNBytes | UDINT | bytes to send for response |

## I_MbDataModel.getUnitId (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | getUnitId | BYTE |

## I_WagoSysModbusDiag.GetChannelErrorCode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetChannelErrorCode | eChannelError |
| Input | uiChannelNumber | UINT |
| Output | stChannelInfo | channel_config |

## I_WagoSysModbusDiag.GetErrorCode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetErrorCode | eRemoteslaveError |

## I_WagoSysModbusDiag.GetNumberOfChannels (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetNumberOfChannels | UINT |

## typIpSettings (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| sHost | STRING | hostname or ip |
| uiPort | UINT | tcp/udp port |

Is used to configure a IPv4 device.

InOut: Is used to configure a IPv4 device.

## typSerialSettings (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| sDevice | STRING | linux tty device (default: /dev/ttyRUNTIME0) |
| uiBaud | UDINT | symbol rate (default: 19200) |
| uiDataBits | UDINT | databits per character (default: 8) |
| eStopBits | eTTYStopBits | stopbit count (default: 1) |
| eParity | eTTYParity | error detection mode (default: even) |
| eFlowCtrl | eTTYHandshake | flow control (default: off) |

Is used to configure a serial RS232 or RS485 device.

InOut: Is used to configure a serial RS232 or RS485 device.

### Interfaces


## I_MbDataModel (ITF)


{attribute ‘conditionalshow’ := ‘wagoapplication’}

{attribute ‘conditionalshow’ := ‘wagoapplication’} - I_MbDataModel.ProcessPdu (METH) - I_MbDataModel.getUnitId (METH)

## I_WagoSysModbusDiag (ITF)


- I_WagoSysModbusDiag.GetChannelErrorCode (METH) - I_WagoSysModbusDiag.GetErrorCode (METH) - I_WagoSysModbusDiag.GetNumberOfChannels (METH)

### Program Organization


## 20 Program Organization Units


- I_MbDataModel (ITF) I_MbDataModel.ProcessPdu (METH) - I_MbDataModel.getUnitId (METH) I_WagoSysModbusDiag (ITF) - I_WagoSysModbusDiag.GetChannelErrorCode (METH) - I_WagoSysModbusDiag.GetErrorCode (METH) - I_WagoSysModbusDiag.GetNumberOfChannels (METH) eChannelError (ENUM) eEvent (ENUM) eIpTransportLayer (ENUM) eRemoteSlaveError (ENUM) typIpSettings (STRUCT) typSerialSettings (STRUCT)

### Internal Components


## 90 Internal


- convert_ip_settings (FUN) - convert_ip_transport_layer (FUN) - convert_serial_physical_layer (FUN) - convert_serial_settings (FUN)

### Global Variable Lists


## VersionHistory (GVL)


| Name | Type |
| --- | --- |
| Info | ProjectInfo |

| Date | Version | Author | Change |
| 28.02.2024 | 1.6.1.2 | u010663 | Compiled SP16.3 |
| 03.12.2020 | 1.6.1.1 | u010545 | I_MbDataModel inherit from IQueryInterface |
| 08.01.2019 | 1.6.1.0 | u015842 | Properties: free placeholder added |
| 23.04.2018 | 1.6.0.6 | u010663 | remove Lisense information |
| 02.11.2017 | 1.6.0.5 | TBi | Added enum-types for Channel and Remote-Slave Diagnostics |
| 11.10.2017 | 1.6.0.4 | TBi | Added Interface I_WagoSysModbusDiag for Modbus Diagnostics |
| 11.09.2017 | 1.6.0.3 | TBi | Added field ‘ErrorReaction’ to channel_config |
| 12.08.2016 | 1.6.0.2 | u010545 | Interface I_MbDataModel implemented |
| 25.09.2015 | 1.6.0.1 | JMü | Update documentation |
| 25.06.2015 | 1.6.0.0 | TC | changes to conform new guideline |
| 02.06.2015 | 1.5.0.0 | TC | set version for release |
| 06.03.2015 | 1.0.0.0 | TC | set version for release |
| 12.02.2015 | 0.0.3.0 | TC | add event ‘None’ |
| 19.11.2014 | 0.0.2.0 | TC | add more documenation |
| 01.11.2014 | 0.0.1.0 | TC | first version |

WagoTypesModbus

WagoTypesModbus TODO: - remove unnecessary events from eEvent

### Other Components


## eChannelError (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| NO_ERROR | 16#0 |  |
| ILLEGAL_FUNCTION | 16#1 | Modbus Exception Codes |
| ILLEGAL_DATA_ADDRESS | 16#2 |  |
| ILLEGAL_DATA_VALUE | 16#3 |  |
| SERVER_DEVICE_FAILURE | 16#4 |  |
| ACKNOWLEDGE | 16#5 |  |
| SERVER_DEVICE_BUSY | 16#6 |  |
| NEGATIVE_ACKNOWLEDGE | 16#7 |  |
| MEMORY_PARITY_ERROR | 16#8 |  |
| GATEWAY_PATH_UNVAILABLE | 16#A |  |
| GATEWAY_TARGET_DEVICE_UNAVAILABLE | 16#B |  |
| INVALID_CRC | 16#C | libmodbus errors |
| INVALID_DATA | 16#D |  |
| INVALID_EXCEPTION_CODE | 16#E |  |
| TOO_MANY_DATA | 16#10 |  |
| INVALID_NODE_ID | 16#11 |  |
| RTU_FRAME_OUT_OF_DATE | 16#12 |  |
| INVALID_CONFIG | 16#101 | channel specific errors |
| SEND_FAILED | 16#102 |  |
| BUSY | 16#103 |  |
| RESPONSE_TIMEOUT | 16#104 |  |
| INACTIVE | 16#FFFF |  |

## eEvent (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| None | 16#0 | no event |
| Connected | 16#1 | on tcp connection establishment |
| Disconnected | 16#2 | on tcp disconnect |
| AppStatechange | 16#4 | on any statechange of any application |
| AppStart | 16#8 | on statechange to run of any application |
| AppStop | 16#10 | on statechange to stopped of any application |
| Onlinechange | 16#20 | on an onlinechange |
| StatusRequest | 16#40 | for internal use |
| ValueChange | 16#80 | input data of a writing function code changed |

used to update function codes on specific events. Since this datatype has a width of 16 bit, userdefined events can be used from bit 8 to bit 15 and be triggered manually over the eActiveEvents input of the master.

InOut: used to update function codes on specific events. Since this datatype has a width of 16 bit, userdefined events can be used from bit 8 to bit 15 and be triggered manually over the eActiveEvents input of the master.

## eIpTransportLayer (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| TCP | 0 | Transmission Control Protocol |
| UDP | 1 | User Datagram Protocol |

Is used to configure a socket.

InOut: Is used to configure a socket.

## eRemoteSlaveError (ENUM)


| Name | Initial |
| --- | --- |
| NO_ERROR | 16#0 |
| CONNECT_FAILED | 16#101 |
| IP_CONFIG_FAILED | 16#102 |
| RTU_CONFIG_FAILED | 16#103 |
| CHANNEL_TIMEOUT | 16#104 |
| THREAD_CREATION_FAILED | 16#105 |
| IP_SOCKET_OPTION_NOT_SET | 16#106 |
| RTU_LINE_MODE_NOT_SET | 16#107 |
| RTU_INTERCHAR_TIMEOUT_NOT_SET | 16#108 |
| RTU_INTERFRAME_TIMEOUT_NOT_SET | 16#109 |
| WARNING | 16#FFFF |