# WagoAppMP_Bus v1.1.4.4

## Overview
WAGO PLC library providing WagoAppMP_Bus functionality.

**Key Features:**
- Communication protocols
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbMpBusFlowMeter
This function block serves to query the Belimo flow meter (FM) This description is valid for models: +------------------------+-------------------------+ |

**Description:**
A rising edge at the ``xEnable`` input starts the query process at the flow meter addressed via the ``bAddress`` input. If the input signal ``xEnable`` is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The ``xReady`` output signal indicates whether the function block has completed the transmission process or if it is still actively connected to one of the slaves.

### FbMpBusEPIV_2way_valve
This function block serves to query and control the Belimo energy valve with thermal energy meter (TEM) This description is valid for models: +------------------------+-------------------------+ |

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the 2-way PI-Valve addressed via the ``bAddress`` input. If the input signal ``xEnable`` is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The 2-way PI-Valve can be controlled in manual operation at ``bSetOverride`` input. The current control signal can be over-ridden using manual operation. The value range for ``bSetOverride`` is documented in the data sheet (Data Pool Values) of the BELIMO drive. The following values can be used: - ``bSetOverride``

### FbMpBus_x_22RTx_19xxx_1
The function block is to communicate with the room sensor and room opearation units x_22RTx_19xxx_1 (from May 2022). The room sensor can be addressed and configured with the Belimo Assistant App.

**Description:**
To address the function block to the required MP-Bus module, the corresponding module index must be entered as a constant at the ``bModule_750_643`` input. The controller automatically recognizes the connected MP-Bus modules and counts them from the left, starting with 1. A rising edge at the "xEnable" input starts the transmission and query process on the drive addressed via the "bAddress" input. If the "xEnable" input signal is permanently switched to the TRUE signal, communication takes place cyclically. The "tCycleTime" input parameter determines the cycle time. The sensor can be configured with "typConfig_x_22RTx_19xxx_1``. - "xROU": True: P-22RTH-1900A-1, P-22RTM-1900A-1, P-22RT-1900D-1, P-22RTH-1900D-1, P-22RTM-1900D-1; False: 22RTM-19-1, 22RTH-19-1, 22RTM-19-1 (from May 2022) - "bSensorType": 5

### FbMpBusThermalEnergyMeter
This function block serves to query the Belimo Thermal Energy Meter This description is valid for models 22PE-...,22PEM-...

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the thermal energy meter addressed via the ``bAddress`` input. If the input signal ``xEnable`` is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The energy valve can be controlled in manual operation at ``bSetOverride`` input. The current control signal can be over-ridden using manual operation. The value range for ``bSetOverride`` is documented in the data sheet (Data Pool Values) of the BELIMO drive. The ``xReady`` output signal indicates whether the function block has completed the transmission process or if it is still actively connected to one of the slaves.

### FbMpBusEnergyValve_TEM
This function block serves to query and control the Belimo energy valve with thermal energy meter (TEM) This description is valid for models: +------------------------+-------------------------+ |

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the energy valve addressed via the ``bAddress`` input. If the input signal ``xEnable`` is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The energy valve can be controlled in manual operation at ``bSetOverride`` input. The current control signal can be over-ridden using manual operation. The value range for ``bSetOverride`` is documented in the data sheet (Data Pool Values) of the BELIMO drive. The following values can be used: - ``bSetOverride``

### FbMpBusVAV_Universal
This function block handles the query and control of the BELIMO VAV Universal actuators (e.g.VRU-D3, VRU-M1, VRU-M1R).

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the zone valve addressed at the ``bAddress`` input. If the input signal ``xEnable`` is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. A rising edge at the ``xReadConfig`` input causes a readout of the configuration parameters. The read values are written to the linked variable at the ``typConfigParameters`` input. The values of the configuration parameters are written to the zone valve by a rising edge at the ``xWriteConfig`` input. The ``xReady`` output signal indicates whether the function block has completed the transmission process or if it is still actively connected to one of the slaves.

