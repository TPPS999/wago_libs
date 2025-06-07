# WagoAppPlcModbus v1.1.5.8

## Overview
WAGO PLC library providing WagoAppPlcModbus functionality.

**Key Features:**
- Time and date operations
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbMbMasterMultiQueryTcp
This function block provides modbus master functionality over a tcp. Follow function codes are supported ============= ============================== Function Code Function ============= ============================== FC01 (0x01) Read Coils FC02 (0x02) Read Discrete Inputs FC03 (0x03) Read Holding Registers FC04 (0x04) Read Input Registers FC05 (0x05) Write Single Coil FC06 (0x06) Write Single Register FC11 (0x0B) Get Comm Event Counter FC15 (0x0F) Write Multiple Coils FC16 (0x10) Write Multiple Registers FC22 (0x16) Mask Write Register FC23 (0x17) Read/Write Multiple Registers FC43 (0x2B) (Mei Type 14) Read Device Identification ============= ============================== It is written to handle a linked list of |FbQuery| For more information please see also the documentation of |FbQuery| and |FbDigitalTwinMbSlaveDevice|. .. note:: You should always call this FB cyclic. It is recommended to call this Fb in the same task like your derived digital twin ( see |FbDigitalTwinMbSlaveDevice| ). Othervise you should use appropriate actions for task synchronisation.

**Methods:**

#### AttachMbQuery
This method attach a Query to the link list of the master. For link the given ``IQuery`` there are some conditions. 1. ``IQuery`` may not be NULL 2. ``IQuery.eQueryState`` must be equal ``WagoAppPlcModbus.eQueryStatus.DONE`` or ``WagoAppPlcModbus.eQueryStatus.EXECUTED`` Otherwise it is not linked. The method returns one of the follow enumerations =================== ==== =================================================================== DONE 0 Query Done -> you may prepare for a new request LOCKED_AND_LINKED 1 Query new added to link list and locked -> waiting for execution -> do not change LOCKED_WAITING 2 Query in link list and waiting for execution -> do not change LOCKED_ACTIVE 3 Query removed from link list but active -> do not change =================== ==== ===================================================================

### FbMbMasterMultiQueryUdp
This function block provides modbus master functionality over UDP. Follow function codes are supported ============= ============================== Function Code Function ============= ============================== FC01 (0x01) Read Coils FC02 (0x02) Read Discrete Inputs FC03 (0x03) Read Holding Registers FC04 (0x04) Read Input Registers FC05 (0x05) Write Single Coil FC06 (0x06) Write Single Register FC11 (0x0B) Get Comm Event Counter FC15 (0x0F) Write Multiple Coils FC16 (0x10) Write Multiple Registers FC22 (0x16) Mask Write Register FC23 (0x17) Read/Write Multiple Registers FC43 (0x2B) (Mei Type 14) Read Device Identification ============= ============================== It is written to handle a linked list of |FbQuery| For more information please see also the documentation of |FbQuery| and |FbDigitalTwinMbSlaveDevice|. .. note:: You should always call this FB cyclic. It is recommended to call this Fb in the same task like your derived digital twin ( see |FbDigitalTwinMbSlaveDevice| ). Othervise you should use appropriate actions for task synchronisation.

**Methods:**

#### AttachMbQuery
This method attach a Query to the link list of the master. For link the given ``IQuery`` there are some conditions. 1. ``IQuery`` may not be NULL 2. ``IQuery.eQueryState`` must be equal ``WagoAppPlcModbus.eQueryStatus.DONE`` or ``WagoAppPlcModbus.eQueryStatus.EXECUTED`` Otherwise it is not linked. The method returns one of the follow enumerations =================== ==== =================================================================== DONE 0 Query Done -> you may prepare for a new request LOCKED_AND_LINKED 1 Query new added to link list and locked -> waiting for execution -> do not change LOCKED_WAITING 2 Query in link list and waiting for execution -> do not change LOCKED_ACTIVE 3 Query removed from link list but active -> do not change =================== ==== ===================================================================

### FbFC68
This function block provides modbus master functionality. It supports three types of frame selected by the input parameter ``eFrameType``. ========== ===================================================================================== ETHERNET Ethernet-Frame with leading modbus tcp header followed by modbus pdu without any crc RTU RTU-Frame with leading slaveaddress and crc at the end ASCII ASCII-Frame with leading slaveaddress and lrc at the end ========== ===================================================================================== The selected frame type will be transported by a udp package. Before you start a service you have to fill the structure ``utQuery`` with your request data. After this you can start the service with set once to TRUE the parameter ``xTxTrigger``. When the job is done the variable at ``xTxTrigger`` is reset by the function block automaticly. After this you should control the output parameter ``xError``. If an error occurred check the status object ``oStatus`` for detailed information. In the other case you will find in the structure ``utResponse`` the information given from the slave. For use of FC65 you have to fill the structure elements * FbFC65.bModbusAddress --> ModbusAddress (Slave) * FbFC65.udiStartingAddress --> 4Bytes The address in NVM memory where the block should be saved from the cache. Least significant byte first convention * FbFC65.udiBlockSize --> 4Bytes Block size in bytes. Least significant byte first convention * FbFC65.udiArithmeticSum --> 4Bytes Arithmetic sum of individual bytes in the whole block (bytes are summed up in the form before XOR operation) Least significant byte first convention .. note:: You should always call this FB cyclic.

