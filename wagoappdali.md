# WagoAppDALI v1.3.1.10

## Overview
WAGO PLC library providing WagoAppDALI functionality.

**Key Features:**
- Time and date operations
- Communication protocols
- Control functions
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbDaliGeneralPurposeSensorIT6
The function block outputs the raw data for the signals transmitted by a standard sensor light instance.

### FbDaliSensorLightPresencePushbutton2
The function block outputs the event based data signals from a Esylux PD-C 360/x BMS DALI-2 sensor with presence, light level and 2 pushbuttons. .. note:: Presence holding time for movement based sensors is configured in sensor configuration |StandardSensorConfiguration|.

### FbDaliSensorPushbutton8
The function block outputs the event based data signals from a standard sensor (DALI2) for 8 push button instances.

### FbDaliSensorPushbutton4_Feedback
The function block outputs the event based data signals from a standard sensor (DALI2) for 4 push button instances.

### FbDaliPushButtonSensorIT1_Feedback
The function block outputs the raw data for the signals transmitted by a standard sensor push button instance.

### FbDaliWritelRGBWAF_Scene
The function block can write the RGBWAF scene.

### FbDaliColourTemperatureDayCurve
This function sends the current colour temperature using a 24 point characteristic for each full hour of the day.

**Description:**
If the function block is enabled via the "xEnable" input, the calculated colour temperature is sent to the DALI bus based on the day curve in the "tUpdateInterval" interval. The colour temperature between the points are determined using a linear equation. A linear equation is automatically generated from the last point of the characteristic curve to the first point of the characteristic curve.

### FbDaliDimDayCurve
This function sends the current actual dim level using a 24 point characteristic for each full hour of the day.

**Description:**
If the function block is enabled via the "xEnable" input, the calculated dimming value is sent to the DALI bus based on the day curve in the "tUpdateInterval" interval. The dim level between the points are determined using a linear equation. A linear equation is automatically generated from the last point of the characteristic curve to the first point of the characteristic curve.

### FbDaliMacroCommandsControlDevices
The function block is used to call up the macros stored in the DALI Multi-Master module.

### FbDaliCommandsControlDevices
The function block can be used to send DALI commands that are specified in the IEC 82386 part 103. The address byte, instance byte and the opcode byte will be send one to one (address byte must be formed as described in IEC 82386). Send Twice or Query will be recognized automatically.

### FbDaliMemoryBankStandardSensor
The function block can be used to read and write the input devices (Sensors) memory banks.

### FbDaliLightSourceDiagnosticsAndMaintenance
The function block reads diagnostic and maintenace reports from the light source.

### FbDaliActiveEnergyAndPower
The function block reads the energy values Active Energy and Active Power from the control gear(ECG).

### FbDaliSensorPresence
The function block outputs the event based presence signals from a standard sensor (DALI-2). .. note:: Presence holding time for movement based sensors is configured in sensor configuration |StandardSensorConfiguration|.

### FbDaliSensorLight
The function block outputs the event based light level signals from a standard sensor (DALI-2). .. note:: Presence holding time for movement based sensors is configured in sensor configuration |StandardSensorConfiguration|.

### FbDaliUniversalSensorIT0
The function block outputs the raw data for the signals querried from a standard sensor universal instance.

### FbDaliAbsoluteInputSensorIT2
The function block outputs the raw data for the signals transmitted by a standard sensor absolute input instance.

### FbDaliWrite_XY_CoordinateScene
The function block can write the scene with xy-coordinates.

### FbDaliWriteColourTemperatureScene
The function block can write the colour temperature scene Tc.

### FbBaseControlGearCommands
### ResetFb
### FbButtonStuck
The function block is used to be the button stuck funtionality for push button standard sensors while it is deactivated by event filter in |StandardSensorConfiguration|.

**Description:**
If ``xButton`` is pressed until the time ``tButtonStuck`` expires, the ``xButtonOut`` will set to FALSE until a negative and new positive edge of the ``xButton`` input. Otherwise the output ``xButtonOut`` follows the input signal ``xButton``.

### FbDaliPushButtonSensorIT1
The function block outputs the raw data for the signals transmitted by a standard sensor push button instance.

### FbDaliSensorLightPresence
The function block outputs the event based data signals from a standard sensor (DALI-2) for presence and light level. .. note:: Presence holding time for movement based sensors is configured in sensor configuration |StandardSensorConfiguration|.

### FbDaliSensorPushbutton4
The function block outputs the event based data signals from a standard sensor (DALI2) for 4 push button instances.

### FbDaliStandardSensor
The function block outputs the values transferred from a standard sensor (DALI2). The outputs are sorted by instance types.