### FbMpBus22Rxxx_19_1
The function block is to communicate with the room sensor 22R...-19-1. The room sensor can be addressed with the Belimo Assistant App.

**Description:**
To address the function block to the required MP-Bus module, the corresponding module index must be entered as a constant at the ``bModule_750_643`` input. The controller detects the connected MP-Bus modules independently and counts them starting with 1 from the left. A rising edge at the ``xEnable`` input starts the transmission and query process at the drive addressed via the ``bAddress`` input. If the ``xEnable`` input signal is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The sensor can be configured with „typConfig22Rxxx_19_1`` . The temperature value read is displayed at the ``rTemperature`` output. The current humidity, CO2, and dew point of the room are indicated at the ``rRelativeHumidity``, ``rCO2``, and „rDewPointTemp`` outputs respectively. „xDigitalInput`` displays tha ctual status oft he digital input oft he room sensor. Three possible error states of the combination sensor are indicated at the outputs: - ``xTemperatureSensorFault`` indicates that the temperature sensor is defective or unavailable. - ``xHumiditySensorFault`` indicates that the humidity sensor is defective/unavailable. - ``xCO2_SensorFault`` indicates that the CO2 sensor is defective/unavailable. The ``xReady`` output signal indicates whether the function block has completed the transmission process or if it is still actively connected to one of the slaves. Communication errors with the drive in question are displayed at the ``bfeedback`` output. For sensors before May 2022!

### FbMpBusEPIV_6way_valve
The function block is used for Electronic pressure independent 6-way characterised control valves using the MP-bus interface from BELIMO (e.g. Typ EP015R-R6+BAC).

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the zone valve addressed at the ``bAddress`` input. If the input signal ``xEnable`` is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The relative setpoint is specified at the ``rSetRelativeSetpoint`` input. Manual override is possible by the value at the ``bSetOverride`` input. The value range for ``bSetOverride`` is documented in the data sheet (Data Pool Values) of the BELIMO drive. The following values can be used: - ``bSetOverride``

### FbMpbusCommunication
Base class for MP-Bus communication block

**Methods:**

#### setClassname
#### setStatusObject
### FbMpBus_POKE
The function block is to set value via MP_POKE command

### FbMpBus_PEEK
The function block is to get value via MP_PEEK command

### FbMpBusSetDataPoolValues
The function block is to set data-pool values

**Description:**
The process data are stored in a so-called Data-Pool-Values data register. Each data register is designated by an identification number, which must be specified during writing by using the ``wID`` input. The size of the data register to be written is specified at the ``bSize`` input. Example: The setpoint of the P6065W800EV-BAC control ball valve is written (see figure below). The control ball valve has the address 4. .. image:: ../../Images/ConfigSetDataPoolValues_Example.png :align: center :alt: ConfigSetDataPoolValues example The following specifications are required to execute the write process: ``bAddress``

### FbMpBusGetDataPoolValues
The function block is to get data-pool values.

**Description:**
The process/configuration data are stored in a so-called Data-Pool-Values data register. Each data register is designated with an identification number, which must be specified for each query at the ``wID`` input. Setting the ``xGet`` variable to TRUE starts the query process at the device addressed using the ``bAddress`` input. If the query process is successful or is aborted, then the ``xGet`` input is reset by the module. The query process is carried out by the MP_Get_Data and the MP_Get_NextBlock commands at the corresponding data register. Example: The temperature of the MS24A-R08-MPX room sensor is queried (see figure below). The room sensor has the address 3. .. image:: ../../Images/ConfigGetDataPoolValues_Example.png :align: center :alt: ConfigGetDataPoolValues example The following specifications are required to execute the query process: ``bAddress``

### FbMpBusConfigDataPoolValues
The function block is to configure data-pool values. The configuration data is password protected.

