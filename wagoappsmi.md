# WagoAppSMI v1.2.0.7

## Overview
WAGO PLC library providing WagoAppSMI functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbSMI_Write_Par
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command for writing a ``dwParameter`` slave parameter is sent by a rising edge at the ``xStart`` input. This requires the designation of the parameter address ``wPar_Addr`` and the length ``bLength`` of the parameter value. Parameters are either 1 byte, 2 bytes or 4 bytes. The three inputs ``xManufacturer``, ``bAddress`` and ``wGroup`` define whether the function block communicates with one or several SMI slaves. The following addressing types are possible: - Broadcast xManufacturer

### FbSMI_Read_Par
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command for reading out a slave parameter is sent by a rising edge at the ``xStart`` input. This requires the designation of the parameter address (``wPar_Addr``) and the length (``bLength``) of the parameter value. Parameters are either 1 byte, 2 bytes or 4 bytes. Reading out the values is only possible in random addressing. The slave address (0-15) that is to be read out is indicated at the ``bAddress`` input. The ``dwParameter`` output returns the read out parameter value of the SMI slave. Communication with the SMI interface is activated when the ``xReady`` output is FALSE. After the communication is completed, the output switches to the TRUE signal. An error can be identified by the current communication status as displayed at output ``sStatus``. .. note:: The input ``xRepeatable`` set to false is only valid from SMI-master-module-FW-version 01.02.00.

### FbSMI_Motor
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The two inputs ``bAddress`` and ``wGroup`` define whether the function block communicates with one or several SMI slaves. Performing group addressing is prioritized. The following addressing types are possible: - Random addressing bAddress

### FbSMI_Write_Pos2
### FbSMI_Write_Pos1
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command is sent by a rising edge at the ``xStart`` input. The three inputs ``xManufacturer``, ``bAddress`` and ``wGroup`` define whether the function block communicates with one or several SMI slaves. The following addressing types are possible: - Broadcast xManufacturer

### FbSMI_Step_Up
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command is sent by a rising edge at the ``xStart`` input. The three inputs ``xManufacturer``, ``bAddress`` and ``wGroup`` define whether the function block communicates with one or several SMI slaves. The following addressing types are possible: - Broadcast xManufacturer

### FbSMI_Step_Down
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command is sent by a rising edge at the ``xStart`` input. The three inputs ``xManufacturer``, ``bAddress`` and ``wGroup`` define whether the function block communicates with one or several SMI slaves. The following addressing types are possible: - Broadcast xManufacturer

### FbSMI_Read_Syn
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command for reading out the manufacturer ID and the motor type is sent by a rising edge at the ``xStart`` input. The manufacturer ID is displayed at the ``bManufac_ID`` output, and the motor type is displayed at the ``bMotor_Type`` output. Reading out these values is only possible in random addressing. The slave address (0-15) that is to be read out is indicated at the ``bAddress`` input. Communication with the SMI interface is activated when the ``xReady`` output is FALSE. After the communication is completed, the output switches to the TRUE signal. An error can be identified by the current communication status as displayed at output ``sStatus``. .. note:: The input ``xRepeatable`` set to false is only valid from SMI-master-module-FW-version 01.02.00.

### FbSMI_Read_Pos
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command for reading out the current position is sent to the SMI slave by a rising edge at the ``xStart`` input. The position value is displayed at the ``rPosition`` output. Reading out the position is only possible in random addressing. The slave address (0-15) that is to be read out is indicated at the ``bAddress`` input. Communication with the SMI interface is activated when the ``xReady`` output is FALSE. After the communication is completed, the output switches to the TRUE signal. An error can be identified by the current communication status as displayed at output ``sStatus``. .. note:: The input ``xRepeatable`` set to false is only valid from SMI-master-module-FW-version 01.02.00.

### FbSMI_Read_Pos2
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command for reading out the fixed position is sent by a rising edge at the ``xStart`` input. The position value is displayed at the ``rPosition`` output. Reading out the position is only possible in random addressing. The slave address (0-15) that is to be read out is indicated at the ``bAddress`` input. Communication with the SMI interface is activated when the ``xReady`` output is FALSE. After the communication is completed, the output switches to the TRUE signal. An error can be identified by the current communication status as displayed at output ``sStatus``. .. note:: The input ``xRepeatable`` set to false is only valid from SMI-master-module-FW-version 01.02.00.

