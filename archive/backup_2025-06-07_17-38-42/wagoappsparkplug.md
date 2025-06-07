# WagoAppSparkplug v1.0.2.1

## Overview
WAGO PLC library providing WagoAppSparkplug functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbStatus_Sparkplug
This function block ``FbStatus_Sparkplug`` indicates the state of the connection to the cloud.

**Description:**
If the input parameter xEnabled is set, the actual state actualised every 5s. .. note:: This function block includes special information only for the Sparkplug Specification. When declaring the function block, it is determined for which of the two cloud connections the function block is intended. For example: .. code-block:: codesys VAR oFbStatus_Sparkplug : WagoAppSparkplug.FbStatus_Sparkplug(eConnection :

### FbValue
### FbDevice
The ``FbDevice`` function block controls the device together with the included metrics.

**Description:**
The device dependents on the EdgeNode and only becomes active when the EdgeNode is activated. Following diagram is showing the state machine of the device: .. figure:: ../../images/Device_StateMachine.PNG :align: center :alt: Sparkplug Device StateMachine .. code-block:: codesys VAR oEdgeNode : WagoAppSparkplug.FbEdgeNode(eConnection :

**Methods:**

#### Rebirth
#### DetachMetric
#### AttachMetric
### FbMetric
The function block FbMetric contains the actual information of the individual sensor or process values. Additional information of the metric can be set via the properties |FbProperty|.

**Description:**
Every metric has a: 1. Name (|FbMetric.Name|) 2. Alias (|FbMetric.Alias|) 3. Timestamp (will be generate automatically) 4. DataType (|FbMetric.DataType|) 5. Value (see FbMetric.IValue) 6. Optional: IsNull (|FbMetric.IsNull|) Sending a new metric value is set via the method |FbMetric.TriggerValue|. If the metric is to be used bidirectionally to receive metric values from the cloud, it must be configured accordingly. For this purpose, an assignment of |FbMetric.CommandMetricCallback| must be implemented. For more information see into |FbMetric.CommandMetricCallback|. .. code-block:: codesys VAR oEdgeNode : WagoAppSparkplug.FbEdgeNode(eConnection :

**Methods:**

#### TriggerValue
#### DetachProperty
#### AttachProperty
### FbEdgeNode
The ``FbEdgeNode`` function block controls the Edge Node together with the included devices and metrics.

**Description:**
An EdgeNode is one of the key roles in any Sparkplug System. The EdgeNode is responsible for managing the lifecycle and state of these connected devices and sensors as well as receiving and sending data for the devices to the broker. Following diagram is showing the state machine of the EdgeNode: .. figure:: ../../images/EdgeNode_StateMachine.PNG :align: center :alt: Sparkplug EdgeNode StateMachine Before starting it is necessary to set the GroupId (|FbEdgeNode.GroupId|) and the name (|FbEdgeNode.Name|) of the EdgeNode. When declaring the function block, it is determined for which of the two cloud connections the function block is intended. For example: .. code-block:: codesys VAR oEdgeNode : WagoAppSparkplug.FbEdgeNode(eConnection :

**Methods:**

#### Rebirth
#### DetachMetric
#### DetachDevice
#### AttachMetric
#### AttachDevice
### FbProperty
The function block FbProperty can be used to assign additional information to a metric (|FbMetric|).

**Description:**
A property (|FbProperty|) can be assigned to multiple metrics (|FbMetric|). The property can be added to the metric with the |FbMetric.AttachProperty|. Primitive data types are also supported for a property (|eDataType|). The property is part of the initial BIRTH message (DATA message without properties). Maximum number of properties can be configured here: |ParameterList.MAX_COUNT_PROPERTIES| .. code-block:: codesys VAR metricEdgeNode_2 : WagoAppSparkplug.FbMetric :

## Data Types

### eSparkplugProtocolVersion
Enumeration type.

### eDeviceStateMachine
Enumeration type.

### eEdgeNodeStateMachine
Enumeration type.

### eDataType
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbStatus_Sparkplug: FbStatus_Sparkplug;
END_VAR

// Basic function block usage
fbFbStatus_Sparkplug(
    // Configure inputs as needed
);

// Check status
IF fbFbStatus_Sparkplug.xValid THEN
    // Operation successful
END_IF

IF fbFbStatus_Sparkplug.xError THEN
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

