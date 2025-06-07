# WagoAppPowerSupply v1.9.0.10

## Overview
WAGO PLC library providing WagoAppPowerSupply functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbPowerSupplyModbusEthernet
Handling power supply Pro 2 with "Modbus TCP" interface

**Description:**
This function block supports several methods to read and write configuration parameter. Additional status information will be continously updated and displayed at the function blocks outputs. Inputs ``xPowerSupplyOn`` and ``xDigitalOutputOn`` will only be used, if they are enabled by ``WriteOutputBehavior.xCtrlByPdOut``. A vizualisation template ``tpl2787_PowerSupplyModbus`` is available. .. note:: Checkbox "visible" and checkbox "Property handling in all element properties aktive" must be activated. This is located in "Project settings/visualization. .. note:: Checkbox "Sichtbar" und Checkbox "Eigenschaften-Behandlung in allen Elementeigenschaften aktivieren" muss angehakt seien. Diese Einstellungen werden unter den Projekteigenschaften/Visualisierung gefunden. .. note:: The placeholder ``myParameter`` is of type ``I_Visu`` therefore each instance of the function block ``FbPowerSupplyModbusEthernet`` may be applied .. note:: Modbus Udp will follow

**Methods:**

#### protAttachMbQuery
This method attach a Query to the link list of the master. For link the given ``IQuery`` there are some conditions. 1. The object input parameter ``FbDigitalTwinMbSlaveDevice.IMbMasterMultiQuery`` may not be NULL 2. ``IQuery`` may not be NULL 3. ``IQuery.eQueryState`` may not stay in one of the follow states * ``WagoAppPlcModbus.eQueryStatus.LOCKED_WAITING`` * ``WagoAppPlcModbus.eQueryStatus.LOCKED_ACTIVE`` Otherwise it is not linked. In case of successful link the method returns 1 otherwise it returns 0 .. note:: After the processing the query by the master the master automatical change the state of the query and remove it from link list.

#### onResponse
#### onError
#### ReadString
A method to read any string within the power supply

The maximum string length supported is 32 char

### xFbEnabled
### FbPowerSupplyModbusRTU
Handling power supply Pro 2 with "Modbus RTU" interface

**Description:**
This function block supports several methods to read and write configuration parameter. Additional status information will be continously updated and displayed at the function blocks outputs. Inputs ``xPowerSupplyOn`` and ``xDigitalOutputOn`` will only be used, if they are enabled by ``WriteOutputBehavior.xCtrlByPdOut``. A vizualisation template ``tpl2787_PowerSupplyModbus`` is available. .. note:: The placeholder ``myParameter`` is of type ``I_Visu`` therefore each instance of the function block ``FbPowerSupplyModbusRTU`` may be applied

**Methods:**

#### onResponse
#### onError
#### ReadString
A method to read any string within the power supply

The maximum string length supported is 32 char

### xFbEnabled
### FbtypSystemParameter
### FbtypOutputBehavior
### FbeModeSystemPowerBehavior
### FbeModeOutputBehavior
### FbeModeDigitalInputBehavior
### FbtypDigitalInputBehavior
### FbByte
### FbBinary
### FbtypDigitalOutputSetting
### FbTest
### xFbEnabled
### xFbEnabled
### FbPowerSupplyIOLink
Handling power supplies generation Pro 2 with IO-Link interface

