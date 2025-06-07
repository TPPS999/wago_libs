# WagoTypesModule_750_464 v1.9.4.0 (WAGO) - Complete Documentation


## 📋 Library Information

- **Company:** WAGO
- **Title:** WagoTypesModule_750_464
- **Version:** 1.9.4.0
- **Categories:** WAGO Internal|Common|Types and Interfaces
- **Author:** WAGO
- **Placeholder:** WagoTypesModule_750_464

### Description ¶


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling modules 750-464 [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling modules 750-464 [1]

### Contents: ¶


Contents: - Documentation Index - Project Information - Library Information - Methods I_Module_750_464.GetModulePsrMode (METH) - I_Module_750_464.GetModuleSettings (METH) - I_Module_750_464.GetRawChannelCalibration (METH) - I_Module_750_464.GetRawChannelConfiguration (METH) - I_Module_750_464.GetRawChannelScaling (METH) - I_Module_750_464.GetRawChannelSettings (METH) - I_Module_750_464.SetModulePsrMode (METH) - I_Module_750_464.SetRawChannelCalibration (METH) - I_Module_750_464.SetRawChannelConfiguration (METH) - I_Module_750_464.SetRawChannelScaling (METH) - ... and 4 more Interfaces - I_Module_750_464 (ITF) - I_Module_750_464_dynConfig (ITF) Program Organization Global Variable Lists - Channels_464 (GVL) - VersionHistory (GVL) Other Components - 10 Enumeration - 15 Datatypes - Channel - Configuration - Module - Raw - ePSRR_Mode (ENUM) - eSensorType (ENUM) - typRawChannelCalibration (STRUCT) - typRawChannelConfiguration (STRUCT) - ... and 1 more

### Indices and tables ¶


| [1] | Based on WagoTypesModule_750_464.library, last modified 25.05.2021, 14:01:55. LibDoc 3.5.15.30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Documentation Index


## WagoTypesModule_750_464 Library Documentation


| Company: | WAGO |
| Title: | WagoTypesModule_750_464 |
| Version: | 1.9.4.0 |
| Categories: | WAGO Internal\|Common\|Types and Interfaces |
| Author: | WAGO |
| Placeholder: | WagoTypesModule_750_464 |

### Description


This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit.

Handling modules 750-464 [1]

This document is automatically generated. Because of this, the chapter 30 Visualization is not shown in this document. If you are interested in getting to know more about visualization, we refer to the library manager of e!Cockpit. Handling modules 750-464 [1]

### Contents:


- 20 Program Organization Units 10 Enumeration - 15 Datatypes - Channels_464 (GVL) - I_Module_750_464 (ITF) - I_Module_750_464_dynConfig (ITF) VersionHistory (GVL)

### Indices and tables


| [1] | Based on WagoTypesModule_750_464.library, last modified 25.05.2021, 14:01:55. LibDoc 3.5.15.30 |

© WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

- File and Project Information - Library Reference © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. For the avoidance of doubt, this copyright notice does not only apply to the information above but also and primarily to the described library itself. Please note that third-party products are always mentioned without reference to intellectual property rights, including patents, utility models, designs and trademarks, accordingly the existence of such rights cannot be excluded. WAGO is a registered trademark of WAGO Verwaltungsgesellschaft mbH.

### Project Information


## File and Project Information


| Scope | Name | Type | Content |
| --- | --- | --- | --- |
| FileHeader | libraryFile | string | WagoTypesModule_750_464.library |
| contentFile | WagoTypesModule_750_464_clr.json |
| productName | e!COCKPIT |
| creationDateTime | date | 25.05.2021, 14:01:59 |
| companyName | string | WAGO |
| ProjectInformation | LastModificationDateTime | date | 25.05.2021, 14:01:55 |
| Description | string | See: Description |
| Copyright | © WAGO Kontakttechnik GmbH & Co. KG, Germany 2018 – All rights reserved. |
| Author | WAGO |
| AutoResolveUnbound | bool | True |
| Placeholder | string | WagoTypesModule_750_464 |
| Company | WAGO |
| DocFormat | reStructuredText |
| Project | WagoTypesModule_750_464 |
| Version | version | 1.9.4.0 |
| Version string | string |  |
| Title | WagoTypesModule_750_464 |
| LibraryCategories | library-category-list | WAGO Internal\|Common\|Types and Interfaces |
| CompiledLibraryCompatibilityVersion | string | CODESYS V3.5 SP16 Patch 3 |

### Library Information


## Library Reference


This is a dictionary of all referenced libraries and their name spaces.

This is a dictionary of all referenced libraries and their name spaces.

### WagoSysErrorBase


#### Library Identification


Placeholder: WagoSysErrorBase Default Resolution: WagoSysErrorBase, * (WAGO) Namespace: WagoSysErrorBase

#### Library Properties


| LinkAllContent: False QualifiedOnly: False | Key: WagoSysErrorBase SystemLibrary: False | Optional: False |

### WagoSysVersion


#### Library Identification


Name: WagoSysVersion Version: 1.0.0.0 Company: WAGO Namespace: WagoSysVersion

#### Library Properties


| LinkAllContent: False QualifiedOnly: True | Key: WagoSysVersion, 1.0.0.0 (WAGO) SystemLibrary: False | Optional: False |

### WagoTypesModuleBase


#### Library Identification


Placeholder: WagoTypesModuleBase Default Resolution: WagoTypesModuleBase, * (WAGO) Namespace: WagoTypesModuleBase

#### Library Properties


| LinkAllContent: False QualifiedOnly: True | Key: WagoTypesModuleBase SystemLibrary: False | Optional: False |

#### Library Parameter


Parameter: MAX_MBX_SIZE = 18

### Methods


## I_Module_750_464.GetModulePsrMode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetModulePsrMode | WagoTypesModuleBase.eServiceState |
| Inout | xTrigger | BOOL |
| ePSRMode | ePSRR_Mode |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Parameter | Value | Description |
| --- | --- | --- |
| ePSRMode | ENABLED_50HZ | Noise filter optimized for 50 Hz |
| ENABLED_60HZ | Noise filter optimized for 60 Hz |
| ENABLED_50_60HZ | Noise filter optimized for 50/60 Hz but lower attenuation |

| Return Value | Description |
| --- | --- |
| WagoTypesModuleBase.eServiceState.DONE | successful |
| WagoTypesModuleBase.eServiceState.ABORT | error -> see oError |
| WagoTypesModuleBase.eServiceState.NO_DATA | call while xTrigger is reset |

```
VAR
    //--- Module Mode Settings ------------------------------
    myPsrMode           :   WagoTypesModule_750_464.ePSRR_Mode;
    xGetModulePsrMode   :   BOOL;  // triggers the function
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- M O D U L E    S E T T I N G S -----------------------
CASE my464.GetModulePsrMode(xGetModulePsrMode, myPsrMode, oError => oError) OF

    eServiceState.DONE : // OK
            ;// process here your myPsrMode

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

Get the psr mode of the module.

Return Values

It is not allowed to reset the xTrigger by the application. This must done by the method.

Graphical Illustration

Graphical Interface of I_Module_750_464.GetModulePsrMode

For get the psr mode from the module.

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the psr mode of the module. Return Values Warning It is not allowed to reset the xTrigger by the application. This must done by the method. Graphical Illustration ![Image](images/wagotypesmodule_750_464_2f9cc522.png) Graphical Interface of I_Module_750_464.GetModulePsrMode Example For get the psr mode from the module. Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_464.GetModuleSettings (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetModuleSettings | WagoTypesModuleBase.eServiceState |
| Inout | xTrigger | BOOL |
| utModuleSettings | typModuleSettings |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| xTwoChannel | FALSE | 4 channels -> 2-wire only |
| TRUE | 2 channels -> 3-wire possible |
| ePSRMode | ENABLED_50HZ | Noise filter optimized for 50 Hz |
| ENABLED_60HZ | Noise filter optimized for 60 Hz |
| ENABLED_50_60HZ | Noise filter optimized for 50/60 Hz but lower attenuation |

| Return Value | Description |
| --- | --- |
| WagoTypesModuleBase.eServiceState.DONE | successful |
| WagoTypesModuleBase.eServiceState.ABORT | error -> see oError |
| WagoTypesModuleBase.eServiceState.NO_DATA | call while xTrigger is reset |

```
VAR
    //--- Module Mode Settings ------------------------------
    utModuleSettings    :   WagoTypesModule_750_464.typModuleSettings;
    xGetModuleSettings  :   BOOL;  // triggers the function
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- M O D U L E    S E T T I N G S -----------------------
CASE my451.GetModuleSettings(xGetModuleSettings, utModuleSettings, oError => oError) OF

    eServiceState.DONE : // OK
            ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

Get the common settings of the module at a struct.

Return Values

It is not allowed to reset the xTrigger by the application. This must done by the method.

Graphical Illustration

Graphical Interface of I_Module_750_464.GetModuleSettings

For get the settings from the module.

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the common settings of the module at a struct. Return Values Warning It is not allowed to reset the xTrigger by the application. This must done by the method. Graphical Illustration ![Image](images/wagotypesmodule_750_464_f1e64e56.png) Graphical Interface of I_Module_750_464.GetModuleSettings Example For get the settings from the module. Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_464.GetRawChannelCalibration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawChannelCalibration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_464) |
| Inout | xTrigger | BOOL |
| utRawChannelCalibration | typRawChannelCalibration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| xUserCalibration | FALSE | The user scaling is switched off |
| TRUE | The user scaling is switched on |
| iUserCalibrationOffset |  |
| uiUserCalibrationGain |  |

