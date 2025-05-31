# WagoSolThermokon v1.2.0.3

## Overview
WAGO PLC library providing WagoSolThermokon functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbShortLongButtonBlind
### FbShortLongButtonLight
### FbNovos3_5_Config
Function block to configurate Thermokon Novos 5 and Novos 3 slaves by the Visualization "VisuNovos3_5_Config".

**Description:**
Function block to configurate Novos 5 and Novos 3 slaves. This function block only works with the "VisuNovos3_5_Config" visualization. Only one config function block is needed for all Novos 5 and Novos 3 slaves on a serial interface. Please change the baudrate of the slaves to 9600 baud or set the globale variable ``WagoSolThermokon.Globale_Variablen.udiBaudrate`` to the baudrate of the slave. Baudrate can be changed with the DIP-switches 7/8. .. note:: It is recommended to set termination and bias resistors!

### FbNovos3
Function block to communicate with a Thermokon Novos 3 slave.

**Description:**
Function block for the communication between one Novos 3 and the WAGO controller. For each NOVOS-Slave one of those Function block is needed. Please change the baudrate of the slaves to 9600 baud or set the globale variable ``WagoSolThermokon.Globale_Variablen.udiBaudrate`` to the baudrate of the slave. Baudrate can be changed with the DIP-switches 7/8 on the Novos slave. .. note:: It is recommended to set termination and bias resistors! The function block will need 350ms to read out the slave with a baud rate of 9600 (750-652 (24 byte)). The reading takes 275ms with a baud rate of 38400 (750-652 (24 byte)).

### FbNovos5
Function block to communicate with a Thermokon Novos 5 slave.

**Description:**
Function block for the communication between one Novos 5 and the WAGO controller. For each NOVOS-Slave one of those Function block is needed. Please change the baudrate of the slaves to 9600 baud or set the globale variable ``WagoSolThermokon.Globale_Variablen.udiBaudrate`` to the baudrate of the slave. Baudrate can be changed with the DIP-switches 7/8 on the Novos slave. .. note:: It is recommended to set termination and bias resistors! The function block will need 350ms to read out the slave with a baud rate of 9600 (750-652 (24 byte)). The reading takes 275ms with a baud rate of 38400 (750-652 (24 byte)).

### FbNovos7_TouchEVO_Config
Function block to configurate Thermokon Novos 7/ Novos Touch or Thanos EVO slaves by the visualization ``VisuNovos7_TouchEVO_Config``.

**Description:**
Function block to configurate Novos 7/ Novos Touch and Thanos EVO slaves. This function block only works with the visualization ``VisuNovos7_TouchEVO_Config``. Only one config function block is needed for all Novos7/ Novos Touch and Thanos EVO slaves on a serial interface. Please change the baudrate of the slaves to 9600 baud or set the globale variable ``WagoSolThermokon.Globale_Variablen.udiBaudrate`` to the baudrate of the slave. Baudrate can be changed in the settings menu of the NOVOS device, the standard-PIN is ``2030``. .. note:: It is recommended to set termination and bias resistors!

### FbNovos7_TouchEVO
Function block to communicate with a Thermokon Novos 7/ Novos Touch or Thanos EVO module.

**Description:**
Function block for the communication between one NOVOS-Slave and the WAGO controller. For each NOVOS-Slave one of those Function block is needed. Please change the baudrate of the slaves to 9600 baud or set the globale variable ``WagoSolThermokon.Globale_Variablen.udiBaudrate`` to the baudrate of the slave. Baudrate can be changed in the settings menu of the NOVOS device, the standard-PIN is ``2030``. The Output ``typLightButton`` can be used to connect other function blocks like DALI or SMI function blocks. .. note:: It is recommended to set termination and bias resistors! The function block will need 350ms to read out the slave with a baud rate of 9600 (750-652 (24 byte)). The reading takes 275ms with a baud rate of 38400 (750-652 (24 byte)).

### FbJOYextended
Function block to communicate with a Thermokon JOY device. Please change baudrate of the JOY device to 9600.

**Description:**
Function Block for the communication between one JOY-Slave and the WAGO controller. For each JOY-Slave one of those Function Block is needed. Please change baudrate of the JOY device to 9600.

### FbJOY
Function block to communicate with a Thermokon JOY module. Please change baudrate of the JOY device to 9600.

**Description:**
Function Block for the communication between one JOY-Slave and the WAGO controller. For each JOY-Slave one of those Function Block is needed. Open the JOY menue by pressing the upper and lower button on the device for more than 3 seconds. Please change the baudrate of the JOY device to 9600 and wait 2 minutes, the JOY device will restart. A continuous TRUE signal at the ``xEnable`` input activates the readout process, and a FALSE signal deactivates it. ``bPortThermokon`` must be connect to ``bPortThermokon`` of the Master function block. The device address is specified at the ``bSlaveNo`` input. By assigning different addresses, you can address multiple devices via one serial I/O module. This input is assigned ``1`` by default. ``dtActualTime`` is used for displaying the date and time on the JOY device. The actual time of the controller can be read out by using the library SysLibRTC. Input ``rBasicSetpoint`` forms the setpoint basis for ``rSetpointTemperature``. If the input ``xSetSetpointAdjustment_In`` are TRUE, the setpoint value ``rSetpointAdjustment_In`` will override the setpoint values ``rSetpointAdjustment_Out``. For example to reset the setpoint to a basic setting. The local operation can be deactivated via``xDisableLocalControl``. To identify an error, the current error code is displayed at the output ``sStatus``. The actual measured room temperature will be outputted on ``rRoomTemperature``. The current setpoint temperature is output on ``rSetpointTemperature`` and the temperature adjustement on ``rSetpointAdjustment_Out``. ``rFanStage`` outputs in steps (typJOY.rStepsFanControl ) the actual fan stage 0-100% and -256

