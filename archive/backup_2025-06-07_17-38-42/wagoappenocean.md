# WagoAppEnocean v1.1.4.19

## Overview
WAGO PLC library providing WagoAppEnocean functionality.

**Key Features:**
- Time and date operations
- Control functions
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### FbD20500_NodOn_RollerShutter_Module
### FbD20500_Blind
### FbD2030A
The Function block encodes and decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbD20112_NodOn_Lighting
### FbD20112
### FbD2010F_NodOn_Multifunction
### FbD2010F
### FbD2010E
### FbD2010C
### FbD2010B
### FbD2010A
### FbD24100
The Function block encodes and decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
.. note:: With the command set unit data (`xSetUnitData`) the dimming level is only relevant for the illumination mode service light. The device controlls the dimming level itself in other illumination modes. .. note:: When using `xSetIlluminationMode` higher illumination modes needs to be cleared before lower modes gets active. Supported EEP:

**Methods:**

#### getMaintenanceData_resp
#### getEnvironmentalData_resp
#### getPresenceData_resp
#### getUnitStatus_resp
#### getUnitOperatingState_resp
#### setOccupancy_Cmd
#### setUnitData_Cmd
#### setUnitOperatingState_Cmd
#### getProductStatus_resp
#### setGetCommand_Cmd
### FbEnoceanShowID_EEP
This function block identifies a device's ID and EEPby means of number of consecutive telegram received by the WAGO-Controller.

### FbEnOceanDevice_A5_D5_F6
With this block, a large number of Enocean devices should be able to be queried. The measured values ​​can be read out with the Get methods. The table below lists the supported EEPs.

**Methods:**

#### getTurnSwitch
#### getSetpointCorrection
#### getRelativeHumidity
#### getBinaryState
#### getTemperatureResolution2BYTE
#### getTemperatureResolution1BYTE
### FbD10710_PeopleCounter
The Function block encodes and decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below:

### FbEnocean_WriteBaseId_750_940
Used to change the base ID (station address) of the gateway 750-940. .. note:: IMPORTANT: Writing can only be used 10 times per gateway. There is no possibility to reset this constraint. Also power off/on will not allow more than 10 changes!

**Description:**
You may use this function when change a defect gateway to set new gateways address to the old one. This allows to change the gateway without new learning bidirectional devices. The current station address (before writing and after writing) will be displayed at communication function block |FbEnOcean_750_940_RS485|. After writing or with reading the remaining writing cycles for the station address will be displayed at output `bRemainingWriteCycles`. Station addresses of the gateway always ends with 16#80 or 16#00. If other end addresses are chosen, the address will automatically reduced to the lower address with that end numbers. e.g.: `dwNewStationAddress`

### FbEnoceanD2FEFE_RoomOperatingPanel
The Function block receives and transmits (bidrectional) Enocean data using SMART-ACK .. note::Support only Thermokon gateway STC65-RS485-EVC.

### FbReceiver_1BS
Base class for receiving 1BS

**Methods:**

#### getDataByte
### FbEnoceanSerial
Base class for Enocean communication over serial

**Methods:**

#### isOpen
#### isValidPortID
#### isRxOverflow
#### isIdle
#### isValidPort
#### Serial
#### isRxBufferFull
### FbEnocean_STC65_RS485_EVC_Config
Advanced configuration for enocean gateway.

**Description:**
Function block sets advance configuration parameters to the Thermokon STC65-RS-485-EVC Gateway with bidirectional communication. .. note:: Changes will take effect after the next controller reboot. .. note:: Support only Thermokon gateway STC65-RS485-EVC from FW 3.0.2.

### FbEnoceanF61000_WindowHandle
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA53003_DigitalInputWakeTemp
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50601_LightSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbBaseA512xx_TempSensor
Base class for temperature sensor with Enocean Profile A5-12-xx or 07-12-xx

### FbEnocean_4BS_Bidirectional
The Function block enncodes and decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below:

### FbEnoceanA50402_TempHumiditySensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnocean_VLD_Send
The function block encodes EnOcean radio telegram of type VLD, which is transmitted via an EnOCean Gateway.

### FbEnoceanA51013_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51009_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanD211xx_RoomOperatingPanel
The Function block receives and transmits (bidrectional) Enocean data using SMART-ACK .. note::Support only Thermokon gateway STC65-RS485-EVC.