**Description:**
This function block supports several methods to read and write configuration parameter. Additional some status information will be continously updated and displayed at the function blocks outputs. A vizualisation template ``tpl2787_PowerSupply_IOL`` is available. .. note:: The placeholder ``myFb`` is of type ``FbPowerSupplyIOLink`` Supported methods: -ReadCustomerCurrentThreshold (IOL Index 16#189) -ReadDigitalInputBehavior (IOL Index 16#1A8) -ReadDigitalOutputSetting (IOL Index 16#1B0) -ReadFuseDelay (IOL Index 16#195) -ReadFuseThreshold (IOL Index 16#194) -ReadIOL_Index Allow reading any IOL Index available by the device -ReadOutputBevior (IOL Index 16#18A) -ReadSetOutputVoltage (IOL Index 16#188) -ReadSwitchOnDelay (IOL Index 16#18B) -ReadSystemParameter (IOL Index 16#1BD) -ReadIOL_String Allow reading any IOL String available by the device -WriteCustomerCurrentThreshold (IOL Index 16#189) -WriteDigitalInputBehavior (IOL Index 16#1A8) -WriteDigitalOutputSetting (IOL Index 16#1B0) -WriteFuseDelay (IOL Index 16#195) -WriteFuseThreshold (IOL Index 16#194) -WriteIOL_Index Allow writing any IOL Index available by the device -WriteOutputBevior (IOL Index 16#18A) -WriteSetOutputVoltage (IOL Index 16#188) -WriteSwitchOnDelay (IOL Index 16#18B) -WriteSystemParameter (IOL Index 16#1BD) -WriteIOL_String Allow writing any IOL String available by the device If writing the configuration fails, output ``wStatus`` will show a number different than zero: 5: Error parameter ``FuseDelay`` 10: Error parameter ``CustomerCurrentThreshold`` 15: Error parameter ``DigitalInputBehavior`` 20: Error parameter ``DigitalOutputBehavior`` 25: Error parameter ``FuseThreshold`` 30: Error parameter ``OutputBehavior`` 35: Error parameter ``SetOutputVoltage`` 40: Error parameter ``SystemParameter`` 45: Error parameter ``OperatingHourLimit`` 50: Error parameter ``SwitchOnDelay``

**Methods:**

#### ReadIOL_Index_DWORD
A method to read any IO-link index within the power supply

Input ``xExecute`` will be reset by the method, if the IOL Call has been performed. In case of an error, output ``xError`` will become TRUE exactely one cycle. Additional output ``typError`` will show detailed error information while output ``xError`` is TRUE. Method return value ``ReadIOL_Index`` is latched after reading and can therefore be read even if the method is no longer executed.

#### ReadIOL_String
A method to read any IO-link string within the power supply

Input ``xExecute`` will be reset by the method, if the IOL Call has been performed. In case of an error, output ``xError`` will become TRUE exactely one cycle. Additional output ``typError`` will show detailed error information while output ``xError`` is TRUE. Method return value ``ReadIOL_String`` is the length of the string. The value is latched after reading and can therefore be read even if the method is no longer executed.

#### ReadIOL_Index
A method to read any IO-link index within the power supply

Input ``xExecute`` will be reset by the method, if the IOL Call has been performed. In case of an error, output ``xError`` will become TRUE exactely one cycle. Additional output ``typError`` will show detailed error information while output ``xError`` is TRUE. Method return value ``ReadIOL_Index`` is latched after reading and can therefore be read even if the method is no longer executed.

### Fb787_1675GetData
This function block reads the parameter from device 787-1675

**Description:**
The module is activated via the input ``xEnable``. The output ``xComPortOpen`` is set to True after the interface has been opened successfully. The output ``xDataValid`` is set to True if a valid data set has been received.

### Fb787_87xGetData
This function block reads the parameter from device 787-87x

**Description:**
The module is activated via the input ``xEnable``. The output ``xComPortOpen`` is set to True after the interface has been opened successfully. The output ``xDataValid`` is set to True if a valid data set has been received. Writing is not supported by this block.

### Fb787_86xGetData
This function block reads the parameter from device 787-86x

**Description:**
The module is activated via the input ``xEnable``. The output ``xComPortOpen`` is set to True after the interface has been opened successfully. The output ``xDataValid`` is set to True if a valid data set has been received. Writing is not supported by this block.

### Fb787_85xGetData
This function block reads the parameter from device 787-85x

**Description:**
The module is activated via the input ``xEnable``. The output ``xComPortOpen`` is set to True after the interface has been opened successfully. The output ``xDataValid`` is set to True if a valid data set has been received. Writing is not supported by this block.

## Data Types

### eModeOutputBehavior
Enumeration type.

### eModeDigitalInputBehavior
Enumeration type.

### eStatus
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbPowerSupplyModbusEthernet: FbPowerSupplyModbusEthernet;
END_VAR

// Basic function block usage
fbFbPowerSupplyModbusEthernet(
    // Configure inputs as needed
);

// Check status
IF fbFbPowerSupplyModbusEthernet.xValid THEN
    // Operation successful
END_IF

IF fbFbPowerSupplyModbusEthernet.xError THEN
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