### FbDaliStandardSensorHighResolution
The function block outputs the values transferred from a standard sensor (DALI2). The outputs are sorted by instance types. The function block shell be used for sensors with high resolution of light instances. After a light event, the value gets querried up to a resolution of 32.

### FbDaliIdentifyStandardSensor
The function block is used to identify the control device (sensor) short addresses.

**Description:**
As long as ``xIdentify`` is active the control device, which is selected in ``bShortAddress``, is identified. If you change the control device selection, the old address stops identification and the new address starts identification.

### FbDaliChangeAddressStandardSensor
The function block is used to change the control device (sensor) short addresses.

### FbDaliAddressingStandardSensor
The function block is used to address the connected DALI control devices (sensors). In addition, the short addresses can be changed or the short addresses can be deleted.

### FbDaliLightSensorIT4
The function block outputs the raw data for the signals transmitted by a standard sensor light instance.

### FbDaliPresenceSensorIT3
The function block outputs the raw data for the signals transmitted by a standard sensor presence instance.

### FbDaliControlGearDiagnosticsAndMaintenance
The function block reads diagnostic and maintenace reports from the control gear(ECG).

### FbDaliLoadSideEnergyAndPower
The function block reads the energy values Active Energy Loadside and Active Power Loadside from the control gear(ECG).

### FbDaliApparentEnergyAndPower
The function block reads the energy values Apparent Energy and Apparent Power from the control gear(ECG).

### FbDaliSwitchOnOff
The function block maps the function of a switch.

### FbDaliRecallRGBWAF
The function block sends the RGBWAF signal.

### FbDaliRecall_XY_Coordinate
The function block is used to call up a color from a "CIE 1931" diagram.

### FbDaliRecallColourTemperature
The function block is used to call up the color temperature Tc.

### FbDaliRecallPrimary
The function block sets the temporary primary dimlevel.

### FbFunctionTest
The function block allows manual start / stop of the function test.

### FbDurationTest
The function block allows manual start / stop of the duration test.

### FbControlEmergencyLighting
The function block sends different control / reset commands to the emergency lighting devices.

### FbCfgAutoTest
The function block can read and write the schedule settings for the emergency lighting device.

### FbOperationTimeEmergencyLighting
The function block readout the operation time of the self-contained emergency lighting.

### FbStatusEmergencyLighting
The function block readout the status of the self-contained emergency lighting.

### FbCfgEmergencyLighting
The function block reads the status of all emergency lighting devices.

### FbReadFactorySettings
The function block readout the manufacture defined parameters

### FbRawDataPushbuttonSensorType2
The function block outputs the raw data for the signals transmitted by the key coupler.

### FbPushbuttonSensorType2
The function block outputs the values transferred from a key coupler.

### FbMultiSensorType2
The function block outputs the values transferred from a multi-sensor.

### FbCfgPushbuttonSensorType2
The function block is used for configuring the key coupler type 2.

### FbCfgMultiSensorType2
The function block is used for configuring the multi-sensor type 2.

### FbRawDataPushbuttonSensorType1
The function block outputs the raw data for the signals transmitted by the key coupler.

### FbPushbuttonSensorType1
The function block outputs the values transferred from a key coupler.

### FbMultiSensorType1
The function block outputs the raw data for the signals transmitted by the key coupler.

### FbCfgPushbuttonSensorType1
The function block is used for configuring the pushbutton sensor type 1.

### FbCfgMultiSensorType1
The function block is used for configuring the multi-sensor type 1.

### FbDaliRestoreActualLevel
The function block is used to store the last known dimming value.

### FbDaliIdentifyControlGears
The function block is used to identify the control gear (ECG) short addresses.

**Description:**
As long as ``xIdentify`` is active the control gear (ECG), which is selected in ``typBallast``, is flashing. If you change the control gear (ECG) selection, the old address stops flashing and the new address starts flashing.

### FbDaliDiagnosticControlGears
The function block block reads out the current status of the control gears (ECG) from the module database and from the DALI bus.

### FbDaliSendFadeTime
The function block writes the fade time to one or more control gears (ECG).

### FbDaliSwitchPowerSupply
The function block can be used to activate/deactivate the internal DALI power supply.

### FbDaliActualLevelControlGears
The function block can be used to read out the available short addresses and the current dimming values for the control gear (ECG). .. note:: Only applicable with PFC family >=FW4

### FbDaliSendDimValue
The function block sends direct dimming levels to the selected DALI control gear (ECG).

**Description:**
If the value change at the ``rDimValue`` input is greater than ``rHysteresis``, or a positive edge is detected at the ``xUpdate`` input, the selected lamps are dimmed to the dimming value set at the ``rDimValue`` input. .. note:: Please consider for a correct function the :ref:`system properties <doc10_SystemProperties>`.

