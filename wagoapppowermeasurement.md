# WagoAppPowerMeasurement v1.7.4.11

## Overview
WAGO PLC library providing WagoAppPowerMeasurement functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbConfiguration_MID_MultiQuery
This function block reads or writes configuration values. In case of a ``879-3040`` the value for the current transformer will only be written if the value ``SCIP_WRITING_CT`` from the ``ParameterList`` is set to ``False``.

**Description:**
A visualization template is available. .. note:: The input ``m_Input_typConfig_MID`` is of type ``typMID_Config`` .. note:: The input ``m_Input_Fb_Configuration`` is of type ``FbConfiguration_MID_MultiQuery``

**Methods:**

#### onError
### FbConfiguration_MID
This function block reads or writes configuration values. It is differentiated between the counter configuration values and the modbus communication values. In case of a ``879-3040`` the value for the current transformer will only be written if the value ``SCIP_WRITING_CT`` from the ``ParameterList`` is set to ``False``. .. note:: It is not really very comfortable to change the modbus parameter by this function block, though it is possible Changing the modbus communication parameter will interrupt the connection with the counter. The communication must be reset and enabled again, with the new parameter. Since the interruption happens immediately only one value at a time is changed, starting with the modbus id, than the baudrate and at last the parity.

**Description:**
A visualization template is available. If you need to change even the modbus communication parameter it is necessary to adjust the variable ``SHOW_MODBUS_PARAMETER_IN_VISU`` from the ``ParameterList``. .. note:: The input ``m_Input_typConfig_MID`` is of type ``typMID_Config`` .. note:: The input ``m_Input_Fb_Configuration`` is of type ``FbConfiguration_MID`` Using this template needs an instance of function block FbConfiguration_MID as input.

### FbAC_Compact_MID
This function block reads the most common AC values of the MID counter 879-3000

**Description:**
A visualization template ``tplStatusAC_Compact_MID`` is available. .. note:: The input ``m_Input_FbAC_Compact`` is of type ``FbAC_Compact_MID`` Using this template needs an instance of function block FbAC_Compact_MID as input.

### FbAC_Base_MID
### FbAC_Compact_MID_MultiQuery
This function block reads the most common AC values of the MID counter 879-3000

**Description:**
A visualization template ``tplStatusAC_Compact_MID_MultiQuery`` is available. .. note:: The input ``m_Input_FbAC_Compact`` is of type ``FbAC_Compact_MID_MultiQuery`` Using this template needs an instance of function block FbAC_Compact_MID_MultiQuery as input.

**Methods:**

#### onError
### FbConfiguration_3PPT_MultiQuery
This function block reads or writes configuration values

**Description:**
Additional energy consumption may be reset or set.

**Methods:**

#### onError
### FbAC_General_3PPT_MultiQuery
This function block allows reading of configuration values as well as process values.

**Description:**
This function block is used to read any value described in the manual.

**Methods:**

#### onError
### FbAC_Compact_3WireWyeDelta_3PPT_MultiQuery
This function block reads the most common AC values of the 3-Phase Power Transducer module if used with 3-Wire Wye/Delta topology

**Methods:**

#### onError
### FbAC_Compact_3PPT_MultiQuery
This function block reads the most common AC values of the 3-Phase Power Transducer Module

**Methods:**

#### onError
### FbConfiguration_3PPT
This function block reads or writes configuration values

**Description:**
Additional energy consumption may be reset or set.

### FbAC_General_3PPT
This function block allows reading of configuration values as well as process values.

**Description:**
This function block is used to read any value described in the manual.

### FbAC_Compact_3WireWyeDelta_3PPT
This function block reads the most common AC values of the 3-Phase Power Transducer module if used with 3-Wire Wye/Delta topology

### FbAC_Compact_3PPT
This function block reads the most common AC values of the 3-Phase Power Transducer Module

### FbMaster3Phase
Configuration from the 3-Phase Power Measurement Module (750-493) and reading process values

**Description:**
This function block allows the process values of 3 phases to be cyclically read and the configuration of the module to be changed. Cyclic polling of the process values is performed if the ``xEnable`` input is TRUE. The ``tCycleTime`` input parameter determines the cycle time. If the timeout time is exceeded or the undervoltage threshold is undershot, ``bError`` output indicates an error. Using transformers for current measurement, the current transformer ratio can be entered via the ``wCurrentTransformerRatio`` input. The current transformer ratio is always 1 : X.

### FbMaster1Phase
Configuring one phase from the 3-Phase Power Measurement Module (750-493) and reading process values

**Description:**
This function block allows the process values of one phase to be cyclically read and the configuration of the module to be changed. Cyclic polling of the process values is performed if the ``xEnable`` input is TRUE. The ``tCycleTime`` input parameter determines the cycle time. If the timeout time is exceeded or the undervoltage threshold is undershot, ``bError`` output indicates an error. Using transformers for current measurement, the current transformer ratio can be entered via the ``wCurrentTransformerRatio`` input. The current transformer ratio is always 1 : X.

### FbConfigurationAndStatus_495_040_010
This function block reads continously the general modul information shown at output ``typModuleInfo``

**Description:**
.. note::This function block must be used with each module and be called cyclic. Additional commands like read or write configuration are possible.

### FbAC_Compact_495_040_010
This function block reads the most common AC values of the 3-Phase Power Measurement module 750-495/040-010