```
VAR
    //--- Channel Calibration ---------------------------------
    utChannelCalibration    :   WagoTypesModule_750_464.typRawChannelCalibration;;
    xGetChannelCalibration  :   BOOL;
    oError                  :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L    C A L I B R A T I O N -----------------------
CASE my464.GetRawChannelCalibration(    usiChannel              := 1,
                                        xTrigger                := xGetChannelCalibration,
                                        utRawChannelCalibration := utChannelCalibration,
                                        oError                  => oError
                                    ) OF

    eServiceState.DONE : // OK
            ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

Get the calibration of a channel at a struct.

Graphical Illustration

Graphical Interface of I_Module_750_464.GetRawChannelCalibration

For get the calibration from channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the calibration of a channel at a struct. Graphical Illustration ![Image](images/wagotypesmodule_750_464_fb2e9a57.png) Graphical Interface of I_Module_750_464.GetRawChannelCalibration Example For get the calibration from channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_464.GetRawChannelConfiguration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawChannelConfiguration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_464) |
| Inout | xTrigger | BOOL |
| utRawChannelConfiguration | typRawChannelConfiguration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

Graphical Illustration

Graphical Interface of I_Module_750_464.GetRawChannelConfiguration

Interface variables Function Get the complete raw configuration of a channel. Graphical Illustration ![Image](images/wagotypesmodule_750_464_a8a6adf9.png) Graphical Interface of I_Module_750_464.GetRawChannelConfiguration Example

## I_Module_750_464.GetRawChannelScaling (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawChannelScaling | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_464) |
| Inout | xTrigger | BOOL |
| utRawChannelScaling | typRawChannelScaling |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| xUserScaling | FALSE | The user scaling is switched off |
| TRUE | The user scaling is switched on |
| xManufacturerScaling | FALSE | The manufacturer scaling is switched off |
| TRUE | The manufacturer scaling is switched on |
| iUserScalingOffset |  |
| uiUserScalingGain |  |
| uiUserScalingWireResistor |  |

```
VAR
    //--- Channel Settings ---------------------------------
    utChannelScaling    :   WagoTypesModule_750_464.typRawChannelScaling;;
    xGetChannelScaling  :   BOOL;
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L   S C A L I N G ------------------------
CASE my464.GetRawChannelScaling(    usiChannel           := 1,
                                    xTrigger             := xGetChannelScaling,
                                    utRawChannelScaling  := utChannelScaling,
                                    oError               => oError
                                ) OF

    eServiceState.DONE : // OK
            ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