**Description:**
The configuration data are stored in a so-called Data-Pool-Values data register. Each data register is designated with an identification number, which must be specified during the write process using the ``wID`` input. The size of the data register to be written is specified at the ``bSize`` input. Writing the configuration data is password protected. The password can be entered at the ``dwPassword`` input in order to enable access for writing the configuration data. The release is carried out by the MP-Log-in command. Example: The upper limit of the flow rate (Vmax) of the P6065W800EV-BAC control ball valve is configured (see figure below). The control ball valve has the address 4 and the preset password is ``16#0000``. .. image:: ../../Images/ConfigDataPoolValues_Example.png :align: center :alt: ConfigDataPoolValues example The following specifications are required to execute the configuration: ``bAddress``

### FbMpBusWindow
This function block serves to control the FLS window ventilation system.

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the drive addressed via the ``bAddress`` input. If the ``xEnable`` input signal is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The ``xManual`` input is used to distinguish between automatic mode and override. If ``xManual``

### FbMpBusVav
This function block handles the query and control of the BELIMO VAV control (e.g.NMV-D2M, VRP-M). The function block also handles the query and control 2-way valves (e.g. Typ EP015R+MP).

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the drive addressed via the ``bAddress`` input. If the input signal ``xEnable`` is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The setpoint for the volume quantity is specified via the value of the ``rAirVolume`` input. The volume flow quantity can be limited using the two input parameters ``rMinAirVolume`` (Vmin) and ``rMaxAirVolume`` (Vmax). The minimum limitation ``Vmin`` is specified depending on the value of the maximum limitation ``Vmax``. The value for the maximum limitation is specified depending on the nominal volume flow (Vnom). The nominal volume flow is specified by the box manufacturer. A rising edge signal at the ``xSet`` input causes the transmission of the ``rMinAirVolume`` and ``rMaxAirVolume`` values to the drive. A rising edge at the ``xRead`` input causes the reading of these values from the drive. They are available at the module as output variables ``rVmin`` and ``rVmax``. The current position of the drive ``rOutPosition`` and the actual value of the volume flow in percent ``rOutAirVolume_perc`` (with respect to the nominal volume of the volume flow regulator) are read out of the function block and displayed. Another important variable that is read out of the drive regulator is the current volume flow in m³/h ``rOutAirVolume_m3_h``. This value depends on the nominal volume flow, which is stored in the device as a parameter. Since most BELIMO drives support connection to multiple types of sensors, the sensor type must be communicated to the module via the ``bSensorType`` input. The sensor value read is displayed at the ``wSensorValue`` output. The switch status (sensor type 1) is evaluated as follows: 1 : open 0 : closed For active sensors (0 … 32 V), the measurement value is depicted as follows: ``wSensorValue`` 0 … 32000 mV. The following auxiliary functions can be used for temperature sensors: Fu_Ni1000 (-25 … 95 °C) Fu_NiI1000_LuS (-30 … 115 °C) Fu_NTC5K (-20 … 145 °C) Fu_Pt1000 (-35 … 155 °C) Three possible error states of the actuator are indicated via separate outputs at the function module. These concern the following errors: - TRUE signal at the ``xControlRangeIncreased`` output indicates that the control range of the drive has increased or that the end position has been exceeded. - TRUE signal at the ``xMechanicalOverload`` output means that the required target position could not be reached, e.g., due to mechanical overload. - TRUE signal at the ``xActuatorHunting`` output indicates that there are control oscillations. In this state, the control signal of the drive oscillates back and forth. The ``xReady`` output signal indicates whether the function block has completed the transmission process or if it is still actively connected to one of the slaves. Communication errors with the drive in question are displayed at the ``bfeedback`` output. If the module detects a fault (e.g., range exceeded) of the sensor signal, then the ``xSensorError`` output signal is set to the TRUE signal. A rising edge at the ``xReset`` input resets the error messages. It is possible to override the input setpoint for the volume flow using the ``xManualOpen`` and ``xManualClose`` input signals and to move the drive into the open or closed position using the so-called override control.

### FbMpBusTHC24
This function block handles the query and control of the BELIMO fire control and smoke exhaust control THC24.

