# WagoAppConfigTool v2.0.1.0

## Overview
WAGO PLC library providing WagoAppConfigTool functionality.

**Key Features:**
- Time and date operations
- Communication protocols
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbSetBridgeConfig
Get ethernet information about the interfaces X11

### FbNetworkConfig
**Methods:**

#### getIpConfig
#### setInterfaceConfig
#### getBridgeConfig
#### setBridgeConfig
#### setIpConfig
#### getInterfaceConfig
### FbGetSnmpV3TrapReceiverData
Get the specified v3 user data

### FbGetSnmpV1V2Community
Get the parameter of the specified by usiNumber v1-v2 community

### FbGetGateway_number
Get detail information about the gateway 2

**Methods:**

#### onFinish
### FbSetGateway_number
Set the parameters of the second gateway

### FbConfigTool
This function block represents the functionality from codesys 2.x. It is able to execute the config scripts documented in the manual of the pfc controller. All these scripts are placed in the folder /etc/config-tools/ of the controller. .. note:: The call of the script have to start with `./` like `./get_coupler_details order-number` This FB need min. FW (09).

### FbGetX12_NetworkAddress
Identifies the parameters currently used for the ETHERNET interface X12. In case of DHCP or BOOTP the ip and subnet mask can be different to the information you get with the |FbGetX12_NetworkAddress|.

**Methods:**

#### onFinish
### FbGetBridgeConfig
Get ethernet information about the interfaces X11

**Methods:**

#### onFinish
### FbGetX12_EthernetConfig
Get ethernet information about the interfaces X12

**Methods:**

#### onFinish
### FbSetX12_EthernetConfig
Set the ethernet configuration of port X12

### FbSetX12_NetworkAddress
Set network address for the interfaces X12. In case of DHCP or BOOTP this ip and subnet mask can be different to the actual used address, because this address is used for static ip only. For get the actual used address use |FbGetX12_ActualNetworkAddress|.

### FbGetX11_NetworkAddress
Identifies the parameters currently used for the ETHERNET interface X11. In case of DHCP or BOOTP the ip and subnet mask can be different to the information you get with the |FbGetX11_NetworkAddress|.

**Methods:**

#### onFinish
### FbGetX11_EthernetConfig
Get ethernet information about the interfaces X11

**Methods:**

#### onFinish
### FbSetX11_EthernetConfig
Set the ethernet configuration of port X11

### FbSetX11_NetworkAddress
Set network address for the interfaces X11. In case of DHCP or BOOTP this ip and subnet mask can be different to the actual used address, because this address is used for static ip only. For get the actual used address use |FbGetX11_ActualNetworkAddress|.

### FbGetNtpActiveState
Get the state of a NTP connection

**Methods:**

#### onFinish
### FbSetFwModbusConfigUdp
Enables / Disables the Modbus-Tcp-Server and set the used Port

### FbSetFwModbusConfigTcp
Enables / Disables the Modbus-Tcp-Server and set the used Port

### FbGetHardwareIndex
Identifies the hardware index of the controller

### FbGetHttps
Get information about HTTPS server state

**Methods:**

#### onFinish
### FbSetHttp
Enables / Disables the HTTP-Server

### FbGetHttp
Get information about HTTP server state

**Methods:**

#### onFinish
### FbSetFtps
Enables / Disables the FTPS-Server

### FbGetFtps
Get information about ftp server state

**Methods:**

#### onFinish
### FbSetFtp
Enables / Disables the FTP-Server

### FbGetFtp
Get information about ftp server state

**Methods:**

#### onFinish
### FbSetSshConfig
Configures the SSH-Server

### FbGetGateway_2
Get detail information about the gateway 2

**Methods:**

#### onFinish
### FbGetX1_ActualNetworkAddress
Identifies the parameters currently used for the ETHERNET interface X1. In case of DHCP or BOOTP the ip and subnet mask can be different to the information you get with the |FbGetX1_NetworkAddress|.

**Methods:**

#### onFinish
### FbGetX2_NetworkAddress
Get network address information about the interfaces X12 In case of DHCP or BOOTP this ip and subnet mask can be different to the actual used address, because this address is used for static ip only. For get the actual used address use |FbGetX2_ActualNetworkAddress|. .. Note:: This address is for separated mode only. (see folder `DSA Mode`)