Get the scaling of a channel at a struct.

Graphical Illustration

Graphical Interface of I_Module_750_464.GetRawChannelScaling

For get the scaling from channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the scaling of a channel at a struct. Graphical Illustration ![Image](images/wagotypesmodule_750_464_83c7e18d.png) Graphical Interface of I_Module_750_464.GetRawChannelScaling Example For get the scaling from channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_464.GetRawChannelSettings (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawChannelSettings | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_464) |
| Inout | xTrigger | BOOL |
| utRawChannelSettings | typRawChannelSettings |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| eSensorType | Sensor types of the 750-464 (RTD) version |
| Pt100_IEC751 | IEC 751 | -200 °C...850 °C |
| Ni100_DIN43760 | DIN 43760 | -60 °C...250 °C |
| Pt1000_IEC751 | IEC 751 | -200 °C...850 °C |
| Pt500_IEC751 | IEC 751 | -200 °C...850 °C |
| Pt200_IEC751 | IEC 751 | -200 °C...850 °C |
| Ni1000_DIN43760 | DIN 43760 | -60 °C...250 °C |
| Ni120_MINCO | Minco | -80 °C...260 °C |
| Ni1000_TK5000 | TK 5000 | -60 °C...250 °C |
| Sensor types of the 750-464/000-002 (NTC) version |
| NTC_10K |  |
| NTC_20K |  |
| NTC_10K_THERMOKON |  |
| xEnable3Wire | FALSE | 2-wire |
| TRUE | 3-wire |
| xEnableWatchdog | FALSE | Watchdog timer is not active |
| TRUE | Watchdog timer is active (terminal box) |
| xEnableAverageFilter | FALSE | The mean value filter is switched off |
| TRUE | The mean value filter is switched on |
| xAmountSignFormat | FALSE | Numeric values appear in two’s complement |
| TRUE | Numeric values appear in amount / sign format |
| xS5FB250Format | FALSE | Numeric values appear in default format |
| TRUE | Numeric values appear in S5-FB250 format |
| xEnableDiag | FALSE | Wire break / short circuit diagnostics disabled |
| TRUE | Wire break / short circuit diagnostics enabled |
| xEnableOverrangeProtection | FALSE | The overflow limit is switched off |
| TRUE | Numeric values are limited to values in R50, R51 |
| iUserUnderrange |  |
| iUserOverrange |  |