### FbSMI_Read_Pos1
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command for reading out the fixed position is sent by a rising edge at the ``xStart`` input. The position value is displayed at the ``rPosition`` output. Reading out the position is only possible in random addressing. The slave address (0-15) that is to be read out is indicated at the ``bAddress`` input. Communication with the SMI interface is activated when the ``xReady`` output is FALSE. After the communication is completed, the output switches to the TRUE signal. An error can be identified by the current communication status as displayed at output ``sStatus``. .. note:: The input ``xRepeatable`` set to false is only valid from SMI-master-module-FW-version 01.02.00.

### FbSMI_Move_Pos_Turn
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. A sequence command (two commands in one telegram) is sent to the SMI drive by a rising edge at the ``xStart`` input. The commands are executed by the drive one after the other. First, the motion command occurs on the height position indicated at the ``rPosition`` input. The lamella opening angle is then adjusted to the angle set at the ``rRad`` input. The direction of the lamella adjustment is defined by the value at the ``xTurn_Up_Down`` input. The inputs ``xManufacturer`` and ``bAddress`` define whether the function block communicates with one or several SMI slaves. The following addressing types are possible: - Broadcast xManufacturer

### FbSMI_Move_Pos
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command is sent by a rising edge at the ``xStart`` input. The three inputs ``xManufacturer``, ``bAddress`` and ``wGroup`` define whether the function block communicates with one or several SMI slaves. The following addressing types are possible: - Broadcast xManufacturer

### FbSMI_Move_Pos2
**Description:**
If the command is sent, the drive is shifted to the configured position. The function block may only be used with the SMI master function block (``FbSMI_Master``). The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command is sent by a rising edge at the ``xStart`` input. The three inputs ``xManufacturer``, ``bAddress`` and ``wGroup`` define whether the function block communicates with one or several SMI slaves. The following addressing types are possible: - Broadcast xManufacturer

### FbSMI_Move_Pos1
**Description:**
If the command is sent, the motor is shifted to the configured position. The function block may only be used with the SMI master function block (``FbSMI_Master``). The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command is sent by a rising edge at the ``xStart`` input. The three inputs ``xManufacturer``, ``bAddress`` and ``wGroup`` define whether the function block communicates with one or several SMI slaves. The following addressing types are possible: - Broadcast xManufacturer

### FbSMI_Diagnostic
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The request for a diagnostic response is initiated by a rising edge at the ``xStart`` input. The inputs ``xManufacturer`` and ``bAddress`` define whether the function block communicates with one or several SMI slaves. The following addressing types are possible: - Broadcast xManufacturer

### FbSMI_SlaveId_Search
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input The command for searching for a SlaveID is sent by a rising edge at the ``xStart`` input. Manufacturer addressing must be used for this function block. The ``bManuf_Adr`` parameter defines the manufacturer's address. The SlaveID being sought must be specified at the ``dwSearch_ID`` input. The outputs ``xLT,`` ´´xGT`` and ``xEQ`` indicate whether there are motors in the SMI installation that have a shorter, longer or identical SlaveIDs as the number specified at the ``dwSearch_ID`` input. Relevant algorithms can therefore be used to identify all activated Slave_IDs of the SMI motors. The TRUE signal at the ``xNO_Adr`` output signals that all motors in the SMI installation have a slave address of 0. The system thus has an initialization stage, since the default slave address of the SMI motors is always 0 in its initial state. Communication with the SMI interface is activated when the ``xReady`` output is FALSE. After the communication is completed, the output switches to the TRUE signal. An error can be identified by the current communication status as displayed at output ``sStatus``.

### FbSMI_SlaveId_Read
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command for writing the slave address is sent by a rising edge at the ``xStart`` input. Manufacturer addressing must be used for this function block. The ``bManuf_Adr`` parameter defines the manufacturer's address. The necessary and unique 32 bit SlaveID of the motor must be entered at the ``dwSlave_ID`` input, and the new slave address is entered at the ``bSlave_Adr`` input. Communication with the SMI interface is activated when the ``xReady`` output is FALSE. After the communication is completed, the output switches to the TRUE signal. An error can be identified by the current communication status as displayed at output ``sStatus``.

### FbSMI_SystemImage
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The following functions are carried out by the function block in the order given below (if multiple queries are pending simultaneously): - If a rising edge is detected on the ``xWriteComments`` input, the command to write the comments contained in the ``typSMI_SlaveID`` input/output is sent. - If a rising edge is detected on the ``xReadSystemImage`` input, the command to read the system image is sent. - If a rising edge is detected on the ``xDeleteAddress`` input, the SMI address on the ``bAddress`` input is deleted from the system image if it was identified as missing from the SMI I/O module 163x by a cyclic scan. Communication with the SMI I/O module is enabled when the ``xReady`` output is FALSE. After the communication is completed, the output switches to TRUE. An error can be identified by the current communication status as displayed at output ``sStatus``.

