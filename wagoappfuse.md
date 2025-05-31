# WagoAppFuse v1.6.1.7

## Overview
WAGO PLC library providing WagoAppFuse functionality.

**Key Features:**
- Professional PLC integration
- Error handling and status reporting

## Core Function Blocks

### GeneralFbManager
Using the visualisations ``VisuSwitch_4Channel`` or ``VisuSwitch_8Channel`` please adjust within the |ParameterList| ``MAX_VISU_SCREENS_4CHANNEL`` and ``MAX_VISU_SCREENS_8CHANNEL`` according to the number of fuses used in the actual project. Each instance of an IO-Link fuse registers itself while the init process at the GeneralFb-Manager. The GeneralFb-Manager holds internal a list with the references and the names of each IO-Link fuse. The GeneralFb-Manager is able to handle up to 10 IO-Link fuse instances by default. In case of more instances you have to modify the |ParameterList| MAX_FB.

### FbIOLink_Fuse_8Channel
Handling electronic 4-channel fuse 787-166/0000-0080

**Description:**
The fuse may be handled by this function block or with the help of the integrated viusalization element. Each channel may be activated or deactivated. For each channel the trip current may be set. Cyclicly reading of the actual current is performed. .. note:: This function block must be used with ``Fb_IOLinkMasterConfig`` Link the input ``typIOL_Sensor`` to output ``aIOL_Device`` of the IO-Link master function block ``Fb_IOLinkMasterConfig`` Input aOnOffReset will override an setting done by the visualization. By the input ``xWriteTripCurrent`` all 8 trip currents will be written. .. note:: The function blocks ``FbIOLink_Fuse_8Channel`` must assign a name in the declaration Example: Fuse2: FbIOLink_Fuse_8Channel('Fuse_OG1');

### FbIOLink_Fuse_4Channel
Handling electronic 4-channel fuse 787-1664/0000-0080

**Description:**
The fuse may be handled by this function block or with the help of the integrated viusalization element. Each channel may be activated or deactivated. For each channel the trip current may be set. Cyclicly reading of the actual current is performed. .. note:: This function block must be used with ``Fb_IOLinkMasterConfig`` Link the input ``I_Port`` to output 1..4 of the IO-Link master function block ``Fb_IOLinkMasterConfig`` Input aOnOffReset will override an setting done by the visualization. By the input ``xWriteTripCurrent`` all 4 trip currents will be written. .. note:: The function blocks ``FbIOLink_Fuse_4Channel`` must assign a name in the declaration Example: Fuse2: FbIOLink_Fuse_4Channel('Fuse_OG1');

### Fb787_2_1668_ReadCurrent
Epsitron electronic fuse (8 channel)

**Description:**
This function block supports the 89-bit protocol to read the current of each channel. Depending on the input ``xReadSetting`` it is differentiated between reading the channels setting or reading the actual current (supported by FW>2.1). Devices without overcurrent protection can only display the channels current setting. The module is activated via the ``xEnable`` input. If configuration of the channels is to be performed using the buttons on the device, the module must be deactivated while configuration is in progress. The connection to the device is made via a digital input ``xS2_Input`` and via a digital output ``xS1_Output``. You can select the channels to be activated via the input ``xChannelxActive``. Configuration is started using the ``xConfig`` input. The ``xDone`` output signals the completion of the configuration procedure. The current status of the various channels is indicated at the ``eChannelxStatus`` outputs. .. note:: This function block must be executed in a task with a call-up interval of 70 ms.

### Fb787_2_1668
Epsitron electronic fuse (8 channel)

**Description:**
The module is activated via the ``xEnable`` input. If configuration of the channels is to be performed using the buttons on the device, the module must be deactivated while configuration is in progress. The connection to the device is made via a digital input ``xS2_Input`` and via a digital output ``xS1_Output``. You can select the channels to be activated via the input ``xChannelxActive``. Configuration is started using the ``xConfig`` input. The ``xDone`` output signals the completion of the configuration procedure. The current status of the various channels is indicated at the ``eChannelxStatus`` outputs. .. note:: This function block must be executed in a task with a call-up interval of 70 ms.