### FbMpBusRoomSensor
The function block is to get value from a room sensor which supports MP data pool functional profiles. This module serves to query a room-combination sensor with an MP-bus interface from BELIMO (e.g., MS24A-Rxx-MPX) for measuring temperature, humidity, CO2, and VOC.

**Description:**
To address the function block to the required MP-Bus module, the corresponding module index must be entered as a constant at the ``bModule_750_643`` input. The controller detects the connected MP-Bus modules independently and counts them starting with 1 from the left. A rising edge at the ``xEnable`` input starts the transmission and query process at the drive addressed via the ``bAddress`` input. If the ``xEnable`` input signal is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The temperature value read is displayed at the ``rTemperature`` output. If the ``xShowTemperature_F`` input is set to TRUE, then the temperature is output in °F. Otherwise, the temperature value is displayed in °C. The current humidity, CO2, and VOC measurements, and the air quality are indicated at the ``rRelativeHumidity``, ``rCO2``, ``rVOC`` and ``bFlushStatus`` outputs respectively. Four possible error states of the combination sensor are indicated at the outputs: - ``xTemperatureSensorFault`` indicates that the temperature sensor is defective or unavailable. - ``xHumiditySensorFault`` indicates that the humidity sensor is defective/unavailable. - ``xCO2_SensorFault`` indicates that the CO2 sensor is defective/unavailable. - ``xVOC_SensorFault`` indicates that the VOC sensor is defective/unavailable. The ``xReady`` output signal indicates whether the function block has completed the transmission process or if it is still actively connected to one of the slaves.

### FbMpBusPTH_Sensor
This function block serves to query a PTH combination sensor for differential pressure, temperature, and humidity measurements

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the drive addressed via the ``bAddress`` input. If the ``xEnable`` input signal is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. Since the PTH sensor supports connection to multiple types of sensors, the sensor type must be communicated to the module via the ``bSensorType`` input. 0

### FbMpBusP_Sensor
This function block serves to query a P sensor for measurements of differential pressure.

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the drive addressed via the ``bAddress`` input. If the ``xEnable`` input signal is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. Since the pressure sensor supports connection to multiple types of sensors, the sensor type must be communicated to the module via the ``bSensorType`` input. 0

### FbMpBusUST5
This module serves to communicate with the UST-5 signal transmitter.

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the drive addressed via the ``bAddress`` input. If the ``xEnable`` input signal is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. To address the function block to the required MP-Bus module, the corresponding module index must be entered as a constant at the ``bModule_750_643`` input. The controller detects the connected MP-Bus modules independently and counts them starting with 1 from the left. The ``rAnalogOutputVoltage1`` and ``rAnalogOutputVoltage2`` inputs specify the voltage for the AO1 and AO2 analog outputs respectively. The three relays (DO1 to DO3) at the UST-5 device can be controlled using the ``xDigitalOutput1``, ``xDigitalOutput2`` and ``xDigitalOutput3`` inputs. The status of the digital inputs is displayed at the ``xDigitalInput1``, ``xDigitalInput2``, ``xDigitalInput3``, ``xDigitalInput4`` and ``xDigitalInput5`` outputs. Since the UST5 signal transmitter supports different measurement ranges, the measurement types of the analog inputs (ADi1 to ADi3) are defined via the ``bSetMeasurementType`` input and displayed to check for accuracy at the ``bMeasurementType`` output. Bit 0 and Bit 1

### FbMpBusSmokeDamper
This function block handles the query and control of the BELIMO smoke and fire protection drives with spring return (e.g. BF24TL).

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the drive addressed via the ``bAddress`` input. If the ``xEnable`` input signal is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The ``xOpenDamper`` input signal controls the opening and closing of the fire protection damper. The TRUE signal at the ``xOpenDamper`` input causes the drive to open the damper by means of the override function. In this case, the drive runs until it reaches the adapted end position or ``Override 100 %`` (runtime 140 s). Due to an increasing slope on the input ``xTest,`` the fire protection damper test run is carried out. The test includes passing through the entire angle range of the damper from the lower to the upper end stop. If the damper does not reach the end position within a nominal runtime, a ``xMechanicalOverload`` error message appears. Via the output ``xDamperTest`` there is an indication of whether the fire protection damper test run is currently active. The ``xOpen`` and ``xClose`` outputs indicate whether the drive is in the open or closed position. The ``xReady`` output signal indicates whether the function block has completed the transmission process or if it is still actively connected to one of the slaves. Communication errors with the drive in question are displayed at the ``bfeedback`` output. A rising edge at the ``xReset`` input resets the error messages.

