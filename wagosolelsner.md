# WagoSolElsner v1.0.1.4

## Overview
WAGO PLC library providing WagoSolElsner functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbUniversalWeatherStation
**Description:**
``I_Port`` must be connected with the serial interface for example: ``IoConfig_Globals.RS232_485_Interface`` The functions block works with the following default settings of the elsner weather station: - Connection: RS485- Half duplex - Slave address: 1 - Baudrate: 19200 - Data bits: 8 - Parity: None - Stop bits: 1 Datas of the weather station will be output in the structure ``typUniversalWeatherStation``. The output values depends on the connected weather station. .. note:: It is recommended to use a 750-652 module as serial interface. If a 750-653/000-003 module will be used, it is necessary to set the program task between 10-30 ms. Otherwise the connection will be lost. ERROR Description/ Trouble shooting: - Watchdog has triggered: No FbSerialInterface to weather station. Turn A and B, set terminal resistances or install a BIASING network(Pull-Up / Pull down resistors). Check cable. - Checksum error: No valid telegram received wait a minute until a valid telegram is received.

### FbMultipleWeatherStation
**Description:**
``I_Port`` must be connected with the serial interface for example: ``IoConfig_Globals.RS232_485_Interface`` The array ``atypWeatherStation`` includes all measured values from the weather stations.

### FbSingleWeatherStation
**Description:**
``I_Port`` must be connected with the serial interface for example: ``IoConfig_Globals.RS232_485_Interface`` Add the modbus slave address of the weather station on ``bSlaveID``. The datas of the weather station will be output on the structure ``typWeatherStation``.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbUniversalWeatherStation: FbUniversalWeatherStation;
END_VAR

// Basic function block usage
fbFbUniversalWeatherStation(
    // Configure inputs as needed
);

// Check status
IF fbFbUniversalWeatherStation.xValid THEN
    // Operation successful
END_IF

IF fbFbUniversalWeatherStation.xError THEN
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

