# WagoAppEnergyDevices v2.0.4.0

## Overview
WAGO PLC library providing WagoAppEnergyDevices functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbSunnyIsland
### FbWalm
### FbIki23
### FbChargePilot
Function block to communicate with a TMH ChargePilot. Protocoll: Modbus TCP & RTU

### FbDataManager
### FbIec60870Base
### FbSmart1
### FbNA011
### FbUmd
### FbComPass
**Methods:**

#### decodeEvent
#### adjustRequestsToVersion
#### mPrepareData
#### mTransferData
#### decodeSystemData
### FbMenckeTegtmeyer
### FbMID30x0
### FbEOnModbus
### FbGridInspectorLight
### FbSmartLogger_old
Function block to communicate with a Huawei SmartLogger. Protocoll: Modbus TCP

**Description:**
The function block ``FbSmartLogger`` reads measured values ​​and status values ​​from the Modbus registers of a Huawei SmartLogger. Furthermore, control commands of the device will be written. The inputs ``sHost``, ``wPort``, ``bUnitID_Logger`` and ``bUnitID_Meteo`` are used to specify the communication parameters of the device. The function block can be released for processing via the ``xEnable`` input. The read values ​​are provided in the structure ``typOutputValues``. The control commands can be described in the structure ``typInputValues``.

### FbComPassB
Function block to communicate with a Horstmann ComPass B. Protocoll: Modbus RTU

**Description:**
The function block ``FbComPassB`` reads measured values ​​and status values ​​from the Modbus registers of a Horstmann ComPass B. Furthermore, control commands of the device will be written. For the communication the additional usage of the function block ``FbModbusRTU_Master`` is mandatory. The link to the function block ``FbModbusRTU_Master`` is realized by the variable ``bMasterID``. The function block can be released for processing via the ``xEnable`` input. At the input ``bUnitID``, the Modbus slave address of the ComPass B specified. The read values ​​are provided in the structure ``typOutputValues``. The control commands can be described in the structure ``typInputValues``. After a successful read operation, the variables will be reset automatically. If an event is detected, the current event data in the structure ``typOutputValues`` provided. The control command ``typInputValues.xDeleteEventMsg`` can be used to confirm an event and the next event in the memory is read. The read out memory location number is displayed via the variable ``typOutputValues.rEventCounter``. Is the entire memory area read out and not another active event detected, the variable returns the value 0.

### FbPM5x00
### FbMiCOM
### FbMRA4
### FbModbusSimpleBase
**Methods:**

#### mPrepareData
#### mTransferData
### FbModbusRTU_Master
Master function block for all Modbus RTU function blocks.

**Description:**
Modbus RTU master for the Modbus RTU communication between the WAGO-Controller and the Modbus RTU slaves via a RS-485 serial interface module. The link to the function block ``FbModbusRTU_Master`` is realized by the variable ``bMasterID``. All slaves in the communication line require the same bMasterID address. One of these function block is needed for each modbus line. Default physical layer

### FbION7x50
Function block to communicate with a Schneider Electric ION 7x50. Protocoll: Modbus TCP & RTU

**Description:**
The function block ``FbION7x50`` reads measured values ​​and status values ​​from the Modbus registers of a Schneider Electric ION 7x50. The inputs ``bUnitID``, ``bMasterID``, ``sHost`` and ``wPort`` are used to specify the communication parameters of the device, depending on the used Modbus type. For Modbus RTU the additional usage of the function block ``FbModbusRTU_Master`` is mandatory. The link to the function block ``FbModbusRTU_Master`` is realized by the variable ``bMasterID``. The function block can be released for processing via the ``xEnable`` input. The read values ​​are provided in the structure ``typOutputValues``.

### FbComPassA
Function block to communicate with a Horstmann ComPass A. Protocoll: Modbus RTU

**Description:**
The function block ``FbComPassA`` reads measured values ​​and status values ​​from the Modbus registers of a Horstmann ComPass A. Furthermore, control commands of the device will be written. For the communication the additional usage of the function block ``FbModbusRTU_Master`` is mandatory. The link to the function block ``FbModbusRTU_Master`` is realized by the variable ``bMasterID``. The function block can be released for processing via the ``xEnable`` input. At the input ``bUnitID``, the Modbus slave address of the ComPass A specified. The read values ​​are provided in the structure ``typOutputValues``. The control commands can be described in the structure ``typInputValues``. After a successful read operation, the variables will be reset automatically. If an event is detected, the current event data in the structure ``typOutputValues`` provided. The control command ``typInputValues.xDeleteEventMsg`` can be used to confirm an event and the next event in the memory is read. The read out memory location number is displayed via the variable ``typOutputValues.rEventCounter``. Is the entire memory area read out and not another active event detected, the variable returns the value 0.

### FbJanitza
Function block to communicate with a Janitza UMG 104/604. Protocoll: Modbus TCP & RTU