### FbEnoceanA51002_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51022_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50908_PureCO2_Sensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50902_CO2_Sensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50230_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbConfigFilterChannel
Gateway filter channel configuration.

### FbEnoceanA51305_DirectionExchange
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50602_LightSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51205_TempContainerSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbBaseA506xx_LightSensor
Base class for Enocean Profile A5-06-xx or 07-06-xx

### FbEnoceanBase
Base class for Enocean function block

**Methods:**

#### setClassname
#### setStatusObject
### FbEnoceanA5100A_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbBaseA504xx_TempHumiditySensor
Base class for Enocean Profile A5-04-xx or 07-04-xx

### FbBaseA510xx_RoomOperatingPanel
Base class for Enocean Profile A5-10-xx or 07-10-xx

**Methods:**

#### getTurnSwitch
#### isBinaryState
#### getRelativeHumidity
#### getSetpointCorrection
### FbEnoceanA51200_Counter
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanD50001_SingleInputContact
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51018_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanShowPushButtonID
This function block identifies a device's of EEP ORG=16#05 or ROPRG=16#F6 (Repeated Switch Communication) by means of number of consecutive telegram received by the WAGO-Controller.

### FbEnoceanA50216_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanA51010_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50907_Particles
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA5140A_Window_DoorSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50703_OccupancySensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbBaseA508xx_LightTempOccupancySensor
Base class for Enocean Profile A5-08-xx or 07-08-xx

### FbEnocean_VLD_Receive
The function block dencodes EnOcean radio telegram of type VLD, which is received from an EnOcean Gateway.

### FbEnoceanA50906_Radon
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanD21107_RoomOperatingPanel
The Function block receives and transmits (bidrectional) Enocean data using SMART-ACK .. note::Support only Thermokon gateway STC65-RS485-EVC.

### FbEnoceanD21105_RoomOperatingPanel
The Function block receives and transmits (bidrectional) Enocean data using SMART-ACK .. note::Support only Thermokon gateway STC65-RS485-EVC.

### FbEnocean_RPS_Send
The function block encodes EnOcean radio telegram of type RPS, which is transmitted via an EnOCean Gateway.

### FbReceiver_4BS
Base class for receiving 4BS

**Methods:**

#### getDataByte
### FbEnoceanA51017_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA52003_LinePoweredActuator
The Function block enncodes and decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below:

### FbEnoceanA50210_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbBaseA530xx_SingleInputContact
Base class for device with Enocean Profile A5-30-xx or 07-30-xx

### FbEnoceanA51001_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50603_LightSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnOcean_WriteFilterStatus
**Methods:**

#### setStatusObject
### FbEnoceanA50802_LightTempOccupancySensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA502xx_TempSensor
The function block outputs value of a temperature sensor.

**Description:**
The Function block decodes all devices with an Enocean Profile A5-02-xx or 07-02-xx; whereby xx refers to Type of device in its individual characteristics (TYPE) and is defined at input ''bType''. Please refer to EnOcean Equipment Profiles (EEP) or the manufacturer's manual to find the TYPE number for your device.

### FbEnoceanA50201_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbFillSmartAckMailbox
Fill mailbox for Smart act devices

### FbEnoceanA51101_LightingController
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA53001_SingleInputContactBateryMonitor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbDeleteSensorFromFilterChannel
Delete sensor from filter channel

### FbConfig_STC65
Base class for gateway configuration

### FbEnoceanA50217_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbBaseF603xx_RockerSwitch_4_Rocker
Base class for Enocean Profile F6-03-xx or 05-03-xx

### FbEnoceanA51409_Window_DoorSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51003_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA513XX_Universal
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanF60201_RockerSwitch_2_Rocker
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA5100B_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50701_OccupancySensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51301_WeatherStation
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbDevice
Base class for a Device

### FbEnoceanA50403_TempHumiditySensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA52012_TempControllerInput
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51302_SunIntensity
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnocean_MSC_Send
The function block encodes EnOcean radio telegram of type MSC, which is transmitted via an EnOCean Gateway.

### FbEnocean_4BS_Send
The function block encodes EnOcean radio telegram of type 4BS, which is transmitted via an EnOCean Gateway.

### FbEnoceanD21104_RoomOperatingPanel
The Function block receives and transmits (bidrectional) Enocean data using SMART-ACK .. note::Support only Thermokon gateway STC65-RS485-EVC.

### FbEnoceanA51023_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbBidirectional
Base class for a bidirectional

