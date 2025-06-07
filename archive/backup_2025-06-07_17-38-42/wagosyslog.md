# WagoSysLog v1.0.2.5

## Overview
WAGO PLC library providing WagoSysLog functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbLogChSysUdpPid
This log-channel is for put Log-Messages to the linux syslog-ng server. The server have to support the udp protocol. The syslog server may be a accessible remote server at the network. At declaration you have to assign a channel name at the constructor. This name will be the Program-Name ( ${PROGRAM} ) at syslog configuration. .. important:: | For this name are only alphanumeric characters allowed. No additional characters are allowed. This is a restriction of syslog. This channel logs the loggername and the given class name as pid ( ${PID} ) so you can separate this informations at the logfile. .. hint:: The default logfile defined at the example configuration is /var/log/wago_plc_log_pid.log .. hint:: | For use this channel you have to register it at one or more logger(s). | For more information see |FbLogger.RegisterLogChannel| or read the documentation of the |LoggerManager|

### FbComportLogger
The main task of the logger is to log the communication on a communication port. .. note:: Each logger should have a unique name.

**Methods:**

#### privWriteHexDump
Generates a well formed log message from the given message and a hex dump from the given data. This message is send to all registered Log-Channels

#### setClassName
Set the name of the class.

#### setLoggerName
Set the name of the logger.

### FbLogger
The main task of the logger is to offer some methods for generate Log-Messages. So the logger offers a method to generate Log-Messages from a simple Text-Message and also the logger provide a method for logging status objects derivated from FbResult. All these methods starts with the item *write...()*. The logger accept all these messages and in case that one or more Log-Channel(s) are registered at the logger it generates a well formed log message and redirect this message to all registered Log-Channels. If there is no channel registered all messages are ignored. You may have many loggers in a project. At declaration you have to assign a logger name at the constructor. .. note:: Each logger should have a unique name.

**Methods:**

#### RegisterLogChannel
This method register the given Log-Channel at this logger. It is possible to register max. 5 Log-Channels at each logger. If you need more you have to modify the |Parameter| MAX_LOG_CHANNELS. After successful registration all Log-Messages are given to the Log-Channel.

#### writeStatusObject
Generates a well formed log message from the given status object and redirect this message to all registered Log-Channels

#### writeHexDump
Generates a well formed log message from the given message and a hex dump from the given data. This message is send to all registered Log-Channels

#### UnRegisterLogChannel
This method unregister the given Log-Channel from this logger.

#### writeMsg
Generates a well formed log message from the given message and redirect this message to all registered Log-Channels

### FbLogChIde
This log-channel is for put Log-Messages to the IDE-Logger. At declaration you have to assign a channel name at the constructor. This name will be the Logger-Name at the IDE. .. hint:: | For use this channel you have to register it at one or more logger(s). | For more information see |FbLogger.RegisterLogChannel| or read the documentation of the |LoggerManager|

### FbLogChSysUdp
.. note:: This function block is for compatibility with old projects. It is recommended to use for new projects the more powerfully |FbLogChSysUdpPid| This log-channel is for put Log-Messages to the linux syslog-ng server. The server have to support the udp protocol. The syslog server may be a accessible remote server at the network. At declaration you have to assign a channel name at the constructor. This name will be the Program-Name at syslog. .. important:: | For this name are only alphanumeric characters allowed. No additional characters are allowed. This is a restriction of syslog. | Since FW 02.06.15 exits a syslog default configuration for a channel with the name *WAGO* .. hint:: | For use this channel you have to register it at one or more logger(s). | For more information see |FbLogger.RegisterLogChannel| or read the documentation of the |LoggerManager|

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbLogChSysUdpPid: FbLogChSysUdpPid;
END_VAR

// Basic function block usage
fbFbLogChSysUdpPid(
    // Configure inputs as needed
);

// Check status
IF fbFbLogChSysUdpPid.xValid THEN
    // Operation successful
END_IF

IF fbFbLogChSysUdpPid.xError THEN
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