### FbFC65
This function block provides modbus master functionality. It supports three types of frame selected by the input parameter ``eFrameType``. ========== ===================================================================================== ETHERNET Ethernet-Frame with leading modbus tcp header followed by modbus pdu without any crc RTU RTU-Frame with leading slaveaddress and crc at the end ASCII ASCII-Frame with leading slaveaddress and lrc at the end ========== ===================================================================================== The selected frame type will be transported by a udp package. Before you start a service you have to fill the structure ``utQuery`` with your request data. After this you can start the service with set once to TRUE the parameter ``xTxTrigger``. When the job is done the variable at ``xTxTrigger`` is reset by the function block automaticly. After this you should control the output parameter ``xError``. If an error occurred check the status object ``oStatus`` for detailed information. In the other case you will find in the structure ``utResponse`` the information given from the slave. For use of FC65 you have to fill the structure elements * FbFC65.bModbusAddress --> ModbusAddress (Slave) * FbFC65.udiDestinationAddress --> 4bytes Address in cache memory Least significant byte first convention * FbFC65.uiNumberOfBytes --> 1byte [0-245]; zero means 246 bytes * FbFC65.aData --> n-bytes data sent byte by byte .. note:: You should always call this FB cyclic.

### FbDanfossWriteRtc
### FbIdentifyMember_REAL
### FbIdentifyMember_UINT
### FbIdentifyMember_STRING
### FbIdentifyMember_USINT
### FbIdentifyBaseObject
### FbMbMasterMultiQuerySerial
This function block provides modbus master functionality over a serial line. It supports Modbus-RTU or Modbus-ASCII. You can select the protocol type by the input parameter ``eFrameType``. Follow function codes are supported ============= ============================== Function Code Function ============= ============================== FC01 (0x01) Read Coils FC02 (0x02) Read Discrete Inputs FC03 (0x03) Read Holding Registers FC04 (0x04) Read Input Registers FC05 (0x05) Write Single Coil FC06 (0x06) Write Single Register FC11 (0x0B) Get Comm Event Counter FC15 (0x0F) Write Multiple Coils FC16 (0x10) Write Multiple Registers FC22 (0x16) Mask Write Register FC23 (0x17) Read/Write Multiple Registers FC43 (0x2B) (Mei Type 14) Read Device Identification ============= ============================== It is written to handle a linked list of |FbQuery| For more information please see also the documentation of |FbQuery| and |FbDigitalTwinMbSlaveDevice|. .. note:: You should always call this FB cyclic. It is recommended to call this Fb in the same task like your derived digital twin ( see |FbDigitalTwinMbSlaveDevice| ). Othervise you should use appropriate actions for task synchronisation.

**Methods:**

#### AttachMbQuery
This method attach a Query to the link list of the master. For link the given ``IQuery`` there are some conditions. 1. ``IQuery`` may not be NULL 2. ``IQuery.eQueryState`` must be equal ``WagoAppPlcModbus.eQueryStatus.DONE`` or ``WagoAppPlcModbus.eQueryStatus.EXECUTED`` Otherwise it is not linked. The method returns one of the follow enumerations =================== ==== =================================================================== DONE 0 Query Done -> you may prepare for a new request LOCKED_AND_LINKED 1 Query new added to link list and locked -> waiting for execution -> do not change LOCKED_WAITING 2 Query in link list and waiting for execution -> do not change LOCKED_ACTIVE 3 Query removed from link list but active -> do not change =================== ==== ===================================================================

### FbDanfossTime
### FbDigitalTwinMbSlaveDevice
This abstract function block provides the base functionality for a digital twin of a remote modbus slave device. For your own remote device see the follow steps

**Methods:**

#### protAttachMbQuery
This method attach a Query to the link list of the master. For link the given ``IQuery`` there are some conditions. 1. The object input parameter ``FbDigitalTwinMbSlaveDevice.IMbMasterMultiQuery`` may not be NULL 2. ``IQuery`` may not be NULL 3. ``IQuery.eQueryState`` may not stay in one of the follow states * ``WagoAppPlcModbus.eQueryStatus.LOCKED_WAITING`` * ``WagoAppPlcModbus.eQueryStatus.LOCKED_ACTIVE`` Otherwise it is not linked. In case of successful link the method returns 1 otherwise it returns 0 .. note:: After the processing the query by the master the master automatical change the state of the query and remove it from link list.