### FbBidirectional_4BS
Base class for bidirectional 4BS

**Methods:**

#### getDataByte
#### setDataByte
### FbBaseA509xx_GasSensor
Base class for device with Enocean Profile A5-09-xx or 07-09-xx

### FbEnoceanA53701_DemandResponse
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50213_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanA51201_Electricity
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50211_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanA50212_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanA50702_OccupancySensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA5021A_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanA53004_DigitalInput8bits
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbShow_ID_ByClick
### FbEnoceanA51407_Window_DoorSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51006_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbBaseD211xx_RoomOperatingPanel
Base class for device with Enocean Profile D2-11-xx .. note::Support only Thermokon gateway STC65-RS485-EVC.

### FbEnoceanA52002_BasicActuator
The Function block enncodes and decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below:

### FbLearnByDeviceID
Teach in sensor via ID

### FbEnoceanA5021B_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanD21108_RoomOperatingPanel
The Function block receives and transmits (bidrectional) Enocean data using SMART-ACK .. note::Support only Thermokon gateway STC65-RS485-EVC.

### FbEnoceanA50220_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbReadGatewayFirmwareVersion
Read gateway firmware version

### FbConfigGateway_STC65
Gateway configuration.

### FbEnoceanA51303_DateExchange
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanF60302_RockerSwitch_4_Rocker
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbReadGatewayChipBaseID
Read gateway chip ID and base ID.

### FbReceiver_RPS
Base class for receiving RPS

**Methods:**

#### getDataByte
### FbTransmitter
Base class for a receiver

### FbEnocean_STC65_RS485_EVC
Enocean master over serial communication (RS485) .. note:: This gateway can handle bidirectional communication.

**Description:**
Function block sets up a link to the Thermokon STC65-RS-485-EVC Gateway to provide communication employing the EnOcean radio protocol. For advanced configuration settings uses the |FbEnocean_STC65_RS485_EVC_Config|. .. note:: Support only Thermokon gateway STC65-RS485-EVC.

### FbESP3_SmartAck
**Methods:**

#### setStatusObject
### FbBaseA502xx_TempSensor
Base class for Enocean Profile A5-02-xx or 07-02-xx

**Methods:**

#### getTemperatureResolution1BYTE
#### getTemperatureResolution2BYTE
### FbEnoceanF60202_RockerSwitch_2_Rocker
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51007_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA5100D_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanD21101_RoomOperatingPanel
The Function block receives and transmits (bidrectional) Enocean data using SMART-ACK .. note::Support only Thermokon gateway STC65-RS485-EVC.

### FbEnoceanA50801_LightTempOccupancySensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbGateway
Base class for Enocean gateway over I_Port

**Methods:**

#### setStatusObject
#### setClassname
### FbEnoceanA51011_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbBaseA512xx_AutomatedMeterReading
Base class for Automated meter reading with Enocean Profile A5-12-xx or 07-12-xx

### FbEnoceanD21103_RoomOperatingPanel
The Function block receives and transmits (bidrectional) Enocean data using SMART-ACK .. note::Support only Thermokon gateway STC65-RS485-EVC.

### FbSmartAckLearnByButton
Teach in sensor via learn button for smart ack

### FbEnoceanA5020B_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnocean_1BS_Send
The function block encodes EnOcean radio telegram of type 1BS, which is transmitted via an EnOCean Gateway.

### FbEnoceanA51310_SunPositionRadiation
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### Fb_EnOceanCom
**Methods:**

#### setStatusObject
### FbEnoceanF60402_KeyCardActivatedSwitchERP2
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbD21500_PeopleActivityCounter
The Function block encodes and decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below:

### FbEnoceanD21102_RoomOperatingPanel
The Function block receives and transmits (bidrectional) Enocean data using SMART-ACK .. note::Support only Thermokon gateway STC65-RS485-EVC.

### FbEnoceanA51304_TimeDateExchange
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanF60401_KeyCardActivatedSwitch
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnocean_1BS_Receive
The function block dencodes EnOcean radio telegram of type 1BS, which is received from an EnOcean Gateway.

### FbFilterTableChannel_STC65
Base class for filter table channel

### FbEnoceanA50218_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbReadGatewayStationAddress
Read gateway station address

### FbEnoceanA50219_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanA50209_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanF60301_RockerSwitch_4_Rocker
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbReadSensorFilterChannel
Read sensor of filter channel

