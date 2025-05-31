# WagoSysModuleBase v2.0.2.10

## Overview
WAGO PLC library providing WagoSysModuleBase functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbModuleParameterMbx2Ext
**Methods:**

#### ReadParameter
Call a Parameter If the parameter channel is free then the wanted service will be triggered and the channel is occupied for other callers. When the method returns with eServiceState.DONE then the wanted job is done. The user MUST handle the return values DONE and ABORT.

#### WriteParameter
| Write the value``uiValue`` at terminals parameter list specified by ``usiParameterNo``. | ``cliCallerID`` have o be an unique WagoClientIdentification.

### FbModuleParameterMbx2
**Methods:**

#### ReadParameter
Call a Parameter If the parameter channel is free then the wanted service will be triggered and the channel is occupied for other callers. When the method returns with eServiceState.DONE then the wanted job is done. The user MUST handle the return values DONE and ABORT.

#### WriteParameter
| Write the value``uiValue`` at terminals parameter list specified by ``usiParameterNo``. | ``cliCallerID`` have o be an unique WagoClientIdentification.

### FbModuleMbx2Ext
**Methods:**

#### MbxCommit
#### MbxPrepare
#### MbxWriteTable
#### MbxWriteRegister
#### MbxWriteMultipleRegister
#### MbxSetPassword
#### MbxSaveUser
#### MbxReadTable
#### MbxReadMultipleRegister
#### MbxReadRegister
### FbModuleMbx2
**Methods:**

#### onAccessServiceRegistered
#### BuildOutputMbxUsedTable
#### GetPosOfMbx
#### RegRemoveMbx
#### RegAddMbx
#### MbxRemoveNextMessage
Removes a complete message with header from pipe in case there is a complete message available. Otherwise this method do nothing. ================ =================================================== Return code Description ================ =================================================== OK message successful removed NO_DATA no message available ================ ===================================================

#### IsMessageAvailable
Check for message available at pipe. Returns TRUE if another message is available

#### MbxGetNexSequencelID
Get the sequence-ID of the next message without remove from pipe ================ =================================================== Return code Description ================ =================================================== 0..255 sequence-ID -1 no message available ================ ===================================================

#### MbxGetNextProtocolID
Get the protocol-ID of the next message without remove from pipe ================ =================================================== Return code Description ================ =================================================== -1 no message available 0 no protocol-ID (may be simple header but not must) 1..255 protocol-ID (it must be an extended header) ================ ===================================================

#### SetProcessOutBit
Set the process output bit specified by ``ByteNo`` and ``BitNo`` to the value ``OutData``.

#### GetProcessOutBit
Get the process output bit specified by ``ByteNo`` and ``BitNo`` of this module.

#### SetProcessOutByte
Set the process output byte specified by ``ByteNo`` to the value ``OutData``.

#### GetProcessOutByte
Get the process output byte specified by ``ByteNo`` of this module.

#### SetProcessOutData
Copy the process output data from the area specified by ``pOutData`` and ``uiNOutData`` to the output process image.

#### GetProcessOutData
Get the process output bytes from byte 0 up to (``uiNOutData`` - 1) and place it at ``pOutData``:

#### MbxIsReady
Check for MBX is ready for data exchange. Returns TRUE if the MBX is synchronized.

#### MbxWrite
Write a message into the FIFO to MBX. If there is not enougth space inside the FIFO the message will be rejected with the result code *FULL*. The given message is checked for valid length in the header before writing. ======================= =================================================== Return code Description ======================= =================================================== OK (0) success FULL not enough buffer space available for new message PRM_INVALID null-pointer or size <2 or size >2G NOT_READY MBX is not ready for communication INVALID_MSG Incosistent message -> invalid length (header) ``udiNdata`` NO_WRITE_WHILE_TCM_MODE Write not possible while TCM-Mode is active ======================= ===================================================

#### MbxGetNextMessage
Get the next message and remove it from pipe. ================ =================================================== Return code Description ================ =================================================== OK successful NO_DATA no message available BUFFER_TO_SMALL buffer not big enought for the next message PRM_INVALID paramter invalid -> null-pointer ================ ===================================================

### FbModuleParameterMbx1
**Methods:**

#### ReadParameter
Call a Parameter If the parameter channel is free then the wanted service will be triggered and the channel is occupied for other callers. When the method returns with eServiceState.DONE then the wanted job is done. The user MUST handle the return values DONE and ABORT.

#### WriteParameter
| Write the value``uiValue`` at terminals parameter list specified by ``usiParameterNo``. | ``cliCallerID`` have o be an unique WagoClientIdentification.

### FbModuleProcessOutputs
**Methods:**

#### SetProcessOutWord
Set the process output word specified by ``ByteNo`` to the value ``OutData``.

#### SetProcessOutDword
Set the process output dword specified by ``ByteNo`` to the value ``OutData``.

#### GetProcessOutWord
Get the process output word specified by ``ByteNo`` of this module.

#### GetProcessOutDword
Get the process output dword specified by ``ByteNo`` of this module.

#### GetModuleOutputSize
Get the process output size [byte] of this module.