### FbDaliMacroCommandsControlGears
The function block is used to call up the macros stored in the DALI Multi-Master module.

### FbDaliCommandsControlGears
The function block can be used to issue the DALI commands specified in standard IEC 82386 (see Table 2 in the appendix).

### FbDaliStoreActualLevelAsScene
The function block can be used to save the set dimming values as scenes.

### FbDaliRecallScene
The function block can be used to call up the DALI light scenes defined in the control gear (ECG).

**Description:**
The DALI light scenes can be called in two different ways: #. With a positive edge at inputs ``xScene0`` to ``xScene15``, the corresponding DALI light scene is called. #. If a value changes at the ``bScene`` input or with a positive edge at the ``xUpdateScene`` input, the DALI light scene specified at the ``bScene`` input is called up.

### FbDaliConstantLightControl
The function block enables constant light to be controlled automatically in connection with a light sensor. .. note:: The maximum short push button time can be set function block individually by property ``tShortPushButton`` or global by ``Commmon.SHORT_PUSHBUTTON``. The last change of both variables willtake effect.

### FbDaliDimSingleButton
The function block can be used to dim the DALI lighting. The lighting is dimmed or powered on and off by controlling one button.

### FbDaliDimDoubleButton
The function block can be used to dim the DALI lighting. The lighting is dimmed or powered on and off by controlling two separate button inputs.

### FbDaliLatchingRelay
The function block maps the function of a latching relay.

### FbDaliConfigControlGears
The function block can read and write the parameters from an control gear (ECG).

### FbDaliConfigSceneControlGears
The function block is used for configuring DALI scenes.

### FbDaliChangeAddressControlGears
The function block is used to change the control gear (ECG) short addresses.

### FbDaliConfigGroupControlGears
The function block is used to configure the DALI groups. In addition to the 16 standard DALI groups, this function block can be used to configure additionally 16 virtual groups.

### FbDaliSendFadeRate
The function block writes the fade rate to one or more control gears (ECG).

### FbDaliOperatingHours
The function block reads and writes the operating hours of the DALI control gear (ECG) into the module database.

### FbDaliMemoryBankControlGears
The function block can be used to read and write the control gears (ECG) memory banks.

### FbDaliAddressingControlGears
The function block is used to address the connected DALI control gears (ECG). In addition, the short addresses can be deleted or the settings can be set to the "reset values". |doc11_DefaultValues|

### FbDaliMaster
The function block is necessary for the interface to the DALI Multi-Master module 753-647. All other function blocks communicate with the DALI Multi-Master module via this function block.

## Data Types

### FuTypPushbuttonSensorType2
The function converts the key coupler addresses to the data type ``typPushbuttonSensorType2``.

### FuTypMultiSensorType2
The function converts the multi-sensor addresses to the data type ``typMultiSensorType2``.

### FuLuxLevelSensorType2
The function converts the measured light intensity from the multi-sensor to a Lux value [lx].

### FbRawDataPushbuttonSensorType2
The function block outputs the raw data for the signals transmitted by the key coupler.

### FbPushbuttonSensorType2
The function block outputs the values transferred from a key coupler.

### FbMultiSensorType2
The function block outputs the values transferred from a multi-sensor.

### FbCfgPushbuttonSensorType2
The function block is used for configuring the key coupler type 2.

### FbCfgMultiSensorType2
The function block is used for configuring the multi-sensor type 2.

### FuTypPushButtonSensorType1
The function converts the key coupler addresses to the data type ``typPushbuttonSensorType1``.

### FuTypMultiSensorType1
The function converts the multi-sensor addresses to the data type ``typMultiSensorType1``.

### FbRawDataPushbuttonSensorType1
The function block outputs the raw data for the signals transmitted by the key coupler.

### FbPushbuttonSensorType1
The function block outputs the values transferred from a key coupler.

### FbMultiSensorType1
The function block outputs the raw data for the signals transmitted by the key coupler.

### FbCfgPushbuttonSensorType1
The function block is used for configuring the pushbutton sensor type 1.

### FbCfgMultiSensorType1
The function block is used for configuring the multi-sensor type 1.

### typBallast
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbDaliGeneralPurposeSensorIT6: FbDaliGeneralPurposeSensorIT6;
END_VAR

// Basic function block usage
fbFbDaliGeneralPurposeSensorIT6(
    // Configure inputs as needed
);

// Check status
IF fbFbDaliGeneralPurposeSensorIT6.xValid THEN
    // Operation successful
END_IF

IF fbFbDaliGeneralPurposeSensorIT6.xError THEN
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

