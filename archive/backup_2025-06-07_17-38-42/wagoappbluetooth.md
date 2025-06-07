# WagoAppBluetooth v1.6.1.0

## Overview
WAGO PLC library providing WagoAppBluetooth functionality.

**Key Features:**
- Time and date operations
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbVisuDiagnosis
**Methods:**

#### TableIndexToSlot
#### SlotToTableIndex
### FbSetAllRemotePiMapping
**Methods:**

#### TableIndexToSlot
#### SlotToTableIndex
### FbVisuPiMapping
**Methods:**

#### TableIndexToSlot
#### SlotToTableIndex
### FbSetAllAllowedDecives
### FbSetAllowDeviceEntry
### FbGetAllAllowedDecives
### FbVisuScanForDevices
### FbSetRemotePiSize
### FbGetRemotePiMapping
### FbGetHostFwVersion
### FbGetAllowDeviceEntry
### FbSetUserfriendlyName
### FbGetUserfriendlyName
### FbScanRemoteDevices
### FbGetRemoteDeviceName
### FbGetRemoteDeviceMacID
### FbSetReconnectionTimePeriod
### FbGetReconnectionTimePeriod
### FbSetConnectionQualityOfService
### FbGetConnectionQualityOfService
### FbUnBindRemoteDevice
### FbGetBoundRemoteDevices
### FbBindRemoteDevice
### FbSetAllowRemoteDevice
### FbGetStatusMessage
### FbGetNetworkStatus
### FbGetLocalDeviceStatus
### FbGetLinkSignalStrength
### FbGetLinkQuality
### FbGetAvailableChannelMap
### FbSetFactorySettings
### FbSetLocalEncryptionMode
### FbGetLocalEncryptionMode
### FbSetLocalDeviceClass
### FbGetLocalDeviceClass
### FbSetLocalAuthenticationMode
### FbGetLocalAuthenticationMode
### FbSetLocalPassword
### FbGetLocalPassword
### FbEraseLocalAuthentication
### FbVisuDeviceConfiguration
### FbSetLocalSubnetMask
### FbSetLocalIPAddress
### FbGetLocalDeviceConfigLen
### FbVisuNetworkConfiguration
### FbSetLocalOperationMode
### FbGetLocalOperationMode
### FbSetLocalDeviceRole
### FbGetLocalDeviceRole
### FbGetLocalSubnetMask
### FbGetLocalIPAddress
### FbSetLocalDeviceName
### FbGetLocalDeviceName
### FbGetLocalMacID
## Usage Examples

### Basic Usage
```iec
VAR
    fbFbVisuDiagnosis: FbVisuDiagnosis;
END_VAR

// Basic function block usage
fbFbVisuDiagnosis(
    // Configure inputs as needed
);

// Check status
IF fbFbVisuDiagnosis.xValid THEN
    // Operation successful
END_IF

IF fbFbVisuDiagnosis.xError THEN
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