### Fb787_2_1664_ReadCurrent
Epsitron electronic fuse (4 channel)

**Description:**
This function block supports the 89-bit protocol to read the current of each channel. Depending on the input ``xReadSetting`` it is differentiated between reading the channels setting or reading the actual current (supported by FW>2.1). Devices without overcurrent protection can only display the channels current setting. The module is activated via the ``xEnable`` input. If configuration of the channels is to be performed using the buttons on the device, the module must be deactivated while configuration is in progress. The connection to the device is made via a digital input ``xS2_Input`` and via a digital output ``xS1_Output``. You can select the channels to be activated via the input ``xChannelxActive``. Configuration is started using the ``xConfig`` input. The ``xDone`` output signals the completion of the configuration procedure. The current status of the various channels is indicated at the ``eChannelxStatus`` outputs. .. note:: This function block must be executed in a task with a call-up interval of 70 ms.

### Fb787_2_1664
Epsitron electronic fuse (4 channel)

**Description:**
The module is activated via the ``xEnable`` input. If configuration of the channels is to be performed using the buttons on the device, the module must be deactivated while configuration is in progress. The connection to the device is made via a digital input ``xS2_Input`` and via a digital output ``xS1_Output``. You can select the channels to be activated via the input ``xChannelxActive``. Configuration is started using the ``xConfig`` input. The ``xDone`` output signals the completion of the configuration procedure. The current status of the various channels is indicated at the ``eChannelxStatus`` outputs. .. note:: This function block must be executed in a task with a call-up interval of 70 ms.

### Fb787_2_1662_ReadCurrent
Epsitron electronic fuse (2 channel)

**Description:**
This function block supports the 89-bit protocol to read the current of each channel. Depending on the input ``xReadSetting`` it is differentiated between reading the channels setting or reading the actual current (supported by FW>2.1). Devices without overcurrent protection can only display the channels current setting. The module is activated via the ``xEnable`` input. If configuration of the channels is to be performed using the buttons on the device, the module must be deactivated while configuration is in progress. The connection to the device is made via a digital input ``xS2_Input`` and via a digital output ``xS1_Output``. You can select the channels to be activated via the input ``xChannelxActive``. Configuration is started using the ``xConfig`` input. The ``xDone`` output signals the completion of the configuration procedure. The current status of the various channels is indicated at the ``eChannelxStatus`` outputs. .. note:: This function block must be executed in a task with a call-up interval of 70 ms.

### Fb787_2_1662
Epsitron electronic fuse (2 channel)

**Description:**
The module is activated via the ``xEnable`` input. If configuration of the channels is to be performed using the buttons on the device, the module must be deactivated while configuration is in progress. The connection to the device is made via a digital input ``xS2_Input`` and via a digital output ``xS1_Output``. You can select the channels to be activated via the input ``xChannelxActive``. Configuration is started using the ``xConfig`` input. The ``xDone`` output signals the completion of the configuration procedure. The current status of the various channels is indicated at the ``eChannelxStatus`` outputs. .. note:: This function block must be executed in a task with a call-up interval of 70 ms.

### Fb787_1668_ReadCurrent
Epsitron electronic fuse (8 channel)

**Description:**
This function block supports the 89-bit protocol to read the current of each channel. Depending on the input ``xReadSetting`` it is differentiated between reading the channels setting or reading the actual current (supported by FW>2.1). Devices without overcurrent protection can only display the channels current setting. The module is activated via the ``xEnable`` input. If configuration of the channels is to be performed using the buttons on the device, the module must be deactivated while configuration is in progress. The connection to the device is made via a digital input ``xS2_Input`` and via a digital output ``xS1_Output``. You can select the channels to be activated via the input ``xChannelxActive``. Configuration is started using the ``xConfig`` input. The ``xDone`` output signals the completion of the configuration procedure. The current status of the various channels is indicated at the ``eChannelxStatus`` outputs. .. note:: This function block must be executed in a task with a call-up interval of 70 ms.

### Fb787_1668
Epsitron electronic fuse (8 channel)