#### onResponse
This method should be overwritten by your derivation. This method is called by the master after a successful processed query. For each attached |FbQuery| is one of the methods |FbDigitalTwinMbSlaveDevice.onError| or |FbDigitalTwinMbSlaveDevice.onResponse| called once. .. note:: Take notice that this method is called by the master at the context of the master. It is recommended to call the master and the digital twin at the same task. Othervise you should use appropriate actions for task synchronisation. (see also |FbDigitalTwinMbSlaveDevice.onError| )

#### onError
This method should be overwritten by your derivation. This method is called by the master after a processed query with error. For each attached |FbQuery| is one of the methods |FbDigitalTwinMbSlaveDevice.onError| or |FbDigitalTwinMbSlaveDevice.onResponse| called once. .. note:: Take notice that this method is called by the master at the context of the master. It is recommended to call the master and the digital twin at the same task. Othervise you should use appropriate actions for task synchronisation. (see also |FbDigitalTwinMbSlaveDevice.onResponse| )

### FbQuery
This oject holds the parameter for a modbus query. You may initalize the object at declaration (see example below). .. note:: While a query object is attached at a |MbMasterMultiQuery| the change of the most query paramters are blocked. You may not write any parameter while |FbQuery.eQueryState| is not equal DONE or EXECUTED.

### FbUdpServer
### Fb_Exit
### FbMbMasterUdp
This function block provides modbus master functionality. It supports three types of frame selected by the input parameter ``eFrameType``. ========== ===================================================================================== ETHERNET Ethernet-Frame with leading modbus tcp header followed by modbus pdu without any crc RTU RTU-Frame with leading slaveaddress and crc at the end ASCII ASCII-Frame with leading slaveaddress and lrc at the end ========== ===================================================================================== The selected frame type will be transported by a udp package. Follow modbus function codes are supported +--------------+-------------------------------------------------+ |

### FbSocketUdpClient
### Fb_exit
### Fb1PortWordAreaKompositor
This Kompositor converts an array of word to an object that can be processed by a special data model. .. note:: You should always call this FB cyclic.

### Fb1PortBoolAreaKompositor
This Kompositor converts an array of bool to an object that can be processed by a special data model. .. note:: You should always call this FB cyclic.

### FbMbSlaveBaseDataModel
This FB provides the basic functionality of a modbus slave. The method ProcessRequestPdu(...) process standard modbus basic binary PDUs like <FC><Startaddres><Number of points><Data>. The method needs as input complete request PDU start at slave address but without any crc. It process the PDU to the given datafields and generates a response PDU with the slave address but without any crc.

**Methods:**

#### RegisterDataAccessListener
This method register a data access listener to this data model.

#### ProcessPdu
#### WriteSingleRegister
#### WriteSingleCoil
#### WriteMultipleRegisters
#### WriteMultipleCoils
#### ReadWriteMultipleRegisters
#### ReadRegisters
#### ReadBitData
#### Diagnostics
### Fb2PortBoolAreaKompositor
This Kompositor combines multiple different arrays of bool with different address ranges to an object that can be processed by a special data model. .. note:: You should always call this FB cyclic.

### FbMbKompositorDataModel
|

**Methods:**

#### RegisterDataAccessListener
This method register a data access listener to this data model.

### Fb2PortWordAreaKompositor
This Kompositor combines multiple different arrays of word with different address ranges to an object that can be processed by a special data model. .. note:: You should always call this FB cyclic.

### FbShowMbAccessInfo
This oject shows in graphical program languages the information of a FbMbAccessInfo.

### Fb4PortModelSwitch
This function block manages four data models for provide the access to a modbus server. There is no need to connect all input parameters but if you want to connect only one parameter you do not need this function block. In this case you can connect direct the input data model to a server. .. note:: You should always call this FB cyclic.

### Fb2PortModelSwitch
This function block manages two data models for provide the access to a modbus server. There is no need to connect both input parameters but if you want to connect only one parameter you do not need this function block. In this case you can connect direct the input data model to a server. .. note:: You should always call this FB cyclic.

### FbMbMultiServer
**Methods:**

#### NotifyReceivedData
### Fb5PortBoolAreaKompositor
This Kompositor combines multiple different arrays of bool with different address ranges to an object that can be processed by a special data model. .. note:: You should always call this FB cyclic.

### Fb4PortBoolAreaKompositor
This Kompositor combines multiple different arrays of bool with different address ranges to an object that can be processed by a special data model. .. note:: You should always call this FB cyclic.

### Fb3PortBoolAreaKompositor
This Kompositor combines multiple different arrays of bool with different address ranges to an object that can be processed by a special data model. .. note:: You should always call this FB cyclic.