**Description:**
The function block ``FbJanitza`` reads measured values ​​and status values ​​from the Modbus registers of a Janitza UMG 104/604. The inputs ``bUnitID``, ``bMasterID``, ``sHost`` and ``wPort`` are used to specify the communication parameters of the device, depending on the used Modbus type. For Modbus RTU the additional usage of the function block ``FbModbusRTU_Master`` is mandatory. The link to the function block ``FbModbusRTU_Master`` is realized by the variable ``bMasterID``. The function block can be released for processing via the ``xEnable`` input. The read values ​​are provided in the structure ``typOutputValues``.

### FbSmartLogger
### FbBaseFree
Function block to communicate with a SolarLog Base (free interface). Protocoll: Modbus TCP

**Description:**
The function block ``FbBaseFree`` reads measured values ​​and status values ​​from the Modbus registers of a SolarLog Base. The inputs ``bUnitID``, ``sHost`` and ``wPort`` are used to specify the communication parameters of the device. The function block can be released for processing via the ``xEnable`` input. The read values ​​are provided in the structure ``typOutputValues``.

### FbSYMAP
Function block to communicate with a Stucke SYMAP Compact. Protocoll: Modbus TCP & RTU

**Description:**
The function block ``FbSYMAP`` reads measured values ​​and status values ​​from the Modbus registers of a Stucke SYMAP Compact. The inputs ``bUnitID``, ``bMasterID``, ``sHost`` and ``wPort`` are used to specify the communication parameters of the device, depending on the used Modbus type. For Modbus RTU the additional usage of the function block ``FbModbusRTU_Master`` is mandatory. The link to the function block ``FbModbusRTU_Master`` is realized by the variable ``bMasterID``. The function block can be released for processing via the ``xEnable`` input. The read values ​​are provided in the structure ``typOutputValues``.

### Fb7SJ80
Function block to communicate with a Siemens 7SJ80. Protocoll: Modbus TCP & RTU

**Description:**
The function block ``Fb7SJ80`` reads measured values ​​and status values ​​from the Modbus registers of a Siemens 7SJ80. The inputs ``bUnitID``, ``bMasterID``, ``sHost`` and ``wPort`` are used to specify the communication parameters of the device, depending on the used Modbus type. For Modbus RTU the additional usage of the function block ``FbModbusRTU_Master`` is mandatory. The link to the function block ``FbModbusRTU_Master`` is realized by the variable ``bMasterID``. The function block can be released for processing via the ``xEnable`` input. The read values ​​are provided in the structure ``typOutputValues``.

### FbBasePM
Function block to communicate with a SolarLog Base (power management interface). Protocoll: Modbus TCP

**Description:**
The function block ``FbBasePM`` reads measured values ​​and status values ​​from the Modbus registers of a SolarLog Base. Furthermore, control commands of the device will be written. The inputs ``bUnitID``, ``sHost`` and ``wPort`` are used to specify the communication parameters of the device. The function block can be released for processing via the ``xEnable`` input. The read values ​​are provided in the structure ``typOutputValues``. The control commands can be described in the structure ``typInputValues``. The output ``xPreLoadedCtrl`` signals a successful first readout of the control values.

### FbEOR_3D
Function block to communicate with a a-eberle EOR-3D. Protocoll: Modbus RTU

**Description:**
The function block ``FbEOR_3D`` reads measured values ​​and status values ​​from the Modbus registers of a a-eberle EOR-3D. Furthermore, control commands of the device will be written. For the communication the additional usage of the function block ``FbModbusRTU_Master`` is mandatory. The link to the function block ``FbModbusRTU_Master`` is realized by the variable ``bMasterID``. The function block can be released for processing via the ``xEnable`` input. At the input ``bUnitID``, the Modbus slave address of the EOR-3D specified. The read values ​​are provided in the structure ``typOutputValues``.

### FbDataManager_old
Function block to communicate with a SMA DataManager M/L. Protocoll: Modbus TCP

**Description:**
The function block ``FbDataManager`` reads measured values ​​and status values ​​from the Modbus registers of a SMA DataManager. Furthermore, control commands of the device will be written. The inputs ``bUnitID``, ``sHost`` and ``wPort`` are used to specify the communication parameters of the device. The DataManager device typically has two UnitIDs, firstly for the device information and secondly for the measured values. Please enter the first UnitID for the device information, the second will be adjusted automatically. The function block can be released for processing via the ``xEnable`` input. The read values ​​are provided in the structure ``typOutputValues``. The control commands can be described in the structure ``typInputValues``. The output ``xPreLoadedCtrl`` signals a successful first readout of the control values.

### FbBlueLog
Function block to communicate with a Meteocontrol BlueLog. Protocoll: Modbus TCP

**Description:**
The function block ``FbBlueLog`` reads measured values ​​and status values ​​from the Modbus registers of a Meteocontrol BlueLog. Furthermore, control commands of the device will be written. The inputs ``bUnitID``, ``sHost`` and ``wPort`` are used to specify the communication parameters of the device. The function block can be released for processing via the ``xEnable`` input. The read values ​​are provided in the structure ``typOutputValues``. The control commands can be described in the structure ``typInputValues``. The output ``xPreLoadedCtrl`` signals a successful first readout of the control values.