### FbEnoceanA50207_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanA50204_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnocean_750_642
Enocean receiver using Wago EnOcean module 750-642 .. note:: This gateway handles only unidirectional communication.

**Description:**
Function block sets up a link to the Wago EnOCean module 750-642 to provide communication employing the EnOcean radio protocol. .. note:: Support only EnOCean module 750-642.

### FbBaseShowID
Base class for Show ID

**Methods:**

#### setStatusObject
#### setClassname
### FbEnoceanA51008_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA52004_HeatingRadiatorValve
The Function block enncodes and decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below:

### FbEnoceanA51306_GeographicPositionExchange
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnocean_MSC_Receive
The function block dencodes EnOcean radio telegram of type MSC, which is received from an EnOcean Gateway.

### FbManageFilterList_750_940
The Function block reads, writes and deletes filter list in gateway 750-940. .. note:: The filter list ``aFilterListReadESP3`` and ``aFilterListWriteESP3`` weren't synchornizised which each other.

**Description:**
``aFilterListWriteESP3``: User's filter list with filter which shall be written to EnOcean module, only marked filter with ``xWrite`` as TRUE will be written to the EnOcean module when trigger the ``xAddAll`` flag. If the user reads all filter only the filter list ``aFilterListReadESP3`` will be updated and not the ``aFilterListWriteESP3`` list. If the user retrigger the ``xAddAll`` flag, the same marked filter will be written again to the EnOcean module which will be seen, when the filter list ``aFilterListReadESP3`` will be updated. If the User add a single filter wich is stored in ``typFilterAddTyp`` with the flag ```xFilterAdd``, the filter will be written to the EnOcean module and if this was successfully, the new filter will be set in ``FilterListWriteESP3`` list on the first entry which is marked with ``xWrite`` as FALSE. ``aFilterListReadESP3``: Every time the ``xReadAll`` flag is triggered, all filters stored in EnOcean module will be read. If the EnOcean module has no filter so far, the list will be empty and all entries will be marked as ``xReady`` with TRUE. If some filter in this list shall be erased on the EnOcean module, the index of the filter in the ``aFilterListReadESP3`` list must be stored in ``bSelectIndexDelete`` an the trigger flag ``xDelete`` must be set. When the process was successfully the filter in the ``aFilterListReadESP3`` list will be erased and marked as ``xReady`` as TRUE, if the user update the list by trigger the ``xReadAll`` flag, the list will be automatically in the corret order. Read all set filter from EnOcean module: 1. trigger ``xReadAll`` once 2. all read filter will be writen to ``aFilterListReadESP3`` and signaled as ready with the flag ``xReady`` Delete all filter from the EnOcean module: 1. trigger ``xDeleteAll`` once 2. if process was successfully, read again all filter from module an check if some active filters are in ``aFilterListReadESP3`` Add a single filter to the EnOcean module: 1. set filter parameter in ``typFilterAddTyp`` 2. trigger ``xFilterAdd`` once 3. if process was successfully, the written filter will be added to ``aFilterListWriteESP3`` and the flag ``xWrite`` will be set Delete single filter from EnOcean module based on a read filter from ``aFilterListReadESP3``: 1. first make sure to actualize the ``aFilterListReadESP3`` list by read all filter from EnOcean module 2. get the index from ``aFilterListReadESP3`` with the filter to delete an store this index in ``bSelectIndexDelete`` 3. trigger ``xDelete`` to start the delete process (maybe this ist optional) 4. if the delete process was successfully, read all filter from the module an in ``aFilterListReadESP3`` the filter must be erased

### FbEnoceanA51204_TempLoadSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50803_LightTempOccupancySensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnOcean_750_940_RS485
Enocean master with 750-940 over serial communication (RS485). .. note:: This gateway can handle bidirectional communication.

**Description:**
Function block sets up a link to the 750-940 Gateway to provide communication employing the EnOcean radio protocol. The communication between this function block and the 750-940 Gateway is handled with the ESP3 protocol. .. note:: Support only 750-940 Gateway.

**Methods:**

#### setStatusObject
### FbEnoceanA51203_Water
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51016_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51403_Window_DoorSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA5100C_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbWriteGatewayConfig
Write gateway configurations

### FbEnOcean_FillMbx_SMACK
**Methods:**

#### setStatusObject
### FbEnoceanA52006_HarvestingPoweredActuator
The Function block enncodes and decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below:

### FbEnoceanA51019_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanShowID
This function block identifies a device's ID by means of number of consecutive telegram received by the WAGO-Controller.

### FbEnoceanA52001_BatteryPoweredActuator
The Function block enncodes and decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below:

### FbEnocean_4BS_Receive
The function block dencodes EnOcean radio telegram of type 4BS, which is received from an EnOcean Gateway.

### FbEnoceanA50905_VOC_Sensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51402_Window_DoorSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbBaseF610xx_WindowHandle
Base class for Enocean Profile F6-10-xx or 05-10-xx

### FbEnoceanA50202_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbLearnByButton
Teach in sensor via learn button

### FbEnoceanA50205_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanA50208_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanA51406_Window_DoorSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51015_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51202_Gas
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51404_Window_DoorSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbBaseD2YYxx_SmartAck
Base class for bidrectional Enocean data using SMART-ACK .. note::Support only Thermokon gateway STC65-RS485-EVC.

### FbEnoceanA50206_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanA51405_Window_DoorSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51005_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA51004_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbReadGatewayConfig
read gateway configurations

### FbReadFilterState
Read filter stateRead filter state

### FbEnoceanA51014_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbBaseA507xx_OccupancySensor
Base class for Enocean Profile A5-07-xx or 07-07-xx

### FbEnoceanA50215_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnocean_RPS_Receive
The function block dencodes EnOcean radio telegram of type RPS, which is received from an EnOcean Gateway.

### FbEnoceanA50401_TempHumiditySensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50203_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanA50501_BarometricSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA5020A_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbReceiver
Base class for a receiver

### FbBaseF604xx_KeyCardActivatedSwitch
Base class for Enocean Profile F6-04-xx or 05-04-xx

### FbEnoceanA50904_CO2_Sensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbManageSmartAckFilterTable
This function block manages gateways smart ack filter table list by reading, learning or deleting Enocean device IDs. .. note:: Support only Thermokon gateway STC65-RS485-EVC.

### FbEnoceanA51012_RoomOperatingPanel
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA50214_TempSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

**Description:**
The supported EnOcean Equipment Profiles (EEP) are listed in the table below.

### FbEnoceanA51408_Window_DoorSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanF61001_WindowHandle_ERP2
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA53002_SingleInputContact
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

### FbEnoceanA510xx_RoomOperatingPanel
The Function block decodes Enocean devices with an Enocean Profile A5-10-xx or 07-10-xx.

**Description:**
The ''bType'' input corresponds to the device individual characteristics (TYPE) and must be input according to the EnOcean Equipment Profile (EEP) used by the sensor. The maximum setpoint correction is specified at the ''rMaxSetpointCorrection'' output. Please refer to EnOcean Equipment Profiles (EEP) or the manufacturer's manual to find the TYPE number for your device.

### FbBaseF602xx_RockerSwitch_2_Rocker
Base class for Enocean Profile F6-02-xx or 05-02-xx

### FbEnoceanD21106_RoomOperatingPanel
The Function block receives and transmits (bidrectional) Enocean data using SMART-ACK .. note::Support only Thermokon gateway STC65-RS485-EVC.

### FbEnoceanA51401_Window_DoorSensor
The Function block decodes Enocean device according to the Enocean Equipment Profiles (EEP).

## Data Types

### typ_SetParameters_D205XX
Structure type.

### typ_ReplyPositionAndAngle_D205XX
Structure type.

### typ_PositionAndAngleBase_D205XX
Structure type.

### typ_GoToPositionAndAngle_D205XX
Structure type.

### typ_StatusResponse_D201XX
Structure type.

### typ_SetLocal_D201XX
Structure type.

### typ_MeasurementReponse_D201XX
Structure type.

### typ_Measurement_D201XX
Structure type.

### typ_ExternalInterfaceSettings_D201XX
Structure type.

### typ_AfterTeachInInfo
Structure type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbFbD20500_NodOn_RollerShutter_Module: FbD20500_NodOn_RollerShutter_Module;
END_VAR

// Basic function block usage
fbFbD20500_NodOn_RollerShutter_Module(
    // Configure inputs as needed
);

// Check status
IF fbFbD20500_NodOn_RollerShutter_Module.xValid THEN
    // Operation successful
END_IF

IF fbFbD20500_NodOn_RollerShutter_Module.xError THEN
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