### FbWRF04extended
Function block to communicate with a Thermokon WRF04 module.

**Description:**
Function Block for the communication between one WRF04-Slave and the WAGO controller. For each WRF04-Slave one of those function block is needed.

### FbWRF07extended
Function block to communicate with a Thermokon WRF07 module.

**Description:**
Function Block for the communication between one WRF07-Slave and the WAGO controller. For each WRF07-Slave one of those function block is needed.

### FbWRF07
Function block to communicate with a Thermokon WRF07 module. The FbWRF07 function block is used to output the current values of a room operating panel. In addition, this function block can be used to change the values of the input register.

**Description:**
A permanent TRUE signal at the input ``xEnable`` enables the output process and a FALSE signal disables it. If the input is not enabled, the output process starts automatically. ``bPortThermokon`` must be connect to ``bPortThermokon`` of the Master function block. The device address is specified at the input ``bSlaveNo.`` By assigning different addresses, multiple devices can be addressed via one serial I/O module. This input is assigned with ``1`` by default. The minimum interval time to be maintained for outputs is determined at the input ``tCycleTime.`` The actual time between the outputs can be greater depending on the number of instantiated output modules on one Modbus® line. As default, no time is set; this ensures operation is as fast as possible. The respective WRF07 can be individually configured with the input structure ``typConfigParameters.`` The configuration values are saved in the WRF EEPROM. Cyclic writing of these values can destroy the room operating panel. The ``sStatus`` output displays the communication error that has occurred. As soon as the presence button on the WRF is pressed, the output ``xPresence`` is switched on for the time TRUE set in ``typConfigParameters.tPresenceTime.`` Whether pressing the button again will restart the presence time can be selected through ``typConfigParameters.xRetriggerPresence.`` The room temperature ``rRoomTemperature`` and the set setpoint correction ``rSetpointCorrection`` can be read out from the outputs on the module.

### FbWRF04
The FbWRF04 function block is used to output the current values of a room operating panel. In addition, this function block can be used to change the values of the input register.

**Description:**
Function Block for the communication between one WRF04-Slave and the WAGO controller. For each WRF04-Slave one of those Function Block is needed. A permanent TRUE signal at the input ``xEnable`` enables the output process and a FALSE signal disables it. If the input is not enabled, the output process starts automatically. ``bPortThermokon`` must be connect to ``bPortThermokon`` of the Master function block. The device address is specified at the input ``bSlaveNo.`` By assigning different addresses, multiple devices can be addressed via one serial I/O module. This input is assigned with ``1`` by default. The minimum interval time to be maintained for outputs is determined at the input ``tCycleTime.`` The actual time between the outputs can be greater depending on the number of instantiated output modules on one Modbus® line. As default, no time is set; this ensures operation is as fast as possible. The respective WRF04 can be individually configured with the input structure ``typConfigParameters.`` The configuration values are saved in the WRF EEPROM. Cyclic writing of these values can destroy the room operating panel. The ``sStatus`` output displays the communication error that has occurred. As soon as the presence button on the WRF is pressed, the output ``xPresence`` is switched on for the time TRUE set in ``typConfigWRF04.tPresenceTime.`` Whether pressing the button again will restart the presence time can be selected through ``typConfigParameters.xRetriggerPresence.`` The room temperature ``rRoomTemperature`` and the set setpoint correction ``rSetpointCorrection`` can be read out from the outputs on the module. If the WRF04 has a potentiometer for the fan stage, the currently set fan stage can be taken from the output structure ``typFanLevel.``

### FbThanosModbusData
The FbThanosModbusData function block is used to send user-specific MODBUS commands to the Thanos room operating panel. It can be used to make changes in or to read the registers of the room operating panels specifically. The ModbusDataThanos visualization interface is used to control communication with the room operating panels.

**Description:**
Function Block for send User Modbus data, only one of these FB is needed. The ModbusDataThanos visualization can be used to transfer MODBUS commands to the room operating panel.

### FbWRF08
The FbWRF08 is used to specify the display values to be displayed on the multifunction room operating unit display. In addition, the current status of the room operating unit is read out.