### FbMpBusUST3
This module serves to communicate with the UST-3 signal transmitter.

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the drive addressed via the ``bAddress`` input. If the ``xEnable`` input signal is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The ``rOutputVoltage`` input specifies the voltage for the analog output. The three relays at the UST-3 device can be controlled using the ``xDigitalOutput1``, ``xDigitalOutput2`` and ``xDigitalOutput3`` inputs. Since the UST3 signal transmitter supports different measurement ranges, the measurement range of the analog inputs is defined via the ``bSetMeasurementRange`` input and for checking it is displayed at the ``bMeasurementRange`` output. Bit 0

### FbMpBusSensor
Base class for a MP-Bus sensor

### FbMpbusMaster
Master function block for communicating with WAGO MP-Bus Module 750-643.

**Description:**
The controller independently detects the connected MP-bus master modules and data is synchronise via the Interface I_Port. ``I_Port`` must be connected with the serial interface for example: ``IoConfig_Globals.MP_Bus_Master`` ``bPortMPBus`` must be connect to the other function blocks. .. note:: This function block may be used only once per MP-bus master module.

### FbMpBusDamperAndValveActuator_MPL
This function block serves to query and control the rotary drive zone using the MP-bus interface from BELIMO (e.g. CQ24A).

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the drive addressed via the ``bAddress`` input. If the ``xEnable`` input signal is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The setpoint for the rotational angle is specified by the ``rPosition`` input value and sent to the drive. The current position of the drive is read by the function block and provided at the ``rOutPosition`` output. The output signal ``xReady`` indicates whether the function block has completed the transmission process or if it is still connected to one of the slaves. .. note:: When using MPL valve actuators exclusively, up to 16 of the devices can be operated on the MP-Bus Master (750-643).

### FbMpBusGenericDataTransfer
Base class for generic data transfer

**Methods:**

#### setClassname
#### setStatusObject
### FbWord2Bytes
Mp bus auxillary function

### FbMpBusAddressing
By using this function block, the connected MP-bus drive can be assigned with a unique MP-bus address.

**Description:**
The addressing can be performed in two different ways: Type 1:

**Methods:**

#### setStatusObject
#### setClassname
### FbMpBusCommand
This function block is used to send single MP commands. #. Up to 7 read bytes. (aData). #. Up to 6 send bytes (aMpData).

**Description:**
Not supported command(bCMD): #. CMD_SET_DATA (To set data to the data pool) #. CMD_GET_DATA (To read data from the data pool ) #. CMD_SET_NEXTBLOCK (To set long data to the data pool ) #. CMD_GET_NEXTBLOCK (To read long data from the data pool ) .. note:: May not support third party MP Commands.

**Methods:**

#### setClassname
#### setStatusObject
### FbMpBusDataPoolValues
Base class for data pool device

**Methods:**

#### setClassname
#### setStatusObject
### FbMpBusEnergyValve
This function block serves to query and control the control ball valve using the MP-bus interface from BELIMO (e.g. EV...R+(K)BAC, EV...R3+BAC or EV..F+(K)BAC ). +------------------------+-------------------------+ |