```
VAR
    //--- Channel Settings ---------------------------------
    utChannelSettings   :   WagoTypesModule_750_464.typRawChannelSettings;;
    xGetChannelSettings :   BOOL;
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L   S E T T I N G S ----------------------
CASE my464.GetRawChannelSettings(   usiChannel           := 1,
                                    xTrigger             := xGetChannelSettings,
                                    utRawChannelSettings := utChannelSettings,
                                    oError               => oError
                                ) OF

    eServiceState.DONE : // OK
        ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
        ;// process here your error handling -> see oError for more information

END_CASE
```

Get the settings of a channel at a struct.

Graphical Illustration

Graphical Interface of I_Module_750_464.GetRawChannelSettings

For get the settings from channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Get the settings of a channel at a struct. Graphical Illustration ![Image](images/wagotypesmodule_750_464_2a5ed557.png) Graphical Interface of I_Module_750_464.GetRawChannelSettings Example For get the settings from channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_464.SetModulePsrMode (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetModulePsrMode | WagoTypesModuleBase.eServiceState |
| Inout | xTrigger | BOOL |
| ePSRMode | ePSRR_Mode |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Parameter | Value | Description |
| --- | --- | --- |
| ePSRMode | ENABLED_50HZ | Noise filter optimized for 50 Hz |
| ENABLED_60HZ | Noise filter optimized for 60 Hz |
| ENABLED_50_60HZ | Noise filter optimized for 50/60 Hz but lower attenuation |

| Return Value | Description |
| --- | --- |
| WagoTypesModuleBase.eServiceState.DONE | successful |
| WagoTypesModuleBase.eServiceState.ABORT | error -> see oError |
| WagoTypesModuleBase.eServiceState.NO_DATA | call while xTrigger is reset |

```
VAR
    myPsrMode           :   WagoTypesModule_750_464.ePSRR_Mode;
    xSetModulePsrMode   :   BOOL;  // triggers the function
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- S E T   M O D U L E    P S R   M O D E ---------------
myPsrMode := WagoTypesModule_750_464.ePSRR_Mode.ENABLED_50HZ; // set my value
CASE my464.SetModulePsrMode(xSetModulePsrMode, myPsrMode, oError => oError) OF

    eServiceState.DONE : // OK

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

Set the psr mode of the module.

Return Values

It is not allowed to reset the xTrigger by the application. This must done by the method.

Graphical Illustration

Graphical Interface of I_Module_750_464.SetModulePsrMode

For set the settings from the module.

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Set the psr mode of the module. Return Values Warning It is not allowed to reset the xTrigger by the application. This must done by the method. Graphical Illustration ![Image](images/wagotypesmodule_750_464_630162b1.png) Graphical Interface of I_Module_750_464.SetModulePsrMode Example For set the settings from the module. Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_464.SetRawChannelCalibration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetRawChannelCalibration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_464) |
| Inout | xTrigger | BOOL |
| utRawChannelCalibration | typRawChannelCalibration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| xUserCalibration | FALSE | The user scaling is switched off |
| TRUE | The user scaling is switched on |
| iUserCalibrationOffset |  |
| uiUserCalibrationGain |  |

```
VAR
    //--- Channel Calibration ---------------------------------
    utChannelCalibration    :   WagoTypesModule_750_464.typRawChannelCalibration;;
    xSetChannelCalibration  :   BOOL;
    oError                  :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L    C A L I B R A T I O N -----------------------
CASE my464.SetRawChannelCalibration(    usiChannel              := 1,
                                        xTrigger                := xSetChannelCalibration,
                                        utRawChannelCalibration := utChannelCalibration,
                                        oError                  => oError
                                   ) OF

    eServiceState.DONE : // OK
            ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

Set the calibration of a channel by a struct.

Graphical Illustration

Graphical Interface of I_Module_750_464.SetRawChannelCalibration

For set the calibration of channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Set the calibration of a channel by a struct. Graphical Illustration ![Image](images/wagotypesmodule_750_464_86252a5a.png) Graphical Interface of I_Module_750_464.SetRawChannelCalibration Example For set the calibration of channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_464.SetRawChannelConfiguration (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetRawChannelConfiguration | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_464) |
| Inout | xTrigger | BOOL |
| utRawChannelConfiguration | typRawChannelConfiguration |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

Graphical Illustration

Graphical Interface of I_Module_750_464.SetRawChannelConfiguration

Interface variables Function Set the complete raw configuration of a channel. Graphical Illustration ![Image](images/wagotypesmodule_750_464_c4522909.png) Graphical Interface of I_Module_750_464.SetRawChannelConfiguration Example

## I_Module_750_464.SetRawChannelScaling (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetRawChannelScaling | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_464) |
| Inout | xTrigger | BOOL |
| utRawChannelScaling | typRawChannelScaling |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| xUserScaling | FALSE | The user scaling is switched off |
| TRUE | The user scaling is switched on |
| xManufacturerScaling | FALSE | The manufacturer scaling is switched off |
| TRUE | The manufacturer scaling is switched on |
| iUserScalingOffset |  |
| uiUserScalingGain |  |
| uiUserScalingWireResistor |  |

```
VAR
    //--- Channel Settings ---------------------------------
    utChannelScaling    :   WagoTypesModule_750_464.typRawChannelScaling;;
    xSetChannelScaling  :   BOOL;
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L   S C A L I N G ------------------------
CASE my464.SetRawChannelScaling(    usiChannel          := 1,
                                    xTrigger            := xSetChannelScaling,
                                    utRawChannelScaling := utChannelScaling,
                                    oError              => oError
                                ) OF

    eServiceState.DONE : // OK
            ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
            ;// process here your error handling -> see oError for more information

END_CASE
```

Set the scaling of a channel by a struct.

Graphical Illustration

Graphical Interface of I_Module_750_464.SetRawChannelScaling

For set the scaling of channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Set the scaling of a channel by a struct. Graphical Illustration ![Image](images/wagotypesmodule_750_464_92931b80.png) Graphical Interface of I_Module_750_464.SetRawChannelScaling Example For set the scaling of channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_464.SetRawChannelSettings (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | SetRawChannelSettings | WagoTypesModuleBase.eServiceState |
| Input | usiChannel | USINT (1..MAX_CHANNEL_464) |
| Inout | xTrigger | BOOL |
| utRawChannelSettings | typRawChannelSettings |
| Output | xError | BOOL |
| oError | WagoSysErrorBase.FbResult |

| Struct member | Value | Description |
| --- | --- | --- |
| eSensorType | Sensor types of the 750-464 (RTD) version |
| Pt100_IEC751 | IEC 751 | -200 °C...850 °C |
| Ni100_DIN43760 | DIN 43760 | -60 °C...250 °C |
| Pt1000_IEC751 | IEC 751 | -200 °C...850 °C |
| Pt500_IEC751 | IEC 751 | -200 °C...850 °C |
| Pt200_IEC751 | IEC 751 | -200 °C...850 °C |
| Ni1000_DIN43760 | DIN 43760 | -60 °C...250 °C |
| Ni120_MINCO | Minco | -80 °C...260 °C |
| Ni1000_TK5000 | TK 5000 | -60 °C...250 °C |
| Sensor types of the 750-464/000-002 (NTC) version |
| NTC_10K |  |
| NTC_20K |  |
| NTC_10K_THERMOKON |  |
| xEnable3Wire | FALSE | 2-wire |
| TRUE | 3-wire |
| xEnableWatchdog | FALSE | Watchdog timer is not active |
| TRUE | Watchdog timer is active (terminal box) |
| xEnableAverageFilter | FALSE | The mean value filter is switched off |
| TRUE | The mean value filter is switched on |
| xAmountSignFormat | FALSE | Numeric values appear in two’s complement |
| TRUE | Numeric values appear in amount / sign format |
| xS5FB250Format | FALSE | Numeric values appear in default format |
| TRUE | Numeric values appear in S5-FB250 format |
| xEnableDiag | FALSE | Wire break / short circuit diagnostics disabled |
| TRUE | Wire break / short circuit diagnostics enabled |
| xEnableOverrangeProtection | FALSE | The overflow limit is switched off |
| TRUE | Numeric values are limited to values in R50, R51 |
| iUserUnderrange |  |
| iUserOverrange |  |

```
VAR
    //--- Channel Settings ---------------------------------
    utChannelSettings   :   WagoTypesModule_750_464.typRawChannelSettings;;
    xSetChannelSettings :   BOOL;
    oError              :   WagoSysErrorBase.FbResult;
END_VAR

//--- C H A N N E L   S E T T I N G S ----------------------
CASE my464.SetRawChannelSettings(   usiChannel           := 1,
                                    xTrigger             := xSetChannelSettings,
                                    utRawChannelSettings := utChannelSettings,
                                    oError               => oError
                                ) OF

    eServiceState.DONE : // OK
        ;// process here your utModuleSettings

    eServiceState.ABORT : // Error
        ;// process here your error handling -> see oError for more information

END_CASE
```

Set the settings for a channel by a struct.

Graphical Illustration

Graphical Interface of I_Module_750_464.SetRawChannelSettings

For set the settings of channel one

You have to call the method cyclic until the method returns with DONE or ABORT.

Interface variables Function Set the settings for a channel by a struct. Graphical Illustration ![Image](images/wagotypesmodule_750_464_99d711da.png) Graphical Interface of I_Module_750_464.SetRawChannelSettings Example For set the settings of channel one Note You have to call the method cyclic until the method returns with DONE or ABORT.

## I_Module_750_464_dynConfig.GetRawProcessValue (METH)


| Scope | Name | Type |
| --- | --- | --- |
| Return | GetRawProcessValue | INT |
| Input | usiChannel | USINT (1..MAX_CHANNEL_464) |

```
VAR
    myiProcessValue :   INT;
END_VAR

myiProcessValue := my451.GetProcessValue(1); // here is the process raw value as INT
```

Get the raw process value of the wanted channel.

In case of error (e.g. an invalid channel number is given) it returns -32768.

Graphical Illustration

Graphical Interface of I_Module_750_464_dynConfig.GetRawProcessValue

Interface variables Function Get the raw process value of the wanted channel. In case of error (e.g. an invalid channel number is given) it returns -32768. Graphical Illustration ![Image](images/wagotypesmodule_750_464_0f2a57a4.png) Graphical Interface of I_Module_750_464_dynConfig.GetRawProcessValue Example For get the process value from first channel of the module.

## typModuleSettings (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| xTwoChannel | BOOL | R47.0 |
| ePSRMode | ePSRR_Mode | R47.8..9 |

## typRawChannelSettings (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| eSensorType | eSensorType | R32.12..15 |
| xEnable3Wire | BOOL | R32.10 |
| xEnableWatchdog | BOOL | R32.2 |
| xEnableAverageFilter | BOOL | R32.7 |
| xAmountSignFormat | BOOL | R32.3 -> Number notation -> 2-complement / amount-sign (Bit 0) |
| xS5FB250Format | BOOL | R32.4 -> S5-Format -> Standard / S5-FB250 format (Bit 1) |
| xEnableDiag | BOOL | R32.6 -> Wire Break / Short Circuit |
| xEnableOverrangeProtection | BOOL | R32.8 |
| iUserUnderrange | INT | R35 |
| iUserOverrange | INT | R36 |

### Interfaces


## I_Module_750_464 (ITF)


- Channel I_Module_750_464.GetRawChannelCalibration (METH) - I_Module_750_464.GetRawChannelScaling (METH) - I_Module_750_464.GetRawChannelSettings (METH) - I_Module_750_464.SetRawChannelCalibration (METH) - I_Module_750_464.SetRawChannelScaling (METH) - I_Module_750_464.SetRawChannelSettings (METH) Configuration - I_Module_750_464.GetRawChannelConfiguration (METH) - I_Module_750_464.SetRawChannelConfiguration (METH) Module - I_Module_750_464.GetModulePsrMode (METH) - I_Module_750_464.GetModuleSettings (METH) - I_Module_750_464.SetModulePsrMode (METH)

## I_Module_750_464_dynConfig (ITF)


- I_Module_750_464_dynConfig.GetRawProcessValue (METH)

### Program Organization


## 20 Program Organization Units


- 10 Enumeration ePSRR_Mode (ENUM) - eSensorType (ENUM) 15 Datatypes - Raw typRawChannelCalibration (STRUCT) - typRawChannelScaling (STRUCT) - typRawChannelSettings (STRUCT) typModuleSettings (STRUCT) typRawChannelConfiguration (STRUCT) Channels_464 (GVL) I_Module_750_464 (ITF) - Channel I_Module_750_464.GetRawChannelCalibration (METH) - I_Module_750_464.GetRawChannelScaling (METH) - I_Module_750_464.GetRawChannelSettings (METH) - I_Module_750_464.SetRawChannelCalibration (METH) - I_Module_750_464.SetRawChannelScaling (METH) - I_Module_750_464.SetRawChannelSettings (METH) Configuration - I_Module_750_464.GetRawChannelConfiguration (METH) - I_Module_750_464.SetRawChannelConfiguration (METH) Module - I_Module_750_464.GetModulePsrMode (METH) - I_Module_750_464.GetModuleSettings (METH) - I_Module_750_464.SetModulePsrMode (METH) I_Module_750_464_dynConfig (ITF) - I_Module_750_464_dynConfig.GetRawProcessValue (METH)

### Global Variable Lists


## Channels_464 (GVL) ¶


## VersionHistory (GVL)


| date | version | author | change |
| 20.01.2021 | 1.9.4.0 | u010545 | Methods for psr mode added |
| 16.07.2019 | 1.9.3.0 | u010545 | Interface for dyn config added |
| 08.01.2019 | 1.9.1.0 | u015842 | Properties: free placeholder added |
| 11.10.2017 | 1.9.0.2 | u010545 | unifications |
| 09.10.2017 | 1.9.0.1 | u010545 | channel quantity modified |
| 27.07.2017 | 1.8.0.0 | u010545 | First release |
| 13.07.2017 | 0.0.0.1 | u010545 | init |

WagoTypesModule_750_464.library

Release Notes:

WagoTypesModule_750_464.library Release Notes:

### Other Components


## 10 Enumeration


- ePSRR_Mode (ENUM) - eSensorType (ENUM)

## 15 Datatypes


- Raw typRawChannelCalibration (STRUCT) - typRawChannelScaling (STRUCT) - typRawChannelSettings (STRUCT) typModuleSettings (STRUCT) typRawChannelConfiguration (STRUCT)

## Channel


- I_Module_750_464.GetRawChannelCalibration (METH) - I_Module_750_464.GetRawChannelScaling (METH) - I_Module_750_464.GetRawChannelSettings (METH) - I_Module_750_464.SetRawChannelCalibration (METH) - I_Module_750_464.SetRawChannelScaling (METH) - I_Module_750_464.SetRawChannelSettings (METH)

## Configuration


- I_Module_750_464.GetRawChannelConfiguration (METH) - I_Module_750_464.SetRawChannelConfiguration (METH)

## Module


- I_Module_750_464.GetModulePsrMode (METH) - I_Module_750_464.GetModuleSettings (METH) - I_Module_750_464.SetModulePsrMode (METH)

## Raw


- typRawChannelCalibration (STRUCT) - typRawChannelScaling (STRUCT) - typRawChannelSettings (STRUCT)

## ePSRR_Mode (ENUM)


| Name | Initial |
| --- | --- |
| ENABLED_50HZ | 0 |
| ENABLED_60HZ | 1 |
| ENABLED_50_60HZ | 2 |

Attributes: qualified_only InOut:

## eSensorType (ENUM)


| Name | Initial | Comment |
| --- | --- | --- |
| Pt100_IEC751 | 16#0 | IEC 751 |
| Ni100_DIN43760 | 16#1 | DIN 43760 |
| Pt1000_IEC751 | 16#2 | IEC 751 |
| Pt500_IEC751 | 16#3 | IEC 751 |
| Pt200_IEC751 | 16#4 | IEC 751 |
| Ni1000_DIN43760 | 16#5 | DIN 43760 |
| Ni120_MINCO | 16#6 | Minco |
| Ni1000_TK5000 | 16#7 | TK 5000 |
| NTC_10K | 16#10 | NTC 10 kOhm |
| NTC_20K | 16#11 | NTC 20 kOhm |
| NTC_10K_THERMOKON | 16#12 | NTC-Thermocon 10 kOhm |

| Name | Initial | Sensor type | Standard |
| --- | --- | --- | --- |
| Pt100_IEC751 | 0 | Pt100 | IEC 751 |
| Ni100_DIN43760 | 1 | Ni100 | DIN 43760 |
| Pt1000_IEC751 | 2 | Pt1000 | IEC 751 |
| Pt500_IEC751 | 3 | Pt500 | IEC 751 |
| Pt200_IEC751 | 4 | Pt200 | IEC 751 |
| Ni1000_DIN43760 | 5 | Ni1000 | DIN 43760 |
| Ni120_MINCO | 6 | Ni120 | Minco |
| Ni1000_TK5000 | 7 | Ni1000 | TK 5000 (Landis+Staefa) |
| POTENTIOMETER | 13 |  |  |
| Resistor_1 | 14 | Resistor | 10 Ohm ... 5.0 kOhm |
| Resistor_2 | 15 | Resistor | 10 Ohm ... 1.2 kOhm |
| NTC_10K | 16 | NTC 10 kOhm | TK 6180 / DIN 43760 |
| NTC_20K | 17 | NTC 20 kOhm | TK 5000 (Landis+Staefa) |
| NTC_10K_THERMOKON | 18 | NTC-Thermocon 10 kOhm | EN 60751 |

Attributes: qualified_only InOut:

## typRawChannelCalibration (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| xUserCalibration | BOOL | R32.5 -> Manufacturer Calibration / User Calibration |
| iUserCalibrationOffset | INT | R39 |
| uiUserCalibrationGain | UINT | R40 |

## typRawChannelConfiguration (STRUCT)


| Name | Type |
| --- | --- |
| Settings | typRawChannelSettings |
| Scaling | typRawChannelScaling |
| Calibration | typRawChannelCalibration |

## typRawChannelScaling (STRUCT)


| Name | Type | Comment |
| --- | --- | --- |
| xUserScaling | BOOL | R32.0 |
| xManufacturerScaling | BOOL | R32.1 |
| iUserScalingOffset | INT | R33 |
| uiUserScalingGain | UINT | R34 |
| uiUserScalingWireResistor | UINT | R21 -> 1/256 Ohm |