**Description:**
The function block can be used for cyclic reading of the most important measured values using collection 10. It can be used multiple times in one project. .. note:: For the correct unit of energy values, the setting for scaling factor ``rSelectedScalingFactor`` must be taken into account. If this function block is used without the function block FbConfigurationAndStatus_495_040_010, then it is neccessary to set the parameter ``USE_FBAC_COMPACT_495_STANDALONE`` to TRUE.

### FbAC_Values_495
This function block reads up to 4 AC values from the 3-Phase Power Measurement Module (750-495).

**Description:**
This function block can be used for cyclic reading of up to 4 process values from collection 10. It can be used multiple times in one project.

### FbHarmonicValues_495
This function block reads the selected harmonic values of the 3-Phase Power Measurement Module (750-495).

**Description:**
This function block can be used for cyclic reading of up to 3 harmonics from collections 20 to 22. It can be used multiple times in one project.

### FbAC_Compact3WireWyeDelta_495
This function block reads the most common AC values of the 3-Phase Power Measurement Module (750-495) in 3-wire Wye/Delta topology.

**Description:**
This function block can be used for cyclic reading of the most important measured values using collection 10. It can be used multiple times in one project. .. note:: For the correct unit of energy values, the setting for scaling factor ``rSelectedScalingFactor`` must be taken into account. If this function block is used without the function block FbConfigurationAndStatus_495, then it is neccessary to set the parameter ``USE_FBAC_COMPACT_495_STANDALONE`` to TRUE.

### FbAC_Compact_495
This function block reads the most common AC values of the 3-Phase Power Measurement module 750-495

**Description:**
The function block can be used for cyclic reading of the most important measured values using collection 10. It can be used multiple times in one project. .. note:: For the correct unit of energy values, the setting for scaling factor ``rSelectedScalingFactor`` must be taken into account. If this function block is used without the function block FbConfigurationAndStatus_495, then it is neccessary to set the parameter ``USE_FBAC_COMPACT_495_STANDALONE`` to TRUE.

### FbConfigurationAndStatus_495
This function block continously reads the general module information shown at output ``typModuleInfo``.

**Description:**
.. note:: This function block must be used with each module and be called cyclically. Additional commands like read or write configuration are possible.

### FbAC_Compact3WireWyeDelta_494
This function block reads the most common AC values of the 3-Phase Power Measurement Module (750-494) in 3-wire Wye/Delta topology

**Description:**
This function block can be used for cyclic reading of the most important measured values using collection 9. It can be used multiple times in one project. .. note:: For the correct unit of energy values, the setting for scaling factor ``rSelectedScalingFactor`` must be taken into account. If this function block is used without the function block FbConfigurationAndStatus_494, it is then neccessary to set the parameter ``USE_FBAC_COMPACT_494_STANDALONE`` to TRUE.

### FbConfigurationAndStatus_494_Shunt
This function block reads continously the general modul information shown at output ``typModuleInfo``

**Description:**
.. note::This function block must be used with each module 750-494/000-005 (shunt version) and be called cyclic. Additional commands like read or write configuration are possible.

### FbDC_Values_494
This function block reads the DC values of the 3-Phase Power Measurement module 750-494

**Description:**
The function block can be used for cyclic reading of up to 4 process values from collection 7. It can be used multiple times in one project.

### FbConfigurationAndStatus_494
This function block reads continously the general modul information shown at output ``typModuleInfo``

**Description:**
.. note::This function block must be used with each module and be called cyclic. Additional commands like read or write configuration are possible.

### FbAC_Values_494
This function block reads up to 4 AC values from the 3-Phase Power Measurement module 750-494

**Description:**
The function block can be used for cyclic reading off up to 4 process values from collection 9. It can be used multiple times in one project.

### FbAC_Compact_494
This function block reads the most common AC values of the 3-Phase Power Measurement module 750-494

**Description:**
The function block can be used for cyclic reading of the most important measured values using collection 9. It can be used multiple times in one project. .. note:: For the correct unit of energy values, the setting for scaling factor ``rSelectedScalingFactor`` must be taken into account. If this function block is used without the function block FbConfigurationAndStatus_494 then it is neccessary to set the parameter ``USE_FBAC_COMPACT_494_STANDALONE`` to TRUE.

### FbHarmonicValues_494
This function block reads the selected harmonic values of the 3-Phase Power Measurement module 750-494

**Description:**
The function block can be used for cyclic reading of up to 3 harmonics from collections 20 to 22. It can be used multiple times in one project.

## Data Types

### e_MID_Feedback
Enumeration type.

### eStatus
Enumeration type.

### eMinMaxValue
Enumeration type.

### eEnergyConsumption
Enumeration type.

### e_3PPT_Feedback
Enumeration type.

### typRegister_493
Structure type.

### typModeSetting
Structure type.

### typConfig3Phase
Structure type.

### typ495_040_010Config
Structure type.

### typ495State
Structure type.

### e495AC_Values
Enumeration type.

### typ495Config
Structure type.

### typChannelConfig
Structure type.

### eHarmonicMeasurand
Enumeration type.

### eHarmonicValues
Enumeration type.

### typ494Config
Structure type.

### e494DC_Values
Enumeration type.

### typ494State
Structure type.

### e494AC_Values
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbConfiguration_MID_MultiQuery: FbConfiguration_MID_MultiQuery;
END_VAR

// Basic function block usage
fbFbConfiguration_MID_MultiQuery(
    // Configure inputs as needed
);

// Check status
IF fbFbConfiguration_MID_MultiQuery.xValid THEN
    // Operation successful
END_IF

IF fbFbConfiguration_MID_MultiQuery.xError THEN
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

