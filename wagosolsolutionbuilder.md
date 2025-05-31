# WagoSolSolutionBuilder v1.0.0.5

## Overview
WAGO PLC library providing WagoSolSolutionBuilder functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbModbusActiveConnection
Function block for a modbus UPD client based on WagoAppPlcModbus.FbMbMasterUdp with cyclic request or started manually.

**Description:**
The connection is automatically opened and closed with each request.

### FbModbusMultipleConnections
Function block to handle equal modbus client requests to multiple modbus servers.

**Description:**
All servers are requested cyclic. There are 'ParameterListApplicationBuilder.MAX_MULTIPLE_MODBUS_CONNECTIONS' parallel connections used. This function can be used to send or request a single query to all servers e.g. to request their temperature or to send central commands. The connection are automatically opened and closed with each request.

### FbModbusMultiServer
Function block for a modbus server where multiple clients can access and each client IP accesses to different variables.

**Description:**
The variables 'I_MbBitAccess_DiscreteInputs', 'I_MbBitAccess_Coils', 'I_MbWordAccess_InputRegisters', 'I_MbWordAccess_HoldingRegisters' are ARRAY [\*,\*] with first array index corresponds to client IP addresses 'asClientIds' and second array index corresponds to modbus registers. .. note:: The bounds are the addresses for modbus access with clients also. .. code-block:: codesys VAR xOpen : BOOL :

### FbRecipeManagement
Function block to handle recipe data applicative. This function block is explicit nesseccary for the communication with the WAGO solution builder.

**Description:**
The defined 'sRecipeDefinition' is read cyclic with 'tCycleTime' and read out, if it is newer than actually loaded. Chosen actions 'xRead' and 'xWrite' are running in second program cycle after triggered, because xBusy is set and there are task blocking functions inside. Following code must be implemented in projects plc program for preventing recipe missmatch (e.g. by extending the recipe variables) .. code-block:: codesys VAR MyRecipe : WagoAppBuildingAutomation.FbRecipeManagement; xRead : BOOL; //Reading Recipe xWrite : BOOL; //Writing Recipe END_VAR code: //call function block with RecipeDefinition 'MyFirstRecipe', created in Recipe Manager MyRecipe(sRecipeDefinition:

**Methods:**

#### WriteRecipe
#### ReadRecipe
## Data Types

### typModbusQuery
Structure type.

### typModbusJob
Structure type.

### typMPBusSubbusDevice
Structure type.

### typModbusRTUSubbusDevice
Structure type.

### typEnOceanSubbusDevice
Structure type.

### typMBusSubbusDevice
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbModbusActiveConnection: FbModbusActiveConnection;
END_VAR

// Basic function block usage
fbFbModbusActiveConnection(
    // Configure inputs as needed
);

// Check status
IF fbFbModbusActiveConnection.xValid THEN
    // Operation successful
END_IF

IF fbFbModbusActiveConnection.xError THEN
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