#### SetProcessOutBit
Set the process output bit specified by ``ByteNo`` and ``BitNo`` to the value ``OutData``.

#### GetProcessOutBit
Get the process output bit specified by ``ByteNo`` and ``BitNo`` of this module.

#### SetProcessOutByte
Set the process output byte specified by ``ByteNo`` to the value ``OutData``.

#### GetProcessOutByte
Get the process output byte specified by ``ByteNo`` of this module.

#### SetProcessOutData
Copy the process output data from the area specified by ``pOutData`` and ``uiNOutData`` to the output process image.

#### GetProcessOutData
Get the process output bytes from byte 0 up to (``uiNOutData`` - 1) and place it at ``pOutData``:

### FbModuleParameter
**Methods:**

#### ReadParameter
Call a Parameter If the parameter channel is free then the wanted service will be triggered and the channel is occupied for other callers. When the method returns with eServiceState.DONE then the wanted job is done. The user MUST handle the return values DONE and ABORT.

#### WriteParameter
| Write the value``uiValue`` at terminals parameter list specified by ``usiParameterNo``. | ``cliCallerID`` have o be an unique WagoClientIdentification.

### FbModuleProcessInputs
**Methods:**

#### GetProcessInWord
Get the process input word specified by ``ByteNo`` of this module.

#### GetProcessInDword
Get the process input dword specified by ``ByteNo`` of this module.

#### GetModuleInputSize
Get the process input size [byte] of this module.

#### GetProcessInBit
Get the process input bit specified by ``ByteNo`` and ``BitNo`` of this module.

#### GetProcessInByte
Get the process input byte specified by ``ByteNo`` of this module.

#### GetProcessInData
Get the process input bytes from byte 0 up to (``uiNInData`` - 1) and place it at ``pInData``:

### FbModuleMbx1
**Methods:**

#### GetFillBytes
#### SwitchMbxOnOff
#### GetMbxOverlapped
Get information about the mailbox mode.

#### SetProcessOutData
Copy the process output data from the area specified by ``pOutData`` and ``uiNOutData`` to the output process image.

#### GetProcessOutData
Get the process output bytes from byte 0 up to (``uiNOutData`` - 1) and place it at ``pOutData``:

#### GetProcessInData
Get the process input bytes from byte 0 up to (``uiNInData`` - 1) and place it at ``pInData``:

#### GetProcessOutBit
Get the process output bit specified by ``ByteNo`` and ``BitNo`` of this module.

#### SetProcessOutByte
Set the process output byte specified by ``ByteNo`` to the value ``OutData``.

#### GetProcessInByte
Get the process input byte specified by ``ByteNo`` of this module.

#### GetProcessOutByte
Get the process output byte specified by ``ByteNo`` of this module.

#### SetProcessOutBit
Set the process output bit specified by ``ByteNo`` and ``BitNo`` to the value ``OutData``.

#### GetProcessInBit
Get the process input bit specified by ``ByteNo`` and ``BitNo`` of this module.

#### GetMbxSize
Call a MBX service If the mailbox is free then the wanted service will be triggered and the mailbox is occupied for other callers. When the method returns with eServiceState.DONE then the wanted job is done. The user MUST handle the return values DONE and ABORT.

#### GetMbxSizeRegisterNo
#### MbxService
Call a MBX service If the mailbox is free then the wanted service will be triggered and the mailbox is occupied for other callers. When the method returns with eServiceState.DONE then the wanted job is done. The user MUST handle the return values DONE and ABORT.

### FbModuleRegister
**Methods:**

#### GetSoftwareVersion
Call a service to get the software version of this module. When the method returns with eServiceState.DONE then the wanted job is done. The user MUST handle the return values DONE and ABORT.

#### WriteRegister
| Write the value``uiValue`` at terminal register specified by ``usiChannel`` and ``usiRegisterNo``. | ``cliCallerID`` have o be an unique WagoClientIdentification.

#### ReadRegister
| Read a terminal register specified by ``usiChannel`` and ``usiRegisterNo``. | ``cliCallerID`` have to be an unique WagoClientIdentification.

### FbModuleProcessInputsOutputs
**Methods:**

#### GetProcessInWord
Get the process input word specified by ``ByteNo`` of this module.

#### GetProcessInDword
Get the process input dword specified by ``ByteNo`` of this module.

#### GetModuleInputSize
Get the process input size [byte] of this module.

#### GetProcessInBit
Get the process input bit specified by ``ByteNo`` and ``BitNo`` of this module.

#### GetProcessInByte
Get the process input byte specified by ``ByteNo`` of this module.

#### GetProcessInData
Get the process input bytes from byte 0 up to (``uiNInData`` - 1) and place it at ``pInData``:

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbModuleParameterMbx2Ext: FbModuleParameterMbx2Ext;
END_VAR

// Basic function block usage
fbFbModuleParameterMbx2Ext(
    // Configure inputs as needed
);

// Check status
IF fbFbModuleParameterMbx2Ext.xValid THEN
    // Operation successful
END_IF

IF fbFbModuleParameterMbx2Ext.xError THEN
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