**Description:**
The ``xEnable`` input enables cyclic reading of the status values from the room operating unit. ``bPortThermokon`` must be connect to ``bPortThermokon`` of the Master function block. The ``bSlaveNo`` input specifies the slave address of the WRF08 room operating unit. The function block transmits the display values when there is a change in the ``typConfigParameters`` structure or when a button is pressed. The ``tCycleTime`` input specifies the minimum time interval for sending new display values. The ``tUpdateClock`` input specifies the interval for synchronizing the time. The time is specified at the ``dtActualTime`` input, with which the room operating unit should be synchronized. The time is not synchronized if the update time is t#0s. A communication error can be identified by the error code displayed at the ``sStatus`` output. The ``xButton1`` to ``xButton12`` outputs display the status of the buttons of the room operating unit. The ``rRoomTemperature`` output displays the room temperature measured by the WRF08 room operating unit. The current setpoints & offset from the room operating unit are displayed in the ``typValueWRF08`` structure. In addition, the fan level and the status of the room occupancy are displayed.

### FbWRF06
The FbWRF06 is used to read the current values of a room operating unit. In addition, this function block can be used to change the values of the input register.

**Description:**
Function Block to communicate with a WRF06-Slave module. For each WRF06-Slave one of those funktion block is needed. The ``xEnable`` input enables cyclic reading of the values and writing of the parameters. The ``eDeviceType`` input specifies the device type. The ``bSlaveNo`` input specifies the address of the WRF06 room operating unit. When a value is changed at the ``typConfigParameters`` input or if the input value of ``bRefresh`` > 2#00000000, the function block sends the values at the ``typConfigParameters`` input to the room operating unit. The ``tUpdateClock`` input specifies the interval for synchronizing the time. The time is specified at the ``dtActualTime`` input, with which the room operating unit should be synchronized. The time is not synchronized if the update time is t#0s. The ``sStatus`` output displays the communication error that has occurred. The output values of the room operating unit are displayed in the form of a data structure at the ``typValueWRF06`` output. .. note:: Configuration of of the output values for the digital outputs is important for interpretation of the signals (see WRF06 Configuration Interface (ConfigWRF06)). .. note:: The type of room operating unit must be set at the ``enumDeviceType`` input. Otherwise, the evaluation if necessary cannot be carried out correctly. The supported device types or input assignments are: typ_2V, typ_DI4, typ_AO2V, typ_DO2R, typ_DO2T, typ_OVR, typ_OVT, typ_2VPS, typ_AOV, typ_AOFV, typ_VSS, typ_VNS, typ_AOK.

### FbThanos
The FbThanos function block is used to read the current values of a room operating panel. In addition, this function block can be used to change the values of the input register.

**Description:**
The ``xEnable`` input enables the function block. ``bPortThermokon`` must be connect to ``bPortThermokon`` of the Master function block. The ``bSlaveNo`` input specifies the MODBUS address of the Thanos room operating panel. The ``typConfigParameters.wRefreshInput`` input can be used to write the values at the respective inputs to the input register of the room operating panel. ``typConfigParameters.xRefreshInputBits`` triggers the transfer of values at the ``typConfigParameters.typThanosInputBits`` input. After successful transfer of the input values, the respective statuses of ``typConfigParameters.wRefreshInput`` and ``typConfigParameters.wRefreshInput`` are again reset. The ``sStatus`` output displays the communication error that has occurred. The status of the room operating panel can be evaluated via the outputs available at the function block. .. note:: - Configuration of the output values for the digital outputs is important for interpretation of the signals. - Not all outputs of the room operating panel except the buttons and digital inputs if necessary are read in each program cycle. - The input values are only transferred when requested (see ``typConfigParameters.wRefreshInput`` and ``typConfigParameters.xRefreshInputBits`` inputs).

### FbWRF08Config
The FbWRF08Config function block is used to configure the WRF08 multifunction room operating units (WRF08-RS-485 Modbus®). The room operating units can only be configured in conjunction with the ConfigWRF08 visualization interface.

**Description:**
Function Block for the configuration of your WRF08 slaves. This function block only works with the "ConfigWRF08 visualisation". Only one config function block is needed for all WRF08 Slaves.

### FbWRF06Config
Function block to configurate the WRF06 modules by the Visualisation "ConfigWRF06". The FbWRF06Config function block is used to configure the WRF06 multifunction room operating units (WRF06LCD RS485 Modbus). The room operating units can only be configured in conjunction with the ConfigWRF06 visualization interface contained in the library.

**Description:**
Function Block for the configuration of your WRF06 slaves. This function block only works with the "ConfigWRF06". Only one config function block is needed for all WRF06 Slaves.

### FbThermokonMaster
Master function block for all Thermokon slave function blocks and modules.

**Description:**
Thermokon Modbus Master for the Modbus communication between the WAGO-Controller and the Thermokon slaves via a RS-485 serial interface module. Only one of these Function block is needed for each modbus line. ``I_Port`` must be connected with the serial interface for example: ``IoConfig_Globals.RS232_485_Interface`` ``bPortThermokon`` must be connect to the other function blocks. .. note:: Default physical layer

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbShortLongButtonBlind: FbShortLongButtonBlind;
END_VAR

// Basic function block usage
fbFbShortLongButtonBlind(
    // Configure inputs as needed
);

// Check status
IF fbFbShortLongButtonBlind.xValid THEN
    // Operation successful
END_IF

IF fbFbShortLongButtonBlind.xError THEN
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