### FbSICAM
Function block to communicate with a Siemens SICAM. Protocoll: Modbus RTU

**Description:**
The function block ``FbSICAM`` reads measured values ​​and status values ​​from the Modbus registers of a Siemens SICAM. For the communication the additional usage of the function block ``FbModbusRTU_Master`` is mandatory. The link to the function block ``FbModbusRTU_Master`` is realized by the variable ``bMasterID``. The function block can be released for processing via the ``xEnable`` input. At the input ``bUnitID``, the Modbus slave address of the SICAM specified. The read values ​​are provided in the structure ``typOutputValues`` and ``typOutputValues2``.

### FbPAC4200
Function block to communicate with a Siemens SENTRON PAC3200 and PAC4200. Protocoll: Modbus TCP & RTU

**Description:**
The function block ``FbPAC4200`` reads measured values ​​and status values ​​from the Modbus registers of a Siemens SENTRON PAC4200. The inputs ``bUnitID``, ``bMasterID``, ``sHost`` and ``wPort`` are used to specify the communication parameters of the device, depending on the used Modbus type. For Modbus RTU the additional usage of the function block ``FbModbusRTU_Master`` is mandatory. The link to the function block ``FbModbusRTU_Master`` is realized by the variable ``bMasterID``. The function block can be released for processing via the ``xEnable`` input. The read values ​​are provided in the structure ``typOutputValues``.

### FbGridInspector
Function block to communicate with a Kries Grid Inspector. Protocoll: Modbus RTU

**Description:**
The function block ``FbGridInspector`` reads measured values ​​and status values ​​from the Modbus registers of a Kries Grid Inspector. Furthermore, control commands of the device will be written. For the communication the additional usage of the function block ``FbModbusRTU_Master`` is mandatory. The link to the function block ``FbModbusRTU_Master`` is realized by the variable ``bMasterID``. The processing of the measured values can be enabled via the input ``xEnableValues``. The processing of the event memory ccan be enabled via the input ``xEnableEvents``. The processing of the status bits can be enabled via the input ``xEnableStatusBits``. The processing of the system settings can be enabled via the input ``xEnableSettings``. At the input ``bUnitID``, the Modbus slave address of the Grid Inspector specified. Note: - Communication to the Grid Inspector device is aborted as soon as the user selects the menu of the IKI device. - Between the displayed values on the display of the Grid Inspector and the read out values within the output structure could be possible rounding differences.

### FbComPassBs
Function block to communicate with a Horstmann ComPass Bs. Protocoll: Modbus RTU

**Description:**
The function block ``FbComPassBs`` reads measured values ​​and status values ​​from the Modbus registers of a Horstmann ComPass Bs. Furthermore, control commands of the device will be written. For the communication the additional usage of the function block ``FbModbusRTU_Master`` is mandatory. The link to the function block ``FbModbusRTU_Master`` is realized by the variable ``bMasterID``. The function block can be released for processing via the ``xEnable`` input. At the input ``bUnitID``, the Modbus slave address of the ComPass Bs specified. The read values ​​are provided in the structure ``typOutputValues``. The control commands can be described in the structure ``typInputValues``. After a successful read operation, the variables will be reset automatically. The ComPass Bs device has a switch-disconnector, which can be usedby the control commands ``typInputValues.xLoadDisconnector_ON`` and ``typInputValues.xLoadDisconnector_OFF``. The device requires a correct execution of a Switching process a proper wiring of the BI inputs. The wiring is described in the manual of the ComPass Bs device. The current status of the switch-disconnector and possible error messages can cause the variables ``typOutputValues.xLoadDisconnector_Status`` and ``typOutputValues.xLoadDisconnector_Fault``. If an event is detected, the current event data in the structure ``typOutputValues`` provided. The control command ``typInputValues.xDeleteEventMsg`` can be used to confirm an event and the next event in the memory is read. The read out memory location number is displayed via the variable ``typOutputValues.rEventCounter``. Is the entire memory area read out and not another active event detected, the variable returns the value 0.

## Data Types

### typIki23_Output
Structure type.

### typNA011_Control
Structure type.

### typNA011_BufferInfo
Structure type.

### typNA011_Event
Structure type.

### typNA011_Fault
Structure type.

### typNA011_Output
Structure type.

### typEOnModbus_Output
Structure type.

### typMID30x0_Output
Structure type.

### typMiCOM_Out
Structure type.

### typSYMAP_Out
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbSunnyIsland: FbSunnyIsland;
END_VAR

// Basic function block usage
fbFbSunnyIsland(
    // Configure inputs as needed
);

// Check status
IF fbFbSunnyIsland.xValid THEN
    // Operation successful
END_IF

IF fbFbSunnyIsland.xError THEN
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

