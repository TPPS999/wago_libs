# WagoAppIOLink v1.8.0.12

## Overview
WAGO PLC library providing WagoAppIOLink functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbIOL_MasterConfiguration
Provides three different modes for master configuration.

**Description:**
The general configuration of the master module 750-657 is selected via input ``typMode``. AutoConfig: The size of each IO-Link port within the master will be configured according to the connected IO-Link sensors. If the size of the IO-Link devices differ from the 18 bytes of the master, the size of each port will automatically be set depending on the number of IO-Link devices, as follows: 1: portAverage:

**Methods:**

#### GetDiagnosisBuffer
This method gives access to the diagnosis buffer

The function block ``FbIOL_MasterConfiguration`` has an internal buffer collecting diagnosis messages. This method allows reading the buffer as well as resetting the counters. The return value will be true, if access to the buffer is possible and false, if e.g. the function block is not ready and therefore no access to the buffer is possible.

#### SetFastParameter
This method must be called once if the mode is set to ``Fast``. For each port the appropriate values (settings of the modul 750-567) must be assigned.

### FbIOL_M_Configuration
Read and write master configuration

**Description:**
Read and write master configuration

### FbIOL_MasterConfiguration_1657
Provides three different modes for master configuration.

**Description:**
The general configuration of the master module 750-1657 is selected via input ``eModeStartUp``. AutoConfig: The size of each IO-Link port within the master will be configured according to the connected IO-Link sensors. Module size 24 is supported in the following manner: If the size of the IO-Link devices differ from the 18 bytes of the master, the size of each port will automatically be set depending on the number of IO-Link devices, as follows: 1: portAverage:

**Methods:**

#### SetFastParameter
This method must be called once if the mode is set to ``Fast``. For each port the appropriate values (settings of the modul 750-1657) must be assigned.

#### GetDiagnosisBuffer
This method gives access to the diagnosis buffer

The function block ``FbIOL_MasterConfiguration`` has an internal buffer collecting diagnosis messages. This method allows reading the buffer as well as resetting the counters. The return value will be true, if access to the buffer is possible and false, if e.g. the function block is not ready and therefore no access to the buffer is possible.

### FbIOL_PortData
Process IO-Link data on port 1..4

**Description:**
This function block is required for each IO-Link sensor connected to one of the four ports. .. note:: Function block FbIOL_ConfigurationAndStatus must be used only once for each IO-Link module. Once enabled, it takes a few seconds to retrieve the channel configuration. During this period, output ``xBusy`` is true. If process values will be received or data can be transmitted, output ``xValid`` is True. If the module is configured for internal data bus diagnosics, output ``xError`` will display port errors, e.g., if the sensor is disconnected.

### FbIOL_ConfigurationAndStatus
This function block reads the status information. Additionally, it is possible to configure the module. .. note:: This function block must be used exactly once for each IO-Link module

**Description:**
This function block establishes the internal communication to the module immediately after starting the plc program. It takes a fews seconds to finish this initialization phase. Output ``xBusy`` indicates this phase while ``oStatus`` shows more datailed information. At the end, output ``xDone`` will be true for at least one cycle and output ``oStatus`` will show OK. Hint for configuration: If one port is configured as digital output, the size of this port must be 0. .. note:: If this function block is used for fieldbus connection, the time ``STARTUP_WAIT_TIME`` from the parameter list must be increased to approx. 10 sec.

### FbIOL_Base
This function block must be extended for each IO Link device

**Description:**
This is the basic function block for any IO Link device. An example may look like: .. code-block:: codesys FUNCTION_BLOCK FbGeneral_IOL_Device EXTENDS FbIOL_Base VAR_INPUT wIndex : WORD; END_VAR VAR_IN_OUT xReadIndex : BOOL; END_VAR VAR_OUTPUT diDistance : UINT; xValid : BOOL; sIndex : STRING; END_VAR VAR b1 : ARRAY[0..81] OF BYTE; b2 : ARRAY[0..81] OF BYTE; b3 : ARRAY[0..81] OF BYTE; mylen : INT; pString : POINTER TO STRING; END_VAR with the following implementation: .. code-block:: codesys SUPER^(); IF typIOL_Sensor.xMasterConfigured AND udiRxNBytes>0 THEN diDistance:

**Methods:**

#### IOL_Call_CompleteRead
Finish the process of reading an IO-Link value referenced by index and subindex

This method must be executed as the second step of reading an IO-Link value

#### IOL_Call_Read_2
This method allows reading any IO-Link value by performing an IOL call

#### IOL_Call_Write_2
This method allows writing any IO-Link value by performing an IOL call

#### IOL_Call_Write
This method allows writing any IO-Link value by performing an IOL call

#### IOL_Call_PrepareRead
The first step of reading an IO Link value referenced by index and subindex

Reading an IO-Link value is done in two steps. The first step is executing the method `IOL_Call_PrepareRead`. Once this method returns with `True` the second step can be executed, which is the method `IOL_Call_CompleteWrite`

#### IOL_Call_ReadWord
This method allows reading any IO-Link value which is a Word by using an IOL call

#### IOL_Call_CompleteWrite
This method waits for the answer according to a write command of an IOL call

#### IOL_Call_Read
This method allows reading any IO-Link value by performing an IOL call

#### IOL_Call_WriteWord
This method allows writing any IO-Link value which is a Word by using an IOL call

#### IOL_Call_PrepareWrite
This method allows writing any IO-Link value by performing an IOL call

### FbIOL_Call
Perform ISDU Call for IO-Link Devices or read data from master module itself

**Description:**
Access to IO-Link sensors is done with iFI_Index

## Data Types

### eStatus
Enumeration type.

### eMasterConfigModeStartUp
Enumeration type.

### eErrorCode
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbIOL_MasterConfiguration: FbIOL_MasterConfiguration;
END_VAR

// Basic function block usage
fbFbIOL_MasterConfiguration(
    // Configure inputs as needed
);

// Check status
IF fbFbIOL_MasterConfiguration.xValid THEN
    // Operation successful
END_IF

IF fbFbIOL_MasterConfiguration.xError THEN
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

