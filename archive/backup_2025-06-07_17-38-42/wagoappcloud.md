# WagoAppCloud v1.3.5.7

## Overview
WAGO PLC library providing WagoAppCloud functionality.

**Key Features:**
- Time and date operations
- Communication protocols
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbDatagramServer_internal_copy
**Methods:**

#### OpenAndListen
**Result Codes:**
| Code | Description |
|------|-------------|
| 0 | success, ready for communication. EACCES the socket could not be created by other reasons EINVAL invalid argument, e.g. malformed adress ENFILE The system limit on the total number of open sockets has been reached. EADDRINUSE The given address / port combination is already in use. EBUSY The socket is already bound to an address. EADDRNOTAVAIL A nonexistent interface was requested or the requested address was not local. ============= ====================================================================================== |

### FbSubscribeMQTT_2
This function block contains a subscription to get data from the cloud. This subscription includes configuration like the topic and the quality of service.

**Description:**
If the input parameter xSubscribe is set the function block will be initialised and the topic are subscriped to the cloud. New data from the cloud can be received in an intervall of 50ms. .. note:: If the count of subscription is greater than the default setting (10 subscription instances) the parameter gSUBSCRIPTIONS in the parameter list Param must be changed. .. note:: If using the Native MQTT Protocol with the function blocks FbPublishMQTT_2 and/or FbSubscribeMQTT_2 it is necessary to configure the Data Protocol *Native MQTT* in the web based management. .. note:: This function block must be executed cyclically in a background task (set the task priority to 15) with cycle interval <

### FbStatus_NativeMQTT_2
This function block give the state of the connection to the cloud.