### FbSMI_SlaveAdr_Write
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command for writing the slave address is sent by a rising edge at the ``xStart`` input. Manufacturer addressing must be used for this function block. The ``bManuf_Adr`` parameter defines the manufacturer's address. The necessary and unique 32 bit SlaveID of the motor must be entered at the ``dwSlave_ID`` input, and the new slave address is entered at the ``bSlave_Adr`` input. Communication with the SMI interface is activated when the ``xReady`` output is FALSE. After the communication is completed, the output switches to the TRUE signal. An error can be identified by the current communication status as displayed at output ``sStatus``.

### FbSMI_Addressing
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The following functions are carried out by the function block: - If a rising edge is identified at the ``xNewAddressing`` input, then all drives connected to the SMI interface are assigned an address (0-15). - When a rising edge is identified at input ``xExtendedAddressing``, only the SMI drives newly added are addressed. - An ongoing addressing process can be interrupted from a rising edge at input ``xReset``. - After automatic addressing is completed, the addresses can be manually swapped or moved to an open address. A rising edge at the input ``xSwap_Address`` means that the addresses specified at the inputs ``bSwapSlave_Adr_1`` and ``bSwapSlave_Adr_2`` are swapped. The ``typSMI_SlaveID`` variable contains a list in which the reference between the slave addresses (0-15) and the 32-bit SlaveIDs is represented. In addition, the list contains the manufacture ID of the drives and a possibly assigned comment. This is illustrated in the following:

### FbSMI_Up
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command is sent by a rising edge at the ``xStart`` input. The three inputs ``xManufacturer``, ``bAddress`` and ``wGroup`` define whether the function block communicates with one or several SMI slaves. The following addressing types are possible: - Broadcast xManufacturer

### FbSMI_Down
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command is sent by a rising edge at the ``xStart`` input. The three inputs ``xManufacturer``, ``bAddress`` and ``wGroup`` define whether the function block communicates with one or several SMI slaves. The following addressing types are possible: - Broadcast xManufacturer

### FbSMI_Stop
**Description:**
The relative number of the inserted SMI I/O module 753-163x is selected via the ``bPortSMI`` input. The command is sent by a rising edge at the ``xStart`` input. The three inputs ``xManufacturer``, ``bAddress`` and ``wGroup`` define whether the function block communicates with one or several SMI slaves. The following addressing types are possible: - Broadcast xManufacturer

### FbSMI_Master
**Description:**
The ``FBSMI_Master`` function block enables access to the WAGO-SMI-configurator while the PLC is running. ``I_Port`` must be connected with the SMI interface for example: ``IoConfig_Globals.SMI_Master230_VAC`` ``bPortSMI`` must be connect to the other function blocks. The SMI I/O module can be put into energy saving mode via the ``xEnableEnergySaverMode`` input. If this input is active, only SMI commands for motions are sent out. After a send out command the energy saving mode will be left by the module. To entry energy saving mode again a new rising edge via ``xEnableEnergySaverMode`` input is required. Via the ``xEnergySaverMode`` output, the current status of the energy saving mode of the SMI I/O module is displayed. The SMI I/O module can be put into energy saving mode via the ``xEnableEnergySaverMode`` input. If the SMI I/O module is in energy saving mode, you can exit energy saving mode via the following travel commands: - DOWN - UP - STOP - Step DOWN - Step UP - Move into position - Move into position 1 - Move into position 2 Sending additional SMI commands is disabled. If a travel command is sent, there must be a rising edge at the “xEnableEnergySaverMode” input to change the SMI I/O module to energy saving mode. An error can be identified by the current communication status as displayed at output ``sStatus``. The ``xStateDigIn`` output signals the status of the digital input of the SMI I/O module. .. note:: All SMI function blocks should be called up in cycles within the same program task as the ``FbSMI_Master`` function block. The assignment of SMI I/O modules to the FbSMI_Master module must be performed with constants; otherwise run-time errors can occur.

## Data Types

### typSMI_SlaveIDList
Structure type.

### typSMI_SlaveID
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbSMI_Write_Par: FbSMI_Write_Par;
END_VAR

// Basic function block usage
fbFbSMI_Write_Par(
    // Configure inputs as needed
);

// Check status
IF fbFbSMI_Write_Par.xValid THEN
    // Operation successful
END_IF

IF fbFbSMI_Write_Par.xError THEN
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