### Fb5PortWordAreaKompositor
This Kompositor combines multiple different arrays of word with different address ranges to an object that can be processed by a special data model. .. note:: You should always call this FB cyclic.

### Fb4PortWordAreaKompositor
This Kompositor combines multiple different arrays of word with different address ranges to an object that can be processed by a special data model. .. note:: You should always call this FB cyclic.

### Fb3PortWordAreaKompositor
This Kompositor combines multiple different arrays of word with different address ranges to an object that can be processed by a special data model. .. note:: You should always call this FB cyclic.

### FbMbBaseMaster
**Methods:**

#### QueryToTxFrame
#### Query_To_RtuFrame
### FbMbSlaveDataModel
|

**Methods:**

#### RegisterDataAccessListener
This method register a data access listener to this data model.

### FbMbServerUdp
This server provides access to a modbus datamodel with a ethernet connection and udp packages. It supports three types of frame selected by the input parameter ``eFrameType``. ========== ===================================================================================== ETHERNET Ethernet-Frame with leading modbus tcp header followed by modbus pdu without any crc RTU RTU-Frame with leading slaveaddress and crc at the end ASCII ASCII-Frame with leading slaveaddress and lrc at the end ========== ===================================================================================== The selected frame type will be transported by an udp package.

### FbMbServerTcp
This server provides access to a modbus datamodel with a TCP-Connection. It supports three types of frame selected by the input parameter ``eFrameType``. ========== ===================================================================================== ETHERNET Ethernet-Frame with leading modbus tcp header followed by modbus pdu without any crc RTU RTU-Frame with leading slaveaddress and crc at the end ASCII ASCII-Frame with leading slaveaddress and lrc at the end ========== ===================================================================================== The selected frame type will be transported by a tcp package. This server is able to hold multiple connections. The quantity of possible connection you can find at the parameter ``uiMultiConnect_NInstanceListSize`` at the library `WagoAppSocket`. You can see at the library manager.

### FbMbServerSerial
This server provides access to a modbus datamodel with a serial connection like RS232 or RS485. It supports two types of frame selected by the input parameter ``eFrameType``. ========== ===================================================================================== RTU RTU-Frame with leading slaveaddress and crc at the end ASCII ASCII-Frame with leading slaveaddress and lrc at the end ========== ===================================================================================== The selected frame type will be transported by a serial line.

**Methods:**

#### SynchronizeFrame
#### DeleteRxBuffer
### FbMbAccessInfo
This oject holds information about the last access to a Modbus Data Model. This object is an output from the data model.

### FbMbSimpleServerUdp
This function block provides Modbus UdP Slave functionality.

**Methods:**

#### RegisterDataAccessListener
This method register a data access listener to this data model.

### FbMbSimpleServerTcp
This function block provides Modbus TCP Slave functionality. This server is able to hold multiple connections. The quantity of possible connection you can find at the parameter ``uiMultiConnect_NInstanceListSize`` at the library `WagoAppSocket` (see at the library manager).

**Methods:**

#### RegisterDataAccessListener
This method register a data access listener to this data model.

### FbMbSimpleServerSerial
This function block provides modbus slave functionality by a serial line. It supports Modbus-RTU and Modbus-ASCII selected by the input parameter ``eFrameType``. ========== ===================================================================================== RTU RTU-Frame with leading slaveaddress and crc at the end ASCII ASCII-Frame with leading slaveaddress and lrc at the end ========== =====================================================================================

**Methods:**

#### RegisterDataAccessListener
This method register a data access listener to this data model.

### FbMbMasterTcp
This function block provides modbus master functionality. It supports three types of frame selected by the input parameter ``eFrameType``. ========== ===================================================================================== ETHERNET Ethernet-Frame with leading modbus tcp header followed by modbus pdu without any crc RTU RTU-Frame with leading slaveaddress and crc at the end ASCII ASCII-Frame with leading slaveaddress and lrc at the end ========== ===================================================================================== The selected frame type will be transported by a tcp package. Follow modbus function codes are supported +--------------+-------------------------------------------------+ |

### FbMbMasterSerial
This function block provides modbus master functionality over a serial line. It supports Modbus-RTU or Modbus-ASCII. You can select the protocol type by the input parameter ``eFrameType``. Follow function codes are supported +--------------+-------------------------------------------------+ |

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbMbMasterMultiQueryTcp: FbMbMasterMultiQueryTcp;
END_VAR

// Basic function block usage
fbFbMbMasterMultiQueryTcp(
    // Configure inputs as needed
);

// Check status
IF fbFbMbMasterMultiQueryTcp.xValid THEN
    // Operation successful
END_IF

IF fbFbMbMasterMultiQueryTcp.xError THEN
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