**Description:**
The module is activated via the ``xEnable`` input. If configuration of the channels is to be performed using the buttons on the device, the module must be deactivated while configuration is in progress. The connection to the device is made via a digital input ``xS2_Input`` and via a digital output ``xS1_Output``. You can select the channels to be activated via the input ``xChannelxActive``. Configuration is started using the ``xConfig`` input. The ``xDone`` output signals the completion of the configuration procedure. The current status of the various channels is indicated at the ``eChannelxStatus`` outputs. .. note:: This function block must be executed in a task with a call-up interval of 70 ms.

### Fb787_1664_ReadCurrent
Epsitron electronic fuse (4 channel)

**Description:**
This function block supports the 89-bit protocol to read the current of each channel. Depending on the input ``xReadSetting`` it is differentiated between reading the channels setting or reading the actual current (supported by FW>2.1). Devices without overcurrent protection can only display the channels current setting. The module is activated via the ``xEnable`` input. If configuration of the channels is to be performed using the buttons on the device, the module must be deactivated while configuration is in progress. The connection to the device is made via a digital input ``xS2_Input`` and via a digital output ``xS1_Output``. You can select the channels to be activated via the input ``xChannelxActive``. Configuration is started using the ``xConfig`` input. The ``xDone`` output signals the completion of the configuration procedure. The current status of the various channels is indicated at the ``eChannelxStatus`` outputs. .. note:: This function block must be executed in a task with a call-up interval of 70 ms.

### Fb787_1664
Epsitron electronic fuse (4 channel)

**Description:**
The module is activated via the ``xEnable`` input. If configuration of the channels is to be performed using the buttons on the device, the module must be deactivated while configuration is in progress. The connection to the device is made via a digital input ``xS2_Input`` and via a digital output ``xS1_Output``. You can select the channels to be activated via the input ``xChannelxActive``. Configuration is started using the ``xConfig`` input. The ``xDone`` output signals the completion of the configuration procedure. The current status of the various channels is indicated at the ``eChannelxStatus`` outputs. .. note:: This function block must be executed in a task with a call-up interval of 70 ms.

### Fb787_1662_ReadCurrent
Epsitron electronic fuse (2 channel)

**Description:**
This function block supports the 89-bit protocol to read the current of each channel. Depending on the input ``xReadSetting`` it is differentiated between reading the channels setting or reading the actual current (supported by FW>2.1). Devices without overcurrent protection can only display the channels current setting. The module is activated via the ``xEnable`` input. If configuration of the channels is to be performed using the buttons on the device, the module must be deactivated while configuration is in progress. The connection to the device is made via a digital input ``xS2_Input`` and via a digital output ``xS1_Output``. You can select the channels to be activated via the input ``xChannelxActive``. Configuration is started using the ``xConfig`` input. The ``xDone`` output signals the completion of the configuration procedure. The current status of the various channels is indicated at the ``eChannelxStatus`` outputs. .. note:: This function block must be executed in a task with a call-up interval of 70 ms.

### Fb787_1662
Epsitron electronic fuse (2 channel)

**Description:**
The module is activated via the ``xEnable`` input. If configuration of the channels is to be performed using the buttons on the device, the module must be deactivated while configuration is in progress. The connection to the device is made via a digital input ``xS2_Input`` and via a digital output ``xS1_Output``. You can select the channels to be activated via the input ``xChannelxActive``. Configuration is started using the ``xConfig`` input. The ``xDone`` output signals the completion of the configuration procedure. The current status of the various channels is indicated at the ``eChannelxStatus`` outputs. .. note:: This function block must be executed in a task with a call-up interval of 70 ms.

## Data Types

### eStatus
Enumeration type.

### eChannelStatus
Enumeration type.

### eEpsitronStatus
Enumeration type.

## Usage Examples

### Basic Usage
```iec
VAR
    fbGeneralFbManager: GeneralFbManager;
END_VAR

// Basic function block usage
fbGeneralFbManager(
    // Configure inputs as needed
);

// Check status
IF fbGeneralFbManager.xValid THEN
    // Operation successful
END_IF

IF fbGeneralFbManager.xError THEN
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