**Methods:**

#### onFinish
### FbGetX1_NetworkAddress
Get network address information about the interfaces X1. In case of DHCP or BOOTP this ip and subnet mask can be different to the actual used address, because this address is used for static ip only. For get the actual used address use |FbGetX1_ActualNetworkAddress|.

**Methods:**

#### onFinish
### FbGetX2_EthernetConfig
Get ethernet information about the interfaces X2

**Methods:**

#### onFinish
### FbGetX1_EthernetConfig
Get ethernet information about the interfaces X1

**Methods:**

#### onFinish
### FbGetDomainName
Identifies the domain name

### FbGetActualHostName
Identifies the actual host name

### FbGetHostName
Identifies the host name

### FbGetHomeDirOnSdCard
Get information where the home dir is placed

**Methods:**

#### onFinish
### FbGetComPortOwner
Get the owner of the onboard comport

**Methods:**

#### onFinish
### FbGetSnmpV3UserData
Get the specified v3 user data

### FbGetSnmpV1V2TrapReceiver
Get the parameter of the specified by usiNumber v1-v2 trap receiver

### FbSetServicePortOwner
Set the owner of the serial onboard service port (COM 1)

### FbSetComPortOwner
Set the owner of the serial onboard com port (COM 0)

### FbSetClockTimeZone
Set the local date of the clock

### FbSetClockHourFormat
Set the local date of the clock

### FbSetClockUtcTime
Set the local date of the clock

### FbSetClockLocalTime
Set the local time of the clock

### FbSetClockLocalDate
Set the local date of the clock

### FbSetNtpConfig
Set the NTP configuration

### FbSetX2_EthernetConfig
Set the ethernet configuration of port X2

### FbSetX1_EthernetConfig
Set the ethernet configuration of port X1

### FbSetDsaMode
Sets the switch configuration.

### FbDnsServerDelete
Remove a DNS server

### FbDnsServerAdd
Add a DNS server

### FbSetGateway_2
Set the parameters of the second gateway

### FbSetGateway_1
Set the parameters of the first gateway

### FbSetX2_NetworkAddress
Set network address for the interfaces X2. In case of DHCP or BOOTP this ip and subnet mask can be different to the actual used address, because this address is used for static ip only. For get the actual used address use |FbGetX2_ActualNetworkAddress|.

### FbSetX1_NetworkAddress
Set network address for the interfaces X1. In case of DHCP or BOOTP this ip and subnet mask can be different to the actual used address, because this address is used for static ip only. For get the actual used address use |FbGetX1_ActualNetworkAddress|.

### FbSetDomainName
Set the domain name

### FbSetHostName
Set the host name

### FbSetHomeDirOnSdCard
Set the home media

### FbGetSnmpGeneralConfig
Get the SNMP general configuration

### FbGetSshConfig
Get information about the SSH server

**Methods:**

#### onFinish
### FbGetActivePartition
Get the media of the active partition.

### FbGetServicePortOwner
Get the owner of the service interface

**Methods:**

#### onFinish
### FbGetClockData
Get Time and Date

### FbGetNtpConfig
Get detail information about the NTP (network time protocol) configuration

**Methods:**

#### onFinish
### FbGetDsaMode
Query the switch configuration:

**Methods:**

#### onFinish
### FbGetDnsServer
Get detail information about a DNS server

### FbGetX2_ActualNetworkAddress
Identifies the parameters currently used for the ETHERNET interface X2 in 'separated' mode. In case of DHCP or BOOTP the ip and subnet mask can be different to the information you get with the |FbGetX2_NetworkAddress|.

**Methods:**

#### onFinish
### FbGetRuntimeConfig
Get information about the runtime environment

### FbGetRtsInfo
Get the plc state

### FbGetCouplerDetails
Identifies various information about the controller

### FbGetGateway_1
Get detail information about the gateway 1

**Methods:**

#### onFinish
### FbConfigScriptBase
Base class for async execute

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbSetBridgeConfig: FbSetBridgeConfig;
END_VAR

// Basic function block usage
fbFbSetBridgeConfig(
    // Configure inputs as needed
);

// Check status
IF fbFbSetBridgeConfig.xValid THEN
    // Operation successful
END_IF

IF fbFbSetBridgeConfig.xError THEN
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

