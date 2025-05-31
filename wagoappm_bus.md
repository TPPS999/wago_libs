# WagoAppM_Bus v1.2.2.8

## Overview
WAGO PLC library providing WagoAppM_Bus functionality.

**Key Features:**
- Communication protocols
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbMBusStatus
The function block is used to request the status from the M-Bus module. Query module status (C2M_STATUS_REQ)

**Description:**
``bPortMBus`` must be connect to the Master function blocks. The ``xStart`` variable starts the module request. If the request is successful, the function block resets the variable. If the request fails, the request is started again. This operation repeats three times by default. The ``g_MBUS_MAX_REPEAT`` global variable can be used to assign how many times the operation repeats. If the request is successful, the ``xUpdate`` output is triggered.

### FbMbusStatistic
The function block is used to request statistics from the M-Bus module. Query module status (C2M_INIT)

**Description:**
``bPortMBus`` must be connect to the Master function blocks. The ``xStart`` variable starts the module request. If the request is successful, the function block resets the variable. If the ``xStatisticReset`` variable is set to TRUE before the request, the module statistics are reset. If the request fails, the request is started again. This operation repeats three times by default. The ``g_MBUS_MAX_REPEAT`` global variable can be used to assign how many times the operation repeats. If the request is successful, the ``xUpdate`` output is triggered.

### FbMBusElectricity
The function block is used to read out and decode M-Bus electricity meter data. It can only be used in connection with the FbMBusMaster M-Bus communication block.

**Description:**
``bPortMBus`` must be connect to the Master function blocks. The ``dwAddress`` input variable is preset with the primary address (<256) or the secondary address (ID) (>

### FbMBusMultiTel
The function block is used to read out and decode the data of a M-Bus multi telegram It can only be used in connection with the M-Bus communication block FbMBusMaster.

**Description:**
``bPortMBus`` must be connect to the Master function blocks. The ``dwAddress`` input variable is preset with the primary address (<256) or the secondary address (ID) (>

### FbMBusHeat
The function block is used to read out and decode M-Bus heat meter data. It can only be used in connection with the M-Bus communication block FbMBusMaster.

**Description:**
``bPortMBus`` must be connect to the Master function blocks. The ``dwAddress`` input variable is preset with the primary address (<256) or the secondary address (ID) (>

### FbMBusWater
The function block is used to read out and decode M-Bus meter data. It can only be used in connection with the FbMBusMaster M-Bus communication block.

**Description:**
``bPortMBus`` must be connect to the Master function blocks. The ``dwAddress`` input variable is preset with the primary address (<256) or the secondary address (ID) (>

### FbMBusMaster
Master function block for communicating with WAGO M-Bus Module 753-649.

**Description:**
The controller independently detects the connected M-bus master modules and data is synchronise via the Interface I_Port to the other M-bus function blocks. ``I_Port`` must be connected with the serial interface for example: ``IoConfig_Globals.MBus_Master`` ``bPortMBus`` must be connect to the other function blocks. .. note:: This function block may be used only once per M-bus module.

### FbUnitConverter_LREAL
The function block unit converter is used to convert a M-Bus record into different types.

**Description:**
The function block is used to convert an M-Bus ``typMBRecord`` data set to a required ``eUnit`` target unit and a meter value of the LREAL type ``lrValue``. ``xError`` indicates whether the conversion into the target unit has been performed without error.

### FbUnitConverter
The function block unit converter is used to convert a M-Bus record into different types. .. note:: That the converted meter values may have rounding errors due to the REAL format. It is not possible to convert input values outside the range of >3 999 999 999

**Description:**
The function block is used to convert an M-Bus ``typMBRecord`` data set to a required ``eUnit`` target unit and a meter value of the REAL type ``rValue``. ``xError`` indicates whether the conversion into the target unit has been performed without error. .. note:: Please note that the converted meter values may have rounding errors due to the REAL format. It is not possible to convert input values outside the range of > 3 999 999 999

### FbMBusScanID
This function block scans the M-Bus network for devices by their identification number (ID). It can only be used in connection with the M-Bus communication block FbMBusMaster. ``bPortMBus`` must be connect to the Master function blocks. With ``xStart`` will start the scnning process and will be switched of by the function block if scanning was finished.

**Description:**
The scanning process will need some time, please wait until xStart is reset to false.

### FbMBusGeneral
The function block is used to read out and decode M-Bus meter data, it returns exactly one meter reading It can only be used in connection with the FbMBusMaster M-Bus communication block.

**Description:**
``bPortMBus`` must be connect to the Master function blocks. The ``dwAddress`` input variable is preset with the primary address (<256) or the secondary address (ID) (>

### FbMBusRawData
The function block is used to read out a M-Bus meter and returns the raw data without analyse in a byte array. Both a byte array with M-Bus raw data and the length of this array are contained in the output variables. It can only be used in connection with the M-Bus communication block FbMBusMaster.

**Description:**
``bPortMBus`` must be connect to the Master function blocks. The ``dwAddress`` input variable is preset with the primary address (<256) or the secondary address (ID) (>

### FbMBusMeter
Base class for a M-Bus Meter

**Methods:**

#### ForwardStatusObject
#### setClassname
#### setStatusObject
### FbMBusProtocol
Base class for a M-Bus Protocol

**Methods:**

#### ForwardStatusObject
#### setStatusObject
#### setClassname
### FbMBusCommunication
Base class for M-Bus communication block

**Methods:**

#### ForwardStatusObject
#### setClassname
#### setStatusObject
### FbMBusSendData
The function block is used to send out datas to an M-Bus meter. It can only be used in connection with the M-Bus communication block FbMBusMaster.

**Description:**
``bPortMBus`` must be connect to the Master function blocks. The ``dwAddress`` input variable is preset with the primary address (<256) or the secondary address (ID) (>

**Methods:**

#### ForwardStatusObject
#### setStatusObject
#### setClassname
## Usage Examples

### Basic Usage
```iec
VAR
    fbFbMBusStatus: FbMBusStatus;
END_VAR

// Basic function block usage
fbFbMBusStatus(
    // Configure inputs as needed
);

// Check status
IF fbFbMBusStatus.xValid THEN
    // Operation successful
END_IF

IF fbFbMBusStatus.xError THEN
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