**Description:**
A rising edge at the ``xEnable`` input starts the transmission and query process at the control ball valve addressed via the ``bAddress`` input. If the input signal ``xEnable`` is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The setpoint for the rotational angle or for the flow rate is specified by the ``rSetRelativeSetpoint`` input value and sent to the control ball valve. The actual position of the control ball valve is read by the function block and provided at the ``rRelativePosition`` output. The ``rAbsolutePosition`` output shows the current opening angle of the valve. The flow rate of the valve can be read at the ``rAbsoluteFlow`` output. The ``rAbsoluteFlow`` output shows the flow rate difference as a percentage value. The control ball valve can be controlled in manual operation at ``bSetOverride`` input. The current control signal can be over-ridden using manual operation. The value range for ``bSetOverride`` is documented in the data sheet (Data Pool Values) of the BELIMO drive. Example: - ``bSetOverride``

### FbMpBusActuator
Base class for MP-Bus actuator

### FbAddJob2List
Mp bus auxillary function

### FbMpBusHandler
Mp bus handler

### FbMpBusDamperAndLinearActuator
This function block serves to query and control the rotary damper and linear actuator with MP-bus interface from BELIMO (e.g. NM, AM, GM, LF, AF, NV, AV, NVS, AVS).

**Description:**
This module serves to query and control the rotary damper and linear actuator with MP-bus interface from BELIMO (e.g., NM, AM, GM, LF, AF, NV, AV, NVS, AVS). A rising edge at the ``xEnable`` input starts the transmission and query process at the drive addressed via the ``bAddress`` input. If the input signal ``xEnable`` is permanently switched to the TRUE signal, then communication occurs cyclically. The ``tCycleTime`` input parameter determines the cycle time. The setpoint for the rotational angle of the damper or for the stroke of the valve drive is specified by the ``rPosition`` input value and sent to the drive. The current position of the drive is read by the function block and provided at the ``rOutPosition`` output. Since most MP-Bus drives support the connection to multiple types of sensors, the sensor type must be communicated to the module via the ``bSensorType`` input. The sensor value read is displayed at the ``wSensorValue`` output. The switch status (sensor type 1) is evaluated as follows: 1 : open 0 : closed For active sensors (0 – 32 V), the measurement value is depicted as follows: ``wSensorValue`` 0 – 32000 mV. The following auxiliary functions can be used for temperature sensors: Fu_Ni1000 (-25 … 95 °C) Fu_Ni1000_LuS (-30 … 115 °C) Fu_NTC5K (-20 … 145 °C) Fu_Pt1000 (-35 … 155 °C) The output signal ``xReady`` indicates whether the function block has completed the transmission process or if it is still connected to one of the slaves. Communication errors with the drive in question are displayed at the ``bfeedback`` output. If the module detects a fault (e.g., range exceeded) of the sensor signal, then the ``xSensorError`` output signal is set to the TRUE signal. Three possible error states of the actuator are indicated via separate outputs at the function module. These concern the following errors: - TRUE signal at the ``xControlRangeIncreased`` output indicates that the control range of the drive has increased or that the end position has been exceeded. - TRUE signal at the ``MechanicalOverload`` output means that the required target position could not be reached, e.g., due to mechanical overload. - TRUE signal at the ``xActuatorHunting`` output indicates that there are control oscillations. In this state, the control signal of the drive oscillates back and forth. A rising edge at the ``xReset`` input resets the error messages. .. note:: The ``xActuatorHunting`` error message can only be permanently cleared by resetting the internal operating hours counter for the drive. This reset is possible if the relationship between runtime and total operating time does not exceed a particular value.

### FbMpBusDevice
Base class for a MP-Bus device

**Methods:**

#### setClassname
#### setStatusObject
### FbIncreaseJobTail
Mp bus auxillary function

## Data Types

### eMpBusMacro
Enumeration type.

### eMpBusMesssageCode
Enumeration type.

### eMpBusCommand
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbMpBusFlowMeter: FbMpBusFlowMeter;
END_VAR

// Basic function block usage
fbFbMpBusFlowMeter(
    // Configure inputs as needed
);

// Check status
IF fbFbMpBusFlowMeter.xValid THEN
    // Operation successful
END_IF

IF fbFbMpBusFlowMeter.xError THEN
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