**Description:**
If the input parameter xEnabled is set the actual state actualised every 5s. When declaring the function block, it is determined for which of the two cloud connections the function block is intended. .. code-block:: codesys VAR oFbStatus_NativeMQTT_2 : WagoAppCloud.FbStatus_NativeMQTT_2(eConnection :

### FbStatus_WagoProtocol_2
This function block give the state of the connection to the cloud.

**Description:**
If the input parameter xEnabled is set the actual state actualised every 5s. .. note:: This function block includes special information only for the Wago Protocol. When declaring the function block, it is determined for which of the two cloud connections the function block is intended. .. code-block:: codesys VAR oFbStatus_WagoProtocol_2 : WagoAppCloud.FbStatus_WagoProtocol_2(eConnection :

### FbCloudStatus
### FbSubscribeDecoderData
### FbSubscribeTopicMQTT
### FbSampleMessageFactory
### FbRegistrationMessageFactory
### FbGetLongTime
### FbCommandRegistrationMessageFactory
### FbCommandRequestDecoder
### FbCommandResponseMessageFactory
### FbAgentBusTransmitter
### FbMessageListener
### FbAgentBusReciever
### FbCommandResponder_2
This Function Block is used to provide the response to a command request which was received from the cloud. (Microsoft Azure)

**Description:**
.. note:: Before response to a command request it is necessary to configure the command in the aplication with the Function Block

### FbCommandListener_2
This Function Block is used to listen and receive command requests from the cloud.

**Description:**
.. note:: Before listen to a command request from the cloud it is necessary to configure the command in the aplication with the Function Block

### FbCommandConfigurator_2
Function Block used to configure custom cloud to device commands.

**Description:**
Registration of Commands using

### FbCollectionLogger_2
This function block should be used to forward variables and their current values to the cloud.

**Description:**
Developer of the IEC 61131-3 program is responsible to group program variables within one or more collections. The list of configured collections should be passed as input together with a number describing the number of collections. Different ways to generate samples are impossible. In the default state (eSamplingMode

### FbPublishMQTT_2
Generate a MQTT message to publish to the cloud.

**Description:**
This function block transmit data to the cloud in the own data structure. The PLC application engineer can choose the topic and his own data structure. The Quality of Service 0, 1 and 2 are supported. To write the data in a JSON format the library WagoAppJSON could be used. .. note:: If using the Native MQTT Protocol with the function blocks FbPublishMQTT_2 and/or FbSubscribeMQTT_2 it is necessary to configure the Data Protocol *Native MQTT* in the web based management. .. note:: For secure data traffic it is recommended to send maximum 65kByte in one task interval. .. note:: This function block must be executed in the background task (set the tasc priority to 15). When declaring the function block, it is determined for which of the two cloud connections the function block is intended. .. code-block:: codesys VAR oFbPublishMQTT_2 : WagoAppCloud.FbPublishMQTT_2(eConnection :

### FbSubscribeMQTT
This function block contains a subscription to get data from the cloud. This subscription includes configuration like the topic and the quality of service.

**Description:**
If the input parameter xSubscribe is set the function block will be initialised and the topic are subscriped to the cloud. New data from the cloud can be received in an intervall of 50ms. .. note:: If the count of subscription is greater than the default setting (10 subscription instances) the parameter gSUBSCRIPTIONS in the parameter list Param must be changed. .. note:: If using the Native MQTT Protocol with the function blocks FbPublishMQTT and/or FbSubscribeMQTT it is necessary to configure the Data Protocol *Native MQTT* in the web based management. .. note:: This function block must be executed cyclically in a background task (set the task priority to 15) with cycle interval <

### FbStatus_NativeMQTT
This function block give the state of the connection to the cloud.

**Description:**
If the input parameter xEnabled is set the actual state actualised every 5s.

### FbPublishMQTT
Generate a MQTT message to publish to the cloud.

**Description:**
This function block transmit data to the cloud in the own data structure. The PLC application engineer can choose the topic and his own data structure. The Quality of Service 0, 1 and 2 are supported. To write the data in a JSON format the library WagoAppJSON could be used. .. note:: If using the Native MQTT Protocol with the function blocks FbPublishMQTT and/or FbSubscribeMQTT it is necessary to configure the Data Protocol *Native MQTT* in the web based management. .. note:: For secure data traffic it is recommended to send maximum 65kByte in one task interval. .. note:: This function block must be executed in the background task (set the tasc priority to 15).

### FbStatus_WagoProtocol
This function block give the state of the connection to the cloud.

**Description:**
If the input parameter xEnabled is set the actual state actualised every 5s. .. note:: This function block includes special information only for the Wago Protocol.

### FbCommandConfigurator
Function Block used to configure custom cloud to device commands.

**Description:**
Registration of Commands using

### FbCommandListener
This Function Block is used to listen and receive command requests from the cloud.

**Description:**
.. note:: Before listen to a command request from the cloud it is necessary to configure the command in the aplication with the Function Block

### FbCommandResponder
This Function Block is used to provide the response to a command request which was received from the cloud. (Microsoft Azure)

**Description:**
.. note:: Before response to a command request it is necessary to configure the command in the aplication with the Function Block

### FbCollectionLogger
This function block should be used to forward variables and their current values to the cloud.

**Description:**
Developer of the IEC 61131-3 program is responsible to group program variables within one or more collections. The list of configured collections should be passed as input together with a number describing the number of collections. Different ways to generate samples are impossible. In the default state (eSamplingMode

## Data Types

### typVariableDescription
Structure type.

### typCommandDescription
Structure type.

### typCommandParameterDescription
Structure type.

### typCollection
Structure type.

### typCommandRequest
Structure type.

### typCommandResponse
Structure type.

### typCommandParameter
Structure type.

### typLoggingState
Structure type.

### eSamplingMode
Enumeration type.

### eVariableValueType
Enumeration type.

### eCommandParameterType
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbDatagramServer_internal_copy: FbDatagramServer_internal_copy;
END_VAR

// Basic function block usage
fbFbDatagramServer_internal_copy(
    // Configure inputs as needed
);

// Check status
IF fbFbDatagramServer_internal_copy.xValid THEN
    // Operation successful
END_IF

IF fbFbDatagramServer_internal_copy.xError THEN
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

